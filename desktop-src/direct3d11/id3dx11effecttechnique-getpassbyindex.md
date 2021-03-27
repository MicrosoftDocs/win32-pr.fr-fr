---
title: Méthode ID3DX11EffectTechnique GetPassByIndex (D3dx11effect. h)
description: Obtenir un passage par index.
ms.assetid: 3c9452f5-c94a-4951-bdd2-e8891b7ceb34
keywords:
- Méthode GetPassByIndex Direct3D 11
- Méthode GetPassByIndex Direct3D 11, interface ID3DX11EffectTechnique
- Interface ID3DX11EffectTechnique Direct3D 11, méthode GetPassByIndex
topic_type:
- apiref
api_name:
- ID3DX11EffectTechnique.GetPassByIndex
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b6af222298cc3d00ad87e5037f9de20139e4fc40
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103953967"
---
# <a name="id3dx11effecttechniquegetpassbyindex-method"></a><span data-ttu-id="1873c-106">ID3DX11EffectTechnique :: GetPassByIndex, méthode</span><span class="sxs-lookup"><span data-stu-id="1873c-106">ID3DX11EffectTechnique::GetPassByIndex method</span></span>

<span data-ttu-id="1873c-107">Obtenir un passage par index.</span><span class="sxs-lookup"><span data-stu-id="1873c-107">Get a pass by index.</span></span>

## <a name="syntax"></a><span data-ttu-id="1873c-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1873c-108">Syntax</span></span>


```C++
ID3DX11EffectPass* GetPassByIndex(
   UINT Index
);
```



## <a name="parameters"></a><span data-ttu-id="1873c-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1873c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1873c-110">*Index*</span><span class="sxs-lookup"><span data-stu-id="1873c-110">*Index*</span></span> 
</dt> <dd>

<span data-ttu-id="1873c-111">Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="1873c-111">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="1873c-112">Index de base zéro.</span><span class="sxs-lookup"><span data-stu-id="1873c-112">A zero-based index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1873c-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="1873c-113">Return value</span></span>

<span data-ttu-id="1873c-114">Type : **[ **ID3DX11EffectPass**](id3dx11effectpass.md)\***</span><span class="sxs-lookup"><span data-stu-id="1873c-114">Type: **[**ID3DX11EffectPass**](id3dx11effectpass.md)\***</span></span>

<span data-ttu-id="1873c-115">Pointeur vers un [**ID3DX11EffectPass**](id3dx11effectpass.md).</span><span class="sxs-lookup"><span data-stu-id="1873c-115">A pointer to a [**ID3DX11EffectPass**](id3dx11effectpass.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="1873c-116">Notes</span><span class="sxs-lookup"><span data-stu-id="1873c-116">Remarks</span></span>

<span data-ttu-id="1873c-117">Une technique contient une ou plusieurs passes ; obtenir une passe à l’aide d’un nom ou d’un index.</span><span class="sxs-lookup"><span data-stu-id="1873c-117">A technique contains one or more passes; get a pass using a name or an index.</span></span>

> [!Note]  
> <span data-ttu-id="1873c-118">Le kit de développement logiciel (SDK) DirectX ne fournit aucun binaire compilé pour les effets.</span><span class="sxs-lookup"><span data-stu-id="1873c-118">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="1873c-119">Vous devez utiliser la source Effects 11 pour créer votre application Effects-type.</span><span class="sxs-lookup"><span data-stu-id="1873c-119">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="1873c-120">Pour plus d’informations sur l’utilisation de la source Effects 11, consultez [différences entre les effets 10 et 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="1873c-120">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="1873c-121">Spécifications</span><span class="sxs-lookup"><span data-stu-id="1873c-121">Requirements</span></span>



| <span data-ttu-id="1873c-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1873c-122">Requirement</span></span> | <span data-ttu-id="1873c-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="1873c-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1873c-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="1873c-124">Header</span></span><br/>  | <dl> <span data-ttu-id="1873c-125"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="1873c-125"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="1873c-126">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="1873c-126">Library</span></span><br/> | <dl> <span data-ttu-id="1873c-127"><dt>N/A (une bibliothèque Effects 11 est disponible en ligne en tant que source partagée.)</dt></span><span class="sxs-lookup"><span data-stu-id="1873c-127"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1873c-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1873c-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1873c-129">ID3DX11EffectTechnique</span><span class="sxs-lookup"><span data-stu-id="1873c-129">ID3DX11EffectTechnique</span></span>](id3dx11effecttechnique.md)
</dt> </dl>

 

