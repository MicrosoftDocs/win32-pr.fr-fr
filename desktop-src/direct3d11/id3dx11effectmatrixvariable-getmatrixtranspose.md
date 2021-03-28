---
title: Méthode ID3DX11EffectMatrixVariable GetMatrixTranspose (D3dx11effect. h)
description: Transposez et récupérez une matrice à virgule flottante.
ms.assetid: a261128c-d1f9-4864-b562-5fe9a69c9969
keywords:
- Méthode GetMatrixTranspose Direct3D 11
- Méthode GetMatrixTranspose Direct3D 11, interface ID3DX11EffectMatrixVariable
- Interface ID3DX11EffectMatrixVariable Direct3D 11, méthode GetMatrixTranspose
topic_type:
- apiref
api_name:
- ID3DX11EffectMatrixVariable.GetMatrixTranspose
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5fa5c8eb8e424041a05461636d1eaf7b65c7cd4f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104043134"
---
# <a name="id3dx11effectmatrixvariablegetmatrixtranspose-method"></a><span data-ttu-id="0a1dd-106">ID3DX11EffectMatrixVariable :: GetMatrixTranspose, méthode</span><span class="sxs-lookup"><span data-stu-id="0a1dd-106">ID3DX11EffectMatrixVariable::GetMatrixTranspose method</span></span>

<span data-ttu-id="0a1dd-107">Transposez et récupérez une matrice à virgule flottante.</span><span class="sxs-lookup"><span data-stu-id="0a1dd-107">Transpose and get a floating-point matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="0a1dd-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0a1dd-108">Syntax</span></span>


```C++
HRESULT GetMatrixTranspose(
   float *pData
);
```



## <a name="parameters"></a><span data-ttu-id="0a1dd-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0a1dd-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0a1dd-110">*pData*</span><span class="sxs-lookup"><span data-stu-id="0a1dd-110">*pData*</span></span> 
</dt> <dd>

<span data-ttu-id="0a1dd-111">Type : **float \***</span><span class="sxs-lookup"><span data-stu-id="0a1dd-111">Type: **float\***</span></span>

<span data-ttu-id="0a1dd-112">Pointeur vers le premier élément d’une matrice transposée.</span><span class="sxs-lookup"><span data-stu-id="0a1dd-112">A pointer to the first element of a transposed matrix.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0a1dd-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="0a1dd-113">Return value</span></span>

<span data-ttu-id="0a1dd-114">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="0a1dd-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="0a1dd-115">Retourne l’un des [codes de retour Direct3D 11](d3d11-graphics-reference-returnvalues.md)suivants.</span><span class="sxs-lookup"><span data-stu-id="0a1dd-115">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="0a1dd-116">Notes</span><span class="sxs-lookup"><span data-stu-id="0a1dd-116">Remarks</span></span>

<span data-ttu-id="0a1dd-117">En transposant une matrice, vous réorganisez l’ordre des données de l’ordre des colonnes de lignes à l’ordre des lignes (ou vice versa).</span><span class="sxs-lookup"><span data-stu-id="0a1dd-117">Transposing a matrix will rearrange the data order from row-column order to column-row order (or vice versa).</span></span>

> [!Note]  
> <span data-ttu-id="0a1dd-118">Le kit de développement logiciel (SDK) DirectX ne fournit aucun binaire compilé pour les effets.</span><span class="sxs-lookup"><span data-stu-id="0a1dd-118">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="0a1dd-119">Vous devez utiliser la source Effects 11 pour créer votre application Effects-type.</span><span class="sxs-lookup"><span data-stu-id="0a1dd-119">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="0a1dd-120">Pour plus d’informations sur l’utilisation de la source Effects 11, consultez [différences entre les effets 10 et 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="0a1dd-120">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="0a1dd-121">Spécifications</span><span class="sxs-lookup"><span data-stu-id="0a1dd-121">Requirements</span></span>



| <span data-ttu-id="0a1dd-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0a1dd-122">Requirement</span></span> | <span data-ttu-id="0a1dd-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="0a1dd-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0a1dd-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="0a1dd-124">Header</span></span><br/>  | <dl> <span data-ttu-id="0a1dd-125"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="0a1dd-125"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="0a1dd-126">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="0a1dd-126">Library</span></span><br/> | <dl> <span data-ttu-id="0a1dd-127"><dt>N/A (une bibliothèque Effects 11 est disponible en ligne en tant que source partagée.)</dt></span><span class="sxs-lookup"><span data-stu-id="0a1dd-127"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0a1dd-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0a1dd-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0a1dd-129">ID3DX11EffectMatrixVariable</span><span class="sxs-lookup"><span data-stu-id="0a1dd-129">ID3DX11EffectMatrixVariable</span></span>](id3dx11effectmatrixvariable.md)
</dt> </dl>

 

 





