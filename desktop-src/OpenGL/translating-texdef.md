---
title: Traduction de texdef
description: L’exemple de code suivant est une définition de texture de la comptabilité IRIS
ms.assetid: bb2d257d-ee74-4a65-b364-c7a97bccaa78
keywords:
- Portage de l’IRIS dans le GL, texture
- Portage à partir de IRIS GL, texture
- portage vers OpenGL à partir de IRIS GL, texture
- Portage OpenGL à partir de IRIS GL, texture
- texture
- Portage du grand livre de l’IRIS, texdef
- Portage à partir de IRIS GL, texdef
- portage vers OpenGL à partir de IRIS GL, texdef
- Portage OpenGL à partir de IRIS GL, texdef
- texdef
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 479af06bcfd3a50daf56fb0629e4c32f24750081
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840694"
---
# <a name="translating-texdef"></a>Traduction de texdef

L’exemple de code suivant est une définition de texture de la comptabilité IRIS :


```C++
float texprops[] = { TX_MINFILTER, TX_POINT, 
                         TX_MAGFILTER, TX_POINT, 
                         TX_WRAP_S, TX_REPEAT, 
                         TX_WRAP_T, TX_REPEAT, 
                         TX_NULL }; 
 
textdef2d(1, 1, 6, 6, granite_texture, 7, texprops);
```



Dans l’exemple précédent, **texdef** spécifie le \_ filtre de point de transmission en tant que Zoom et le filtre de minimisation, et TX \_ REPEAT comme mécanisme d’habillage. Il spécifie également l’image de texture : **\_ texture granit**.

Dans OpenGL, [**glTexImage**](glteximage1d.md) spécifie l’image et [glTexParameter](gltexparameter-functions.md) définit la propriété. Pour traduire les définitions de texture d’IRIS GL, remplacez la fonction **textdef** par **glTexImage** et un ou plusieurs appels à **glTexParameter**.

Le code de la comptabilité IRIS précédent ressemble à celui-ci lorsqu’il est traduit en OpenGL :


```C++
GLfloat nearest[] = {GL_NEAREST}; 
GLfloat repeat = {GL_REPEAT}; 
glTexParameterfv( GL_TEXTURE_1D, GL_TEXTURE_MIN_FILTER, nearest); 
glTexParameterfv( GL_TEXTURE_1D, GL_TEXTURE_MAGILTER, nearest); 
glTexParameterfv( GL_TEXTURE_1D, GL_TEXTURE_WRAP_S, repeat); 
glTexParameterfv( GL_TEXTURE_1D, GL_TEXTURE_WRAP_T, nearest); 
glTexImage1D( GL_TEXTURE_1D, 0, 1, 6, 0, GL_RGB, GL_UNSIGNED_SHORT, granite_texture);
```



Le tableau suivant répertorie les paramètres d’IRIS GL texture et leurs paramètres OpenGL équivalents.



| Paramètre de texture IRIS GL | Paramètre de texture OpenGL                                  |
|---------------------------|-----------------------------------------------------------|
| TX \_ MINFILTER             | filtre de la \_ texture GL \_ min. \_                                  |
| TX \_ MAGFILTER             | filtre de la \_ texture GL \_ \_                                  |
| TX \_ Wrap, TX \_ Wrap \_ S     | \_ \_ encapsuler la texture GL \_ S                                      |
| TX \_ Wrap, TX \_ Wrap \_ T     | \_couleur de \_ bordure de la \_ texture TGL de la \_ \_ texture \_ GL<br/> |



 

Le tableau suivant répertorie les valeurs possibles des paramètres de texture IRIS GL et leurs paramètres OpenGL équivalents.



| Paramètre de texture IRIS GL | Paramètre de texture OpenGL     |
|---------------------------|------------------------------|
| POINT de transmission \_                 | GL \_ le plus proche                  |
| unilinéaire TX \_              | linéaire du GL \_                   |
| \_point MIPMAP \_ TX         | MIPMAP du GL le plus proche \_ \_ \_ le plus proche |
| \_MIPMAP en \_ BIlinéaire TX      | \_MIPMAP linéaire \_ GL \_ le plus proche  |
| \_MIPMAP TX \_ linéaire        | MIPMAP linéaire de la comptabilité la \_ plus proche \_ \_  |
| TX \_ TRIlinéaire             | MIPMAP linéaire du GL du GL \_ \_ \_   |



 

 

 





