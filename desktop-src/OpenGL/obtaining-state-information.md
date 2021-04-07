---
title: Obtention d’informations d’État
description: Obtention d’informations d’État
ms.assetid: 86fc8503-92b9-4b5b-8a28-4c9783983ac6
keywords:
- OpenGL, informations d’État
- OpenGL, variables d’État
- informations d’État OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cfac92233e971104fd4d343970a9ecc79496ed54
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103672678"
---
# <a name="obtaining-state-information"></a>Obtention d’informations d’État

OpenGL gère de nombreuses variables d’État qui affectent le comportement de nombreuses fonctions. Certaines de ces variables ont des fonctions de requête spécialisées.



|                                          |                                                    |                                                          |
|------------------------------------------|----------------------------------------------------|----------------------------------------------------------|
| [**glGetClipPlane**](glgetclipplane.md) | [**glGetPixelMap**](glgetpixelmap.md)             | [**glGetTexImage**](glgetteximage.md)                   |
| [**glGetLight**](glgetlight.md)         | [**glGetPolygonStipple**](glgetpolygonstipple.md) | [**glGetTexLevelParameter**](glgettexlevelparameter.md) |
| [**glGetMap**](glgetmap.md)             | [**glGetTexEnv**](glgettexenv.md)                 | [**glGetTexParameter**](glgettexparameter.md)           |
| [**glGetMaterial**](glgetmaterial.md)   | [**glGetTexGen**](glgettexgen.md)                 |                                                          |



 

Pour obtenir la valeur d’autres variables d’État, utilisez [**glGetBooleanv**](glgetbooleanv.md), [**glGetDoublev**](glgetdoublev.md), [**glGetFloatv**](glgetfloatv.md)ou [**glGetIntegerv**](glgetintegerv.md), selon le cas. Pour plus d’informations sur l’utilisation de ces fonctions, consultez [**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) . Les autres fonctions de requête que vous pouvez utiliser sont [**glGetError**](glgeterror.md), [**glGetString**](glgetstring.md)et [**glIsEnabled**](glisenabled.md). (Pour plus d’informations sur les fonctions liées à la gestion des erreurs, consultez [gestion des erreurs](handling-errors.md) .) Pour enregistrer et restaurer des ensembles de variables d’État, utilisez [**glPushAttrib**](glpushattrib.md) et [**glPopAttrib**](glpopattrib.md).

-   [Utilisation des fonctions de requête](using-the-query-functions.md)
-   [Gestion des erreurs](error-handling.md)
-   [Codes d’erreur OpenGL](opengl-error-codes.md)
-   [Enregistrement et restauration de jeux de variables d’État](saving-and-restoring-sets-of-state-variables.md)
-   [Variables d’État OpenGL](opengl-state-variables.md)
-   [Informations de référence sur l’État](state-information-reference.md)

 

 




