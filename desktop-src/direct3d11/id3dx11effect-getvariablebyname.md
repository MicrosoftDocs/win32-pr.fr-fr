---
title: Méthode ID3DX11Effect GetVariableByName (D3dx11effect. h)
description: Obtient une variable par nom.
ms.assetid: d20c5a85-51a5-482f-b5b0-197d8e993910
keywords:
- Méthode GetVariableByName Direct3D 11
- Méthode GetVariableByName Direct3D 11, interface ID3DX11Effect
- Interface ID3DX11Effect Direct3D 11, méthode GetVariableByName
topic_type:
- apiref
api_name:
- ID3DX11Effect.GetVariableByName
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9e6079e7f45c21d9d7326021b2c439ab12e4e031
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104992336"
---
# <a name="id3dx11effectgetvariablebyname-method"></a><span data-ttu-id="01d2c-106">ID3DX11Effect :: GetVariableByName, méthode</span><span class="sxs-lookup"><span data-stu-id="01d2c-106">ID3DX11Effect::GetVariableByName method</span></span>

<span data-ttu-id="01d2c-107">Obtient une variable par nom.</span><span class="sxs-lookup"><span data-stu-id="01d2c-107">Get a variable by name.</span></span>

## <a name="syntax"></a><span data-ttu-id="01d2c-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="01d2c-108">Syntax</span></span>


```C++
ID3DX11EffectVariable* GetVariableByName(
   LPCSTR Name
);
```



## <a name="parameters"></a><span data-ttu-id="01d2c-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="01d2c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="01d2c-110">*Nom*</span><span class="sxs-lookup"><span data-stu-id="01d2c-110">*Name*</span></span> 
</dt> <dd>

<span data-ttu-id="01d2c-111">Type : **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="01d2c-111">Type: **[**LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="01d2c-112">Nom de la variable.</span><span class="sxs-lookup"><span data-stu-id="01d2c-112">The variable name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="01d2c-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="01d2c-113">Return value</span></span>

<span data-ttu-id="01d2c-114">Type : **[ **ID3DX11EffectVariable**](id3dx11effectvariable.md)\***</span><span class="sxs-lookup"><span data-stu-id="01d2c-114">Type: **[**ID3DX11EffectVariable**](id3dx11effectvariable.md)\***</span></span>

<span data-ttu-id="01d2c-115">Pointeur vers un [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span><span class="sxs-lookup"><span data-stu-id="01d2c-115">A pointer to an [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span></span> <span data-ttu-id="01d2c-116">Retourne une variable non valide si le nom spécifié est introuvable.</span><span class="sxs-lookup"><span data-stu-id="01d2c-116">Returns an invalid variable if the specified name cannot be found.</span></span>

## <a name="remarks"></a><span data-ttu-id="01d2c-117">Notes</span><span class="sxs-lookup"><span data-stu-id="01d2c-117">Remarks</span></span>

<span data-ttu-id="01d2c-118">Un effet peut contenir une ou plusieurs variables.</span><span class="sxs-lookup"><span data-stu-id="01d2c-118">An effect may contain one or more variables.</span></span> <span data-ttu-id="01d2c-119">Les variables en dehors d’une technique sont considérées comme globales pour tous les effets, celles qui se trouvent à l’intérieur d’une technique sont locales à cette technique.</span><span class="sxs-lookup"><span data-stu-id="01d2c-119">Variables outside of a technique are considered global to all effects, those located inside of a technique are local to that technique.</span></span> <span data-ttu-id="01d2c-120">Vous pouvez accéder à une variable Effect à l’aide de son nom ou d’un index.</span><span class="sxs-lookup"><span data-stu-id="01d2c-120">You can access an effect variable using its name or with an index.</span></span>

<span data-ttu-id="01d2c-121">La méthode retourne un pointeur vers une [**interface d’effet-variable,**](id3dx11effectvariable.md) qu’il existe ou non une variable.</span><span class="sxs-lookup"><span data-stu-id="01d2c-121">The method returns a pointer to an [**effect-variable interface**](id3dx11effectvariable.md) whether or not a variable is found.</span></span> <span data-ttu-id="01d2c-122">[**ID3DX11Effect :: IsValid**](id3dx11effect-isvalid.md) doit être appelé pour vérifier si le nom existe.</span><span class="sxs-lookup"><span data-stu-id="01d2c-122">[**ID3DX11Effect::IsValid**](id3dx11effect-isvalid.md) should be called to verify whether or not the name exists.</span></span>

> [!Note]  
> <span data-ttu-id="01d2c-123">Le kit de développement logiciel (SDK) DirectX ne fournit aucun binaire compilé pour les effets.</span><span class="sxs-lookup"><span data-stu-id="01d2c-123">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="01d2c-124">Vous devez utiliser la source Effects 11 pour créer votre application Effects-type.</span><span class="sxs-lookup"><span data-stu-id="01d2c-124">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="01d2c-125">Pour plus d’informations sur l’utilisation de la source Effects 11, consultez [différences entre les effets 10 et 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="01d2c-125">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="01d2c-126">Spécifications</span><span class="sxs-lookup"><span data-stu-id="01d2c-126">Requirements</span></span>



| <span data-ttu-id="01d2c-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="01d2c-127">Requirement</span></span> | <span data-ttu-id="01d2c-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="01d2c-128">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="01d2c-129">En-tête</span><span class="sxs-lookup"><span data-stu-id="01d2c-129">Header</span></span><br/>  | <dl> <span data-ttu-id="01d2c-130"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="01d2c-130"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="01d2c-131">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="01d2c-131">Library</span></span><br/> | <dl> <span data-ttu-id="01d2c-132"><dt>N/A (une bibliothèque Effects 11 est disponible en ligne en tant que source partagée.)</dt></span><span class="sxs-lookup"><span data-stu-id="01d2c-132"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="01d2c-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="01d2c-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="01d2c-134">ID3DX11Effect</span><span class="sxs-lookup"><span data-stu-id="01d2c-134">ID3DX11Effect</span></span>](id3dx11effect.md)
</dt> </dl>

 

