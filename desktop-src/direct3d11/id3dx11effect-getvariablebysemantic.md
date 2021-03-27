---
title: Méthode ID3DX11Effect GetVariableBySemantic (D3dx11effect. h)
description: Obtenir une variable par sémantique.
ms.assetid: fe731af6-3e9b-4f3e-9761-121796ac8c48
keywords:
- Méthode GetVariableBySemantic Direct3D 11
- Méthode GetVariableBySemantic Direct3D 11, interface ID3DX11Effect
- Interface ID3DX11Effect Direct3D 11, méthode GetVariableBySemantic
topic_type:
- apiref
api_name:
- ID3DX11Effect.GetVariableBySemantic
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b8276b1850242bd83639883bf75fc927d8484765
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104211892"
---
# <a name="id3dx11effectgetvariablebysemantic-method"></a><span data-ttu-id="7ae05-106">ID3DX11Effect :: GetVariableBySemantic, méthode</span><span class="sxs-lookup"><span data-stu-id="7ae05-106">ID3DX11Effect::GetVariableBySemantic method</span></span>

<span data-ttu-id="7ae05-107">Obtenir une variable par sémantique.</span><span class="sxs-lookup"><span data-stu-id="7ae05-107">Get a variable by semantic.</span></span>

## <a name="syntax"></a><span data-ttu-id="7ae05-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7ae05-108">Syntax</span></span>


```C++
ID3DX11EffectVariable* GetVariableBySemantic(
   LPCSTR Semantic
);
```



## <a name="parameters"></a><span data-ttu-id="7ae05-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7ae05-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7ae05-110">*Équivalent*</span><span class="sxs-lookup"><span data-stu-id="7ae05-110">*Semantic*</span></span> 
</dt> <dd>

<span data-ttu-id="7ae05-111">Type : **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="7ae05-111">Type: **[**LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="7ae05-112">Nom sémantique.</span><span class="sxs-lookup"><span data-stu-id="7ae05-112">The semantic name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7ae05-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="7ae05-113">Return value</span></span>

<span data-ttu-id="7ae05-114">Type : **[ **ID3DX11EffectVariable**](id3dx11effectvariable.md)\***</span><span class="sxs-lookup"><span data-stu-id="7ae05-114">Type: **[**ID3DX11EffectVariable**](id3dx11effectvariable.md)\***</span></span>

<span data-ttu-id="7ae05-115">Pointeur vers la variable d’effet indiquée par la sémantique.</span><span class="sxs-lookup"><span data-stu-id="7ae05-115">A pointer to the effect variable indicated by the Semantic.</span></span> <span data-ttu-id="7ae05-116">Consultez [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span><span class="sxs-lookup"><span data-stu-id="7ae05-116">See [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="7ae05-117">Notes</span><span class="sxs-lookup"><span data-stu-id="7ae05-117">Remarks</span></span>

<span data-ttu-id="7ae05-118">Chaque variable Effect peut avoir une sémantique jointe, qui est une chaîne de métadonnées définie par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="7ae05-118">Each effect variable can have a semantic attached, which is a user defined metadata string.</span></span> <span data-ttu-id="7ae05-119">Certaines [sémantiques de valeurs système](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-semantics) sont des mots réservés qui déclenchent des fonctionnalités intégrées par étapes de pipeline.</span><span class="sxs-lookup"><span data-stu-id="7ae05-119">Some [system-value semantics](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-semantics) are reserved words that trigger built in functionality by pipeline stages.</span></span>

<span data-ttu-id="7ae05-120">La méthode retourne un pointeur vers une [**interface de variable Effect**](id3dx11effectvariable.md) si une variable est introuvable ; vous pouvez appeler [**ID3DX11Effect :: IsValid**](id3dx11effect-isvalid.md) pour vérifier si la sémantique existe.</span><span class="sxs-lookup"><span data-stu-id="7ae05-120">The method returns a pointer to an [**effect-variable interface**](id3dx11effectvariable.md) if a variable is not found; you can call [**ID3DX11Effect::IsValid**](id3dx11effect-isvalid.md) to verify whether or not the semantic exists.</span></span>

> [!Note]  
> <span data-ttu-id="7ae05-121">Le kit de développement logiciel (SDK) DirectX ne fournit aucun binaire compilé pour les effets.</span><span class="sxs-lookup"><span data-stu-id="7ae05-121">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="7ae05-122">Vous devez utiliser la source Effects 11 pour créer votre application Effects-type.</span><span class="sxs-lookup"><span data-stu-id="7ae05-122">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="7ae05-123">Pour plus d’informations sur l’utilisation de la source Effects 11, consultez [différences entre les effets 10 et 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="7ae05-123">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="7ae05-124">Spécifications</span><span class="sxs-lookup"><span data-stu-id="7ae05-124">Requirements</span></span>



| <span data-ttu-id="7ae05-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7ae05-125">Requirement</span></span> | <span data-ttu-id="7ae05-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="7ae05-126">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7ae05-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="7ae05-127">Header</span></span><br/>  | <dl> <span data-ttu-id="7ae05-128"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="7ae05-128"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="7ae05-129">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="7ae05-129">Library</span></span><br/> | <dl> <span data-ttu-id="7ae05-130"><dt>N/A (une bibliothèque Effects 11 est disponible en ligne en tant que source partagée.)</dt></span><span class="sxs-lookup"><span data-stu-id="7ae05-130"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7ae05-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7ae05-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7ae05-132">ID3DX11Effect</span><span class="sxs-lookup"><span data-stu-id="7ae05-132">ID3DX11Effect</span></span>](id3dx11effect.md)
</dt> </dl>

 

