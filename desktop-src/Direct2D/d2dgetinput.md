---
title: D2DGetInput, fonction (D2d1effecthelpers. h)
description: Retourne la couleur de l’entrée N à la coordonnée d’entrée. Disponible uniquement pour les entrées simples.
ms.assetid: 74B6F814-53C7-4C8C-B45C-3CB23B9D8BED
keywords:
- D2DGetInput fonction Direct2D
topic_type:
- apiref
api_name:
- D2DGetInput
api_location:
- d2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dd6ec0fe858149ee53da1f8ca8a02c12756d6a90
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526407"
---
# <a name="d2dgetinput-function"></a><span data-ttu-id="737b9-105">D2DGetInput fonction)</span><span class="sxs-lookup"><span data-stu-id="737b9-105">D2DGetInput function</span></span>

<span data-ttu-id="737b9-106">Retourne la couleur de l’entrée N à la coordonnée d’entrée.</span><span class="sxs-lookup"><span data-stu-id="737b9-106">Returns the color of input N at the input coordinate.</span></span> <span data-ttu-id="737b9-107">Disponible uniquement pour les entrées simples.</span><span class="sxs-lookup"><span data-stu-id="737b9-107">Only available for simple inputs.</span></span>

## <a name="syntax"></a><span data-ttu-id="737b9-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="737b9-108">Syntax</span></span>

``` syntax
float4 WINAPI D2DGetInput(
  in uint N
);
```

## <a name="parameters"></a><span data-ttu-id="737b9-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="737b9-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="737b9-110">*N* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="737b9-110">*N* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="737b9-111">Numéro d’entrée.</span><span class="sxs-lookup"><span data-stu-id="737b9-111">The input number.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="737b9-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="737b9-112">Return value</span></span>

<span data-ttu-id="737b9-113">La fonction retourne un **float4**, contenant la couleur RVBA dans le format d’entrée.</span><span class="sxs-lookup"><span data-stu-id="737b9-113">The function returns a **float4**, containing the RGBA color in the format INPUTN.</span></span>

## <a name="remarks"></a><span data-ttu-id="737b9-114">Notes</span><span class="sxs-lookup"><span data-stu-id="737b9-114">Remarks</span></span>

<span data-ttu-id="737b9-115">L’exemple suivant illustre la fonction utilisée dans le cadre d’un effet composite arithmétique.</span><span class="sxs-lookup"><span data-stu-id="737b9-115">The following example shows the function being used as part of an arithmetic composite effect.</span></span>

``` syntax
  
D2D_PS_ENTRY(PS_NAME)  
{  
    MIN_TYPE(float4) sourceColor = D2DGetInput(0);  
    MIN_TYPE(float4) destColor   = D2DGetInput(1);  
      
    MIN_TYPE(float4) output = // TODO: add math to composite source and dest

    return output;  
}  
```

<span data-ttu-id="737b9-116">Reportez-vous également à la section Remarques sur l’entrée de l' [ \_ \_ élément](d2d-ps-entry.md) de rapport D2D pour obtenir un autre exemple d’utilisation de cette fonction.</span><span class="sxs-lookup"><span data-stu-id="737b9-116">Also, refer to the remarks for [D2D\_PS\_ENTRY](d2d-ps-entry.md) for another example of the use of this function.</span></span>

## <a name="requirements"></a><span data-ttu-id="737b9-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="737b9-117">Requirements</span></span>



| <span data-ttu-id="737b9-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="737b9-118">Requirement</span></span> | <span data-ttu-id="737b9-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="737b9-119">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="737b9-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="737b9-120">Header</span></span><br/> | <dl> <span data-ttu-id="737b9-121"><dt>D2d1effecthelpers. hlsli</dt></span><span class="sxs-lookup"><span data-stu-id="737b9-121"><dt>D2d1effecthelpers.hlsli</dt></span></span> </dl> |
| <span data-ttu-id="737b9-122">DLL</span><span class="sxs-lookup"><span data-stu-id="737b9-122">DLL</span></span><br/>    | <dl> <span data-ttu-id="737b9-123"><dt>D2d1.dll</dt></span><span class="sxs-lookup"><span data-stu-id="737b9-123"><dt>D2d1.dll</dt></span></span> </dl>                |



## <a name="see-also"></a><span data-ttu-id="737b9-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="737b9-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="737b9-125">Liaison de nuanceurs d’effet</span><span class="sxs-lookup"><span data-stu-id="737b9-125">Effect Shader Linking</span></span>](effect-shader-linking.md)
</dt> <dt>

[<span data-ttu-id="737b9-126">Applications auxiliaires HLSL</span><span class="sxs-lookup"><span data-stu-id="737b9-126">HLSL Helpers</span></span>](hlsl-helpers.md)
</dt> </dl>

 

 





