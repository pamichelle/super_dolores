# Super Dolores · una SuperApp completa con TDD

Mensajería · Pagos · Comercio · Transporte en un solo ecosistema.
Mini-apps con permisos, bus de eventos, kill switch, lealtad y métricas de retención.
Manual TDD · Desarrollo Móvil Integral · UTNG.

> ⚠️ Simulación didáctica: el monedero es de juguete, los conductores son simulados y todo vive en memoria. No mueve dinero real.

## Estructura

```
lib/
  dominio/        dinero excepciones eventos monedero mensajeria comercio transporte
                  mini_app contexto plataforma lealtad analitica notificaciones sugerencias
  presentacion/
    vm/           inicio monedero chat tienda viajes metricas
    pantallas/    inicio monedero chat tienda viajes metricas horoscopo widgets
  main.dart       la "concha" (shell) de la SuperApp
test/             dominio_test servicios_test retencion_test vms_test
```

## Preparar (primera vez)

Abre en VS Code la carpeta `super_dolores` (la que tiene `pubspec.yaml`):

```bash
flutter create . --project-name super_dolores
del test\widget_test.dart
flutter pub get
flutter test
```

No usa paquetes externos ni permisos de Android.

## Pruebas

| Archivo | Rondas | Qué prueba |
|---|---|---|
| `test/dominio_test.dart` | 2–5, 8 | Dinero, monedero, bus de eventos, mensajería, mini-apps y permisos |
| `test/servicios_test.dart` | 6–7 | Comercio con comisión, transporte y máquina de estados, integración |
| `test/retencion_test.dart` | 9–11 | Lealtad, analítica (DAU/WAU/MAU, cohortes), notificaciones, sugerencias |
| `test/vms_test.dart` | 12 | ViewModels de inicio, monedero, chat, tienda, viajes y métricas |

## Ejecutar

```bash
flutter run
```

En Inicio puedes cambiar de persona (Ana, Luis, Marta), probar el kill switch de Viajes,
ver el tablero de retención y la mini-app de un tercero (Horóscopo) que intenta hacer cosas indebidas.
