# Ne
Proyectar domali
{
  "windows_suite": {
    "bucle_arranque": {
      "error": "No bootable device / Reinicios",
      "entorno": "Consola CMD desde USB de instalación",
      "comando": "bootrec /fixmbr && bootrec /fixboot && bootrec /rebuildbcd"
    },
    "sistema_corrupto": {
      "error": "Pantallazo Azul (BSOD) o congelamientos",
      "entorno": "Consola CMD en Modo Seguro",
      "comando": "sfc /scannow && DISM /Online /Cleanup-Image /RestoreHealth"
    }
  },
  "macos_suite": {
    "disco_perdido": {
      "error": "Carpeta con signo de interrogación parpadeando",
      "entorno": "Modo Recuperación (Cmd+R o mantener botón de encendido)",
      "accion": "Abrir Utilidad de Discos -> Reparar el volumen APFS principal"
    },
    "bloqueo_total": {
      "error": "El sistema no responde o se va a entregar a un cliente",
      "entorno": "Recuperación por Internet / Apple Configurator 2",
      "accion": "Seleccionar 'Reinstalar macOS' para descargar copia limpia oficial"
    }
  },
  "linux_suite": {
    "grub_roto": {
      "error": "Pantalla negra con indicador 'grub rescue>'",
      "entorno": "Live USB de Ubuntu/Debian -> Terminal",
      "comando": "sudo grub-install /dev/sda && sudo update-grub"
    },
    "fallo_montaje": {
      "error": "El sistema no pasa de la carga inicial por discos secundarios",
      "entorno": "Consola de emergencia (Modo lectura/escritura)",
      "comando": "nano /etc/fstab (comentar o corregir UUID del disco que falla)"
    }
  }
}
