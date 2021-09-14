---
title: Noms des fonctions OpenGL
description: De nombreuses fonctions OpenGL sont des variations les unes des autres, qui se différencient principalement dans les types de données de leurs arguments.
ms.assetid: 2d30e2e4-9671-4e57-962d-0328b13159f3
keywords:
- OpenGL, noms de fonctions
- noms de fonctions OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e06d04d1acde3ddf9baebd4c5ab44b4f55cb126
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127233543"
---
# <a name="opengl-function-names"></a>Noms des fonctions OpenGL

De nombreuses fonctions OpenGL sont des variations les unes des autres, qui se différencient principalement dans les types de données de leurs arguments. Certaines fonctions diffèrent dans le nombre d’arguments associés et si ces arguments peuvent être spécifiés en tant que vecteurs ou s’ils doivent être spécifiés séparément dans une liste. Par exemple, si vous utilisez la fonction **glVertex2f** , vous devez fournir des coordonnées x et y en tant que nombres à virgule flottante 32 bits ; avec **glVertex3sv**, vous devez fournir un tableau de trois valeurs entières courtes (16 bits) pour x, y et z. Seul le nom de base de la fonction est utilisé dans les rubriques qui suivent. Un astérisque indique que le nom de fonction réel peut être plus grand que ce qui est indiqué. Par exemple, [glVertex \*](glvertex-functions.md) correspond à toutes les variantes de la fonction que vous utilisez pour spécifier des vertex : **glVertex2d**, **glVertex2f**, **glVertex2i**, etc.

L’effet d’une fonction OpenGL peut varier selon que certains modes sont activés ou non. Par exemple, vous devez activer l’éclairage si les fonctions liées à l’éclairage produisent un objet correctement éclairé. Pour activer un mode particulier, utilisez la fonction [**glEnable**](glenable.md) et fournissez la constante appropriée pour identifier le mode (par exemple, l’éclairage du GL \_ ). Pour désactiver un mode, utilisez [**glDisable**](gldisable.md). Consultez **glEnable** pour obtenir la liste complète des modes qui peuvent être activés.

 

 




