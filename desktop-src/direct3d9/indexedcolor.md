---
description: Se compose d’un paramètre d’index et d’une couleur RVBA et est utilisé pour définir des couleurs de vertex de maillage. L’index définit le vertex auquel la couleur est appliquée.
ms.assetid: 63909c54-c2de-4065-9882-58fca2b4e893
title: IndexedColor
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c895cf56efedfa7214bcfa6acafd32ab9324bbe8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104317658"
---
# <a name="indexedcolor"></a><span data-ttu-id="c6309-104">IndexedColor</span><span class="sxs-lookup"><span data-stu-id="c6309-104">IndexedColor</span></span>

<span data-ttu-id="c6309-105">Se compose d’un paramètre d’index et d’une couleur RVBA et est utilisé pour définir des couleurs de vertex de maillage.</span><span class="sxs-lookup"><span data-stu-id="c6309-105">Consists of an index parameter and an RGBA color and is used for defining mesh vertex colors.</span></span> <span data-ttu-id="c6309-106">L’index définit le vertex auquel la couleur est appliquée.</span><span class="sxs-lookup"><span data-stu-id="c6309-106">The index defines the vertex to which the color is applied.</span></span>

``` syntax
template IndexedColor
{
    < 1630B820-7842-11cf-8F52-0040333594A3 >
    DWORD index;
    ColorRGBA indexColor;
} 
```

<span data-ttu-id="c6309-107">Où :</span><span class="sxs-lookup"><span data-stu-id="c6309-107">Where:</span></span>

-   <span data-ttu-id="c6309-108">index : DWORD.</span><span class="sxs-lookup"><span data-stu-id="c6309-108">index - A DWORD.</span></span> <span data-ttu-id="c6309-109">Consultez la description ci-dessus.</span><span class="sxs-lookup"><span data-stu-id="c6309-109">See the description above.</span></span>
-   <span data-ttu-id="c6309-110">indexColor : modèle ColorRGBA.</span><span class="sxs-lookup"><span data-stu-id="c6309-110">indexColor - A ColorRGBA template.</span></span> <span data-ttu-id="c6309-111">Consultez [**ColorRGBA**](colorrgba.md).</span><span class="sxs-lookup"><span data-stu-id="c6309-111">See [**ColorRGBA**](colorrgba.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="c6309-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c6309-112">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c6309-113">Modèles</span><span class="sxs-lookup"><span data-stu-id="c6309-113">Templates</span></span>](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



