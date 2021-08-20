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
ms.openlocfilehash: af6990d2292399cb1ccaf00ba6ec42d680c5ace887b2495daf8640db2da30ac5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118132408"
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

 

 




