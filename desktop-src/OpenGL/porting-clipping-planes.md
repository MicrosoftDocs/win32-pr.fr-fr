---
title: Portage des plans de découpage
description: OpenGL implémente les plans de découpage de la même façon que l’IRIS GL. En outre, dans OpenGL, vous pouvez interroger des plans de découpage. Le tableau suivant répertorie les fonctions d’IRIS dans le plan de découpage du GL et leurs fonctions OpenGL équivalentes.
ms.assetid: bfca59c3-b7ef-4545-8b8d-022ea782569b
keywords:
- Portage de l’IRIS dans le GL, plans de découpage
- Portage à partir de IRIS GL, plans de découpage
- portage vers OpenGL à partir de IRIS GL, plans de découpage
- Portage OpenGL à partir de IRIS GL, plans de découpage
- plans de découpage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d3b531b39daf6670a3a99d9a4cbcf55158ea2d4f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103675254"
---
# <a name="porting-clipping-planes"></a>Portage des plans de découpage

OpenGL implémente les plans de découpage de la même façon que l’IRIS GL. En outre, dans OpenGL, vous pouvez interroger des plans de découpage. Le tableau suivant répertorie les fonctions d’IRIS dans le plan de découpage du GL et leurs fonctions OpenGL équivalentes.



| Fonction IRIS GL                          | Fonction OpenGL                                                                               | Signification                                  |
|-------------------------------------------|-----------------------------------------------------------------------------------------------|------------------------------------------|
| **clipplane** (i, **CP \_ on**, params)     | [**glEnable**](glenable.md) ( \_ plan de coupe GL \_ )                                             | Active le découpage sur le plan i.             |
| **clipplane**(i, **CP \_ define**, plan) | [**glClipPlane**](glclipplane.md) ( \_ plan de coupe GL \_ , plan)                                | Définit le plan de découpage.                  |
|                                           | [**glGetClipPlane**](glgetclipplane.md)                                                      | Retourne l’équation du plan de découpage.         |
|                                           | [**glIsEnabled**](glisenabled.md) ( \_ plan de coupe GL \_ )                                       | Retourne la valeur true si le plan de découpage est activé. |
| **scrmask**                               | [**glScissor**](glscissor.md)                                                                | Définit la zone de ciseaux.                 |
| **getscrmask**                            | [**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) (zone de ciseaux de GL \_ \_ ) | Retourne la zone de la ciseaux actuelle.         |



 

Pour activer le test de ciseaux, appelez **glEnable** à l’aide de \_ \_ la zone de ciseaux du GL comme paramètre.

??

 

 




