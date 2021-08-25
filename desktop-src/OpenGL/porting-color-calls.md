---
title: Portage des appels de couleur
description: Le tableau suivant répertorie les fonctions IRIS GL Color et leurs fonctions OpenGL équivalentes.
ms.assetid: 4ca6c311-d6c8-4d10-9e9c-770a8e6de4bb
keywords:
- Portage du GL IRIS, couleur
- Portage à partir de IRIS GL, couleur
- portage vers OpenGL à partir de IRIS GL, couleur
- Portage OpenGL à partir de IRIS GL, couleur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e15774f66964c11527955b57651e69db26f6f3d3704d114fdfa4de9a0d5b97c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119777049"
---
# <a name="porting-color-calls"></a>Portage des appels de couleur

Le tableau suivant répertorie les fonctions IRIS GL Color et leurs fonctions OpenGL équivalentes.



| Fonction IRIS GL                  | Fonction OpenGL                                                                                                                               | Signification                                              |
|-----------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| **c**                             | [glColor](glcolor-functions.md)                                                                                                              | Définit la couleur RVB.                                      |
| **color**                         | [glIndex](glindex-functions.md)                                                                                                              | Définit l’index de couleur.                                |
| **GetColor**                      | [**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) (index actuel de la comptabilité \_ \_ )                                               | Retourne l’index de couleur actuel.                     |
| **getmcolor**                     |                                                                                                                                               | Obtient une copie des valeurs RVB pour une entrée de la carte des couleurs. |
| **gRGBcolor**                     | **glGet**( \_ couleur actuelle du GL \_ )                                                                                                               | Obtient les valeurs de couleur RVB actuelles.                   |
| **mapcolor**                      |                                                                                                                                               |                                                      |
| **RGBcolor**                      | **glColor**                                                                                                                                   | Définit la couleur RVB.                                      |
| **writemask**                     | [**glIndexMask**](glindexmask.md)                                                                                                            | Définit le masque de couleur du mode d’index des couleurs.                |
| **wmpackRGBwritemask**<br/> | [**glColorMask**](glcolormask.md)                                                                                                            | Définit le masque du mode de couleurs RVB.                        |
| **getwritemask**                  | [**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) (GL \_ Color \_ WRITEMASK)**glGet**(GL \_ index \_ WRITEMASK)<br/> | Obtient le masque de couleur.                                 |
| **gRGBmask**                      | **glGet**( \_ couleur GL \_ WRITEMASK)                                                                                                             | Obtient le masque de couleur.                                 |
| **zwritemask**                    | [**glDepthMask**](gldepthmask.md)                                                                                                            |                                                      |



 

> [!Note]
>
> Soyez prudent lors du remplacement de **zwritemask** par [**glDepthMask**](gldepthmask.md); **glDepthMask** accepte un argument booléen, tandis que **zwritemask** prend un champ de bits.

 

si vous souhaitez utiliser plusieurs cartes de couleurs, vous devez utiliser les fonctions de mappage des couleurs Windows appropriées. Par conséquent, **Multimap**, **onemap**, **getcmmode**, **setmap** et **GetMap** n’ont pas d’équivalents OpenGL.

 

 





