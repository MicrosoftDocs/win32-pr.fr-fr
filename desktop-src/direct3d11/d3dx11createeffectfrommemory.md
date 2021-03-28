---
title: D3DX11CreateEffectFromMemory, fonction (D3dx11effect. h)
description: Crée un effet à partir d’un fichier ou d’un effet binaire.
ms.assetid: 4aa65efb-4c6b-4faf-b48f-01329bdff6cd
keywords:
- Fonction D3DX11CreateEffectFromMemory Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11CreateEffectFromMemory
api_location:
- d3dx11effect.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 467d2094a7124b96a08c7bab6d7a4209deee9996
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104992280"
---
# <a name="d3dx11createeffectfrommemory-function"></a><span data-ttu-id="703d9-104">D3DX11CreateEffectFromMemory fonction)</span><span class="sxs-lookup"><span data-stu-id="703d9-104">D3DX11CreateEffectFromMemory function</span></span>

<span data-ttu-id="703d9-105">Crée un effet à partir d’un fichier ou d’un effet binaire.</span><span class="sxs-lookup"><span data-stu-id="703d9-105">Creates an effect from a binary effect or file.</span></span>

## <a name="syntax"></a><span data-ttu-id="703d9-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="703d9-106">Syntax</span></span>


```C++
HRESULT D3DX11CreateEffectFromMemory(
   void          *pData,
   SIZE_T        DataLength,
   UINT          FXFlags,
   ID3D11Device  *pDevice,
   ID3DX11Effect **ppEffect
);
```



## <a name="parameters"></a><span data-ttu-id="703d9-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="703d9-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="703d9-108">*pData*</span><span class="sxs-lookup"><span data-stu-id="703d9-108">*pData*</span></span> 
</dt> <dd>

<span data-ttu-id="703d9-109">Type : **void \***</span><span class="sxs-lookup"><span data-stu-id="703d9-109">Type: **void\***</span></span>

<span data-ttu-id="703d9-110">Objet blob de données d’effet compilé.</span><span class="sxs-lookup"><span data-stu-id="703d9-110">Blob of compiled effect data.</span></span>

</dd> <dt>

<span data-ttu-id="703d9-111">*DataLength*</span><span class="sxs-lookup"><span data-stu-id="703d9-111">*DataLength*</span></span> 
</dt> <dd>

<span data-ttu-id="703d9-112">Type : **[ **taille \_ T**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="703d9-112">Type: **[**SIZE\_T**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="703d9-113">Longueur de l’objet blob de données.</span><span class="sxs-lookup"><span data-stu-id="703d9-113">Length of the data blob.</span></span>

</dd> <dt>

<span data-ttu-id="703d9-114">*FXFlags*</span><span class="sxs-lookup"><span data-stu-id="703d9-114">*FXFlags*</span></span> 
</dt> <dd>

<span data-ttu-id="703d9-115">Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="703d9-115">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="703d9-116">Il n’existe aucun indicateur d’effet.</span><span class="sxs-lookup"><span data-stu-id="703d9-116">No effect flags exist.</span></span> <span data-ttu-id="703d9-117">Définit la valeur zéro.</span><span class="sxs-lookup"><span data-stu-id="703d9-117">Set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="703d9-118">*pDevice*</span><span class="sxs-lookup"><span data-stu-id="703d9-118">*pDevice*</span></span> 
</dt> <dd>

<span data-ttu-id="703d9-119">Type : **[ **ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device)\***</span><span class="sxs-lookup"><span data-stu-id="703d9-119">Type: **[**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device)\***</span></span>

<span data-ttu-id="703d9-120">Pointeur vers le [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) sur lequel créer des ressources d’effet.</span><span class="sxs-lookup"><span data-stu-id="703d9-120">Pointer to the [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) on which to create Effect resources.</span></span>

</dd> <dt>

<span data-ttu-id="703d9-121">*ppEffect*</span><span class="sxs-lookup"><span data-stu-id="703d9-121">*ppEffect*</span></span> 
</dt> <dd>

<span data-ttu-id="703d9-122">Type : **[ **ID3DX11Effect**](id3dx11effect.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="703d9-122">Type: **[**ID3DX11Effect**](id3dx11effect.md)\*\***</span></span>

<span data-ttu-id="703d9-123">Adresse de l’interface [**ID3DX11Effect**](id3dx11effect.md) nouvellement créée.</span><span class="sxs-lookup"><span data-stu-id="703d9-123">Address of the newly created [**ID3DX11Effect**](id3dx11effect.md) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="703d9-124">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="703d9-124">Return value</span></span>

<span data-ttu-id="703d9-125">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="703d9-125">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="703d9-126">La valeur de retour est l’une des valeurs indiquées dans les [codes de retour Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="703d9-126">The return value is one of the values listed in [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="703d9-127">Notes</span><span class="sxs-lookup"><span data-stu-id="703d9-127">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="703d9-128">Vous devez utiliser la [source Effects 11](https://github.com/Microsoft/FX11) pour créer votre application Effects-type.</span><span class="sxs-lookup"><span data-stu-id="703d9-128">You must use [Effects 11 source](https://github.com/Microsoft/FX11) to build your effects-type application.</span></span> <span data-ttu-id="703d9-129">Pour plus d’informations sur l’utilisation de la source Effects 11, consultez [différences entre les effets 10 et 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="703d9-129">For more info about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="703d9-130">Spécifications</span><span class="sxs-lookup"><span data-stu-id="703d9-130">Requirements</span></span>



| <span data-ttu-id="703d9-131">Condition requise</span><span class="sxs-lookup"><span data-stu-id="703d9-131">Requirement</span></span> | <span data-ttu-id="703d9-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="703d9-132">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="703d9-133">En-tête</span><span class="sxs-lookup"><span data-stu-id="703d9-133">Header</span></span><br/> | <dl> <span data-ttu-id="703d9-134"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="703d9-134"><dt>D3dx11effect.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="703d9-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="703d9-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="703d9-136">Effets 11 fonctions</span><span class="sxs-lookup"><span data-stu-id="703d9-136">Effects 11 Functions</span></span>](d3d11-graphics-reference-effects11-functions.md)
</dt> </dl>

 

