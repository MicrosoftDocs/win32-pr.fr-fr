---
description: L’attribut Color spécifie la couleur du stylet.
ms.assetid: ce775359-65fc-40d0-8725-b392cc0464a6
title: Couleur du stylet
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92d831994ac444207832574dc104a9d5c2582db8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528300"
---
# <a name="pen-color"></a><span data-ttu-id="2d247-103">Couleur du stylet</span><span class="sxs-lookup"><span data-stu-id="2d247-103">Pen Color</span></span>

<span data-ttu-id="2d247-104">L’attribut Color spécifie la couleur du stylet.</span><span class="sxs-lookup"><span data-stu-id="2d247-104">The color attribute specifies the pen's color.</span></span> <span data-ttu-id="2d247-105">Une application peut créer un stylet cosmétique avec une couleur unique à l’aide de la macro [**RGB**](/windows/desktop/api/Wingdi/nf-wingdi-rgb) pour stocker l’triplet rouge, vert et bleu qui spécifie la couleur souhaitée dans une structure [COLORREF](colorref.md) et transmettant l’adresse de cette structure à la fonction [**CreatePen**](/windows/desktop/api/Wingdi/nf-wingdi-createpen), [**CreatePenIndirect**](/windows/desktop/api/Wingdi/nf-wingdi-createpenindirect)ou [**ExtCreatePen**](/windows/desktop/api/Wingdi/nf-wingdi-extcreatepen) .</span><span class="sxs-lookup"><span data-stu-id="2d247-105">An application can create a cosmetic pen with a unique color by using the [**RGB**](/windows/desktop/api/Wingdi/nf-wingdi-rgb) macro to store the red, green, blue triplet that specifies the desired color in a [COLORREF](colorref.md) structure and passing this structure's address to the [**CreatePen**](/windows/desktop/api/Wingdi/nf-wingdi-createpen), [**CreatePenIndirect**](/windows/desktop/api/Wingdi/nf-wingdi-createpenindirect), or [**ExtCreatePen**](/windows/desktop/api/Wingdi/nf-wingdi-extcreatepen) function.</span></span> <span data-ttu-id="2d247-106">(Les plumes d’action sont limitées en noir, blanc et invisible.) Pour plus d’informations sur les triplets et la couleur RVB, consultez [couleurs](colors.md).</span><span class="sxs-lookup"><span data-stu-id="2d247-106">(The stock pens are limited to black, white, and invisible.) For more information about RGB triplets and color, see [Colors](colors.md).</span></span>

 

 



