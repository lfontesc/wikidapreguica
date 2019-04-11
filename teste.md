## Welcome to SlackWiki

Teste Post 1: Configurando 2 monitores no SlackWare

### Iniciando....

Use o comando xrandr para listar os dispositivos de videos conectados.

```markdown
A saida do comando deve ser algo como isso.

Screen 0: minimum 8 x 8, current 1366 x 768, maximum 32767 x 32767
eDP1 connected primary 1366x768+0+0 (normal left inverted right x axis y axis) 340mm x 190mm
   1366x768      60.00 +  48.01  
   1280x720      59.86    60.00    59.74  
HDMI1 connected (normal left inverted right x axis y axis)
   1280x1024     60.02 +  75.02  
   1920x1080     60.00    59.94  
   1152x864      75.00  
```

No meu caso o monitor principal está com o nome de "eDP1", e o meu monitor secundario está listado como HDMI1.

### Escolhendo as configurações
Sintaxe do comando
```bash
xrandr --output "NOME_MONITOR_SECUNDARIO" --auto "LEFT ou RIGHT"-of "NOME_MONITOR_PRIMARIO".
```
Para manter o monitor secundario a esquerda utilize
```bash
xrandr --output HDMI1 --auto --left-of eDP1
```
Para manter o monitor secundario a direita utilize
```bash
xrandr --output HDMI1 --auto --right-of eDP1
```

### Support or Contact

Estou somente testando pra ver como funciona isso.