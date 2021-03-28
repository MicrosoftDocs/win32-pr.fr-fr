---
title: Méthode ID3DX11EffectGroup GetTechniqueByName (D3dx11effect. h)
description: Obtient une technique par nom. | Méthode ID3DX11EffectGroup GetTechniqueByName (D3dx11effect. h)
ms.assetid: 160c6d57-bec4-4718-8fad-fc9c0746736c
keywords:
- Méthode GetTechniqueByName Direct3D 11
- Méthode GetTechniqueByName Direct3D 11, interface ID3DX11EffectGroup
- Interface ID3DX11EffectGroup Direct3D 11, méthode GetTechniqueByName
topic_type:
- apiref
api_name:
- ID3DX11EffectGroup.GetTechniqueByName
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c5121f67345ba863d773d8e7a73a5d6fa8b69895
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104974571"
---
# <a name="id3dx11effectgroupgettechniquebyname-method"></a><span data-ttu-id="fec1f-107">ID3DX11EffectGroup :: GetTechniqueByName, méthode</span><span class="sxs-lookup"><span data-stu-id="fec1f-107">ID3DX11EffectGroup::GetTechniqueByName method</span></span>

<span data-ttu-id="fec1f-108">Obtient une technique par nom.</span><span class="sxs-lookup"><span data-stu-id="fec1f-108">Get a technique by name.</span></span>

## <a name="syntax"></a><span data-ttu-id="fec1f-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fec1f-109">Syntax</span></span>


```C++
ID3DX11EffectTechnique* GetTechniqueByName(
   LPCSTR Name
);
```



## <a name="parameters"></a><span data-ttu-id="fec1f-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="fec1f-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fec1f-111">*Nom*</span><span class="sxs-lookup"><span data-stu-id="fec1f-111">*Name*</span></span> 
</dt> <dd>

<span data-ttu-id="fec1f-112">Type : **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="fec1f-112">Type: **[**LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="fec1f-113">Nom de la technique.</span><span class="sxs-lookup"><span data-stu-id="fec1f-113">The name of the technique.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fec1f-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="fec1f-114">Return value</span></span>

<span data-ttu-id="fec1f-115">Type : **[ **ID3DX11EffectTechnique**](id3dx11effecttechnique.md)\***</span><span class="sxs-lookup"><span data-stu-id="fec1f-115">Type: **[**ID3DX11EffectTechnique**](id3dx11effecttechnique.md)\***</span></span>

<span data-ttu-id="fec1f-116">Pointeur vers un [**ID3DX11EffectTechnique**](id3dx11effecttechnique.md), ou **null** si la technique est introuvable.</span><span class="sxs-lookup"><span data-stu-id="fec1f-116">A pointer to an [**ID3DX11EffectTechnique**](id3dx11effecttechnique.md), or **NULL** if the technique is not found.</span></span>

## <a name="remarks"></a><span data-ttu-id="fec1f-117">Notes</span><span class="sxs-lookup"><span data-stu-id="fec1f-117">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="fec1f-118">Le kit de développement logiciel (SDK) DirectX ne fournit aucun binaire compilé pour les effets.</span><span class="sxs-lookup"><span data-stu-id="fec1f-118">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="fec1f-119">Vous devez utiliser la source Effects 11 pour créer votre application Effects-type.</span><span class="sxs-lookup"><span data-stu-id="fec1f-119">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="fec1f-120">Pour plus d’informations sur l’utilisation de la source Effects 11, consultez [différences entre les effets 10 et 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="fec1f-120">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="fec1f-121">Spécifications</span><span class="sxs-lookup"><span data-stu-id="fec1f-121">Requirements</span></span>



| <span data-ttu-id="fec1f-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="fec1f-122">Requirement</span></span> | <span data-ttu-id="fec1f-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="fec1f-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fec1f-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="fec1f-124">Header</span></span><br/>  | <dl> <span data-ttu-id="fec1f-125"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="fec1f-125"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="fec1f-126">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="fec1f-126">Library</span></span><br/> | <dl> <span data-ttu-id="fec1f-127"><dt>N/A (une bibliothèque Effects 11 est disponible en ligne en tant que source partagée.)</dt></span><span class="sxs-lookup"><span data-stu-id="fec1f-127"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fec1f-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fec1f-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fec1f-129">ID3DX11EffectGroup</span><span class="sxs-lookup"><span data-stu-id="fec1f-129">ID3DX11EffectGroup</span></span>](id3dx11effectgroup.md)
</dt> </dl>

 

