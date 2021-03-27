---
title: Méthode ID3DX11EffectVariable AsMatrix (D3dx11effect. h)
description: Obtenir une variable de matrice.
ms.assetid: 5d2baf65-ab0d-44df-bc6f-6ffae16cbb01
keywords:
- Méthode AsMatrix Direct3D 11
- Méthode AsMatrix Direct3D 11, interface ID3DX11EffectVariable
- Interface ID3DX11EffectVariable Direct3D 11, méthode AsMatrix
topic_type:
- apiref
api_name:
- ID3DX11EffectVariable.AsMatrix
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c26acd38124a976b53ea950f54e929e717d56555
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104996333"
---
# <a name="id3dx11effectvariableasmatrix-method"></a><span data-ttu-id="3c62b-106">ID3DX11EffectVariable :: AsMatrix, méthode</span><span class="sxs-lookup"><span data-stu-id="3c62b-106">ID3DX11EffectVariable::AsMatrix method</span></span>

<span data-ttu-id="3c62b-107">Obtenir une variable de matrice.</span><span class="sxs-lookup"><span data-stu-id="3c62b-107">Get a matrix variable.</span></span>

## <a name="syntax"></a><span data-ttu-id="3c62b-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3c62b-108">Syntax</span></span>


```C++
ID3DX11EffectMatrixVariable* AsMatrix();
```



## <a name="parameters"></a><span data-ttu-id="3c62b-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3c62b-109">Parameters</span></span>

<span data-ttu-id="3c62b-110">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="3c62b-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="3c62b-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="3c62b-111">Return value</span></span>

<span data-ttu-id="3c62b-112">Type : **[ **ID3DX11EffectMatrixVariable**](id3dx11effectmatrixvariable.md)\***</span><span class="sxs-lookup"><span data-stu-id="3c62b-112">Type: **[**ID3DX11EffectMatrixVariable**](id3dx11effectmatrixvariable.md)\***</span></span>

<span data-ttu-id="3c62b-113">Pointeur vers une variable de matrice.</span><span class="sxs-lookup"><span data-stu-id="3c62b-113">A pointer to a matrix variable.</span></span> <span data-ttu-id="3c62b-114">Consultez [**ID3DX11EffectMatrixVariable**](id3dx11effectmatrixvariable.md).</span><span class="sxs-lookup"><span data-stu-id="3c62b-114">See [**ID3DX11EffectMatrixVariable**](id3dx11effectmatrixvariable.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="3c62b-115">Notes</span><span class="sxs-lookup"><span data-stu-id="3c62b-115">Remarks</span></span>

<span data-ttu-id="3c62b-116">AsMatrix retourne une version de la variable Effect qui a été spécialisée pour une variable de matrice.</span><span class="sxs-lookup"><span data-stu-id="3c62b-116">AsMatrix returns a version of the effect variable that has been specialized to a matrix variable.</span></span> <span data-ttu-id="3c62b-117">Comme pour un cast, cette spécialisation retourne un objet non valide si la variable Effect ne contient pas de données de matrice.</span><span class="sxs-lookup"><span data-stu-id="3c62b-117">Similar to a cast, this specialization will return an invalid object if the effect variable does not contain matrix data.</span></span>

<span data-ttu-id="3c62b-118">Les applications peuvent tester la validité de l’objet retourné en appelant [**IsValid**](id3dx11effectvariable-isvalid.md).</span><span class="sxs-lookup"><span data-stu-id="3c62b-118">Applications can test the returned object for validity by calling [**IsValid**](id3dx11effectvariable-isvalid.md).</span></span>

> [!Note]  
> <span data-ttu-id="3c62b-119">Le kit de développement logiciel (SDK) DirectX ne fournit aucun binaire compilé pour les effets.</span><span class="sxs-lookup"><span data-stu-id="3c62b-119">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="3c62b-120">Vous devez utiliser la source Effects 11 pour créer votre application Effects-type.</span><span class="sxs-lookup"><span data-stu-id="3c62b-120">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="3c62b-121">Pour plus d’informations sur l’utilisation de la source Effects 11, consultez [différences entre les effets 10 et 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="3c62b-121">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="3c62b-122">Spécifications</span><span class="sxs-lookup"><span data-stu-id="3c62b-122">Requirements</span></span>



| <span data-ttu-id="3c62b-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3c62b-123">Requirement</span></span> | <span data-ttu-id="3c62b-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="3c62b-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3c62b-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="3c62b-125">Header</span></span><br/>  | <dl> <span data-ttu-id="3c62b-126"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="3c62b-126"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="3c62b-127">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="3c62b-127">Library</span></span><br/> | <dl> <span data-ttu-id="3c62b-128"><dt>N/A (une bibliothèque Effects 11 est disponible en ligne en tant que source partagée.)</dt></span><span class="sxs-lookup"><span data-stu-id="3c62b-128"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3c62b-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3c62b-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3c62b-130">ID3DX11EffectVariable</span><span class="sxs-lookup"><span data-stu-id="3c62b-130">ID3DX11EffectVariable</span></span>](id3dx11effectvariable.md)
</dt> </dl>

 

 





