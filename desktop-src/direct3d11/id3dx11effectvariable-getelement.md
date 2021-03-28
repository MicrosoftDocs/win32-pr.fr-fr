---
title: ID3DX11EffectVariable GetElement, méthode (D3dx11effect. h)
description: Obtient un élément de tableau.
ms.assetid: 3edf2084-570a-4423-8205-0b94a2a0cfde
keywords:
- Méthode GetElement Direct3D 11
- GetElement, méthode Direct3D 11, interface ID3DX11EffectVariable
- Interface ID3DX11EffectVariable Direct3D 11, méthode GetElement
topic_type:
- apiref
api_name:
- ID3DX11EffectVariable.GetElement
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9a5b887bb9e4c1d40f4d3eb0d36b9a7b4d2698b5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104974467"
---
# <a name="id3dx11effectvariablegetelement-method"></a><span data-ttu-id="c2b28-106">ID3DX11EffectVariable :: GetElement, méthode</span><span class="sxs-lookup"><span data-stu-id="c2b28-106">ID3DX11EffectVariable::GetElement method</span></span>

<span data-ttu-id="c2b28-107">Obtient un élément de tableau.</span><span class="sxs-lookup"><span data-stu-id="c2b28-107">Get an array element.</span></span>

## <a name="syntax"></a><span data-ttu-id="c2b28-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c2b28-108">Syntax</span></span>


```C++
ID3DX11EffectVariable* GetElement(
   UINT Index
);
```



## <a name="parameters"></a><span data-ttu-id="c2b28-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c2b28-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c2b28-110">*Index*</span><span class="sxs-lookup"><span data-stu-id="c2b28-110">*Index*</span></span> 
</dt> <dd>

<span data-ttu-id="c2b28-111">Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="c2b28-111">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="c2b28-112">Index de base zéro ; Sinon, 0.</span><span class="sxs-lookup"><span data-stu-id="c2b28-112">A zero-based index; otherwise 0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c2b28-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="c2b28-113">Return value</span></span>

<span data-ttu-id="c2b28-114">Type : **[ **ID3DX11EffectVariable**](id3dx11effectvariable.md)\***</span><span class="sxs-lookup"><span data-stu-id="c2b28-114">Type: **[**ID3DX11EffectVariable**](id3dx11effectvariable.md)\***</span></span>

<span data-ttu-id="c2b28-115">Pointeur vers un [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span><span class="sxs-lookup"><span data-stu-id="c2b28-115">A pointer to an [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="c2b28-116">Notes</span><span class="sxs-lookup"><span data-stu-id="c2b28-116">Remarks</span></span>

<span data-ttu-id="c2b28-117">Si la variable d’effet est un tableau, utilisez cette méthode pour retourner l’un des éléments.</span><span class="sxs-lookup"><span data-stu-id="c2b28-117">If the effect variable is an array, use this method to return one of the elements.</span></span>

> [!Note]  
> <span data-ttu-id="c2b28-118">Le kit de développement logiciel (SDK) DirectX ne fournit aucun binaire compilé pour les effets.</span><span class="sxs-lookup"><span data-stu-id="c2b28-118">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="c2b28-119">Vous devez utiliser la source Effects 11 pour créer votre application Effects-type.</span><span class="sxs-lookup"><span data-stu-id="c2b28-119">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="c2b28-120">Pour plus d’informations sur l’utilisation de la source Effects 11, consultez [différences entre les effets 10 et 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="c2b28-120">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="c2b28-121">Spécifications</span><span class="sxs-lookup"><span data-stu-id="c2b28-121">Requirements</span></span>



| <span data-ttu-id="c2b28-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c2b28-122">Requirement</span></span> | <span data-ttu-id="c2b28-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="c2b28-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c2b28-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="c2b28-124">Header</span></span><br/>  | <dl> <span data-ttu-id="c2b28-125"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="c2b28-125"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="c2b28-126">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="c2b28-126">Library</span></span><br/> | <dl> <span data-ttu-id="c2b28-127"><dt>N/A (une bibliothèque Effects 11 est disponible en ligne en tant que source partagée.)</dt></span><span class="sxs-lookup"><span data-stu-id="c2b28-127"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c2b28-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c2b28-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c2b28-129">ID3DX11EffectVariable</span><span class="sxs-lookup"><span data-stu-id="c2b28-129">ID3DX11EffectVariable</span></span>](id3dx11effectvariable.md)
</dt> </dl>

 

