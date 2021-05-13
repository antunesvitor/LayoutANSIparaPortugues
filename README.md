# Layout ANSI p/ português no Linux
---
Arquivos usados por mim para melhorar o layout do Keychron K2 para português.
As modificações são duas: substituir o PrintScreen por Insert e alterar algumas dead keys

### Arquivos

- us_layout 
Esse arquivo é uma cópia do arquivo que fica em `/usr/share/X11/xkb/symbols/us` ele contém todos os layouts americanos para inglês, então caso queria modificar um layout britânico deve procurar no arquivo `uk`.
Foi criado um novo layout `English (US ANSI p/ pt)` logo abaixo do `English (US, alt. intl.)` que é o layout o qual o meu se baseia, no caso ele altera o lugar do cedilha ao invés de ser `AtlGr+<+c` é apenas `AltGr+c` e para maiúsculo basta usar `AltGr+shift+c`
Outra alteração foi remover o trema do lugar da aspas duplas

- evdev
Esse arquivo faz o bind das teclas com o keycode, se você não deseja inverter teclas de lugar não use-o
No caso ele inverte o Delete com o PgDown, e Substitui o PgUp por Insert e o PrintScreen por PgUp. No caso do keychron K2 as teclas de paginação vão para cima do backspace e o insert/delete para o lado direito da mesma tecla, mais cômodo para mim.
O evdev fica em `/usr/share/X11/xkb/keycodes/evdev`

- evdev.xml
Esse arquivo é apenas para adicionar o novo Layout na lista de layouts do sistema, para isso bastou adicionar o seguinte trecho na lista de variantes do teclado us:
```
<variant>
    <configItem>
        <name>ansi-pt</name>
        <description>English (US ANSI p/ pt)</description>
    </configItem>
</variant>
```


