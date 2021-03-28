---
title: Méthode ID3DX11EffectType GetMemberTypeByIndex (D3dx11effect. h)
description: Obtient un type de membre par index.
ms.assetid: 6421f08f-0236-4d8f-b3c2-ef7ec5ffe2a1
keywords:
- Méthode GetMemberTypeByIndex Direct3D 11
- Méthode GetMemberTypeByIndex Direct3D 11, interface ID3DX11EffectType
- Interface ID3DX11EffectType Direct3D 11, méthode GetMemberTypeByIndex
topic_type:
- apiref
api_name:
- ID3DX11EffectType.GetMemberTypeByIndex
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: da5023e064539f57af9998c788385f2a1316433f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104530969"
---
# <a name="id3dx11effecttypegetmembertypebyindex-method"></a><span data-ttu-id="03365-106">ID3DX11EffectType :: GetMemberTypeByIndex, méthode</span><span class="sxs-lookup"><span data-stu-id="03365-106">ID3DX11EffectType::GetMemberTypeByIndex method</span></span>

<span data-ttu-id="03365-107">Obtient un type de membre par index.</span><span class="sxs-lookup"><span data-stu-id="03365-107">Get a member type by index.</span></span>

## <a name="syntax"></a><span data-ttu-id="03365-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="03365-108">Syntax</span></span>


```C++
ID3DX11EffectType* GetMemberTypeByIndex(
   UINT Index
);
```



## <a name="parameters"></a><span data-ttu-id="03365-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="03365-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="03365-110">*Index*</span><span class="sxs-lookup"><span data-stu-id="03365-110">*Index*</span></span> 
</dt> <dd>

<span data-ttu-id="03365-111">Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="03365-111">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="03365-112">Index de base zéro.</span><span class="sxs-lookup"><span data-stu-id="03365-112">A zero-based index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="03365-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="03365-113">Return value</span></span>

<span data-ttu-id="03365-114">Type : **[ **ID3DX11EffectType**](id3dx11effecttype.md)\***</span><span class="sxs-lookup"><span data-stu-id="03365-114">Type: **[**ID3DX11EffectType**](id3dx11effecttype.md)\***</span></span>

<span data-ttu-id="03365-115">Pointeur vers un [**ID3DX11EffectType**](id3dx11effecttype.md).</span><span class="sxs-lookup"><span data-stu-id="03365-115">A pointer to an [**ID3DX11EffectType**](id3dx11effecttype.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="03365-116">Notes</span><span class="sxs-lookup"><span data-stu-id="03365-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="03365-117">Le kit de développement logiciel (SDK) DirectX ne fournit aucun binaire compilé pour les effets.</span><span class="sxs-lookup"><span data-stu-id="03365-117">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="03365-118">Vous devez utiliser la source Effects 11 pour créer votre application Effects-type.</span><span class="sxs-lookup"><span data-stu-id="03365-118">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="03365-119">Pour plus d’informations sur l’utilisation de la source Effects 11, consultez [différences entre les effets 10 et 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="03365-119">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="03365-120">Spécifications</span><span class="sxs-lookup"><span data-stu-id="03365-120">Requirements</span></span>



| <span data-ttu-id="03365-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="03365-121">Requirement</span></span> | <span data-ttu-id="03365-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="03365-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="03365-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="03365-123">Header</span></span><br/>  | <dl> <span data-ttu-id="03365-124"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="03365-124"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="03365-125">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="03365-125">Library</span></span><br/> | <dl> <span data-ttu-id="03365-126"><dt>N/A (une bibliothèque Effects 11 est disponible en ligne en tant que source partagée.)</dt></span><span class="sxs-lookup"><span data-stu-id="03365-126"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="03365-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="03365-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="03365-128">ID3DX11EffectType</span><span class="sxs-lookup"><span data-stu-id="03365-128">ID3DX11EffectType</span></span>](id3dx11effecttype.md)
</dt> </dl>

 

