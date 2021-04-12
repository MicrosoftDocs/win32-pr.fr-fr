---
description: Démarre une technique active.
ms.assetid: 6598d77b-8b53-4f2d-aa43-adf358ad486d
title: 'ID3DXEffect :: Begin, méthode (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffect.Begin
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 1912698fbb6d6ac13f119161c4d05926f05d245b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104211795"
---
# <a name="id3dxeffectbegin-method"></a><span data-ttu-id="19524-103">ID3DXEffect :: Begin, méthode</span><span class="sxs-lookup"><span data-stu-id="19524-103">ID3DXEffect::Begin method</span></span>

<span data-ttu-id="19524-104">Démarre une technique active.</span><span class="sxs-lookup"><span data-stu-id="19524-104">Starts an active technique.</span></span>

## <a name="syntax"></a><span data-ttu-id="19524-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="19524-105">Syntax</span></span>


```C++
HRESULT Begin(
  [out] UINT  *pPasses,
  [in]  DWORD Flags
);
```



## <a name="parameters"></a><span data-ttu-id="19524-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="19524-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="19524-107">*pPasses* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="19524-107">*pPasses* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="19524-108">Type : **[ **uint**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="19524-108">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="19524-109">Pointeur vers une valeur retournée qui indique le nombre de passes nécessaires pour restituer la technique actuelle.</span><span class="sxs-lookup"><span data-stu-id="19524-109">Pointer to a value returned that indicates the number of passes needed to render the current technique.</span></span>

</dd> <dt>

<span data-ttu-id="19524-110">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="19524-110">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="19524-111">Type : **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="19524-111">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="19524-112">Valeur DWORD qui détermine si l’état modifié par un effet est enregistré et restauré.</span><span class="sxs-lookup"><span data-stu-id="19524-112">DWORD that determines if state modified by an effect is saved and restored.</span></span> <span data-ttu-id="19524-113">La valeur par défaut 0 spécifie que **ID3DXEffect :: Begin** et [**ID3DXEffect :: end**](id3dxeffect--end.md) vont enregistrer et restaurer tous les États modifiés par l’effet (y compris les constantes de nuanceur de pixels et de vertex).</span><span class="sxs-lookup"><span data-stu-id="19524-113">The default value 0 specifies that **ID3DXEffect::Begin** and [**ID3DXEffect::End**](id3dxeffect--end.md) will save and restore all state modified by the effect (including pixel and vertex shader constants).</span></span> <span data-ttu-id="19524-114">Les indicateurs valides peuvent être affichés à l' [État Effects Save et Restore Flags](d3dxfx.md).</span><span class="sxs-lookup"><span data-stu-id="19524-114">Valid flags can be seen at [Effect State Save and Restore Flags](d3dxfx.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="19524-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="19524-115">Return value</span></span>

<span data-ttu-id="19524-116">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="19524-116">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="19524-117">Si la méthode est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="19524-117">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="19524-118">Si la méthode échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ INVALIDCALL, D3DXERR \_ sera déplacé.</span><span class="sxs-lookup"><span data-stu-id="19524-118">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="remarks"></a><span data-ttu-id="19524-119">Notes</span><span class="sxs-lookup"><span data-stu-id="19524-119">Remarks</span></span>

<span data-ttu-id="19524-120">Une application définit une technique active dans le système d’effet en appelant **ID3DXEffect :: Begin**.</span><span class="sxs-lookup"><span data-stu-id="19524-120">An application sets one active technique in the effect system by calling **ID3DXEffect::Begin**.</span></span> <span data-ttu-id="19524-121">Le système d’effet répond en capturant tout l’état du pipeline qui peut être modifié par la technique dans un bloc d’État.</span><span class="sxs-lookup"><span data-stu-id="19524-121">The effect system responds by capturing all the pipeline state that can be changed by the technique in a state block.</span></span> <span data-ttu-id="19524-122">Une application signale la fin d’une technique en appelant [**ID3DXEffect :: end**](id3dxeffect--end.md), qui utilise le bloc d’État pour restaurer l’état d’origine.</span><span class="sxs-lookup"><span data-stu-id="19524-122">An application signals the end of a technique by calling [**ID3DXEffect::End**](id3dxeffect--end.md), which uses the state block to restore the original state.</span></span> <span data-ttu-id="19524-123">Le système d’effet prend donc en charge l’enregistrement de l’État lorsqu’une technique devient active et la restauration de l’État lorsqu’une technique se termine.</span><span class="sxs-lookup"><span data-stu-id="19524-123">The effect system, therefore, takes care of saving state when a technique becomes active and restoring state when a technique ends.</span></span> <span data-ttu-id="19524-124">Si vous choisissez de désactiver cette fonctionnalité d’enregistrement et de restauration, consultez [D3DXFX \_ DONOTSAVESAMPLERSTATE](d3dxfx.md).</span><span class="sxs-lookup"><span data-stu-id="19524-124">If you choose to disable this save and restore functionality, see [D3DXFX\_DONOTSAVESAMPLERSTATE](d3dxfx.md).</span></span>

<span data-ttu-id="19524-125">Dans la paire **ID3DXEffect :: Begin** et [**ID3DXEffect :: end**](id3dxeffect--end.md) , une application utilise [**ID3DXEffect :: BeginPass**](id3dxeffect--beginpass.md) pour définir la passe active, [**ID3DXEffect :: CommitChanges**](id3dxeffect--commitchanges.md) si des modifications d’État se sont produites après l’activation de la passe, et [**ID3DXEffect :: EndPass**](id3dxeffect--endpass.md) pour terminer la passe active.</span><span class="sxs-lookup"><span data-stu-id="19524-125">Within the **ID3DXEffect::Begin** and [**ID3DXEffect::End**](id3dxeffect--end.md) pair, an application uses [**ID3DXEffect::BeginPass**](id3dxeffect--beginpass.md) to set the active pass, [**ID3DXEffect::CommitChanges**](id3dxeffect--commitchanges.md) if any state changes occurred after the pass was activated, and [**ID3DXEffect::EndPass**](id3dxeffect--endpass.md) to end the active pass.</span></span>

## <a name="requirements"></a><span data-ttu-id="19524-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="19524-126">Requirements</span></span>



| <span data-ttu-id="19524-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="19524-127">Requirement</span></span> | <span data-ttu-id="19524-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="19524-128">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="19524-129">En-tête</span><span class="sxs-lookup"><span data-stu-id="19524-129">Header</span></span><br/>  | <dl> <span data-ttu-id="19524-130"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="19524-130"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="19524-131">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="19524-131">Library</span></span><br/> | <dl> <span data-ttu-id="19524-132"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="19524-132"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="19524-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="19524-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="19524-134">ID3DXEffect</span><span class="sxs-lookup"><span data-stu-id="19524-134">ID3DXEffect</span></span>](id3dxeffect.md)
</dt> </dl>

 

 
