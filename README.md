# SECOP Monitor Process

Refresh routine for the "Monitor de Procesos" artifact: users follow SECOP II processes, and a scheduled cloud agent
looks them up in the SECOP database, compares them with the last stored copy and records what changed.

- `ROUTINE_PROMPT.md` - the self-contained instructions the scheduled agent runs (twice a day, 9:30 and 15:30 Bogota time).

Fields compared: estado, apertura, fase, valor, fecha_cierre, fecha_apertura_ofertas, fecha_adjudicacion, adjudicado, proveedor, proponentes.
The first time a process is seen it is stored as a baseline, with no change events.
