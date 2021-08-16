---
title: Transformations de matrice
description: Les vertex et les normales sont transformés par les matrices de projection et de modelview avant d’être utilisées pour produire une image dans le trame.
ms.assetid: 9fd0b236-9152-4494-b5c7-dadb5943269e
keywords:
- Pipeline de traitement OpenGL, matrices
- matrices OpenGL
- matrice modelview
- matrice de projection
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0e3c88ffcfebc989400cfa9a85c16f355c0a7090ff4d16531cf03c3697ee869
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118937318"
---
# <a name="matrix-transformations"></a>Transformations de matrice

Les vertex et les normales sont transformés par les matrices de projection et de modelview avant d’être utilisées pour produire une image dans le trame. Utilisez des fonctions telles [**que glMatrixMode**](glmatrixmode.md), [ * *glMultMatrix \** _](glmultmatrix.md), [_*glRotate \**_](glrotate.md), [_*glTranslate \**_](gltranslate.md)et [_*glScale \**_](glscale.md) pour composer les transformations souhaitées. Ou spécifiez des matrices directement avec [_*glLoadMatrix \**_](glloadmatrix.md) et [_ *glLoadIdentity* *](glloadidentity.md). Utilisez [**glPushMatrix**](glpushmatrix.md) et [**glPopMatrix**](glpopmatrix.md) pour enregistrer et restaurer les matrices modelview et de projection sur leurs piles respectives.

 

 




