## Trabajo práctico final InfoVis 2021
Para correr estre proyecto es necesario tener instalado y funcionando postgresql (en docker o local).

Luego, cargar el dump de nuestra base de datos que esta guardado como un archivo .rar llamado dump.rar.

Para cargarlo en docker hacer:
```
cat dump.sql | docker exec -i your-db-container psql -U your-db-user -d your-db-name
```

Para cargarlo si no se tuebe corriendo postgres en docker hacer:
```
pg_restore -U username -d dbname -1 filename.dump
```

Una vez hecho esto correr nuestra api con el siguiente comando:
```
uvicorn app:app --reload
```

¡Listo!
