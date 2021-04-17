---
title: SV_InnerCoverage
description: SV \_ InputCoverage représente des informations de pixellisation conservatrice sous-estimées (par exemple, si un pixel est garanti comme étant entièrement couvert).
ms.assetid: 5BB3C3FB-E5ED-4395-B389-300DE67C984B
keywords:
- SV_InnerCoverage HLSL
topic_type:
- apiref
api_name:
- SV_InnerCoverage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a2f1393a6a11a95c8c08746f57083fe193791a60
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104990997"
---
# <a name="sv_innercoverage"></a><span data-ttu-id="a18d5-104">SV \_ InnerCoverage</span><span class="sxs-lookup"><span data-stu-id="a18d5-104">SV\_InnerCoverage</span></span>

<span data-ttu-id="a18d5-105">SV \_ InputCoverage représente des informations de pixellisation conservatrice sous-estimées (par exemple, si un pixel est garanti comme étant entièrement couvert).</span><span class="sxs-lookup"><span data-stu-id="a18d5-105">SV\_InputCoverage represents underestimated conservative rasterization information (i.e. whether a pixel is guaranteed-to-be-fully covered).</span></span>

## <a name="type"></a><span data-ttu-id="a18d5-106">Type</span><span class="sxs-lookup"><span data-stu-id="a18d5-106">Type</span></span>



|      |
|------|
| <span data-ttu-id="a18d5-107">Type</span><span class="sxs-lookup"><span data-stu-id="a18d5-107">Type</span></span> |
| <span data-ttu-id="a18d5-108">uint</span><span class="sxs-lookup"><span data-stu-id="a18d5-108">uint</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="a18d5-109">Notes</span><span class="sxs-lookup"><span data-stu-id="a18d5-109">Remarks</span></span>

<span data-ttu-id="a18d5-110">Cette valeur générée par le système est requise pour la prise en charge de niveau 3 et n’est disponible que dans ce niveau.</span><span class="sxs-lookup"><span data-stu-id="a18d5-110">This system generated value is required for tier 3 support, and is only available in that tier.</span></span> <span data-ttu-id="a18d5-111">Cette entrée s’exclut mutuellement avec la \_ couverture SV-les deux ne peuvent pas être utilisés.</span><span class="sxs-lookup"><span data-stu-id="a18d5-111">This input is mutually exclusive with SV\_Coverage - both cannot be used.</span></span>

<span data-ttu-id="a18d5-112">Pour accéder à SV \_ InnerCoverage, il doit être déclaré en tant que composant unique parmi l’un des registres d’entrée de nuanceur de pixels.</span><span class="sxs-lookup"><span data-stu-id="a18d5-112">To access SV\_InnerCoverage, it must be declared as a single component out of one of the pixel shader input registers.</span></span> <span data-ttu-id="a18d5-113">Le mode d’interpolation sur la déclaration doit être constant (l’interpolation ne s’applique pas).</span><span class="sxs-lookup"><span data-stu-id="a18d5-113">The interpolation mode on the declaration must be constant (interpolation does not apply).</span></span>

<span data-ttu-id="a18d5-114">La pixellisation conservatrice est disponible à la fois dans D3D 11.3 et D3D12.</span><span class="sxs-lookup"><span data-stu-id="a18d5-114">Conservative rasterization is available in both D3D11.3 and D3D12.</span></span> <span data-ttu-id="a18d5-115">Consultez :</span><span class="sxs-lookup"><span data-stu-id="a18d5-115">Refer to:</span></span>

-   [<span data-ttu-id="a18d5-116">Pixellisation de D3D 11,3 en toute prudence</span><span class="sxs-lookup"><span data-stu-id="a18d5-116">D3D11.3 Conservative Rasterization</span></span>](/windows/desktop/direct3d11/conservative-rasterization)
-   [<span data-ttu-id="a18d5-117">Pixellisation D3D12</span><span class="sxs-lookup"><span data-stu-id="a18d5-117">D3D12 Conservative Rasterization</span></span>](/windows/desktop/direct3d12/conservative-rasterization)

## <a name="see-also"></a><span data-ttu-id="a18d5-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a18d5-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a18d5-119">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="a18d5-119">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> <dt>

[<span data-ttu-id="a18d5-120">Valeurs système du modèle de nuanceur 5,1</span><span class="sxs-lookup"><span data-stu-id="a18d5-120">Shader Model 5.1 System Values</span></span>](shader-model-5-1-system-values.md)
</dt> </dl>

 

 