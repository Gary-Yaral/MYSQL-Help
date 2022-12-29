# No tienes llaves foraneas pero te aparece este error al querer eliminar una tabla
## Cannot delete or update a parent row: a foreign key constraint fails - MYSQL
Entonces lo que debes hacer es desactivar la comprobación de las llaves foráneas y ahí podrás eliminar la tabla, luego de que se elimine la tabla, debes volver a activar la comprobación. 

**Nota**: Procura ejecutar las sentencias una por una.

A continuación te dejo las sentencias que debes usar.

``` sql
SET FOREIGN_KEY_CHECKS=0; -- deshabilitas
DROP TABLE table_name
SET FOREIGN_KEY_CHECKS=1; -- habilitas nuevamente
```

