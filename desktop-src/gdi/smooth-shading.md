---
description: L’ombrage lissé est une méthode d’ombrage d’une zone avec un dégradé de couleur.
ms.assetid: 94f26d15-fb76-47ec-b805-f04975d41b43
title: Ombrage lissé
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd5bfa54fef8d0a6810a3230e88e4e3144f7ecf4b62f7313f5daf4213e948c00
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119965199"
---
# <a name="smooth-shading"></a>Ombrage lissé

L' *ombrage lissé* est une méthode d’ombrage d’une zone avec un dégradé de couleur. L’inclusion des informations de couleur, ainsi que des limites de la primitive de dessin, spécifie le dégradé de couleur. GDI interpole de manière linéaire la couleur de l’intérieur de la primitive transmise sur les points de terminaison de couleur. Les informations de couleur et de vertex sont incluses avec les informations de position dans la structure de [**TRIVERTEX**](/windows/desktop/api/Wingdi/ns-wingdi-trivertex) .

Utilisez la fonction [**GradientFill**](/windows/desktop/api/WinGdi/nf-wingdi-gradientfill) pour remplir une structure de triangle ou de rectangle. Pour remplir un triangle avec un ombrage lissé, appelez **GradientFill** avec les trois points de terminaison triangulaires. Pour remplir un rectangle avec un ombrage lissé, appelez **GradientFill** avec les coordonnées de rectangle supérieur gauche et inférieur droit. **GradientFill** fait référence aux structures [**TRIVERTEX**](/windows/desktop/api/Wingdi/ns-wingdi-trivertex), [**\_ rectangle de dégradé**](/windows/desktop/api/Wingdi/ns-wingdi-gradient_rect)et [**\_ triangle de dégradé**](/windows/desktop/api/Wingdi/ns-wingdi-gradient_triangle) .

Pour obtenir un exemple, consultez [dessin d’un triangle ombré](drawing-a-shaded-triangle.md).

 

 



