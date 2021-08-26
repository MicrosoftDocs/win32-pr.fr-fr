---
title: Gestion des erreurs (OpenGL)
description: La fonction gluErrorString récupère les chaînes d’erreur qui correspondent aux codes d’erreur OpenGL ou GLU.
ms.assetid: 59f93c1c-9d15-4980-b246-19257c66b6b8
keywords:
- Utilitaire OpenGL (GLU), codes d’erreur
- GLU (utilitaire OpenGL), codes d’erreur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75ac3fd9010862dd9c567cb7688f7f96286cae06f7e3b0e4ffe73d3b41ca9b67
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120035189"
---
# <a name="handling-errors-opengl"></a>Gestion des erreurs (OpenGL)

La fonction **gluErrorString** récupère les chaînes d’erreur qui correspondent aux codes d’erreur OpenGL ou Glu. Les codes d’erreur OpenGL actuellement définis sont décrits dans [**glGetError**](glgeterror.md). Les codes d’erreur GLU sont répertoriés dans [**gluErrorString**](gluerrorstring.md), [*gluTessCallback*](glutess.md), [*gluQuadricCallback*](gluquadric.md)et [*gluNurbsCallback*](glunurbs.md).

La valeur de retour pour **gluErrorString** est un pointeur vers une chaîne descriptive qui correspond au numéro d’erreur OpenGL, Glu ou glx passé dans le paramètre *ErrorCode* . Les codes d’erreur définis sont décrits dans le *Manuel de référence OpenGL* avec la fonction ou la fonction qui peut les générer.

 

 




