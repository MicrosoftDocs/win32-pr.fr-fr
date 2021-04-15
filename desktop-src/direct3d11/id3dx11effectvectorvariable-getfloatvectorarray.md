---
title: Méthode ID3DX11EffectVectorVariable GetFloatVectorArray (D3dx11effect. h)
description: Obtient un tableau de vecteurs à quatre composants qui contiennent des données à virgule flottante.
ms.assetid: 30ecbd97-c16d-4ea9-b7d9-364887f42a04
keywords:
- Méthode GetFloatVectorArray Direct3D 11
- Méthode GetFloatVectorArray Direct3D 11, interface ID3DX11EffectVectorVariable
- Interface ID3DX11EffectVectorVariable Direct3D 11, méthode GetFloatVectorArray
topic_type:
- apiref
api_name:
- ID3DX11EffectVectorVariable.GetFloatVectorArray
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 18a4c53b884c623ca3d11fb4a9a44660ce21d8a8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104974643"
---
# <a name="id3dx11effectvectorvariablegetfloatvectorarray-method"></a><span data-ttu-id="cdd19-106">ID3DX11EffectVectorVariable :: GetFloatVectorArray, méthode</span><span class="sxs-lookup"><span data-stu-id="cdd19-106">ID3DX11EffectVectorVariable::GetFloatVectorArray method</span></span>

<span data-ttu-id="cdd19-107">Obtient un tableau de vecteurs à quatre composants qui contiennent des données à virgule flottante.</span><span class="sxs-lookup"><span data-stu-id="cdd19-107">Get an array of four-component vectors that contain floating-point data.</span></span>

## <a name="syntax"></a><span data-ttu-id="cdd19-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="cdd19-108">Syntax</span></span>


```C++
HRESULT GetFloatVectorArray(
   float *pData,
   UINT  Offset,
   UINT  Count
);
```



## <a name="parameters"></a><span data-ttu-id="cdd19-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="cdd19-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cdd19-110">*pData*</span><span class="sxs-lookup"><span data-stu-id="cdd19-110">*pData*</span></span> 
</dt> <dd>

<span data-ttu-id="cdd19-111">Type : **float \***</span><span class="sxs-lookup"><span data-stu-id="cdd19-111">Type: **float\***</span></span>

<span data-ttu-id="cdd19-112">Pointeur vers le début des données à définir.</span><span class="sxs-lookup"><span data-stu-id="cdd19-112">A pointer to the start of the data to set.</span></span>

</dd> <dt>

<span data-ttu-id="cdd19-113">*Offset*</span><span class="sxs-lookup"><span data-stu-id="cdd19-113">*Offset*</span></span> 
</dt> <dd>

<span data-ttu-id="cdd19-114">Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="cdd19-114">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="cdd19-115">Doit avoir la valeur 0 ; elle est réservée à une utilisation ultérieure.</span><span class="sxs-lookup"><span data-stu-id="cdd19-115">Must be set to 0; this is reserved for future use.</span></span>

</dd> <dt>

<span data-ttu-id="cdd19-116">*Count*</span><span class="sxs-lookup"><span data-stu-id="cdd19-116">*Count*</span></span> 
</dt> <dd>

<span data-ttu-id="cdd19-117">Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="cdd19-117">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="cdd19-118">Nombre d’éléments de tableau à définir.</span><span class="sxs-lookup"><span data-stu-id="cdd19-118">The number of array elements to set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cdd19-119">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="cdd19-119">Return value</span></span>

<span data-ttu-id="cdd19-120">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="cdd19-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="cdd19-121">Retourne l’un des [codes de retour Direct3D 11](d3d11-graphics-reference-returnvalues.md)suivants.</span><span class="sxs-lookup"><span data-stu-id="cdd19-121">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="cdd19-122">Notes</span><span class="sxs-lookup"><span data-stu-id="cdd19-122">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="cdd19-123">Le kit de développement logiciel (SDK) DirectX ne fournit aucun binaire compilé pour les effets.</span><span class="sxs-lookup"><span data-stu-id="cdd19-123">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="cdd19-124">Vous devez utiliser la source Effects 11 pour créer votre application Effects-type.</span><span class="sxs-lookup"><span data-stu-id="cdd19-124">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="cdd19-125">Pour plus d’informations sur l’utilisation de la source Effects 11, consultez [différences entre les effets 10 et 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="cdd19-125">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="cdd19-126">Spécifications</span><span class="sxs-lookup"><span data-stu-id="cdd19-126">Requirements</span></span>



| <span data-ttu-id="cdd19-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="cdd19-127">Requirement</span></span> | <span data-ttu-id="cdd19-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="cdd19-128">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cdd19-129">En-tête</span><span class="sxs-lookup"><span data-stu-id="cdd19-129">Header</span></span><br/>  | <dl> <span data-ttu-id="cdd19-130"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="cdd19-130"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="cdd19-131">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="cdd19-131">Library</span></span><br/> | <dl> <span data-ttu-id="cdd19-132"><dt>N/A (une bibliothèque Effects 11 est disponible en ligne en tant que source partagée.)</dt></span><span class="sxs-lookup"><span data-stu-id="cdd19-132"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cdd19-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cdd19-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cdd19-134">ID3DX11EffectVectorVariable</span><span class="sxs-lookup"><span data-stu-id="cdd19-134">ID3DX11EffectVectorVariable</span></span>](id3dx11effectvectorvariable.md)
</dt> </dl>

 

