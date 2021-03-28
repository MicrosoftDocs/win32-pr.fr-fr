---
description: L’ombrage lissé est une méthode d’ombrage d’une zone avec un dégradé de couleur.
ms.assetid: 94f26d15-fb76-47ec-b805-f04975d41b43
title: Ombrage lissé
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a5b73738c03147083099a5070e61fe21ca5cac76
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104203884"
---
# <a name="smooth-shading"></a>Ombrage lissé

L' *ombrage lissé* est une méthode d’ombrage d’une zone avec un dégradé de couleur. L’inclusion des informations de couleur, ainsi que des limites de la primitive de dessin, spécifie le dégradé de couleur. GDI interpole de manière linéaire la couleur de l’intérieur de la primitive transmise sur les points de terminaison de couleur. Les informations de couleur et de vertex sont incluses avec les informations de position dans la structure de [**TRIVERTEX**](/windows/desktop/api/Wingdi/ns-wingdi-trivertex) .

Utilisez la fonction [**GradientFill**](/windows/desktop/api/WinGdi/nf-wingdi-gradientfill) pour remplir une structure de triangle ou de rectangle. Pour remplir un triangle avec un ombrage lissé, appelez **GradientFill** avec les trois points de terminaison triangulaires. Pour remplir un rectangle avec un ombrage lissé, appelez **GradientFill** avec les coordonnées de rectangle supérieur gauche et inférieur droit. **GradientFill** fait référence aux structures [**TRIVERTEX**](/windows/desktop/api/Wingdi/ns-wingdi-trivertex), [**\_ rectangle de dégradé**](/windows/desktop/api/Wingdi/ns-wingdi-gradient_rect)et [**\_ triangle de dégradé**](/windows/desktop/api/Wingdi/ns-wingdi-gradient_triangle) .

Pour obtenir un exemple, consultez [dessin d’un triangle ombré](drawing-a-shaded-triangle.md).

 

 



