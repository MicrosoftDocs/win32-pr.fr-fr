---
title: Portage de l’écran et des commandes de vidage de la mémoire tampon
description: OpenGL remplace toute une série de fonctions d’IRIS du GL en clair (telles que zclear, aclear, sclear, etc.) par une seule fonction, glClear. Spécifiez exactement ce que vous souhaitez effacer en transmettant des masques à glClear.
ms.assetid: 52ba503d-e412-4815-a039-a039b41327f4
keywords:
- Le portage du GL IRIS, fonctions Clear
- Portage à partir de IRIS GL, fonctions Clear
- portage vers OpenGL à partir de IRIS GL, fonctions Clear
- Portage OpenGL à partir de IRIS GL, fonctions Clear
- fonctions Clear
- Portage des commandes d’affichage de l’écran
- Portage à partir de IRIS GL, commandes d’effacement d’écran
- portage vers OpenGL à partir de l’IRIS GL, commandes d’effacement d’écran
- Portage OpenGL à partir de IRIS GL, commandes d’effacement d’écran
- commandes d’effacement d’écran
- Portage de l’IRIS dans le GL, commandes de vidage de la mémoire tampon
- Portage à partir de IRIS GL, commandes de vidage de mémoire tampon
- portage vers OpenGL à partir de l’IRIS GL, commandes de vidage de la mémoire tampon
- Portage OpenGL à partir de IRIS GL, commandes de vidage de mémoire tampon
- commandes de vidage de la mémoire tampon
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fbff0fed3472fd4374605cb96dbae845998c0ba2d8ce488420f9b4c6895a07c9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117794874"
---
# <a name="porting-screen-and-buffer-clearing-commands"></a>Portage de l’écran et des commandes de vidage de la mémoire tampon

OpenGL remplace toute une série de fonctions d’IRIS du GL en **clair** (telles que **zclear**, **aclear**, **sclear**, etc.) par une seule fonction, [**glClear**](glclear.md). Spécifiez exactement ce que vous souhaitez effacer en transmettant des masques à **glClear**.

Gardez les points suivants à l’esprit lors du Portage des commandes de mémoire tampon et d’écran :

-   OpenGL gère l’effacement des couleurs séparément des couleurs de dessin, avec des appels tels que [**glClearColor**](glclearcolor.md) et [**glClearIndex**](glclearindex.md). Veillez à définir la couleur d’effacement pour chaque mémoire tampon avant l’effacement.
-   Au lieu d’utiliser l’un des nombreux appels Clear nommés différemment, vous désactivez maintenant plusieurs mémoires tampons avec un appel, [**glClear**](glclear.md), par **ou** ING. Par exemple, **czclear** est remplacé par :

    ``` syntax
    glClear( GL_COLOR_BUFFER_BIT | GL_DEPTH_BUFFER_BIT )
    ```

-   IRIS GL fait référence au polygone stipple et à la couleur writemask. OpenGL ignore le polygone stipple mais référence la couleur writemask. (La fonction **czclear** ignore les deux polygones stipple et Color writemask.)

Le tableau suivant répertorie les différentes fonctions IRIS GL Clear avec leurs fonctions OpenGL équivalentes.



| Appel du GL IRIS         | Appel OpenGL                                                               | Signification                                           |
|----------------------|---------------------------------------------------------------------------|---------------------------------------------------|
| **acbuf**(AC \_ Clear) | **glClear**( \_ bit de tampon amort GL \_ \_ )                                     | Effacez la mémoire tampon d’accumulation.                    |
|                      | **glClearColor**                                                          | Définissez la couleur d’effacement RVBA.                         |
|                      | **glClearIndex**                                                          | Définissez l’index Clear-Color.                        |
| **clear**            | **glClear**( \_ bits de \_ mémoire tampon de couleur GL \_ )                                     | Effacez la mémoire tampon de couleur.                           |
|                      | **glClearDepth**                                                          | Spécifiez la valeur Clear pour la mémoire tampon de profondeur.     |
| **zclear**           | **glClear**(bits de la \_ mémoire tampon de profondeur GL \_ \_ )                                     | Effacez le tampon de profondeur.                           |
| **czclear**          | **glClear**(bits de la mémoire tampon de la couleur GL- \_ \_ bit de \_ \| \_ mémoire tampon de profondeur GL \_ \_ )<br/> | Effacez la mémoire tampon de couleur et la mémoire tampon de profondeur.      |
|                      | **glClearAccum**                                                          | Spécifiez des valeurs claires pour la mémoire tampon d’accumulation. |
|                      | **glClearStencil**                                                        | Spécifiez la valeur Clear pour la mémoire tampon du stencil.   |
| **sclear**           | **glClear**(bits de tampon de stencil du GL \_ \_ \_ )                                   | Effacez la mémoire tampon du stencil.                         |



 

Lorsque votre code de la comptabilité IRIS utilise à la fois **gclear** et **sclear**, vous pouvez les combiner en un seul appel **glClear** . peut améliorer les performances de votre programme.

 

 





