## Lenguaje

### Hola Mundo

Código para el típico programa de Hola Mundo, crear un archivo llamado holamundo.prg

```
funcion holamundo
    clear
    ? "hola mundo"
    ? "hoy es:", date()
return
```
Para ejecutarlo entrar a VFP y teclear: 
```
do hola-mundo
```

### IDE de VFP
VFP cuenta con su propio editor de archivos, para editar un archivo con extesion PRG usar: 
```
modify command holamundo
```
Tambien podemos usar la forma abreviada, la cual consiste en usar las primeras 4 letras, asi:
```
modi comm holamundo
```

### Comentarios en codigo
Para comentar un codigo se puede usar:
- Iniciar una linea con asterisco *
- A la derecha de una linea, usar doble ampersand &&
Ejemplos
```
funcion holamundo
    * Esta es mi primer programa en VFP 
    clear
    ? "hola mundo"         && Podemos usar " o ' en los strings o cadenas
    ? "hoy es:", date()
return
```


### Continuar una linea
A veces es necesario usar varias lineas en una sola instrucion para facilitar la lectura del codigo, para continuar una linea, se usa ; 
```
    * Calcular total de la factura
    nTotal = nSubtotal  ;
                + nImpuesto1 ;
                + nImpuesto2 ; 
                - nDescuento ;
                - nRetenciones
    ? nTotal

```


### Tipos de Datos
VFP maneja los siguientes tipos de datos:
|Tipo|Ejemlo|
|-|-|
|Numeric| 5 |
|| 3.14|
|Strings | "Hola"|
| | 'Hola'|
|Logic| .t.|
| | .f.|
|Date| {^2022/12/31}|
|Datetime|{{1970/12/03 14:35:59}}|

### Operadores
|Operador|Significado|Ejemplo|
|-|-|-|
|	==	| igualdad |	if nTotal == 0 |
|	<>	| diferente |	if nTotal <> 0 |
|	+	| sumar |	x = x + 1 |
|	-	| restar |	y = y - 1 |
|	/	| dividir |	nFactor = nValor / 1.1 |
|	*	| multiplicar |	nImporte = nTotal * nTC |
|	%	| residuo en div|	nResiduo = nValor % 2 |

### Asignacion de Variables
Ejemplos:
```
function asignar
local nTotal, cNombre, dFecha1, lEncontro
    nTotal = 10
    cNombre = 'Juan Perez'
    dFecha1 = date()
    lEncontro = .t.
    ? nTotal, cNombre, dFecha1, lEncontro
return
```




