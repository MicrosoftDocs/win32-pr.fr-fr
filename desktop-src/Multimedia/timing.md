---
title: Minutage (Windows Multimedia)
description: Minutage
ms.assetid: 9ab284c7-eebc-4b44-b9e1-cc95efde22c1
keywords:
- DrawDib, minutage
- DrawDibTime fonction)
- DrawDib, débogage
- débogage DrawDib
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: adddd43ff5067d08334a40f2e52e79109c8a8bb7
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104464071"
---
# <a name="timing-windows-multimedia"></a><span data-ttu-id="e18dd-107">Minutage (Windows Multimedia)</span><span class="sxs-lookup"><span data-stu-id="e18dd-107">Timing (Windows Multimedia)</span></span>

<span data-ttu-id="e18dd-108">Dans le cadre du débogage d’une application, vous pouvez obtenir des informations sur la durée nécessaire pour effectuer des opérations DrawDib répétitives.</span><span class="sxs-lookup"><span data-stu-id="e18dd-108">As part of debugging an application, you can obtain information about the amount of time required to complete repetitive DrawDib operations.</span></span> <span data-ttu-id="e18dd-109">La fonction [**DrawDibTime**](/windows/desktop/api/Vfw/nf-vfw-drawdibtime) retourne des informations de temporisation pour les opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="e18dd-109">The [**DrawDibTime**](/windows/desktop/api/Vfw/nf-vfw-drawdibtime) function returns timing information for the following operations:</span></span>

-   <span data-ttu-id="e18dd-110">Dessin d’une image bitmap</span><span class="sxs-lookup"><span data-stu-id="e18dd-110">Drawing a bitmap</span></span>
-   <span data-ttu-id="e18dd-111">Décompression d’une image bitmap</span><span class="sxs-lookup"><span data-stu-id="e18dd-111">Decompressing a bitmap</span></span>
-   <span data-ttu-id="e18dd-112">Tramage d’une image bitmap</span><span class="sxs-lookup"><span data-stu-id="e18dd-112">Dithering a bitmap</span></span>
-   <span data-ttu-id="e18dd-113">Étirement d’une image bitmap</span><span class="sxs-lookup"><span data-stu-id="e18dd-113">Stretching a bitmap</span></span>
-   <span data-ttu-id="e18dd-114">Transfert d’une bitmap à l’aide de la fonction [**BitBlt**](/windows/desktop/api/wingdi/nf-wingdi-bitblt)</span><span class="sxs-lookup"><span data-stu-id="e18dd-114">Transferring a bitmap by using the [**BitBlt**](/windows/desktop/api/wingdi/nf-wingdi-bitblt) function</span></span>
-   <span data-ttu-id="e18dd-115">Transfert d’une bitmap à l’aide de la fonction [**StretchDIBits**](/windows/desktop/api/wingdi/nf-wingdi-stretchdibits)</span><span class="sxs-lookup"><span data-stu-id="e18dd-115">Transferring a bitmap by using the [**StretchDIBits**](/windows/desktop/api/wingdi/nf-wingdi-stretchdibits) function</span></span>

<span data-ttu-id="e18dd-116">Après avoir récupéré un ensemble de valeurs, [**DrawDibTime**](/windows/desktop/api/Vfw/nf-vfw-drawdibtime) réinitialise le nombre et la valeur pour chaque opération.</span><span class="sxs-lookup"><span data-stu-id="e18dd-116">After retrieving a set of values, [**DrawDibTime**](/windows/desktop/api/Vfw/nf-vfw-drawdibtime) resets the count and value for each operation.</span></span>

<span data-ttu-id="e18dd-117">La fonction [**DrawDibTime**](/windows/desktop/api/Vfw/nf-vfw-drawdibtime) est disponible uniquement dans la version Debug des fonctions DrawDib.</span><span class="sxs-lookup"><span data-stu-id="e18dd-117">The [**DrawDibTime**](/windows/desktop/api/Vfw/nf-vfw-drawdibtime) function is available only in the debug version of the DrawDib functions.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e18dd-118">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="e18dd-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e18dd-119">Rendu d’image</span><span class="sxs-lookup"><span data-stu-id="e18dd-119">Image Rendering</span></span>](image-rendering.md)
</dt> </dl>

 

 
