---
title: Gestion des erreurs (OpenGL)
description: La fonction gluErrorString récupère les chaînes d’erreur qui correspondent aux codes d’erreur OpenGL ou GLU.
ms.assetid: 59f93c1c-9d15-4980-b246-19257c66b6b8
keywords:
- Utilitaire OpenGL (GLU), codes d’erreur
- GLU (utilitaire OpenGL), codes d’erreur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab319fd978cd5ea901133fc9961caf1c66f3185d
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104316985"
---
# <a name="handling-errors-opengl"></a>Gestion des erreurs (OpenGL)

La fonction **gluErrorString** récupère les chaînes d’erreur qui correspondent aux codes d’erreur OpenGL ou Glu. Les codes d’erreur OpenGL actuellement définis sont décrits dans [**glGetError**](glgeterror.md). Les codes d’erreur GLU sont répertoriés dans [**gluErrorString**](gluerrorstring.md), [*gluTessCallback*](glutess.md), [*gluQuadricCallback*](gluquadric.md)et [*gluNurbsCallback*](glunurbs.md).

La valeur de retour pour **gluErrorString** est un pointeur vers une chaîne descriptive qui correspond au numéro d’erreur OpenGL, Glu ou glx passé dans le paramètre *ErrorCode* . Les codes d’erreur définis sont décrits dans le *Manuel de référence OpenGL* avec la fonction ou la fonction qui peut les générer.

 

 




