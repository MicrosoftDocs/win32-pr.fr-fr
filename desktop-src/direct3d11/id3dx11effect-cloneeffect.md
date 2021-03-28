---
title: Méthode ID3DX11Effect CloneEffect (D3dx11effect. h)
description: Crée une copie d’une interface d’effet.
ms.assetid: 98cc8e25-38c5-4b87-99eb-39d2edd9053c
keywords:
- Méthode CloneEffect Direct3D 11
- Méthode CloneEffect Direct3D 11, interface ID3DX11Effect
- Interface ID3DX11Effect Direct3D 11, méthode CloneEffect
topic_type:
- apiref
api_name:
- ID3DX11Effect.CloneEffect
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b9dc7e47d1c50d0e41c29c90102afaaebdce8dda
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104982602"
---
# <a name="id3dx11effectcloneeffect-method"></a><span data-ttu-id="fe12e-106">ID3DX11Effect :: CloneEffect, méthode</span><span class="sxs-lookup"><span data-stu-id="fe12e-106">ID3DX11Effect::CloneEffect method</span></span>

<span data-ttu-id="fe12e-107">Crée une copie d’une interface d’effet.</span><span class="sxs-lookup"><span data-stu-id="fe12e-107">Creates a copy of an effect interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="fe12e-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fe12e-108">Syntax</span></span>


```C++
HRESULT CloneEffect(
   UINT          Flags,
   ID3DX11Effect **ppClonedEffect
);
```



## <a name="parameters"></a><span data-ttu-id="fe12e-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="fe12e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fe12e-110">*Indicateurs*</span><span class="sxs-lookup"><span data-stu-id="fe12e-110">*Flags*</span></span> 
</dt> <dd>

<span data-ttu-id="fe12e-111">Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="fe12e-111">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="fe12e-112">Indicateurs qui affectent la création de l’effet cloné.</span><span class="sxs-lookup"><span data-stu-id="fe12e-112">Flags affecting the creation of the cloned effect.</span></span> <span data-ttu-id="fe12e-113">Peut avoir la valeur 0 ou l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="fe12e-113">Can be 0 or one of the following values.</span></span>



| <span data-ttu-id="fe12e-114">Indicateur</span><span class="sxs-lookup"><span data-stu-id="fe12e-114">Flag</span></span>                                    | <span data-ttu-id="fe12e-115">Description</span><span class="sxs-lookup"><span data-stu-id="fe12e-115">Description</span></span>                                                                                                                                      |
|-----------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fe12e-116">\_Effet de \_ clonage de la \_ force \_ D3DX11</span><span class="sxs-lookup"><span data-stu-id="fe12e-116">D3DX11\_EFFECT\_CLONE\_FORCE\_NONSINGLE</span></span> | <span data-ttu-id="fe12e-117">Ignore tous les qualificateurs « uniques » sur cbuffers.</span><span class="sxs-lookup"><span data-stu-id="fe12e-117">Ignore all "single" qualifiers on cbuffers.</span></span> <span data-ttu-id="fe12e-118">Toutes les cbuffers auront leur propre [**ID3D11Buffer**](/windows/desktop/api/D3D11/nn-d3d11-id3d11buffer)créé dans l’effet cloné.</span><span class="sxs-lookup"><span data-stu-id="fe12e-118">All cbuffers will have their own [**ID3D11Buffer**](/windows/desktop/api/D3D11/nn-d3d11-id3d11buffer)s created in the cloned effect.</span></span> |



 

</dd> <dt>

<span data-ttu-id="fe12e-119">*ppClonedEffect*</span><span class="sxs-lookup"><span data-stu-id="fe12e-119">*ppClonedEffect*</span></span> 
</dt> <dd>

<span data-ttu-id="fe12e-120">Type : **[ **ID3DX11Effect**](id3dx11effect.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="fe12e-120">Type: **[**ID3DX11Effect**](id3dx11effect.md)\*\***</span></span>

<span data-ttu-id="fe12e-121">Pointeur vers un pointeur [**ID3DX11Effect**](id3dx11effect.md) qui sera défini sur la copie de l’effet.</span><span class="sxs-lookup"><span data-stu-id="fe12e-121">Pointer to an [**ID3DX11Effect**](id3dx11effect.md) pointer that will be set to the copy of the effect.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fe12e-122">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="fe12e-122">Return value</span></span>

<span data-ttu-id="fe12e-123">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="fe12e-123">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="fe12e-124">Retourne l’un des [codes de retour Direct3D 11](d3d11-graphics-reference-returnvalues.md)suivants.</span><span class="sxs-lookup"><span data-stu-id="fe12e-124">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="fe12e-125">Notes</span><span class="sxs-lookup"><span data-stu-id="fe12e-125">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="fe12e-126">Le kit de développement logiciel (SDK) DirectX ne fournit aucun binaire compilé pour les effets.</span><span class="sxs-lookup"><span data-stu-id="fe12e-126">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="fe12e-127">Vous devez utiliser la source Effects 11 pour créer votre application Effects-type.</span><span class="sxs-lookup"><span data-stu-id="fe12e-127">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="fe12e-128">Pour plus d’informations sur l’utilisation de la source Effects 11, consultez [différences entre les effets 10 et 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="fe12e-128">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="fe12e-129">Spécifications</span><span class="sxs-lookup"><span data-stu-id="fe12e-129">Requirements</span></span>



| <span data-ttu-id="fe12e-130">Condition requise</span><span class="sxs-lookup"><span data-stu-id="fe12e-130">Requirement</span></span> | <span data-ttu-id="fe12e-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="fe12e-131">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fe12e-132">En-tête</span><span class="sxs-lookup"><span data-stu-id="fe12e-132">Header</span></span><br/>  | <dl> <span data-ttu-id="fe12e-133"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="fe12e-133"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="fe12e-134">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="fe12e-134">Library</span></span><br/> | <dl> <span data-ttu-id="fe12e-135"><dt>N/A (une bibliothèque Effects 11 est disponible en ligne en tant que source partagée.)</dt></span><span class="sxs-lookup"><span data-stu-id="fe12e-135"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fe12e-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fe12e-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fe12e-137">ID3DX11Effect</span><span class="sxs-lookup"><span data-stu-id="fe12e-137">ID3DX11Effect</span></span>](id3dx11effect.md)
</dt> </dl>

 

