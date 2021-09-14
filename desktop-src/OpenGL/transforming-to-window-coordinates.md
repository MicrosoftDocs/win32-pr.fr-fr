---
title: Transformer en coordonnées de fenêtre
description: Avant que les coordonnées de clip soient converties en coordonnées de fenêtre, elles sont divisées par la valeur de w pour produire des coordonnées de périphérique normalisées.
ms.assetid: 4c2d0bf6-89e8-485a-9080-c0599f989943
keywords:
- Pipeline de traitement OpenGL, conversion en coordonnées de fenêtre
- convertir en coordonnées de fenêtre OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c8ec3d8922890cfa3a79c5dacd94e93a06c53a73
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127311633"
---
# <a name="transforming-to-window-coordinates"></a>Transformer en coordonnées de fenêtre

Avant que les coordonnées de clip soient converties en coordonnées de fenêtre, elles sont divisées par la valeur de *w* pour produire des coordonnées de périphérique normalisées. La transformation de Viewport appliquée à ces coordonnées normalisées produit des coordonnées de fenêtre. Vous contrôlez la fenêtre d’affichage, qui détermine la zone de la fenêtre à l’écran qui affiche une image, avec [**glDepthRange**](gldepthrange.md) et [**glViewport**](glviewport.md).

 

 




