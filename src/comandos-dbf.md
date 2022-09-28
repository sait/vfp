## Comandos DBFs

VFP procede del DBase un lenguaje que improviso un manejo de base de datos por comandos especiales


### Crear una tabla
```
create dbfs alumnos ( id N(10), nombre C(100), grado N(2), fechanac D(8))
```

### Crear un indice
```
use alumnos exclusive
select alumnos
index on id tag id
```

### Abrir una tabla
```
* Abrir en modo compartido
use alumnos share
* Abrir en modo exclusivo
use alumnos exclusive
```
En la mayoria de las veces, las tablas se abren en modo compartido, para que varios usuarios puedan afectarlas, solamente se abren en modo exclusivo cuando es necesario regenerar el archivo indice o cuando se van a realizar operaciones importantes.

### Cerrar una tabla
```
select alumnos
use
```

### Cerrar todas las tablas
```
close databases
```

### Modificar la estructura
```
modify struct alumnos
```

### Crear un registro una tabla
```
select alumnos
append blank
replace id with 1,;
        nombre with 'Juan Perez',;
        grado with 2,;
        fechanac with  {^1997/08/31}
```

Con comentarios:
```

* seleccionar el area o tabla que se afectará
select alumnos

* crear un registro nuevo
append blank

* Guardar los datos 
replace id with 1,;
        nombre with 'Juan Perez',;
        grado with 2,;
        fechanac with  {^1997/08/31}
```

### Buscar registros
Usando el comando seek y la funcion found()
```
use alumnos order by id
nId = 10
select alumnos 
seek nId
if found()
    ? 'Encontre al alumnos con ID:', nId
else
    ? 'No se encuentra el alumno con ID:', nId
endif
```

Otro forma usando la funcion seek()
```
use alumnos order by id
nId = 10
select alumnos
if seek(nId)
    ? 'Encontre al alumnos con ID:', nId
else
    ? 'No se encuentra el alumno con ID:', nId
endif
```
Otro forma usando la funcion seek() con 2 parametros
```
use alumnos order by id
nId = 10
if seek(nId,'alumnos')
    ? 'Encontre al alumnos con ID:', nId
else
    ? 'No se encuentra el alumno con ID:', nId
endif
```
Otro forma usando la funcion seek() con 3 parametros
```
use alumnos
nId = 10
if seek(nId,'alumnos','id')
    ? 'Encontre al alumnos con ID:', nId
else
    ? 'No se encuentra el alumno con ID:', nId
endif
```




