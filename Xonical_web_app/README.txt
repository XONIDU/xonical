HORARIO ITSE WEB V1

Uso:
1. Abre index.html en un navegador.
2. Carga XLSX, XLS o CSV.
3. Filtra por materia, grupo, profesor, día u hora.
4. Selecciona un grupo por materia.
5. Los grupos que se traslapan con la selección aparecen en rojo.
6. Consulta el calendario semanal.
7. Exporta el horario seleccionado a CSV o XLSX.

La app no tiene servidor/backend y procesa el archivo en el navegador.
Nota: XLSX se carga mediante SheetJS desde jsDelivr; por tanto la primera apertura requiere Internet. La V2 puede empaquetar esa librería para funcionar 100% offline.


V1.1 - Logica de grupos ITSE
El grupo base (1309) se mantiene al seleccionar un complementario (1309A/B/C). Entre complementarios del mismo grupo base solo puede haber uno: seleccionar 1309C reemplaza 1309B, pero conserva 1309.
