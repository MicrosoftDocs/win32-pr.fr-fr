---
title: Méthode ID3DX11EffectVariable GetMemberByName (D3dx11effect. h)
description: Obtient un membre de structure par nom.
ms.assetid: 09f7f2f8-f55f-411c-8130-6ae44015d58a
keywords:
- Méthode GetMemberByName Direct3D 11
- Méthode GetMemberByName Direct3D 11, interface ID3DX11EffectVariable
- Interface ID3DX11EffectVariable Direct3D 11, méthode GetMemberByName
topic_type:
- apiref
api_name:
- ID3DX11EffectVariable.GetMemberByName
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9851a2f74502a79b5cc85c494e468c4a346798f0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104996280"
---
# <a name="id3dx11effectvariablegetmemberbyname-method"></a><span data-ttu-id="456d6-106">ID3DX11EffectVariable :: GetMemberByName, méthode</span><span class="sxs-lookup"><span data-stu-id="456d6-106">ID3DX11EffectVariable::GetMemberByName method</span></span>

<span data-ttu-id="456d6-107">Obtient un membre de structure par nom.</span><span class="sxs-lookup"><span data-stu-id="456d6-107">Get a structure member by name.</span></span>

## <a name="syntax"></a><span data-ttu-id="456d6-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="456d6-108">Syntax</span></span>


```C++
ID3DX11EffectVariable* GetMemberByName(
   LPCSTR Name
);
```



## <a name="parameters"></a><span data-ttu-id="456d6-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="456d6-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="456d6-110">*Nom*</span><span class="sxs-lookup"><span data-stu-id="456d6-110">*Name*</span></span> 
</dt> <dd>

<span data-ttu-id="456d6-111">Type : **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="456d6-111">Type: **[**LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="456d6-112">Nom du membre.</span><span class="sxs-lookup"><span data-stu-id="456d6-112">Member name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="456d6-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="456d6-113">Return value</span></span>

<span data-ttu-id="456d6-114">Type : **[ **ID3DX11EffectVariable**](id3dx11effectvariable.md)\***</span><span class="sxs-lookup"><span data-stu-id="456d6-114">Type: **[**ID3DX11EffectVariable**](id3dx11effectvariable.md)\***</span></span>

<span data-ttu-id="456d6-115">Pointeur vers un [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span><span class="sxs-lookup"><span data-stu-id="456d6-115">A pointer to an [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="456d6-116">Notes</span><span class="sxs-lookup"><span data-stu-id="456d6-116">Remarks</span></span>

<span data-ttu-id="456d6-117">Si la variable d’effet est une structure, utilisez cette méthode pour rechercher un membre par son nom.</span><span class="sxs-lookup"><span data-stu-id="456d6-117">If the effect variable is an structure, use this method to look up a member by name.</span></span>

> [!Note]  
> <span data-ttu-id="456d6-118">Le kit de développement logiciel (SDK) DirectX ne fournit aucun binaire compilé pour les effets.</span><span class="sxs-lookup"><span data-stu-id="456d6-118">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="456d6-119">Vous devez utiliser la source Effects 11 pour créer votre application Effects-type.</span><span class="sxs-lookup"><span data-stu-id="456d6-119">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="456d6-120">Pour plus d’informations sur l’utilisation de la source Effects 11, consultez [différences entre les effets 10 et 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="456d6-120">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="456d6-121">Spécifications</span><span class="sxs-lookup"><span data-stu-id="456d6-121">Requirements</span></span>



| <span data-ttu-id="456d6-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="456d6-122">Requirement</span></span> | <span data-ttu-id="456d6-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="456d6-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="456d6-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="456d6-124">Header</span></span><br/>  | <dl> <span data-ttu-id="456d6-125"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="456d6-125"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="456d6-126">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="456d6-126">Library</span></span><br/> | <dl> <span data-ttu-id="456d6-127"><dt>N/A (une bibliothèque Effects 11 est disponible en ligne en tant que source partagée.)</dt></span><span class="sxs-lookup"><span data-stu-id="456d6-127"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="456d6-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="456d6-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="456d6-129">ID3DX11EffectVariable</span><span class="sxs-lookup"><span data-stu-id="456d6-129">ID3DX11EffectVariable</span></span>](id3dx11effectvariable.md)
</dt> </dl>

 

