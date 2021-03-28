---
title: Méthode ID3DX11EffectPass GetAnnotationByIndex (D3dx11effect. h)
description: Obtient une annotation par index. | Méthode ID3DX11EffectPass GetAnnotationByIndex (D3dx11effect. h)
ms.assetid: 734eeeca-58c2-4f0c-84d1-2898394a03d6
keywords:
- Méthode GetAnnotationByIndex Direct3D 11
- Méthode GetAnnotationByIndex Direct3D 11, interface ID3DX11EffectPass
- Interface ID3DX11EffectPass Direct3D 11, méthode GetAnnotationByIndex
topic_type:
- apiref
api_name:
- ID3DX11EffectPass.GetAnnotationByIndex
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: afd43a52758e82434a0e0a4161484ea0d4dcc611
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104974670"
---
# <a name="id3dx11effectpassgetannotationbyindex-method"></a><span data-ttu-id="9e1e6-107">ID3DX11EffectPass :: GetAnnotationByIndex, méthode</span><span class="sxs-lookup"><span data-stu-id="9e1e6-107">ID3DX11EffectPass::GetAnnotationByIndex method</span></span>

<span data-ttu-id="9e1e6-108">Obtient une annotation par index.</span><span class="sxs-lookup"><span data-stu-id="9e1e6-108">Get an annotation by index.</span></span>

## <a name="syntax"></a><span data-ttu-id="9e1e6-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9e1e6-109">Syntax</span></span>


```C++
ID3DX11EffectVariable* GetAnnotationByIndex(
   UINT Index
);
```



## <a name="parameters"></a><span data-ttu-id="9e1e6-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9e1e6-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9e1e6-111">*Index*</span><span class="sxs-lookup"><span data-stu-id="9e1e6-111">*Index*</span></span> 
</dt> <dd>

<span data-ttu-id="9e1e6-112">Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="9e1e6-112">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="9e1e6-113">Index de base zéro.</span><span class="sxs-lookup"><span data-stu-id="9e1e6-113">A zero-based index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9e1e6-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="9e1e6-114">Return value</span></span>

<span data-ttu-id="9e1e6-115">Type : **[ **ID3DX11EffectVariable**](id3dx11effectvariable.md)\***</span><span class="sxs-lookup"><span data-stu-id="9e1e6-115">Type: **[**ID3DX11EffectVariable**](id3dx11effectvariable.md)\***</span></span>

<span data-ttu-id="9e1e6-116">Pointeur vers un [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span><span class="sxs-lookup"><span data-stu-id="9e1e6-116">A pointer to an [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="9e1e6-117">Notes</span><span class="sxs-lookup"><span data-stu-id="9e1e6-117">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="9e1e6-118">Le kit de développement logiciel (SDK) DirectX ne fournit aucun binaire compilé pour les effets.</span><span class="sxs-lookup"><span data-stu-id="9e1e6-118">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="9e1e6-119">Vous devez utiliser la source Effects 11 pour créer votre application Effects-type.</span><span class="sxs-lookup"><span data-stu-id="9e1e6-119">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="9e1e6-120">Pour plus d’informations sur l’utilisation de la source Effects 11, consultez [différences entre les effets 10 et 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="9e1e6-120">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="9e1e6-121">Spécifications</span><span class="sxs-lookup"><span data-stu-id="9e1e6-121">Requirements</span></span>



| <span data-ttu-id="9e1e6-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9e1e6-122">Requirement</span></span> | <span data-ttu-id="9e1e6-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="9e1e6-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9e1e6-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="9e1e6-124">Header</span></span><br/>  | <dl> <span data-ttu-id="9e1e6-125"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="9e1e6-125"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="9e1e6-126">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="9e1e6-126">Library</span></span><br/> | <dl> <span data-ttu-id="9e1e6-127"><dt>N/A (une bibliothèque Effects 11 est disponible en ligne en tant que source partagée.)</dt></span><span class="sxs-lookup"><span data-stu-id="9e1e6-127"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9e1e6-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9e1e6-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9e1e6-129">ID3DX11EffectPass</span><span class="sxs-lookup"><span data-stu-id="9e1e6-129">ID3DX11EffectPass</span></span>](id3dx11effectpass.md)
</dt> </dl>

 

