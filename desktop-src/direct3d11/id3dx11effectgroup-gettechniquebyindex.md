---
title: Méthode ID3DX11EffectGroup GetTechniqueByIndex (D3dx11effect. h)
description: Obtient une technique par index. | Méthode ID3DX11EffectGroup GetTechniqueByIndex (D3dx11effect. h)
ms.assetid: b0962957-20d1-4ec6-9f8e-acc7a62c5f4e
keywords:
- Méthode GetTechniqueByIndex Direct3D 11
- Méthode GetTechniqueByIndex Direct3D 11, interface ID3DX11EffectGroup
- Interface ID3DX11EffectGroup Direct3D 11, méthode GetTechniqueByIndex
topic_type:
- apiref
api_name:
- ID3DX11EffectGroup.GetTechniqueByIndex
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fe42d71886ae93bdaff7ac956554ff9a97fc9f8f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103953918"
---
# <a name="id3dx11effectgroupgettechniquebyindex-method"></a><span data-ttu-id="41685-107">ID3DX11EffectGroup :: GetTechniqueByIndex, méthode</span><span class="sxs-lookup"><span data-stu-id="41685-107">ID3DX11EffectGroup::GetTechniqueByIndex method</span></span>

<span data-ttu-id="41685-108">Obtient une technique par index.</span><span class="sxs-lookup"><span data-stu-id="41685-108">Get a technique by index.</span></span>

## <a name="syntax"></a><span data-ttu-id="41685-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="41685-109">Syntax</span></span>


```C++
ID3DX11EffectTechnique* GetTechniqueByIndex(
   UINT Index
);
```



## <a name="parameters"></a><span data-ttu-id="41685-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="41685-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="41685-111">*Index*</span><span class="sxs-lookup"><span data-stu-id="41685-111">*Index*</span></span> 
</dt> <dd>

<span data-ttu-id="41685-112">Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="41685-112">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="41685-113">Index de base zéro.</span><span class="sxs-lookup"><span data-stu-id="41685-113">A zero-based index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="41685-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="41685-114">Return value</span></span>

<span data-ttu-id="41685-115">Type : **[ **ID3DX11EffectTechnique**](id3dx11effecttechnique.md)\***</span><span class="sxs-lookup"><span data-stu-id="41685-115">Type: **[**ID3DX11EffectTechnique**](id3dx11effecttechnique.md)\***</span></span>

<span data-ttu-id="41685-116">Pointeur vers un [**ID3DX11EffectTechnique**](id3dx11effecttechnique.md).</span><span class="sxs-lookup"><span data-stu-id="41685-116">A pointer to an [**ID3DX11EffectTechnique**](id3dx11effecttechnique.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="41685-117">Notes</span><span class="sxs-lookup"><span data-stu-id="41685-117">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="41685-118">Le kit de développement logiciel (SDK) DirectX ne fournit aucun binaire compilé pour les effets.</span><span class="sxs-lookup"><span data-stu-id="41685-118">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="41685-119">Vous devez utiliser la source Effects 11 pour créer votre application Effects-type.</span><span class="sxs-lookup"><span data-stu-id="41685-119">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="41685-120">Pour plus d’informations sur l’utilisation de la source Effects 11, consultez [différences entre les effets 10 et 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="41685-120">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="41685-121">Spécifications</span><span class="sxs-lookup"><span data-stu-id="41685-121">Requirements</span></span>



| <span data-ttu-id="41685-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="41685-122">Requirement</span></span> | <span data-ttu-id="41685-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="41685-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="41685-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="41685-124">Header</span></span><br/>  | <dl> <span data-ttu-id="41685-125"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="41685-125"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="41685-126">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="41685-126">Library</span></span><br/> | <dl> <span data-ttu-id="41685-127"><dt>N/A (une bibliothèque Effects 11 est disponible en ligne en tant que source partagée.)</dt></span><span class="sxs-lookup"><span data-stu-id="41685-127"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="41685-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="41685-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="41685-129">ID3DX11EffectGroup</span><span class="sxs-lookup"><span data-stu-id="41685-129">ID3DX11EffectGroup</span></span>](id3dx11effectgroup.md)
</dt> </dl>

 

