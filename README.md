# Cosmic-Manifest

Manifest de [`repo`](https://gerrit.googlesource.com/git-repo) para descargar todo el árbol de CosmicOS.

La rama del manifest es el canal:

| Rama | Canal |
|---|---|
| `eventhorizon` | ultraexperimental (rama actual) |
| `quasar` | rolling |
| `pulsar` | beta |
| `nebula` | estable |
| `singularity` | LTS |

## Descargar

```sh
mkdir cosmicos && cd cosmicos
repo init -u https://github.com/Open-Cosmic-Project/Cosmic-Manifest.git -b eventhorizon -g desktop-dev
repo sync -j4
```

## Grupos

| Grupo | Uso |
|---|---|
| `desktop-dev` | Árbol de trabajo: todos los crates de Rust |
| `mobile` | Árbol para dispositivo |
| `milestone1` | Hito 1 (meta de compilación; no basta para `cargo check`) |
| `kernel`, `ui`, `launcher` | Subconjuntos |

Para subir cambios usa SSH (`git@github.com:Open-Cosmic-Project/<Repo>.git`); el manifest descarga por HTTPS.
