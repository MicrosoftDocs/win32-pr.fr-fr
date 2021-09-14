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
ms.openlocfilehash: 3db0ebd8bd13b8d2cee32b8873f697ab073140bd
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127233598"
---
# <a name="matrix-transformations"></a>Transformations de matrice

Les vertex et les normales sont transformés par les matrices de projection et de modelview avant d’être utilisées pour produire une image dans le trame. Utilisez des fonctions telles [**que glMatrixMode**](glmatrixmode.md), [ * *glMultMatrix \** _](glmultmatrix.md), [_*glRotate \**_](glrotate.md), [_*glTranslate \**_](gltranslate.md)et [_*glScale \**_](glscale.md) pour composer les transformations souhaitées. Ou spécifiez des matrices directement avec [_*glLoadMatrix \**_](glloadmatrix.md) et [_ *glLoadIdentity* *](glloadidentity.md). Utilisez [**glPushMatrix**](glpushmatrix.md) et [**glPopMatrix**](glpopmatrix.md) pour enregistrer et restaurer les matrices modelview et de projection sur leurs piles respectives.

 

 




