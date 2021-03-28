---
title: Méthode ID3DX11EffectScalarVariable GetFloatArray (D3dx11effect. h)
description: Obtient un tableau de variables à virgule flottante.
ms.assetid: e5e0dbee-47f5-46ed-89a0-01782345498f
keywords:
- Méthode GetFloatArray Direct3D 11
- Méthode GetFloatArray Direct3D 11, interface ID3DX11EffectScalarVariable
- Interface ID3DX11EffectScalarVariable Direct3D 11, méthode GetFloatArray
topic_type:
- apiref
api_name:
- ID3DX11EffectScalarVariable.GetFloatArray
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 90cc760b7b7b57172becee0b9df9765be4d097f1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104982519"
---
# <a name="id3dx11effectscalarvariablegetfloatarray-method"></a><span data-ttu-id="d1c0e-106">ID3DX11EffectScalarVariable :: GetFloatArray, méthode</span><span class="sxs-lookup"><span data-stu-id="d1c0e-106">ID3DX11EffectScalarVariable::GetFloatArray method</span></span>

<span data-ttu-id="d1c0e-107">Obtient un tableau de variables à virgule flottante.</span><span class="sxs-lookup"><span data-stu-id="d1c0e-107">Get an array of floating-point variables.</span></span>

## <a name="syntax"></a><span data-ttu-id="d1c0e-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d1c0e-108">Syntax</span></span>


```C++
HRESULT GetFloatArray(
   float *pData,
   UINT  Offset,
   UINT  Count
);
```



## <a name="parameters"></a><span data-ttu-id="d1c0e-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d1c0e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d1c0e-110">*pData*</span><span class="sxs-lookup"><span data-stu-id="d1c0e-110">*pData*</span></span> 
</dt> <dd>

<span data-ttu-id="d1c0e-111">Type : **float \***</span><span class="sxs-lookup"><span data-stu-id="d1c0e-111">Type: **float\***</span></span>

<span data-ttu-id="d1c0e-112">Pointeur vers le début des données à définir.</span><span class="sxs-lookup"><span data-stu-id="d1c0e-112">A pointer to the start of the data to set.</span></span>

</dd> <dt>

<span data-ttu-id="d1c0e-113">*Offset*</span><span class="sxs-lookup"><span data-stu-id="d1c0e-113">*Offset*</span></span> 
</dt> <dd>

<span data-ttu-id="d1c0e-114">Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="d1c0e-114">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="d1c0e-115">Doit avoir la valeur 0 ; elle est réservée à une utilisation ultérieure.</span><span class="sxs-lookup"><span data-stu-id="d1c0e-115">Must be set to 0; this is reserved for future use.</span></span>

</dd> <dt>

<span data-ttu-id="d1c0e-116">*Count*</span><span class="sxs-lookup"><span data-stu-id="d1c0e-116">*Count*</span></span> 
</dt> <dd>

<span data-ttu-id="d1c0e-117">Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="d1c0e-117">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="d1c0e-118">Nombre d’éléments de tableau à définir.</span><span class="sxs-lookup"><span data-stu-id="d1c0e-118">The number of array elements to set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d1c0e-119">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="d1c0e-119">Return value</span></span>

<span data-ttu-id="d1c0e-120">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="d1c0e-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="d1c0e-121">Retourne l’un des [codes de retour Direct3D 11](d3d11-graphics-reference-returnvalues.md)suivants.</span><span class="sxs-lookup"><span data-stu-id="d1c0e-121">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="d1c0e-122">Notes</span><span class="sxs-lookup"><span data-stu-id="d1c0e-122">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="d1c0e-123">Le kit de développement logiciel (SDK) DirectX ne fournit aucun binaire compilé pour les effets.</span><span class="sxs-lookup"><span data-stu-id="d1c0e-123">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="d1c0e-124">Vous devez utiliser la source Effects 11 pour créer votre application Effects-type.</span><span class="sxs-lookup"><span data-stu-id="d1c0e-124">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="d1c0e-125">Pour plus d’informations sur l’utilisation de la source Effects 11, consultez [différences entre les effets 10 et 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="d1c0e-125">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="d1c0e-126">Spécifications</span><span class="sxs-lookup"><span data-stu-id="d1c0e-126">Requirements</span></span>



| <span data-ttu-id="d1c0e-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d1c0e-127">Requirement</span></span> | <span data-ttu-id="d1c0e-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="d1c0e-128">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d1c0e-129">En-tête</span><span class="sxs-lookup"><span data-stu-id="d1c0e-129">Header</span></span><br/>  | <dl> <span data-ttu-id="d1c0e-130"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="d1c0e-130"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="d1c0e-131">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="d1c0e-131">Library</span></span><br/> | <dl> <span data-ttu-id="d1c0e-132"><dt>N/A (une bibliothèque Effects 11 est disponible en ligne en tant que source partagée.)</dt></span><span class="sxs-lookup"><span data-stu-id="d1c0e-132"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d1c0e-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d1c0e-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d1c0e-134">ID3DX11EffectScalarVariable</span><span class="sxs-lookup"><span data-stu-id="d1c0e-134">ID3DX11EffectScalarVariable</span></span>](id3dx11effectscalarvariable.md)
</dt> </dl>

 

