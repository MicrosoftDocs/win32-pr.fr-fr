---
title: Triangles de Portage
description: Vous pouvez dessiner trois types de triangles dans OpenGL séparent les triangles, les bandes triangulaires et les ventilateurs à triangle.
ms.assetid: 48617892-c9a0-4c67-b42e-afa4243023e7
keywords:
- Portage de l’IRIS dans le GL, triangles
- Portage à partir de IRIS GL, triangles
- portage vers OpenGL à partir de IRIS GL, triangles
- Portage OpenGL à partir de IRIS GL, triangles
- fonctions de dessin, triangles
- triangles
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85acc650a709650495b93cdd00176400f00168cc8fe6445a23505f12b332abf9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119011997"
---
# <a name="porting-triangles"></a>Triangles de Portage

Vous pouvez dessiner trois types de triangles dans OpenGL : des triangles distincts, des bandes triangulaires et des ventilateurs à triangle.

OpenGL n’a pas d’équivalent pour la fonction IRIS GL **swaptmesh** . Vous pouvez obtenir le même effet à l’aide d’une combinaison de triangles, de bandes triangulaires et de ventilateurs triangulaires.

Le tableau suivant répertorie les fonctions IRIS GL permettant de dessiner des triangles et leurs fonctions OpenGL équivalentes.



| Fonction IRIS GL           | Paramètre glBegin équivalent | Signification                                       |
|----------------------------|------------------------------|-----------------------------------------------|
|                            | \_TRIangles GL                | Triples de vertex interprétés comme des triangles. |
| **bgntmesh**, **endtmesh** | \_bande triangulaire GL \_          | Bandes liées de triangles.                   |
|                            | \_ventilateur à triangles GL \_            | Ventilateurs liés d’un triangle.                     |



 

??

 

 




