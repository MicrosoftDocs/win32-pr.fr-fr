---
title: Utilisation des fonctions d’anticrénelage
description: Le tableau suivant répertorie les fonctions d’anticrénelage du GL d’IRIS et leurs fonctions OpenGL équivalentes.
ms.assetid: d54990b6-5645-4389-82ca-7d7f0a7fd7e9
keywords:
- Portage de l’IRIS dans le GL, anticrénelage
- Portage à partir de IRIS GL, anticrénelage
- portage vers OpenGL à partir de IRIS GL, anticrénelage
- Portage OpenGL depuis IRIS GL, anticrénelage
- anticrénelage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 896d02dec050c72e59762ff5ee139b0bd091d9a8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104196577"
---
# <a name="using-antialiasing-functions"></a>Utilisation des fonctions d’anticrénelage

Le tableau suivant répertorie les fonctions d’anticrénelage du GL d’IRIS et leurs fonctions OpenGL équivalentes.



| Fonction IRIS GL | Fonction OpenGL                                      | Signification                           |
|------------------|------------------------------------------------------|-----------------------------------|
| **pntsmooth**    | [**glEnable**](glenable.md) ( \_ Smooth point GL \_ )   | Permet l’anticrénelage des points.   |
| **linesmooth**   | **glEnable**(lisse de la \_ ligne GL \_ )                     | Permet l’anticrénelage des lignes.    |
| **polylisse**   | [**glEnable**](glenable.md) ( \_ polygones GL \_ lisse) | Permet l’anticrénelage des polygones. |



 

Utilisez les appels [**glDisable**](gldisable.md) équivalents pour désactiver l’anticrénelage.

Dans IRIS GL, vous pouvez contrôler la qualité de l’anticrénelage en appelant :


```C++
linesmooth(SML_ON + SML_SMOOTHER);
```



OpenGL fournit des [**glHint**](glhint.md)controluse similaires :


```C++
glHint(GL_POINT_SMOOTH_HINT, hintMode); 
glHint(GL_LINE_SMOOTH_HINT, hintMode); 
glHint(GL_POLYGON_SMOOTH_HINT, hintMode);
```



où *hintMode* est l’un des éléments suivants :

-   Grand livrest \_ (utilisez le lissage de qualité le plus élevé).
-   GL plus \_ rapide (utilisez le lissage le plus efficace).
-   comptabilité \_ générale \_

IRIS GL autorise également la correction finale en appelant :


```C++
linesmooth(SML_ON +  SML_END_CORRECT);
```



OpenGL n’a pas d’équivalent pour cette fonction.

 

 




