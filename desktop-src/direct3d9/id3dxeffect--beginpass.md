---
description: Commence une passe, dans la technique active.
ms.assetid: fbb2bf1c-e37a-4117-8c3c-5f5b6a267301
title: 'ID3DXEffect :: BeginPass, méthode (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffect.BeginPass
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 56a2648f65c3747f8a98fc0cdbd3ed06cea560b9
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106522963"
---
# <a name="id3dxeffectbeginpass-method"></a><span data-ttu-id="04b1b-103">ID3DXEffect :: BeginPass, méthode</span><span class="sxs-lookup"><span data-stu-id="04b1b-103">ID3DXEffect::BeginPass method</span></span>

<span data-ttu-id="04b1b-104">Commence une passe, dans la technique active.</span><span class="sxs-lookup"><span data-stu-id="04b1b-104">Begins a pass, within the active technique.</span></span>

## <a name="syntax"></a><span data-ttu-id="04b1b-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="04b1b-105">Syntax</span></span>


```C++
HRESULT BeginPass(
  [in] UINT Pass
);
```



## <a name="parameters"></a><span data-ttu-id="04b1b-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="04b1b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="04b1b-107">*Passer* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="04b1b-107">*Pass* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="04b1b-108">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="04b1b-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="04b1b-109">Index entier de base zéro dans la technique.</span><span class="sxs-lookup"><span data-stu-id="04b1b-109">A zero-based integer index into the technique.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="04b1b-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="04b1b-110">Return value</span></span>

<span data-ttu-id="04b1b-111">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="04b1b-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="04b1b-112">Si la méthode est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="04b1b-112">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="04b1b-113">Si la méthode échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ INVALIDCALL, D3DXERR \_ sera déplacé.</span><span class="sxs-lookup"><span data-stu-id="04b1b-113">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="remarks"></a><span data-ttu-id="04b1b-114">Notes</span><span class="sxs-lookup"><span data-stu-id="04b1b-114">Remarks</span></span>

<span data-ttu-id="04b1b-115">Une application définit une passe active (au sein d’une technique active) dans le système d’effet en appelant **ID3DXEffect :: BeginPass**.</span><span class="sxs-lookup"><span data-stu-id="04b1b-115">An application sets one active pass (within one active technique) in the effect system by calling **ID3DXEffect::BeginPass**.</span></span> <span data-ttu-id="04b1b-116">Une application signale la fin de la passe active en appelant [**ID3DXEffect :: EndPass**](id3dxeffect--endpass.md).</span><span class="sxs-lookup"><span data-stu-id="04b1b-116">An application signals the end of the active pass by calling [**ID3DXEffect::EndPass**](id3dxeffect--endpass.md).</span></span> <span data-ttu-id="04b1b-117">**ID3DXEffect :: BeginPass** et **ID3DXEffect :: EndPass** doivent se produire dans une paire correspondante, dans une paire correspondante d' [**ID3DXEffect :: Begin**](id3dxeffect--begin.md) et [**ID3DXEffect :: end**](id3dxeffect--end.md) .</span><span class="sxs-lookup"><span data-stu-id="04b1b-117">**ID3DXEffect::BeginPass** and **ID3DXEffect::EndPass** must occur in a matching pair, within a matching pair of [**ID3DXEffect::Begin**](id3dxeffect--begin.md) and [**ID3DXEffect::End**](id3dxeffect--end.md) calls.</span></span>

<span data-ttu-id="04b1b-118">Si l’application modifie un état d’effet à l’aide de l’une des méthodes [**Effect :: setX**](id3dxeffect.md) à l’intérieur d’une paire de correspondances **ID3DXEffect :: BeginPass** / [**ID3DXEffect :: EndPass**](id3dxeffect--endpass.md) , l’application doit appeler [**ID3DXEffect :: CommitChanges**](id3dxeffect--commitchanges.md) pour définir la mise à jour de l’appareil avec les changements d’État.</span><span class="sxs-lookup"><span data-stu-id="04b1b-118">If the application changes any effect state using any of the [**Effect::Setx**](id3dxeffect.md) methods inside of a **ID3DXEffect::BeginPass**/[**ID3DXEffect::EndPass**](id3dxeffect--endpass.md) matching pair, the application must call [**ID3DXEffect::CommitChanges**](id3dxeffect--commitchanges.md) to set the update the device with the state changes.</span></span> <span data-ttu-id="04b1b-119">Si aucun changement d’État ne se produit dans une paire de correspondances **ID3DXEffect :: BeginPass** et **ID3DXEffect :: EndPass** , il n’est pas nécessaire d’appeler **ID3DXEffect :: CommitChanges**.</span><span class="sxs-lookup"><span data-stu-id="04b1b-119">If no state changes occur within a **ID3DXEffect::BeginPass** and **ID3DXEffect::EndPass** matching pair, it is not necessary to call **ID3DXEffect::CommitChanges**.</span></span>

## <a name="requirements"></a><span data-ttu-id="04b1b-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="04b1b-120">Requirements</span></span>



| <span data-ttu-id="04b1b-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="04b1b-121">Requirement</span></span> | <span data-ttu-id="04b1b-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="04b1b-122">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="04b1b-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="04b1b-123">Header</span></span><br/>  | <dl> <span data-ttu-id="04b1b-124"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="04b1b-124"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="04b1b-125">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="04b1b-125">Library</span></span><br/> | <dl> <span data-ttu-id="04b1b-126"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="04b1b-126"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="04b1b-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="04b1b-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="04b1b-128">ID3DXEffect</span><span class="sxs-lookup"><span data-stu-id="04b1b-128">ID3DXEffect</span></span>](id3dxeffect.md)
</dt> </dl>

 

 
