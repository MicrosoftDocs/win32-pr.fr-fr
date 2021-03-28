---
title: Méthode ID3DX11Effect GetTechniqueByIndex (D3dx11effect. h)
description: Obtient une technique par index. | Méthode ID3DX11Effect GetTechniqueByIndex (D3dx11effect. h)
ms.assetid: ee9c0cc3-0ca1-42e8-bd37-5878fd56cff1
keywords:
- Méthode GetTechniqueByIndex Direct3D 11
- Méthode GetTechniqueByIndex Direct3D 11, interface ID3DX11Effect
- Interface ID3DX11Effect Direct3D 11, méthode GetTechniqueByIndex
topic_type:
- apiref
api_name:
- ID3DX11Effect.GetTechniqueByIndex
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 81d3be5ec403fb25ab3a49792ed77fd4d96bf571
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103953954"
---
# <a name="id3dx11effectgettechniquebyindex-method"></a><span data-ttu-id="7d38e-107">ID3DX11Effect :: GetTechniqueByIndex, méthode</span><span class="sxs-lookup"><span data-stu-id="7d38e-107">ID3DX11Effect::GetTechniqueByIndex method</span></span>

<span data-ttu-id="7d38e-108">Obtient une technique par index.</span><span class="sxs-lookup"><span data-stu-id="7d38e-108">Get a technique by index.</span></span>

## <a name="syntax"></a><span data-ttu-id="7d38e-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7d38e-109">Syntax</span></span>


```C++
ID3DX11EffectTechnique* GetTechniqueByIndex(
   UINT Index
);
```



## <a name="parameters"></a><span data-ttu-id="7d38e-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7d38e-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7d38e-111">*Index*</span><span class="sxs-lookup"><span data-stu-id="7d38e-111">*Index*</span></span> 
</dt> <dd>

<span data-ttu-id="7d38e-112">Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="7d38e-112">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="7d38e-113">Index de base zéro.</span><span class="sxs-lookup"><span data-stu-id="7d38e-113">A zero-based index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7d38e-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="7d38e-114">Return value</span></span>

<span data-ttu-id="7d38e-115">Type : **[ **ID3DX11EffectTechnique**](id3dx11effecttechnique.md)\***</span><span class="sxs-lookup"><span data-stu-id="7d38e-115">Type: **[**ID3DX11EffectTechnique**](id3dx11effecttechnique.md)\***</span></span>

<span data-ttu-id="7d38e-116">Pointeur vers un [**ID3DX11EffectTechnique**](id3dx11effecttechnique.md).</span><span class="sxs-lookup"><span data-stu-id="7d38e-116">A pointer to an [**ID3DX11EffectTechnique**](id3dx11effecttechnique.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="7d38e-117">Notes</span><span class="sxs-lookup"><span data-stu-id="7d38e-117">Remarks</span></span>

<span data-ttu-id="7d38e-118">Un effet contient une ou plusieurs techniques ; chaque technique contient une ou plusieurs passes.</span><span class="sxs-lookup"><span data-stu-id="7d38e-118">An effect contains one or more techniques; each technique contains one or more passes.</span></span> <span data-ttu-id="7d38e-119">Vous pouvez accéder à une technique à l’aide de son nom ou d’un index.</span><span class="sxs-lookup"><span data-stu-id="7d38e-119">You can access a technique using its name or with an index.</span></span>

> [!Note]  
> <span data-ttu-id="7d38e-120">Le kit de développement logiciel (SDK) DirectX ne fournit aucun binaire compilé pour les effets.</span><span class="sxs-lookup"><span data-stu-id="7d38e-120">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="7d38e-121">Vous devez utiliser la source Effects 11 pour créer votre application Effects-type.</span><span class="sxs-lookup"><span data-stu-id="7d38e-121">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="7d38e-122">Pour plus d’informations sur l’utilisation de la source Effects 11, consultez [différences entre les effets 10 et 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="7d38e-122">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="7d38e-123">Spécifications</span><span class="sxs-lookup"><span data-stu-id="7d38e-123">Requirements</span></span>



| <span data-ttu-id="7d38e-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7d38e-124">Requirement</span></span> | <span data-ttu-id="7d38e-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="7d38e-125">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7d38e-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="7d38e-126">Header</span></span><br/>  | <dl> <span data-ttu-id="7d38e-127"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="7d38e-127"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="7d38e-128">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="7d38e-128">Library</span></span><br/> | <dl> <span data-ttu-id="7d38e-129"><dt>N/A (une bibliothèque Effects 11 est disponible en ligne en tant que source partagée.)</dt></span><span class="sxs-lookup"><span data-stu-id="7d38e-129"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7d38e-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7d38e-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7d38e-131">ID3DX11Effect</span><span class="sxs-lookup"><span data-stu-id="7d38e-131">ID3DX11Effect</span></span>](id3dx11effect.md)
</dt> </dl>

 

