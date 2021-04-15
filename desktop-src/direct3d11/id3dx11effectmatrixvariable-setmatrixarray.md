---
title: Méthode ID3DX11EffectMatrixVariable SetMatrixArray (D3dx11effect. h)
description: Définissez un tableau de matrices à virgule flottante.
ms.assetid: c90d621c-7500-49c3-ab40-2d0630fc4bec
keywords:
- Méthode SetMatrixArray Direct3D 11
- Méthode SetMatrixArray Direct3D 11, interface ID3DX11EffectMatrixVariable
- Interface ID3DX11EffectMatrixVariable Direct3D 11, méthode SetMatrixArray
topic_type:
- apiref
api_name:
- ID3DX11EffectMatrixVariable.SetMatrixArray
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6ffe0f6a81e0086a9afd6da9e464f09ae577dab2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104974623"
---
# <a name="id3dx11effectmatrixvariablesetmatrixarray-method"></a><span data-ttu-id="0b443-106">ID3DX11EffectMatrixVariable :: SetMatrixArray, méthode</span><span class="sxs-lookup"><span data-stu-id="0b443-106">ID3DX11EffectMatrixVariable::SetMatrixArray method</span></span>

<span data-ttu-id="0b443-107">Définissez un tableau de matrices à virgule flottante.</span><span class="sxs-lookup"><span data-stu-id="0b443-107">Set an array of floating-point matrices.</span></span>

## <a name="syntax"></a><span data-ttu-id="0b443-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0b443-108">Syntax</span></span>


```C++
HRESULT SetMatrixArray(
   float *pData,
   UINT  Offset,
   UINT  Count
);
```



## <a name="parameters"></a><span data-ttu-id="0b443-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0b443-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0b443-110">*pData*</span><span class="sxs-lookup"><span data-stu-id="0b443-110">*pData*</span></span> 
</dt> <dd>

<span data-ttu-id="0b443-111">Type : **float \***</span><span class="sxs-lookup"><span data-stu-id="0b443-111">Type: **float\***</span></span>

<span data-ttu-id="0b443-112">Pointeur vers la première matrice.</span><span class="sxs-lookup"><span data-stu-id="0b443-112">A pointer to the first matrix.</span></span>

</dd> <dt>

<span data-ttu-id="0b443-113">*Offset*</span><span class="sxs-lookup"><span data-stu-id="0b443-113">*Offset*</span></span> 
</dt> <dd>

<span data-ttu-id="0b443-114">Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="0b443-114">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="0b443-115">Nombre d’éléments de matrice à ignorer à partir du début du tableau.</span><span class="sxs-lookup"><span data-stu-id="0b443-115">The number of matrix elements to skip from the start of the array.</span></span>

</dd> <dt>

<span data-ttu-id="0b443-116">*Count*</span><span class="sxs-lookup"><span data-stu-id="0b443-116">*Count*</span></span> 
</dt> <dd>

<span data-ttu-id="0b443-117">Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="0b443-117">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="0b443-118">Nombre d’éléments à définir.</span><span class="sxs-lookup"><span data-stu-id="0b443-118">The number of elements to set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0b443-119">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="0b443-119">Return value</span></span>

<span data-ttu-id="0b443-120">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="0b443-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="0b443-121">Retourne l’un des [codes de retour Direct3D 11](d3d11-graphics-reference-returnvalues.md)suivants.</span><span class="sxs-lookup"><span data-stu-id="0b443-121">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="0b443-122">Notes</span><span class="sxs-lookup"><span data-stu-id="0b443-122">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="0b443-123">Le kit de développement logiciel (SDK) DirectX ne fournit aucun binaire compilé pour les effets.</span><span class="sxs-lookup"><span data-stu-id="0b443-123">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="0b443-124">Vous devez utiliser la source Effects 11 pour créer votre application Effects-type.</span><span class="sxs-lookup"><span data-stu-id="0b443-124">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="0b443-125">Pour plus d’informations sur l’utilisation de la source Effects 11, consultez [différences entre les effets 10 et 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="0b443-125">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="0b443-126">Spécifications</span><span class="sxs-lookup"><span data-stu-id="0b443-126">Requirements</span></span>



| <span data-ttu-id="0b443-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0b443-127">Requirement</span></span> | <span data-ttu-id="0b443-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="0b443-128">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0b443-129">En-tête</span><span class="sxs-lookup"><span data-stu-id="0b443-129">Header</span></span><br/>  | <dl> <span data-ttu-id="0b443-130"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="0b443-130"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="0b443-131">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="0b443-131">Library</span></span><br/> | <dl> <span data-ttu-id="0b443-132"><dt>N/A (une bibliothèque Effects 11 est disponible en ligne en tant que source partagée.)</dt></span><span class="sxs-lookup"><span data-stu-id="0b443-132"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0b443-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0b443-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0b443-134">ID3DX11EffectMatrixVariable</span><span class="sxs-lookup"><span data-stu-id="0b443-134">ID3DX11EffectMatrixVariable</span></span>](id3dx11effectmatrixvariable.md)
</dt> </dl>

 

