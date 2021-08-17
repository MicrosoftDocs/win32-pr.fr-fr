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
ms.openlocfilehash: ab36f41e3b639447b4f246d706e11c134d8f920528cde1e946d26af057a95951
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117980345"
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

 

 




