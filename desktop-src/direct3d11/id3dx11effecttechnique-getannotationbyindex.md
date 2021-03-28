---
title: Méthode ID3DX11EffectTechnique GetAnnotationByIndex (D3dx11effect. h)
description: Obtient une annotation par index. | Méthode ID3DX11EffectTechnique GetAnnotationByIndex (D3dx11effect. h)
ms.assetid: 703663b0-ee00-4686-a038-6c99ce61266b
keywords:
- Méthode GetAnnotationByIndex Direct3D 11
- Méthode GetAnnotationByIndex Direct3D 11, interface ID3DX11EffectTechnique
- Interface ID3DX11EffectTechnique Direct3D 11, méthode GetAnnotationByIndex
topic_type:
- apiref
api_name:
- ID3DX11EffectTechnique.GetAnnotationByIndex
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e30712ba38f1360a992a8e409c249a746cca036
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104996221"
---
# <a name="id3dx11effecttechniquegetannotationbyindex-method"></a><span data-ttu-id="1e070-107">ID3DX11EffectTechnique :: GetAnnotationByIndex, méthode</span><span class="sxs-lookup"><span data-stu-id="1e070-107">ID3DX11EffectTechnique::GetAnnotationByIndex method</span></span>

<span data-ttu-id="1e070-108">Obtient une annotation par index.</span><span class="sxs-lookup"><span data-stu-id="1e070-108">Get an annotation by index.</span></span>

## <a name="syntax"></a><span data-ttu-id="1e070-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1e070-109">Syntax</span></span>


```C++
ID3DX11EffectVariable* GetAnnotationByIndex(
   UINT Index
);
```



## <a name="parameters"></a><span data-ttu-id="1e070-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1e070-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1e070-111">*Index*</span><span class="sxs-lookup"><span data-stu-id="1e070-111">*Index*</span></span> 
</dt> <dd>

<span data-ttu-id="1e070-112">Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="1e070-112">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="1e070-113">Index de base zéro du pointeur d’interface.</span><span class="sxs-lookup"><span data-stu-id="1e070-113">The zero-based index of the interface pointer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1e070-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="1e070-114">Return value</span></span>

<span data-ttu-id="1e070-115">Type : **[ **ID3DX11EffectVariable**](id3dx11effectvariable.md)\***</span><span class="sxs-lookup"><span data-stu-id="1e070-115">Type: **[**ID3DX11EffectVariable**](id3dx11effectvariable.md)\***</span></span>

<span data-ttu-id="1e070-116">Pointeur vers un [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span><span class="sxs-lookup"><span data-stu-id="1e070-116">A pointer to an [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="1e070-117">Notes</span><span class="sxs-lookup"><span data-stu-id="1e070-117">Remarks</span></span>

<span data-ttu-id="1e070-118">Utilisez une annotation pour attacher un élément de métadonnées à une technique.</span><span class="sxs-lookup"><span data-stu-id="1e070-118">Use an annotation to attach a piece of metadata to a technique.</span></span>

> [!Note]  
> <span data-ttu-id="1e070-119">Le kit de développement logiciel (SDK) DirectX ne fournit aucun binaire compilé pour les effets.</span><span class="sxs-lookup"><span data-stu-id="1e070-119">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="1e070-120">Vous devez utiliser la source Effects 11 pour créer votre application Effects-type.</span><span class="sxs-lookup"><span data-stu-id="1e070-120">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="1e070-121">Pour plus d’informations sur l’utilisation de la source Effects 11, consultez [différences entre les effets 10 et 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="1e070-121">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="1e070-122">Spécifications</span><span class="sxs-lookup"><span data-stu-id="1e070-122">Requirements</span></span>



| <span data-ttu-id="1e070-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1e070-123">Requirement</span></span> | <span data-ttu-id="1e070-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="1e070-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1e070-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="1e070-125">Header</span></span><br/>  | <dl> <span data-ttu-id="1e070-126"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="1e070-126"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="1e070-127">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="1e070-127">Library</span></span><br/> | <dl> <span data-ttu-id="1e070-128"><dt>N/A (une bibliothèque Effects 11 est disponible en ligne en tant que source partagée.)</dt></span><span class="sxs-lookup"><span data-stu-id="1e070-128"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1e070-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1e070-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1e070-130">ID3DX11EffectTechnique</span><span class="sxs-lookup"><span data-stu-id="1e070-130">ID3DX11EffectTechnique</span></span>](id3dx11effecttechnique.md)
</dt> </dl>

 

