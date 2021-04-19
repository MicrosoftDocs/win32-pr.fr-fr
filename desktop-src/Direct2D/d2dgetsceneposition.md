---
title: D2DGetScenePosition, fonction (D2d1effecthelpers. h)
description: Retourne la valeur de la position de la scène d’entrée \_ . Disponible uniquement lorsque D2D \_ requiert \_ que \_ la position de scène soit déclarée dans le fichier source.
ms.assetid: 451E4C31-D93D-44B6-81D1-AC5FD986ACBD
keywords:
- D2DGetScenePosition fonction Direct2D
topic_type:
- apiref
api_name:
- D2DGetScenePosition
api_location:
- d2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ace0ee4d60f8c140825e41ba47de941bca09e67c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106534868"
---
# <a name="d2dgetsceneposition-function"></a><span data-ttu-id="824ff-105">D2DGetScenePosition fonction)</span><span class="sxs-lookup"><span data-stu-id="824ff-105">D2DGetScenePosition function</span></span>

<span data-ttu-id="824ff-106">Retourne la valeur de la position de la scène d’entrée \_ .</span><span class="sxs-lookup"><span data-stu-id="824ff-106">Returns the value of the input SCENE\_POSITION.</span></span> <span data-ttu-id="824ff-107">Disponible uniquement lorsque D2D \_ requiert \_ que \_ la position de scène soit déclarée dans le fichier source.</span><span class="sxs-lookup"><span data-stu-id="824ff-107">Only available when D2D\_REQUIRES\_SCENE\_POSITION is declared in the source file.</span></span>

## <a name="syntax"></a><span data-ttu-id="824ff-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="824ff-108">Syntax</span></span>

``` syntax
float4 WINAPI D2DGetScenePosition(void);
```

## <a name="parameters"></a><span data-ttu-id="824ff-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="824ff-109">Parameters</span></span>

<span data-ttu-id="824ff-110">Cette fonction n’a pas de paramètres.</span><span class="sxs-lookup"><span data-stu-id="824ff-110">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="824ff-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="824ff-111">Return value</span></span>

<span data-ttu-id="824ff-112">La fonction retourne un **float4** au format position de la scène \_ .</span><span class="sxs-lookup"><span data-stu-id="824ff-112">The function returns a **float4** in the format SCENE\_POSITION.</span></span>

## <a name="remarks"></a><span data-ttu-id="824ff-113">Notes</span><span class="sxs-lookup"><span data-stu-id="824ff-113">Remarks</span></span>

<span data-ttu-id="824ff-114">L’exemple suivant illustre l’utilisation de la fonction dans la génération d’un modèle de dissolution.</span><span class="sxs-lookup"><span data-stu-id="824ff-114">The following example shows the use of the function in generating a dissolve pattern.</span></span>

``` syntax
D2D_PS_ENTRY(BlendDissolve)  
{  
    min16float4 dest   = D2DGetInput(0);  
    min16float4 source = D2DGetInput(1);  
  
    min16float4 color = dest;  
  
    if ((source.a > 0.0) && (source.a >= Rand((min16float2)D2DGetScenePosition().xy)))  
    {  
        // TODO: perform  dissovlve math
    }  
  
    return color;  
}  
```

## <a name="requirements"></a><span data-ttu-id="824ff-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="824ff-115">Requirements</span></span>



| <span data-ttu-id="824ff-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="824ff-116">Requirement</span></span> | <span data-ttu-id="824ff-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="824ff-117">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="824ff-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="824ff-118">Header</span></span><br/> | <dl> <span data-ttu-id="824ff-119"><dt>D2d1effecthelpers. hlsli</dt></span><span class="sxs-lookup"><span data-stu-id="824ff-119"><dt>D2d1effecthelpers.hlsli</dt></span></span> </dl> |
| <span data-ttu-id="824ff-120">DLL</span><span class="sxs-lookup"><span data-stu-id="824ff-120">DLL</span></span><br/>    | <dl> <span data-ttu-id="824ff-121"><dt>D2d1.dll</dt></span><span class="sxs-lookup"><span data-stu-id="824ff-121"><dt>D2d1.dll</dt></span></span> </dl>                |



## <a name="see-also"></a><span data-ttu-id="824ff-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="824ff-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="824ff-123">Liaison de nuanceurs d’effet</span><span class="sxs-lookup"><span data-stu-id="824ff-123">Effect Shader Linking</span></span>](effect-shader-linking.md)
</dt> <dt>

[<span data-ttu-id="824ff-124">Applications auxiliaires HLSL</span><span class="sxs-lookup"><span data-stu-id="824ff-124">HLSL Helpers</span></span>](hlsl-helpers.md)
</dt> </dl>

 

 





