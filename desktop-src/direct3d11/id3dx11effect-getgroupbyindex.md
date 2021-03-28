---
title: Méthode ID3DX11Effect GetGroupByIndex (D3dx11effect. h)
description: Obtient un groupe d’effets par index.
ms.assetid: b38ecdbf-0920-48ff-a599-9629a3581d75
keywords:
- Méthode GetGroupByIndex Direct3D 11
- Méthode GetGroupByIndex Direct3D 11, interface ID3DX11Effect
- Interface ID3DX11Effect Direct3D 11, méthode GetGroupByIndex
topic_type:
- apiref
api_name:
- ID3DX11Effect.GetGroupByIndex
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1dd0f629a60255ed28aa5cc426b99198867e0b23
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103953955"
---
# <a name="id3dx11effectgetgroupbyindex-method"></a><span data-ttu-id="cb9f2-106">ID3DX11Effect :: GetGroupByIndex, méthode</span><span class="sxs-lookup"><span data-stu-id="cb9f2-106">ID3DX11Effect::GetGroupByIndex method</span></span>

<span data-ttu-id="cb9f2-107">Obtient un groupe d’effets par index.</span><span class="sxs-lookup"><span data-stu-id="cb9f2-107">Gets an effect group by index.</span></span>

## <a name="syntax"></a><span data-ttu-id="cb9f2-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="cb9f2-108">Syntax</span></span>


```C++
ID3DX11EffectGroup* GetGroupByIndex(
   UINT Index
);
```



## <a name="parameters"></a><span data-ttu-id="cb9f2-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="cb9f2-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cb9f2-110">*Index*</span><span class="sxs-lookup"><span data-stu-id="cb9f2-110">*Index*</span></span> 
</dt> <dd>

<span data-ttu-id="cb9f2-111">Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="cb9f2-111">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="cb9f2-112">Index du groupe d’effets.</span><span class="sxs-lookup"><span data-stu-id="cb9f2-112">Index of the effect group.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cb9f2-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="cb9f2-113">Return value</span></span>

<span data-ttu-id="cb9f2-114">Type : **[ **ID3DX11EffectGroup**](id3dx11effectgroup.md)\***</span><span class="sxs-lookup"><span data-stu-id="cb9f2-114">Type: **[**ID3DX11EffectGroup**](id3dx11effectgroup.md)\***</span></span>

<span data-ttu-id="cb9f2-115">Pointeur vers une interface [**ID3DX11EffectGroup**](id3dx11effectgroup.md) .</span><span class="sxs-lookup"><span data-stu-id="cb9f2-115">A pointer to an [**ID3DX11EffectGroup**](id3dx11effectgroup.md) interface.</span></span>

## <a name="remarks"></a><span data-ttu-id="cb9f2-116">Notes</span><span class="sxs-lookup"><span data-stu-id="cb9f2-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="cb9f2-117">Le kit de développement logiciel (SDK) DirectX ne fournit aucun binaire compilé pour les effets.</span><span class="sxs-lookup"><span data-stu-id="cb9f2-117">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="cb9f2-118">Vous devez utiliser la source Effects 11 pour créer votre application Effects-type.</span><span class="sxs-lookup"><span data-stu-id="cb9f2-118">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="cb9f2-119">Pour plus d’informations sur l’utilisation de la source Effects 11, consultez [différences entre les effets 10 et 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="cb9f2-119">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="cb9f2-120">Spécifications</span><span class="sxs-lookup"><span data-stu-id="cb9f2-120">Requirements</span></span>



| <span data-ttu-id="cb9f2-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="cb9f2-121">Requirement</span></span> | <span data-ttu-id="cb9f2-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="cb9f2-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cb9f2-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="cb9f2-123">Header</span></span><br/>  | <dl> <span data-ttu-id="cb9f2-124"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="cb9f2-124"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="cb9f2-125">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="cb9f2-125">Library</span></span><br/> | <dl> <span data-ttu-id="cb9f2-126"><dt>N/A (une bibliothèque Effects 11 est disponible en ligne en tant que source partagée.)</dt></span><span class="sxs-lookup"><span data-stu-id="cb9f2-126"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cb9f2-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cb9f2-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cb9f2-128">ID3DX11Effect</span><span class="sxs-lookup"><span data-stu-id="cb9f2-128">ID3DX11Effect</span></span>](id3dx11effect.md)
</dt> </dl>

 

