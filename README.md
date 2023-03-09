
<h1 align="center">
  <br>
  <img src=img/tty-clock-example.png alt="tty-clock" width="200"/>
  <br>
  tty-clock
  <br>
</h1>


<h4 align="center">Un reloj digital para la terminal de linux.</h4>

<p align="center"> Repositorio original:
  <a href="https://aur.archlinux.org/tty-clock.git">
    https://aur.archlinux.org/tty-clock.git
  </a>
</p>

## Descripción del repositorio 
Con tty-clock tendrás un reloj digital simple en la terminal. Sin opciones que obstaculicen la vista del objetivo principal, mostrar la hora.

### Requisito
Para realizar la instalación debes de tener instalado git:

```
sudo pacman -Sy git
```

### Instalación del proyecto en ArchLinux
Debes de clonar el repositorio e iniciar la instalación del paquete

- Clonar el repositorio

```
$ git clone https://github.com/RaulAntonioMoralesBarros/tty-clock.git
```

- Entrar en el repositorio

```
$ cd tty-clock
```

- Instalar paquete

```
$ makepkg -si
```

> **Note**
> Estas instrucciones solo son aplicables para el sistema operativo LInux distribución ArchLInux


### Bug resuelto

- ttyclock.c:278:73: error: format not a string literal and no format arguments [-Werror=format-security]


### Creditos

Proyecto original:

- [AUR](https://aur.archlinux.org/tty-clock.git)


---

> GitHub [@RaulAntonioMoralesBarros](https://github.com/RaulAntonioMoralesBarros) &nbsp;&middot;&nbsp;

