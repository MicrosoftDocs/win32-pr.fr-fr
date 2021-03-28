---
title: Méthode ID3DX11EffectPass GetAnnotationByName (D3dx11effect. h)
description: Obtient une annotation par nom. | Méthode ID3DX11EffectPass GetAnnotationByName (D3dx11effect. h)
ms.assetid: b54a4fb0-62c7-4d96-af30-f9ae04ff7dab
keywords:
- Méthode GetAnnotationByName Direct3D 11
- Méthode GetAnnotationByName Direct3D 11, interface ID3DX11EffectPass
- Interface ID3DX11EffectPass Direct3D 11, méthode GetAnnotationByName
topic_type:
- apiref
api_name:
- ID3DX11EffectPass.GetAnnotationByName
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d129f1548e7f63c47906ac736cbddb5f6b2548b2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103953936"
---
# <a name="id3dx11effectpassgetannotationbyname-method"></a><span data-ttu-id="e3f87-107">ID3DX11EffectPass :: GetAnnotationByName, méthode</span><span class="sxs-lookup"><span data-stu-id="e3f87-107">ID3DX11EffectPass::GetAnnotationByName method</span></span>

<span data-ttu-id="e3f87-108">Obtient une annotation par nom.</span><span class="sxs-lookup"><span data-stu-id="e3f87-108">Get an annotation by name.</span></span>

## <a name="syntax"></a><span data-ttu-id="e3f87-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e3f87-109">Syntax</span></span>


```C++
ID3DX11EffectVariable* GetAnnotationByName(
   LPCSTR Name
);
```



## <a name="parameters"></a><span data-ttu-id="e3f87-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e3f87-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e3f87-111">*Nom*</span><span class="sxs-lookup"><span data-stu-id="e3f87-111">*Name*</span></span> 
</dt> <dd>

<span data-ttu-id="e3f87-112">Type : **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="e3f87-112">Type: **[**LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="e3f87-113">Nom de l’annotation.</span><span class="sxs-lookup"><span data-stu-id="e3f87-113">The name of the annotation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e3f87-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="e3f87-114">Return value</span></span>

<span data-ttu-id="e3f87-115">Type : **[ **ID3DX11EffectVariable**](id3dx11effectvariable.md)\***</span><span class="sxs-lookup"><span data-stu-id="e3f87-115">Type: **[**ID3DX11EffectVariable**](id3dx11effectvariable.md)\***</span></span>

<span data-ttu-id="e3f87-116">Pointeur vers un [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span><span class="sxs-lookup"><span data-stu-id="e3f87-116">A pointer to an [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="e3f87-117">Notes</span><span class="sxs-lookup"><span data-stu-id="e3f87-117">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="e3f87-118">Le kit de développement logiciel (SDK) DirectX ne fournit aucun binaire compilé pour les effets.</span><span class="sxs-lookup"><span data-stu-id="e3f87-118">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="e3f87-119">Vous devez utiliser la source Effects 11 pour créer votre application Effects-type.</span><span class="sxs-lookup"><span data-stu-id="e3f87-119">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="e3f87-120">Pour plus d’informations sur l’utilisation de la source Effects 11, consultez [différences entre les effets 10 et 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="e3f87-120">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="e3f87-121">Spécifications</span><span class="sxs-lookup"><span data-stu-id="e3f87-121">Requirements</span></span>



| <span data-ttu-id="e3f87-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e3f87-122">Requirement</span></span> | <span data-ttu-id="e3f87-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="e3f87-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e3f87-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="e3f87-124">Header</span></span><br/>  | <dl> <span data-ttu-id="e3f87-125"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="e3f87-125"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="e3f87-126">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="e3f87-126">Library</span></span><br/> | <dl> <span data-ttu-id="e3f87-127"><dt>N/A (une bibliothèque Effects 11 est disponible en ligne en tant que source partagée.)</dt></span><span class="sxs-lookup"><span data-stu-id="e3f87-127"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e3f87-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e3f87-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e3f87-129">ID3DX11EffectPass</span><span class="sxs-lookup"><span data-stu-id="e3f87-129">ID3DX11EffectPass</span></span>](id3dx11effectpass.md)
</dt> </dl>

 

