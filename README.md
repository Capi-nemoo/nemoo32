```bash
esp32-projects/
├── docs/                  # Documentación básica
│   └── README.md          # Introducción general del repositorio
├── firmware/              # Código del proyecto
│   ├── esp32_project1/    # Proyecto individual
│   │   ├── esp32_project1.ino
│   │   └── platformio.ini # Configuración de plataforma (opcional, si usas PlatformIO)
│   ├── esp32_project2/    # Otro proyecto (opcional)
├── hardware/              # Archivos relacionados con hardware
│   ├── pcb/               # Diseños de PCB
│   └── datasheets/        # Datasheets relevantes
├── LICENSE                # Licencia del proyecto
└── README.md              # Introducción y guía rápida
```

# ESP32 Projects with Arduino CLI
Este repositorio contiene proyectos para ESP32 utilizando Arduino CLI.

## Requisitos
- [Arduino CLI](https://arduino.github.io/arduino-cli) instalado.
- Configuración de ESP32 en el gestor de placas:

  ```bash
  arduino-cli core update-index
  arduino-cli core install esp32:esp32
```

## Estructura

   * docs/: Documentación del proyecto.
   * firmware/: Proyectos individuales organizados en carpetas.
   * hardware/: Diseños de hardware y datasheets relevantes.
