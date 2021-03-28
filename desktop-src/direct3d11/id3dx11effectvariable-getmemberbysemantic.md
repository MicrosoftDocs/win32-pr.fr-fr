---
title: Méthode ID3DX11EffectVariable GetMemberBySemantic (D3dx11effect. h)
description: Obtenir un membre de structure par sémantique.
ms.assetid: e4ae1f6a-43d2-45df-9dba-833d4f767818
keywords:
- Méthode GetMemberBySemantic Direct3D 11
- Méthode GetMemberBySemantic Direct3D 11, interface ID3DX11EffectVariable
- Interface ID3DX11EffectVariable Direct3D 11, méthode GetMemberBySemantic
topic_type:
- apiref
api_name:
- ID3DX11EffectVariable.GetMemberBySemantic
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5af8b628247dcc89f8df99c6ffebb04d500e76a1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104996216"
---
# <a name="id3dx11effectvariablegetmemberbysemantic-method"></a><span data-ttu-id="77a38-106">ID3DX11EffectVariable :: GetMemberBySemantic, méthode</span><span class="sxs-lookup"><span data-stu-id="77a38-106">ID3DX11EffectVariable::GetMemberBySemantic method</span></span>

<span data-ttu-id="77a38-107">Obtenir un membre de structure par sémantique.</span><span class="sxs-lookup"><span data-stu-id="77a38-107">Get a structure member by semantic.</span></span>

## <a name="syntax"></a><span data-ttu-id="77a38-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="77a38-108">Syntax</span></span>


```C++
ID3DX11EffectVariable* GetMemberBySemantic(
   LPCSTR Semantic
);
```



## <a name="parameters"></a><span data-ttu-id="77a38-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="77a38-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="77a38-110">*Équivalent*</span><span class="sxs-lookup"><span data-stu-id="77a38-110">*Semantic*</span></span> 
</dt> <dd>

<span data-ttu-id="77a38-111">Type : **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="77a38-111">Type: **[**LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="77a38-112">Sémantique.</span><span class="sxs-lookup"><span data-stu-id="77a38-112">The semantic.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="77a38-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="77a38-113">Return value</span></span>

<span data-ttu-id="77a38-114">Type : **[ **ID3DX11EffectVariable**](id3dx11effectvariable.md)\***</span><span class="sxs-lookup"><span data-stu-id="77a38-114">Type: **[**ID3DX11EffectVariable**](id3dx11effectvariable.md)\***</span></span>

<span data-ttu-id="77a38-115">Pointeur vers un [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span><span class="sxs-lookup"><span data-stu-id="77a38-115">A pointer to an [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="77a38-116">Notes</span><span class="sxs-lookup"><span data-stu-id="77a38-116">Remarks</span></span>

<span data-ttu-id="77a38-117">Si la variable d’effet est une structure, utilisez cette méthode pour rechercher un membre à l’aide de la sémantique jointe.</span><span class="sxs-lookup"><span data-stu-id="77a38-117">If the effect variable is an structure, use this method to look up a member by attached semantic.</span></span>

> [!Note]  
> <span data-ttu-id="77a38-118">Le kit de développement logiciel (SDK) DirectX ne fournit aucun binaire compilé pour les effets.</span><span class="sxs-lookup"><span data-stu-id="77a38-118">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="77a38-119">Vous devez utiliser la source Effects 11 pour créer votre application Effects-type.</span><span class="sxs-lookup"><span data-stu-id="77a38-119">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="77a38-120">Pour plus d’informations sur l’utilisation de la source Effects 11, consultez [différences entre les effets 10 et 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="77a38-120">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="77a38-121">Spécifications</span><span class="sxs-lookup"><span data-stu-id="77a38-121">Requirements</span></span>



| <span data-ttu-id="77a38-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="77a38-122">Requirement</span></span> | <span data-ttu-id="77a38-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="77a38-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="77a38-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="77a38-124">Header</span></span><br/>  | <dl> <span data-ttu-id="77a38-125"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="77a38-125"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="77a38-126">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="77a38-126">Library</span></span><br/> | <dl> <span data-ttu-id="77a38-127"><dt>N/A (une bibliothèque Effects 11 est disponible en ligne en tant que source partagée.)</dt></span><span class="sxs-lookup"><span data-stu-id="77a38-127"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="77a38-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="77a38-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="77a38-129">ID3DX11EffectVariable</span><span class="sxs-lookup"><span data-stu-id="77a38-129">ID3DX11EffectVariable</span></span>](id3dx11effectvariable.md)
</dt> </dl>

 

