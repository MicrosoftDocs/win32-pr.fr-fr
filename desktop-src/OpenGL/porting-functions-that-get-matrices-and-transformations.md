---
title: Portage de fonctions qui obtiennent des matrices et des transformations
description: Le tableau suivant répertorie les fonctions d’IRIS GL qui obtiennent l’état des matrices et des transformations et leurs équivalents OpenGL.
ms.assetid: 53546bc0-ce1d-47e0-ab5e-5d6789c6db2a
keywords:
- Portage de l’IRIS dans le GL, matrices
- Portage à partir de IRIS GL, matrices
- portage vers OpenGL à partir de IRIS GL, matrices
- Portage OpenGL à partir de IRIS GL, matrices
- matrices
- Portage de l’IRIS dans le GL, transformations
- Portage à partir de IRIS GL, transformations
- portage vers OpenGL à partir de IRIS GL, transformations
- Portage OpenGL depuis IRIS GL, transformations
- transformations
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93b32ab017e81c9875666785786b29d9c94c7fd1
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127119110"
---
# <a name="porting-functions-that-get-matrices-and-transformations"></a>Portage de fonctions qui obtiennent des matrices et des transformations

Le tableau suivant répertorie les fonctions d’IRIS GL qui obtiennent l’état des matrices et des transformations et leurs équivalents OpenGL.



| Requête Matrix GL IRIS                  | Requête de matrice glGet OpenGL         | Signification                                                         |
|---------------------------------------|-----------------------------------|-----------------------------------------------------------------|
| **getmmode**                          | \_mode de matrice du GL \_                  | Retourne le mode matrice actuel.                                |
| **getmatrix** en mode **MVIEWING**    | \_matrice MODELVIEW \_ GL             | Retourne une copie de la matrice de vue de modèle actuelle.                |
| **getmatrix** en mode **MPROJECTION** | \_matrice de projection GL \_            | Retourne une copie de la matrice de projection actuelle.                |
| **getmatrix** en mode **MTEXTURE**    | \_matrice de texture GL \_               | Retourne une copie de la matrice de texture actuelle.                   |
| Non applicable.                       | \_profondeur de \_ la \_ pile \_ MODELVIEW GL Max  | Retourne la profondeur maximale prise en charge de la pile de matrices de vue de modèle. |
| Non applicable.                       | profondeur de la \_ \_ pile de projection Max \_ GL \_ | Retourne la profondeur maximale prise en charge de la pile de la matrice de projection. |
| Non applicable.                       | profondeur de la \_ \_ pile de texture Max \_ . GL \_    | Retourne la profondeur maximale prise en charge de la pile de matrices de texture.    |
| Non applicable.                       | profondeur de la \_ pile MODELVIEW GL \_ \_       | Retourne le nombre de matrices sur la pile de la vue de modèle.             |
| Non applicable.                       | profondeur de la \_ pile de projection GL \_ \_      | Retourne le nombre de matrices sur la pile de projection.             |
| Non applicable.                       | profondeur de la \_ pile de textures GL \_ \_         | Retourne le nombre de matrices sur la pile de texture.                |



 

??

 

 




