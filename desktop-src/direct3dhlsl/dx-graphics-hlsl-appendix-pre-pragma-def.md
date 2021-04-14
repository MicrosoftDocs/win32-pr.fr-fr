---
title: DEF (directive pragma)
description: Directive pragma qui alloue manuellement un registre de nuanceur à virgule flottante.
ms.assetid: 45db94c4-f6f6-4c88-9bf2-4eaa9abf7844
keywords:
- DEF (directive de pragma)
topic_type:
- apiref
api_name:
- def pragma Directive
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2a921e17f8ddee4aaabfe50e75f42ce44812863d
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104990680"
---
# <a name="def-pragma-directive"></a><span data-ttu-id="bacb2-104">DEF (directive pragma)</span><span class="sxs-lookup"><span data-stu-id="bacb2-104">def pragma Directive</span></span>

<span data-ttu-id="bacb2-105">Directive pragma qui alloue manuellement un registre de nuanceur à virgule flottante.</span><span class="sxs-lookup"><span data-stu-id="bacb2-105">Pragma directive that manually allocates a floating-point shader register.</span></span>



| <span data-ttu-id="bacb2-106">\#pragma def ( *target*, *Register*, *val1*, *val2*,*val3*, *Val4* )</span><span class="sxs-lookup"><span data-stu-id="bacb2-106">\#pragma def( *target*, *register*, *val1*, *val2*,*val3*, *val4* )</span></span> |
|---------------------------------------------------------------------|



 

## <a name="parameters"></a><span data-ttu-id="bacb2-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="bacb2-107">Parameters</span></span>



| <span data-ttu-id="bacb2-108">Élément</span><span class="sxs-lookup"><span data-stu-id="bacb2-108">Item</span></span>                                                                        | <span data-ttu-id="bacb2-109">Description</span><span class="sxs-lookup"><span data-stu-id="bacb2-109">Description</span></span>                                                                 |
|-----------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| <span data-ttu-id="bacb2-110"><span id="target"></span><span id="TARGET"></span>*Indicatif*</span><span class="sxs-lookup"><span data-stu-id="bacb2-110"><span id="target"></span><span id="TARGET"></span>*target*</span></span><br/>       | <span data-ttu-id="bacb2-111">Cible qui contient le registre à allouer.</span><span class="sxs-lookup"><span data-stu-id="bacb2-111">Target that contains the register to allocate.</span></span> <br/>                  |
| <span data-ttu-id="bacb2-112"><span id="register"></span><span id="REGISTER"></span>*annuler*</span><span class="sxs-lookup"><span data-stu-id="bacb2-112"><span id="register"></span><span id="REGISTER"></span>*register*</span></span><br/> | <span data-ttu-id="bacb2-113">Registre de nuanceur à virgule flottante à allouer.</span><span class="sxs-lookup"><span data-stu-id="bacb2-113">Floating-point shader register to allocate.</span></span> <br/>                     |
| <span data-ttu-id="bacb2-114"><span id="val0"></span><span id="VAL0"></span>*val0*</span><span class="sxs-lookup"><span data-stu-id="bacb2-114"><span id="val0"></span><span id="VAL0"></span>*val0*</span></span><br/>             | <span data-ttu-id="bacb2-115">Premier octet de la valeur à allouer au registre spécifié.</span><span class="sxs-lookup"><span data-stu-id="bacb2-115">First byte of the value to allocate to the specified register.</span></span> <br/>  |
| <span data-ttu-id="bacb2-116"><span id="val1"></span><span id="VAL1"></span>*val1*</span><span class="sxs-lookup"><span data-stu-id="bacb2-116"><span id="val1"></span><span id="VAL1"></span>*val1*</span></span><br/>             | <span data-ttu-id="bacb2-117">Deuxième octet de la valeur à allouer au registre spécifié.</span><span class="sxs-lookup"><span data-stu-id="bacb2-117">Second byte of the value to allocate to the specified register.</span></span> <br/> |
| <span data-ttu-id="bacb2-118"><span id="val2"></span><span id="VAL2"></span>*val2*</span><span class="sxs-lookup"><span data-stu-id="bacb2-118"><span id="val2"></span><span id="VAL2"></span>*val2*</span></span><br/>             | <span data-ttu-id="bacb2-119">Troisième octet de la valeur à allouer au registre spécifié.</span><span class="sxs-lookup"><span data-stu-id="bacb2-119">Third byte of the value to allocate to the specified register.</span></span> <br/>  |
| <span data-ttu-id="bacb2-120"><span id="val3"></span><span id="VAL3"></span>*val3*</span><span class="sxs-lookup"><span data-stu-id="bacb2-120"><span id="val3"></span><span id="VAL3"></span>*val3*</span></span><br/>             | <span data-ttu-id="bacb2-121">Quatrième octet de la valeur à allouer au registre spécifié.</span><span class="sxs-lookup"><span data-stu-id="bacb2-121">Fourth byte of the value to allocate to the specified register.</span></span> <br/> |



 

## <a name="remarks"></a><span data-ttu-id="bacb2-122">Notes</span><span class="sxs-lookup"><span data-stu-id="bacb2-122">Remarks</span></span>

<span data-ttu-id="bacb2-123">Le pragma def permet à un développeur de préremplir un registre de nuanceur à virgule flottante avec la valeur spécifiée.</span><span class="sxs-lookup"><span data-stu-id="bacb2-123">The def pragma allows a developer to prefill a floating-point shader register with the specified value.</span></span> <span data-ttu-id="bacb2-124">Ce pragma est rarement utilisé.</span><span class="sxs-lookup"><span data-stu-id="bacb2-124">This pragma is infrequently used.</span></span>

## <a name="see-also"></a><span data-ttu-id="bacb2-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bacb2-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bacb2-126">Directives de préprocesseur (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="bacb2-126">Preprocessor Directives (DirectX HLSL)</span></span>](dx-graphics-hlsl-appendix-preprocessor.md)
</dt> <dt>

[<span data-ttu-id="bacb2-127">\#Directive pragma (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="bacb2-127">\#pragma Directive (DirectX HLSL)</span></span>](dx-graphics-hlsl-appendix-pre-pragma.md)
</dt> </dl>

 

 





