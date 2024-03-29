
# Ayuda para solicitudes de fusión en GitHub

<http://bit.ly/usethis-te-ayuda>

<https://twitter.com/mauro_lepore>

[Licencia CCO](https://creativecommons.org/choose/zero/?lang=es)

## Por que usar solicitudes de fusión?

Las solicitudes de fusión (**PR: *pull requests***) son el componente
central de las contribuciones al código abierto.

<img src="https://i.imgur.com/VA5kiWA.png" width=760 />

## Por que usethis?

Las conexiones son complejas y es fácil equivocarse.

<img src="https://i.imgur.com/3r95UJw.png" width=760 />

## Por que usethis?

[Las ayudantes para solicitudes de fusión de
GitHub](https://usethis.r-lib.org/reference/pr_init.html):

  - Automatizan lo automatizable.
  - Implementan las mejores practicas.
  - Evitan errores.

## Ejemplo

**@forestgeoguest** contribuye a **an-org/abc**:

  - Bifurca y clona el repositorio.
  - Hace cambios y somete una PR.
  - Nota conflictos.
  - Sincroniza, soluciona, y actualiza la PR.
  - Nota que la PR fue aceptada.
  - Finaliza la PR.

## `create_from_github()`

<img src="https://i.imgur.com/8WhfKjZ.png" width=760 />

…

## …

    # Bifurca (Fork) el repositorio fuente en GitHub. 
    # Luego:
    git clone https://github.com/forestgeoguest/abc.git
    cd abc
    
    # forestgeoguest@LAPTOP ~/abc (master)
    git remote add upstream https://github.com/an-org/abc.git
    git pull upstream master

## `git_sitrep()`

<img src="https://i.imgur.com/3VJY7JN.png" width=600 />

    # forestgeoguest@LAPTOP ~/abc (master)
    git remote -v

## `pr_init("pr")`

<img src="https://i.imgur.com/i6NNP9x.png" width=760>

    # forestgeoguest@LAPTOP ~/abc (master)
    git pull upstream master
    git branch pr
    git checkout pr

## `pr_push()`

<img src="https://i.imgur.com/Msc9YGw.png" width = 750 />

    # forestgeoguest@LAPTOP ~/abc (pr)
    git push origin
    git branch --set-upstream-to=origin/pr

## 

### <https://github.com/forestgeoguest/abc/compare/pr>

<img src="https://i.imgur.com/S5FWZMu.png" width = 750 />

<img src="https://i.imgur.com/ND8vC7e.png" width = 750 />

## 

**Pero antes de fusionar la PR, la administradora del repositorio agrega
un cambio al repositorio fuente.**

<img src="https://i.imgur.com/dp64HxK.png" width = 700 />

**Y ese cambio entra en conflicto con la PR.**

<img src="https://i.imgur.com/z9OP7rP.png" width = 700 />

## `pr_sync()`

<img src="https://i.imgur.com/4DwVcTM.png" width = 550 />

    # forestgeoguest@LAPTOP ~/abc (pr)
    # Atajo configurado via `git branch --set-upstream-to=origin/pr`
    git pull
    git pull upstream master
    git push

## Resolver conflictos de fusión

<img src="https://i.imgur.com/bw70s0R.png" width = 750 />

## `pr_push()`

<img src="https://i.imgur.com/lysBvtt.png" width = 700 />

    # forestgeoguest@LAPTOP ~/abc (pr)
    # Reintenta soncronizar
    git pull
    git push

## La solicitud de fusión es aceptada

**“pr” ya no tiene conflictos con “upstream:master”**

<img src="https://i.imgur.com/bVkV0PP.png" width = 650 />

## Historia del repositorio fuente

<img src="https://i.imgur.com/OezvXhH.png" width = 650 />

## `pr_finish()`

<img src="https://i.imgur.com/jT5gfJY.png" width = 750 />

    # forestgeoguest@LAPTOP ~/abc (pr)
    git checkout master
    
    # forestgeoguest@LAPTOP ~/abc (master)
    git pull upstream master
    git push -d origin pr
    git branch -d pr

# **Déjate ayudar por usethis**

**“No subes al nivel de tus metas. Caes el nivel de tus sistemas.” -
[James Clear](https://jamesclear.com/atomic-habits)**

<http://bit.ly/usethis-te-ayuda>
