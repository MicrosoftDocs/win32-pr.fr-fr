---
description: Une application peut convertir un chemin d’accès en région en appelant la fonction PathToRegion.
ms.assetid: c4261516-7872-4118-99e2-138f0ac3c38a
title: Conversion de chemins d’accès en régions
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc3a576f04035f6e29bb37a23de956322639daf1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103754476"
---
# <a name="conversion-of-paths-to-regions"></a><span data-ttu-id="b1afb-103">Conversion de chemins d’accès en régions</span><span class="sxs-lookup"><span data-stu-id="b1afb-103">Conversion of Paths to Regions</span></span>

<span data-ttu-id="b1afb-104">Une application peut convertir un chemin d’accès en région en appelant la fonction [**PathToRegion**](/windows/desktop/api/Wingdi/nf-wingdi-pathtoregion) .</span><span class="sxs-lookup"><span data-stu-id="b1afb-104">An application can convert a path into a region by calling the [**PathToRegion**](/windows/desktop/api/Wingdi/nf-wingdi-pathtoregion) function.</span></span> <span data-ttu-id="b1afb-105">Comme [**SelectClipPath**](/windows/desktop/api/Wingdi/nf-wingdi-selectclippath), **PathToRegion** est utile lors de la création d’effets graphiques spéciaux.</span><span class="sxs-lookup"><span data-stu-id="b1afb-105">Like [**SelectClipPath**](/windows/desktop/api/Wingdi/nf-wingdi-selectclippath), **PathToRegion** is useful in the creation of special graphics effects.</span></span> <span data-ttu-id="b1afb-106">Par exemple, il n’existe aucune fonction permettant à une application de compenser un chemin d’accès ; Toutefois, il existe une fonction qui permet à une application de décaler une région ([**OffsetRgn**](/windows/desktop/api/Wingdi/nf-wingdi-offsetrgn)).</span><span class="sxs-lookup"><span data-stu-id="b1afb-106">For example, there are no functions that allow an application to offset a path; however, there is a function that enables an application to offset a region ([**OffsetRgn**](/windows/desktop/api/Wingdi/nf-wingdi-offsetrgn)).</span></span> <span data-ttu-id="b1afb-107">À l’aide de **PathToRegion** , une application peut créer l’effet de l’animation d’une forme complexe en créant un tracé qui définit la forme, en convertissant le tracé en une région (en appelant **PathToRegion**), puis en dessinant, en déplaçant et en effaçant à plusieurs reprises la région (en appelant des fonctions dans une séquence, telles que [**FillRgn**](/windows/desktop/api/Wingdi/nf-wingdi-fillrgn), **OffsetRgn** et **FillRgn**).</span><span class="sxs-lookup"><span data-stu-id="b1afb-107">Using **PathToRegion** , an application can create the effect of animating a complex shape by creating a path that defines the shape, converting the path into a region (by calling **PathToRegion**), and then repeatedly painting, moving, and erasing the region (by calling functions in a sequence, such as [**FillRgn**](/windows/desktop/api/Wingdi/nf-wingdi-fillrgn), **OffsetRgn** , and **FillRgn**).</span></span>

 

 



