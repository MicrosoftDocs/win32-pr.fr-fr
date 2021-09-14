---
title: Portage des fonctions de texture
description: Portage des fonctions de texture
ms.assetid: 03e0b0fc-3812-4744-a0f1-3dcb466d679d
keywords:
- Portage de l’IRIS dans le GL, texture
- Portage à partir de IRIS GL, texture
- portage vers OpenGL à partir de IRIS GL, texture
- Portage OpenGL à partir de IRIS GL, texture
- texture
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b2cba8b105089553084a93f997517d19cf371e8
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127311726"
---
# <a name="porting-texture-functions"></a>Portage des fonctions de texture

Lors du Portage des fonctions de texture du GL IRIS vers OpenGL, gardez les points suivants à l’esprit :

-   OpenGL ne gère pas les tables de textures ; elle utilise une texture 1D et une texture 2D uniquement. Pour réutiliser les textures de votre code IRIS GL, placez-les dans une liste d’affichage.
-   OpenGL ne génère pas automatiquement des mipmaps. Si vous utilisez des mipmaps, vous devez d’abord appeler la fonction [**gluBuild2DMipmaps**](glubuild2dmipmaps.md) .
-   Dans OpenGL, vous utilisez [**glEnable**](glenable.md) et [**glDisable**](gldisable.md) pour activer et désactiver les fonctionnalités de texture.
-   Dans OpenGL, la taille de la texture est plus rigoureusement régulée que dans IRIS GL. La taille d’une texture OpenGL doit être :

    2 *n* + 2 *b*

    où *n* est un entier et *b* est :

    -   0, si la texture n’a pas de bordure
    -   1, si la texture a un pixel de bordure (les textures OpenGL peuvent avoir des bordures de 1 pixel.)

Le tableau suivant répertorie les fonctions de texture de l’IRIS dans le GL et leurs équivalents OpenGL généraux.



| Fonction IRIS GL | Fonction OpenGL                                                                                                                                                                                                                                                       | Signification                                                                                     |
|------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| **textdef2d**    | [**glTexImage2D**](glteximage2d.md)[**glTexParameter**](gltexparameter-functions.md)<br/> [**gluBuild2DMipmaps**](glubuild2dmipmaps.md)<br/>                                                                                                           | Spécifie une image de texture 2D.                                                              |
| **textbind**     | **glTexImage2DglTexParameter**<br/> **gluBuild2DMipmaps**<br/>                                                                                                                                                                                            | Sélectionne une fonction de texture.                                                                 |
| **tevdef**       | [**glTexEnv**](gltexenv-functions.md)                                                                                                                                                                                                                                | Définit un environnement de mappage de texture.                                                      |
| **tevbind**      | **glTexEnv**[**glTexImage1D**](glteximage1d.md)<br/>                                                                                                                                                                                                           | Sélectionne un environnement de texture.                                                              |
| **H2**           | [**glTexCoord**](gltexcoord-functions.md)                                                                                                                                                                                                                            | Définit les coordonnées de texture actuelles.                                                       |
| **texgen**       | [**glTexGen**](gltexgen-functions.md)[**glGetTexParameter**](glgettexparameter.md)<br/> [**gluBuild1DMipmaps**](glubuild1dmipmaps.md)<br/> [**gluBuild2DMipmaps**](glubuild2dmipmaps.md)<br/> [**gluScaleImage**](gluscaleimage.md)<br/> | Contrôle la génération des coordonnées de texture. Met à l’échelle une image à une taille arbitraire.<br/> |



 

Pour plus d’informations sur la texturation, consultez le *Guide de programmation OpenGL*.

Cette rubrique contient des informations sur les éléments suivants.

-   [Traduction de tevdef](translating-tevdef.md)
-   [Traduction de texdef](translating-texdef.md)
-   [Traduction de texgen](translating-texgen.md)

 

 





