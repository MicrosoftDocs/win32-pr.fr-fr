---
title: Traduction de texgen
description: La fonction IRIS GL texgen est traduite en glTexGen pour OpenGL.
ms.assetid: ddf398ed-37d4-4fb6-97be-20fe0564cb77
keywords:
- Portage de l’IRIS dans le GL, texture
- Portage à partir de IRIS GL, texture
- portage vers OpenGL à partir de IRIS GL, texture
- Portage OpenGL à partir de IRIS GL, texture
- texture
- Portage du grand livre de l’IRIS, texgen
- Portage à partir de IRIS GL, texgen
- portage vers OpenGL à partir de IRIS GL, texgen
- Portage OpenGL à partir de IRIS GL, texgen
- texgen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 07654fc35e20096ed71c3fe74ff9279214eb45c8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106510844"
---
# <a name="translating-texgen"></a>Traduction de texgen

La fonction IRIS GL **texgen** est traduite en [glTexGen](gltexgen-functions.md) pour OpenGL.

Avec IRIS GL, vous appelez **texgen** deux fois : une fois pour définir simultanément le mode et l’équation plan, et une fois pour activer la génération des coordonnées de texture. Par exemple :


```C++
texgen(TX_S, TG_LINEAR, planeParams); 
texgen(TX_S, TG_ON, NULL);
```



Avec OpenGL, vous effectuez trois appels : deux à **glTexGen** (une fois pour définir le mode et une fois pour définir l’équation du plan) et un à [**glEnable**](glenable.md). Par exemple, le code OpenGL équivalent au code de la comptabilité IRIS ci-dessus est le suivant :


```C++
glTexGen(GL_S, GLTEXTURE_GEN_MODE, modeName); 
glTextGen(GL_S, GL_OBJECT_PLANE, planeParameters); 
glEnable(GL_TEXTURE_GEN_S);
```



Le tableau suivant répertorie les noms des coordonnées de texture et leurs équivalents OpenGL.



| Coordonnée de texture du GL IRIS | Coordonnée de texture OpenGL | argument glEnable   |
|----------------------------|---------------------------|---------------------|
| TX \_ S                      | GL \_ S                     | GL \_ texture \_ GEN \_ S |
| TX \_ T                      | GL \_ T                     | GL \_ texture \_ GEN \_ T |
| TX \_ R                      | GL \_ R                     | GL \_ texture \_ GEN \_ R |
| TX \_ Q                      | \_Q                     | GL \_ texture \_ GEN \_ Q |



 

Le tableau suivant répertorie les modes de génération de texture de l’IRIS dans le GL ainsi que les modes de texture et les noms de plans OpenGL équivalents.



| Mode de texture du GL IRIS | Mode de texture OpenGL | Nom du plan OpenGL |
|----------------------|---------------------|-------------------|
| TG en \_ linéaire           | \_objet \_ linéaire de la comptabilité  | \_plan d’objet GL \_ |
| \_contour TG          | linéaire de l' \_ oeil GL \_     | \_plan oculaire \_ GL    |
| TG \_ SPHEREMAP        | \_carte de sphère GL \_     |                   |



 

 

 




