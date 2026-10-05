# Fundamentos de los Sistemas Operativos · Aula interactiva (UTI)

**Aula en línea:** https://andresrubiop.github.io/fso-uti/

Nueve unidades con presentación, animaciones interactivas con datos reales, manual, laboratorio resuelto en C,
cuestionario y videos. En español, inglés, francés, catalán y japonés. Universidad Tecnológica Indoamérica.

## Usarla

- **En línea:** abre https://andresrubiop.github.io/fso-uti/ (funciona en Firefox y Chrome; tu progreso queda guardado en tu navegador).
- **Sin conexión:** *Code → Download ZIP* (o `git clone https://github.com/andresrubiop/fso-uti.git`) y abre `index.html` con doble clic.
- **PDF:** `materiales/unidad-N/` (manual `M#`, presentación `P#`, laboratorio `TD#`; `.pdf` en español, `.en/.fr/.ca/.ja.pdf` en los demás idiomas).

## Sin Ubuntu: GitHub Codespaces

[![Abrir en GitHub Codespaces](https://github.com/codespaces/badge.svg)](https://codespaces.new/andresrubiop/fso-uti)

Un Ubuntu 26.04 en la nube, con gcc, strace y los laboratorios ya compilados, y una terminal en el navegador.
No hace falta instalar nada.

1. Botón de arriba (o *Code → Codespaces → Create codespace on main*). La primera vez tarda unos minutos.
2. En la terminal de abajo: `python3 tds/terminal.py`
3. Abre el enlace `https://…app.github.dev/?terminal=aqui.…` que imprime: es el aula con su terminal conectada al
   Codespace, con «▶ Ejecutar» y «Preparar» funcionando.

- **Cuota:** usa la cuota gratuita de Codespaces de tu cuenta de GitHub. Detén el codespace al terminar (se detiene
  solo tras 30 minutos sin uso).
- **Puerto privado:** el puerto 8765 debe quedar **privado** (así viene). No lo hagas público.
- **Mediciones:** las de un Codespace (memoria, tiempos, Landlock del TD8) pueden diferir de las de un Ubuntu instalado.

## Laboratorios (Ubuntu 26.04 LTS: instalado, en máquina virtual o en WSL 2)

```bash
sudo apt install build-essential manpages-dev manpages-posix-dev strace gdb curl netcat-openbsd iproute2 e2fsprogs python3 python3-numpy
git clone https://github.com/andresrubiop/fso-uti.git && cd fso-uti
make -C tds                 # compila todos los laboratorios con gcc -Wall -Wextra -Werror
tds/tests/run.sh td1        # prepara y comprueba un laboratorio (deja su carpeta en tds/tests/tmp/td1)
python3 tds/terminal.py     # terminal del aula: abre el enlace que imprime
```

**Terminal dentro del aula:** funciona con la copia descargada y en un Codespace, no desde la página en línea.
El puente `tds/terminal.py` escucha únicamente en 127.0.0.1, usa una clave nueva en cada sesión y rechaza las
páginas de otros sitios, también la de GitHub Pages. Así ninguna página web puede abrir una terminal en tu
equipo. Detalles en el aula: Unidad 1 → Laboratorio TD0.

**Uso de IA generativa:** permitido y declarado. Cada laboratorio trae un desafío con IA. Se evalúa que
puedas explicar y verificar cada decisión.

---

# Fundamentals of Operating Systems · Interactive course hub (UTI)

**Online:** https://andresrubiop.github.io/fso-uti/ · **Offline:** *Code → Download ZIP* and open `index.html`. Labs: Ubuntu 26.04, the
commands above. **No Ubuntu?** Open the repository in GitHub Codespaces (button above), run
`python3 tds/terminal.py` and open the `https://…app.github.dev/?terminal=aqui.…` link it prints. The in-hub
terminal works with the downloaded copy or in a Codespace, never from the online page, by design: the bridge
listens on 127.0.0.1 only, uses a fresh key per session and rejects pages from other sites.
