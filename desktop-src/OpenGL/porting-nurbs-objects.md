---
title: Portage d’objets NURBS
description: OpenGL traite la courbe NURBS comme des objets, de la même manière qu’elle traite Quadrics vous créez un objet NURBS, puis spécifiez la façon dont il doit être rendu. Le tableau suivant répertorie les fonctions GLU OpenGL pour la gestion des objets NURBS.
ms.assetid: baddf81b-219f-44bb-aa17-37404028b258
keywords:
- Portage de l’IRIS dans le GL, objets NURBS
- Portage à partir de IRIS GL, objets NURBS
- portage vers OpenGL à partir de IRIS GL, objets NURBS
- Portage OpenGL à partir de IRIS GL, objets NURBS
- Objets NURBS
- NURBS (non-uniform rational B-spline)
- B-spline rationnelle non uniforme (NURBS)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e0e56c06eea4e4a9a48f9062205277f8b999499
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104380117"
---
# <a name="porting-nurbs-objects"></a>Portage d’objets NURBS

OpenGL traite la courbe NURBS comme des objets, de la même manière qu’elle traite Quadrics : vous créez un objet NURBS, puis vous spécifiez comment il doit être rendu. Le tableau suivant répertorie les fonctions GLU OpenGL pour la gestion des objets NURBS.



| Fonction OpenGL GLU                                      | Signification                                                        |
|----------------------------------------------------------|----------------------------------------------------------------|
| [**gluNewNurbsRenderer**](glunewnurbsrenderer.md)       | Crée un nouvel objet NURBS.                                    |
| [**gluDeleteNurbsRenderer**](gludeletenurbsrenderer.md) | Supprime un objet NURBS.                                        |
| [*gluNurbsCallback*](glunurbs.md)                       | Associe un rappel à un objet NURBS pour la gestion des erreurs. |



 

Lors du Portage du code NURBS du GL IRIS vers OpenGL, gardez les points suivants à l’esprit :

-   Les points de contrôle NURBS sont des valeurs float, et non des doubles.
-   Le paramètre Stride est compté en valeurs float, et non en octets.
-   Si vous utilisez l’éclairage et que vous ne spécifiez pas de normales, appelez [**glEnable**](glenable.md) avec GL \_ auto \_ normal comme paramètre pour générer automatiquement des normales.

??

 

 




