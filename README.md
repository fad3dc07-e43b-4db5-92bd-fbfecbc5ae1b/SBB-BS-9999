# SBB-BS-9999

Este repositorio representa un activo arquitectónico gobernado.

- El código del activo es `SBB-BS-9999`.
- El repositorio no está acoplado a un formato ni a una herramienta específica.
- Las personas pueden modelar en ArchiMate u otros lenguajes de diseño equivalentes.
- `Open Exchange` es hoy el formato de intercambio del artefacto, no el lenguaje de diseño del repositorio.
- `artifact/source/` aloja la fuente editable del diseño o un ejemplo de trabajo.
- `artifact/exchange/` aloja el artefacto de intercambio versionado.
- El artefacto actual vive en `artifact/exchange/design.openexchange.xml`.
- La validación se ejecuta mediante un engine declarativo centralizado en `ci-architecture-governance`.
- El repositorio de gobierno publica un manifest de reglas y el repo de diseño solo lo consume.
- La regla activa cubre la compatibilidad Archi/ArchiMate de `artifact/source/design.archimate`.
- Futuras versiones podrán agregar validaciones de metamodelo, reglas de arquitectura, trazabilidad, semántica, owners, dominios y versionado por tags.

Estructura mínima esperada:

```txt
/
├── artifact/
│   ├── source/
│   └── exchange/
│       └── design.openexchange.xml
├── README.md
└── .github/
    └── workflows/
        └── validate.yml
```

Flujo esperado:

```txt
Activo arquitectónico
→ artefacto versionable
→ workflow local liviano
→ validación centralizada
→ Pull Request controlado
→ merge a main
→ tag de versión
```
