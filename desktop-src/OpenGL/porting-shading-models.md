---
title: Portage de modèles d’ombrage
description: Comme IRIS GL, OpenGL vous permet de basculer entre l’ombrage lisse (Gouraud) et l’ombrage plat. Le tableau suivant répertorie les fonctions d’ombrage et de tramage de l’IRIS et leurs fonctions OpenGL équivalentes.
ms.assetid: 93e8f437-381f-4620-ad6f-52ce830d99b6
keywords:
- Portage de l’IRIS dans le GL, ombrage
- Portage à partir de IRIS GL, ombrage
- portage vers OpenGL à partir de IRIS GL, ombrage
- Portage OpenGL à partir de IRIS GL, ombrage
- ombrage lissé
- Ombrage Gouraud
- ombrage plat
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ee4265341e17843dbe4752bb51e5728aa54914ec5670c08b6b7921537050a6f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119012037"
---
# <a name="porting-shading-models"></a>Portage de modèles d’ombrage

Comme IRIS GL, OpenGL vous permet de basculer entre l’ombrage lisse (Gouraud) et l’ombrage plat. Le tableau suivant répertorie les fonctions d’ombrage et de tramage de l’IRIS et leurs fonctions OpenGL équivalentes.



| Fonction IRIS GL                                   | Fonction OpenGL                                                                                    | Signification                      |
|----------------------------------------------------|----------------------------------------------------------------------------------------------------|------------------------------|
| **shademodel**(plat)                               | [**glShadeModel**](glshademodel.md) (GL \_ plat)                                                  | Il s’agit d’un ombrage plat.           |
| **shademodel**(Gouraud)                            | **glShadeModel**(GL \_ Smooth)                                                                     | Effectue un ombrage lissé.         |
| **est**                                          | [**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) ( \_ modèle d’ombrage GL \_ )      | Retourne le modèle d’ombrage actuel. |
| **tramage (DT** \_ on) **tramé**(DT \_ off) <br/> | [**glEnable**](glenable.md) (GL de \_ tramage)[**glDisable**](gldisable.md)(GL de \_ tramage)<br/> | Active/désactive le tramage.      |



 

??

 

 





