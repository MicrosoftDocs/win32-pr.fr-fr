---
title: Points de Portage
description: OpenGL n’a aucune commande pour dessiner un point unique. Sinon, les fonctions de point de Portage sont simples. Le tableau suivant répertorie les fonctions d’IRIS dans le GL pour les points de dessin et leurs fonctions OpenGL équivalentes.
ms.assetid: 348c7767-321a-43c6-bc88-7dc00f426f50
keywords:
- Portage de l’IRIS dans le GL, points
- Portage à partir de IRIS GL, points
- portage vers OpenGL à partir de IRIS GL, points
- Portage OpenGL à partir de IRIS GL, points
- fonctions de dessin, points
- points
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18ef24ad81942681b3d70a303a22e89e9573aa609d3f08f52a92583ae88e0e9a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119012067"
---
# <a name="porting-points"></a>Points de Portage

OpenGL n’a aucune commande pour dessiner un point unique. Sinon, les fonctions de point de Portage sont simples. Le tableau suivant répertorie les fonctions d’IRIS dans le GL pour les points de dessin et leurs fonctions OpenGL équivalentes.



| Fonction IRIS GL           | Fonction OpenGL                                                   | Signification                                                                                                                                              |
|----------------------------|-------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| **PNT**                    |                                                                   | Dessine un point unique.                                                                                                                                |
| **bgnpoint**, **point de terminaison** | [**glBegin**](glbegin.md) ( \_ points GL), [ **glEnd**](glend.md) | Interprète les vertex comme des points.                                                                                                                       |
| **pntsize**                | [**glPointSize**](glpointsize.md)                                | Définit la taille du point en pixels.                                                                                                                           |
| **pntsmooth**              | [**glEnable**](glenable.md) ( \_ Smooth point GL \_ )                | Active l’anticrénelage de point. (Pour plus d’informations sur l’anticrénelage des points, consultez [Portage de fonctions d’anticrénelage](porting-antialiasing-functions.md).) |



 

Pour plus d’informations sur les fonctions d’extraction associées, consultez [**glPointSize**](glpointsize.md).

??

 

 




