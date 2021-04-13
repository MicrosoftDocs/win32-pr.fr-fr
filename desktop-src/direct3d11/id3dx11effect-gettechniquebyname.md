---
title: Méthode ID3DX11Effect GetTechniqueByName (D3dx11effect. h)
description: Obtient une technique par nom. | Méthode ID3DX11Effect GetTechniqueByName (D3dx11effect. h)
ms.assetid: 0f7fa02c-dfbf-4971-86ad-3429f99f84e0
keywords:
- Méthode GetTechniqueByName Direct3D 11
- Méthode GetTechniqueByName Direct3D 11, interface ID3DX11Effect
- Interface ID3DX11Effect Direct3D 11, méthode GetTechniqueByName
topic_type:
- apiref
api_name:
- ID3DX11Effect.GetTechniqueByName
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d26b6067352d4ca898cc1fc970524040d407bda1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104974655"
---
# <a name="id3dx11effectgettechniquebyname-method"></a><span data-ttu-id="bffcc-107">ID3DX11Effect :: GetTechniqueByName, méthode</span><span class="sxs-lookup"><span data-stu-id="bffcc-107">ID3DX11Effect::GetTechniqueByName method</span></span>

<span data-ttu-id="bffcc-108">Obtient une technique par nom.</span><span class="sxs-lookup"><span data-stu-id="bffcc-108">Get a technique by name.</span></span>

## <a name="syntax"></a><span data-ttu-id="bffcc-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="bffcc-109">Syntax</span></span>


```C++
ID3DX11EffectTechnique* GetTechniqueByName(
   LPCSTR Name
);
```



## <a name="parameters"></a><span data-ttu-id="bffcc-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="bffcc-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bffcc-111">*Nom*</span><span class="sxs-lookup"><span data-stu-id="bffcc-111">*Name*</span></span> 
</dt> <dd>

<span data-ttu-id="bffcc-112">Type : **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="bffcc-112">Type: **[**LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="bffcc-113">Nom de la technique.</span><span class="sxs-lookup"><span data-stu-id="bffcc-113">The name of the technique.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bffcc-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="bffcc-114">Return value</span></span>

<span data-ttu-id="bffcc-115">Type : **[ **ID3DX11EffectTechnique**](id3dx11effecttechnique.md)\***</span><span class="sxs-lookup"><span data-stu-id="bffcc-115">Type: **[**ID3DX11EffectTechnique**](id3dx11effecttechnique.md)\***</span></span>

<span data-ttu-id="bffcc-116">Pointeur vers un [**ID3DX11EffectTechnique**](id3dx11effecttechnique.md).</span><span class="sxs-lookup"><span data-stu-id="bffcc-116">A pointer to an [**ID3DX11EffectTechnique**](id3dx11effecttechnique.md).</span></span> <span data-ttu-id="bffcc-117">Si une technique portant le nom approprié est introuvable, une technique non valide est retournée.</span><span class="sxs-lookup"><span data-stu-id="bffcc-117">If a technique with the appropriate name is not found an invalid technique is returned.</span></span> <span data-ttu-id="bffcc-118">[**ID3DX11EffectTechnique :: IsValid**](id3dx11effecttechnique-isvalid.md) doit être appelé sur la technique retournée pour déterminer s’il est valide.</span><span class="sxs-lookup"><span data-stu-id="bffcc-118">[**ID3DX11EffectTechnique::IsValid**](id3dx11effecttechnique-isvalid.md) should be called on the returned technique to determine whether it is valid.</span></span>

## <a name="remarks"></a><span data-ttu-id="bffcc-119">Notes</span><span class="sxs-lookup"><span data-stu-id="bffcc-119">Remarks</span></span>

<span data-ttu-id="bffcc-120">Un effet contient une ou plusieurs techniques ; chaque technique contient une ou plusieurs passes.</span><span class="sxs-lookup"><span data-stu-id="bffcc-120">An effect contains one or more techniques; each technique contains one or more passes.</span></span> <span data-ttu-id="bffcc-121">Vous pouvez accéder à une technique à l’aide de son nom ou d’un index.</span><span class="sxs-lookup"><span data-stu-id="bffcc-121">You can access a technique using its name or with an index.</span></span>

> [!Note]  
> <span data-ttu-id="bffcc-122">Le kit de développement logiciel (SDK) DirectX ne fournit aucun binaire compilé pour les effets.</span><span class="sxs-lookup"><span data-stu-id="bffcc-122">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="bffcc-123">Vous devez utiliser la source Effects 11 pour créer votre application Effects-type.</span><span class="sxs-lookup"><span data-stu-id="bffcc-123">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="bffcc-124">Pour plus d’informations sur l’utilisation de la source Effects 11, consultez [différences entre les effets 10 et 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="bffcc-124">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="bffcc-125">Spécifications</span><span class="sxs-lookup"><span data-stu-id="bffcc-125">Requirements</span></span>



| <span data-ttu-id="bffcc-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="bffcc-126">Requirement</span></span> | <span data-ttu-id="bffcc-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="bffcc-127">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bffcc-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="bffcc-128">Header</span></span><br/>  | <dl> <span data-ttu-id="bffcc-129"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="bffcc-129"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="bffcc-130">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="bffcc-130">Library</span></span><br/> | <dl> <span data-ttu-id="bffcc-131"><dt>N/A (une bibliothèque Effects 11 est disponible en ligne en tant que source partagée.)</dt></span><span class="sxs-lookup"><span data-stu-id="bffcc-131"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bffcc-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bffcc-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bffcc-133">ID3DX11Effect</span><span class="sxs-lookup"><span data-stu-id="bffcc-133">ID3DX11Effect</span></span>](id3dx11effect.md)
</dt> </dl>

 

