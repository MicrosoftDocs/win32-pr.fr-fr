---
description: Définit des effets à virgule flottante. Ce modèle remplace le modèle EffectFloats.
ms.assetid: 7b41d0dc-209f-4ade-a7ed-aa54f421e520
title: EffectParamFloats
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b0954ce7679691920c2e104277d12a48f7a34ddf
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104033437"
---
# <a name="effectparamfloats"></a><span data-ttu-id="6ce93-104">EffectParamFloats</span><span class="sxs-lookup"><span data-stu-id="6ce93-104">EffectParamFloats</span></span>

<span data-ttu-id="6ce93-105">Définit des effets à virgule flottante.</span><span class="sxs-lookup"><span data-stu-id="6ce93-105">Defines effect floating-point numbers.</span></span> <span data-ttu-id="6ce93-106">Ce modèle remplace le modèle [**EffectFloats**](effectfloats.md) .</span><span class="sxs-lookup"><span data-stu-id="6ce93-106">This template replaces the [**EffectFloats**](effectfloats.md) template.</span></span>

``` syntax
template EffectParamFloats
{
    < 3014B9A0-62F5-478c-9B86-E4AC9F4E418B >
    STRING ParamName;
    DWORD nFloats;
    array float Floats[nFloats];
} 
```

<span data-ttu-id="6ce93-107">Où :</span><span class="sxs-lookup"><span data-stu-id="6ce93-107">Where:</span></span>

-   <span data-ttu-id="6ce93-108">ParamName-nom du tableau de valeurs float.</span><span class="sxs-lookup"><span data-stu-id="6ce93-108">ParamName - Name of the array of floats.</span></span>
-   <span data-ttu-id="6ce93-109">nFloats : nombre de valeurs à virgule flottante dans le tableau.</span><span class="sxs-lookup"><span data-stu-id="6ce93-109">nFloats - Number of floating-point values in the array.</span></span>
-   <span data-ttu-id="6ce93-110">FLOTTE \[ nFloats \] -tableau de valeurs à virgule flottante.</span><span class="sxs-lookup"><span data-stu-id="6ce93-110">Floats\[nFloats\] - Array of floating-point values.</span></span>

## <a name="see-also"></a><span data-ttu-id="6ce93-111">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6ce93-111">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6ce93-112">Modèles</span><span class="sxs-lookup"><span data-stu-id="6ce93-112">Templates</span></span>](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



