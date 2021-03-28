---
description: Le système gère les couleurs dans les bitmaps différemment des couleurs des stylets, des pinceaux et du texte.
ms.assetid: c315dd6e-87ee-4905-b193-186ea580ac0a
title: Couleur dans les bitmaps
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 834744f35ccc8bd0c8714fa5bbb438b59c8b8db3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114702"
---
# <a name="color-in-bitmaps"></a><span data-ttu-id="767d3-103">Couleur dans les bitmaps</span><span class="sxs-lookup"><span data-stu-id="767d3-103">Color in Bitmaps</span></span>

<span data-ttu-id="767d3-104">Le système gère les couleurs dans les bitmaps différemment des couleurs des stylets, des pinceaux et du texte.</span><span class="sxs-lookup"><span data-stu-id="767d3-104">The system handles colors in bitmaps differently than colors in pens, brushes, and text.</span></span> <span data-ttu-id="767d3-105">Les bitmaps compatibles, créées à l’aide de la fonction [**CreateBitmap**](/windows/desktop/api/Wingdi/nf-wingdi-createbitmap) ou [**CreateCompatibleBitmap**](/windows/desktop/api/Wingdi/nf-wingdi-createcompatiblebitmap) , sont spécifiques aux appareils et conservent les informations de couleur dans un format dépendant du périphérique.</span><span class="sxs-lookup"><span data-stu-id="767d3-105">Compatible bitmaps, created by using the [**CreateBitmap**](/windows/desktop/api/Wingdi/nf-wingdi-createbitmap) or [**CreateCompatibleBitmap**](/windows/desktop/api/Wingdi/nf-wingdi-createcompatiblebitmap) function, are device specific and retain color information in a device-dependent format.</span></span> <span data-ttu-id="767d3-106">Aucune valeur de couleur n’est utilisée, et les couleurs ne sont pas soumises aux approximations et au tramage.</span><span class="sxs-lookup"><span data-stu-id="767d3-106">No color values are used, and the colors are not subject to approximations and dithering.</span></span>

<span data-ttu-id="767d3-107">Les bitmaps indépendantes du périphérique (DIB) conservent les informations de couleur en tant que valeurs de couleur ou index de palette de couleurs.</span><span class="sxs-lookup"><span data-stu-id="767d3-107">Device-independent bitmaps (DIBs) retain color information either as color values or color palette indexes.</span></span> <span data-ttu-id="767d3-108">Si des valeurs de couleur sont utilisées, les couleurs sont sujettes à approximation, mais pas à l’interpolation.</span><span class="sxs-lookup"><span data-stu-id="767d3-108">If color values are used, the colors are subject to approximation, but not dithering.</span></span> <span data-ttu-id="767d3-109">Les index de palette de couleurs ne peuvent être utilisés qu’avec les appareils qui prennent en charge les palettes de couleurs.</span><span class="sxs-lookup"><span data-stu-id="767d3-109">Color palette indexes can only be used with devices that support color palettes.</span></span> <span data-ttu-id="767d3-110">Bien que le système n’effectue pas de couleurs approximatives ou de trames identifiées par des index, la couleur résultante peut être différente de celle prévue, car les index produisent des résultats valides uniquement dans le contexte de la palette de couleurs actuelle au moment de la création de l’image bitmap.</span><span class="sxs-lookup"><span data-stu-id="767d3-110">Although the system does not approximate or dither colors identified by indexes, the resulting color may be different than that intended, because the indexes yield valid results only in the context of the color palette that was current at the time the bitmap was created.</span></span> <span data-ttu-id="767d3-111">Si la palette change, effectuez les couleurs dans le bitmap.</span><span class="sxs-lookup"><span data-stu-id="767d3-111">If the palette changes, so do the colors in the bitmap.</span></span> <span data-ttu-id="767d3-112">Pour plus d’informations sur les index de palette, consultez [palette par défaut](default-palette.md) et [**PALETTEINDEX**](/windows/desktop/api/Wingdi/nf-wingdi-paletteindex).</span><span class="sxs-lookup"><span data-stu-id="767d3-112">For more information on palette indexes, see [Default Palette](default-palette.md) and [**PALETTEINDEX**](/windows/desktop/api/Wingdi/nf-wingdi-paletteindex).</span></span>

<span data-ttu-id="767d3-113">En plus de faire référence à la palette logique, une application peut également faire référence à une valeur dans une table de couleurs DIB.</span><span class="sxs-lookup"><span data-stu-id="767d3-113">In addition to referencing the logical palette, an application can also reference a value in a DIB color table.</span></span> <span data-ttu-id="767d3-114">Pour sélectionner une couleur dans une table de couleurs DIB, appelez [**DIBINDEX**](/windows/desktop/api/Mmsystem/nf-mmsystem-dibindex).</span><span class="sxs-lookup"><span data-stu-id="767d3-114">To select a color in a DIB color table, call [**DIBINDEX**](/windows/desktop/api/Mmsystem/nf-mmsystem-dibindex).</span></span> <span data-ttu-id="767d3-115">Notez que cela n’est possible que pour un contexte de périphérique pour lequel un DIB est sélectionné.</span><span class="sxs-lookup"><span data-stu-id="767d3-115">Note that this is only possible for a device context that has a DIB selected into it.</span></span>

 

 



