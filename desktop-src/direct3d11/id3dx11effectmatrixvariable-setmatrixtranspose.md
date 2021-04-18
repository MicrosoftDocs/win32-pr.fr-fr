---
title: Méthode ID3DX11EffectMatrixVariable SetMatrixTranspose (D3dx11effect. h)
description: Transposez et définissez une matrice à virgule flottante.
ms.assetid: 228546c9-0141-4e17-bc8f-bff7201825d7
keywords:
- Méthode SetMatrixTranspose Direct3D 11
- Méthode SetMatrixTranspose Direct3D 11, interface ID3DX11EffectMatrixVariable
- Interface ID3DX11EffectMatrixVariable Direct3D 11, méthode SetMatrixTranspose
topic_type:
- apiref
api_name:
- ID3DX11EffectMatrixVariable.SetMatrixTranspose
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5daf77b6e2e9578dcbc6c9cfe80f57b149097c32
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104974550"
---
# <a name="id3dx11effectmatrixvariablesetmatrixtranspose-method"></a><span data-ttu-id="03629-106">ID3DX11EffectMatrixVariable :: SetMatrixTranspose, méthode</span><span class="sxs-lookup"><span data-stu-id="03629-106">ID3DX11EffectMatrixVariable::SetMatrixTranspose method</span></span>

<span data-ttu-id="03629-107">Transposez et définissez une matrice à virgule flottante.</span><span class="sxs-lookup"><span data-stu-id="03629-107">Transpose and set a floating-point matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="03629-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="03629-108">Syntax</span></span>


```C++
HRESULT SetMatrixTranspose(
   float *pData
);
```



## <a name="parameters"></a><span data-ttu-id="03629-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="03629-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="03629-110">*pData*</span><span class="sxs-lookup"><span data-stu-id="03629-110">*pData*</span></span> 
</dt> <dd>

<span data-ttu-id="03629-111">Type : **float \***</span><span class="sxs-lookup"><span data-stu-id="03629-111">Type: **float\***</span></span>

<span data-ttu-id="03629-112">Pointeur vers le premier élément d’une matrice.</span><span class="sxs-lookup"><span data-stu-id="03629-112">A pointer to the first element of a matrix.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="03629-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="03629-113">Return value</span></span>

<span data-ttu-id="03629-114">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="03629-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="03629-115">Retourne l’un des [codes de retour Direct3D 11](d3d11-graphics-reference-returnvalues.md)suivants.</span><span class="sxs-lookup"><span data-stu-id="03629-115">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="03629-116">Notes</span><span class="sxs-lookup"><span data-stu-id="03629-116">Remarks</span></span>

<span data-ttu-id="03629-117">En transposant une matrice, vous réorganisez l’ordre des données de l’ordre des colonnes de lignes à l’ordre des lignes (ou vice versa).</span><span class="sxs-lookup"><span data-stu-id="03629-117">Transposing a matrix will rearrange the data order from row-column order to column-row order (or vice versa).</span></span>

> [!Note]  
> <span data-ttu-id="03629-118">Le kit de développement logiciel (SDK) DirectX ne fournit aucun binaire compilé pour les effets.</span><span class="sxs-lookup"><span data-stu-id="03629-118">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="03629-119">Vous devez utiliser la source Effects 11 pour créer votre application Effects-type.</span><span class="sxs-lookup"><span data-stu-id="03629-119">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="03629-120">Pour plus d’informations sur l’utilisation de la source Effects 11, consultez [différences entre les effets 10 et 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="03629-120">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="03629-121">Spécifications</span><span class="sxs-lookup"><span data-stu-id="03629-121">Requirements</span></span>



| <span data-ttu-id="03629-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="03629-122">Requirement</span></span> | <span data-ttu-id="03629-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="03629-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="03629-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="03629-124">Header</span></span><br/>  | <dl> <span data-ttu-id="03629-125"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="03629-125"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="03629-126">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="03629-126">Library</span></span><br/> | <dl> <span data-ttu-id="03629-127"><dt>N/A (une bibliothèque Effects 11 est disponible en ligne en tant que source partagée.)</dt></span><span class="sxs-lookup"><span data-stu-id="03629-127"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="03629-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="03629-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="03629-129">ID3DX11EffectMatrixVariable</span><span class="sxs-lookup"><span data-stu-id="03629-129">ID3DX11EffectMatrixVariable</span></span>](id3dx11effectmatrixvariable.md)
</dt> </dl>

 

 





