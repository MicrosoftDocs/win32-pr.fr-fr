---
title: Méthode ID3DX11Effect GetVariableByIndex (D3dx11effect. h)
description: Obtient une variable par index.
ms.assetid: af25b945-9526-45c2-8746-8b62f8166de7
keywords:
- Méthode GetVariableByIndex Direct3D 11
- Méthode GetVariableByIndex Direct3D 11, interface ID3DX11Effect
- Interface ID3DX11Effect Direct3D 11, méthode GetVariableByIndex
topic_type:
- apiref
api_name:
- ID3DX11Effect.GetVariableByIndex
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fd262ea0aa778f03c2d723dec99f531f3419f3be
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104992340"
---
# <a name="id3dx11effectgetvariablebyindex-method"></a><span data-ttu-id="62bfe-106">ID3DX11Effect :: GetVariableByIndex, méthode</span><span class="sxs-lookup"><span data-stu-id="62bfe-106">ID3DX11Effect::GetVariableByIndex method</span></span>

<span data-ttu-id="62bfe-107">Obtient une variable par index.</span><span class="sxs-lookup"><span data-stu-id="62bfe-107">Get a variable by index.</span></span>

## <a name="syntax"></a><span data-ttu-id="62bfe-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="62bfe-108">Syntax</span></span>


```C++
ID3DX11EffectVariable* GetVariableByIndex(
   UINT Index
);
```



## <a name="parameters"></a><span data-ttu-id="62bfe-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="62bfe-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="62bfe-110">*Index*</span><span class="sxs-lookup"><span data-stu-id="62bfe-110">*Index*</span></span> 
</dt> <dd>

<span data-ttu-id="62bfe-111">Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="62bfe-111">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="62bfe-112">Index de base zéro.</span><span class="sxs-lookup"><span data-stu-id="62bfe-112">A zero-based index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="62bfe-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="62bfe-113">Return value</span></span>

<span data-ttu-id="62bfe-114">Type : **[ **ID3DX11EffectVariable**](id3dx11effectvariable.md)\***</span><span class="sxs-lookup"><span data-stu-id="62bfe-114">Type: **[**ID3DX11EffectVariable**](id3dx11effectvariable.md)\***</span></span>

<span data-ttu-id="62bfe-115">Pointeur vers un [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span><span class="sxs-lookup"><span data-stu-id="62bfe-115">A pointer to a [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="62bfe-116">Notes</span><span class="sxs-lookup"><span data-stu-id="62bfe-116">Remarks</span></span>

<span data-ttu-id="62bfe-117">Un effet peut contenir une ou plusieurs variables.</span><span class="sxs-lookup"><span data-stu-id="62bfe-117">An effect may contain one or more variables.</span></span> <span data-ttu-id="62bfe-118">Les variables en dehors d’une technique sont considérées comme globales pour tous les effets, celles qui se trouvent à l’intérieur d’une technique sont locales à cette technique.</span><span class="sxs-lookup"><span data-stu-id="62bfe-118">Variables outside of a technique are considered global to all effects, those located inside of a technique are local to that technique.</span></span> <span data-ttu-id="62bfe-119">Vous pouvez accéder à n’importe quelle variable d’effet non statique locale à l’aide de son nom ou d’un index.</span><span class="sxs-lookup"><span data-stu-id="62bfe-119">You can access any local non-static effect variable using its name or with an index.</span></span>

<span data-ttu-id="62bfe-120">La méthode retourne un pointeur vers une [**interface de variable Effect**](id3dx11effectvariable.md) si une variable est introuvable ; vous pouvez appeler [**ID3DX11Effect :: IsValid**](id3dx11effect-isvalid.md) pour vérifier si l’index existe.</span><span class="sxs-lookup"><span data-stu-id="62bfe-120">The method returns a pointer to an [**effect-variable interface**](id3dx11effectvariable.md) if a variable is not found; you can call [**ID3DX11Effect::IsValid**](id3dx11effect-isvalid.md) to verify whether or not the index exists.</span></span>

> [!Note]  
> <span data-ttu-id="62bfe-121">Le kit de développement logiciel (SDK) DirectX ne fournit aucun binaire compilé pour les effets.</span><span class="sxs-lookup"><span data-stu-id="62bfe-121">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="62bfe-122">Vous devez utiliser la source Effects 11 pour créer votre application Effects-type.</span><span class="sxs-lookup"><span data-stu-id="62bfe-122">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="62bfe-123">Pour plus d’informations sur l’utilisation de la source Effects 11, consultez [différences entre les effets 10 et 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="62bfe-123">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="62bfe-124">Spécifications</span><span class="sxs-lookup"><span data-stu-id="62bfe-124">Requirements</span></span>



| <span data-ttu-id="62bfe-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="62bfe-125">Requirement</span></span> | <span data-ttu-id="62bfe-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="62bfe-126">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="62bfe-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="62bfe-127">Header</span></span><br/>  | <dl> <span data-ttu-id="62bfe-128"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="62bfe-128"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="62bfe-129">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="62bfe-129">Library</span></span><br/> | <dl> <span data-ttu-id="62bfe-130"><dt>N/A (une bibliothèque Effects 11 est disponible en ligne en tant que source partagée.)</dt></span><span class="sxs-lookup"><span data-stu-id="62bfe-130"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="62bfe-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="62bfe-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="62bfe-132">ID3DX11Effect</span><span class="sxs-lookup"><span data-stu-id="62bfe-132">ID3DX11Effect</span></span>](id3dx11effect.md)
</dt> </dl>

 

