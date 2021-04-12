---
description: Propage les modifications d’État qui se produisent à l’intérieur d’une passe active à l’appareil avant le rendu.
ms.assetid: 3a779b63-c106-4a81-afeb-82bd6e556de4
title: 'ID3DXEffect :: CommitChanges, méthode (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffect.CommitChanges
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 41516c52b29dfe277cc857e44003de7783282a3a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104211793"
---
# <a name="id3dxeffectcommitchanges-method"></a><span data-ttu-id="74072-103">ID3DXEffect :: CommitChanges, méthode</span><span class="sxs-lookup"><span data-stu-id="74072-103">ID3DXEffect::CommitChanges method</span></span>

<span data-ttu-id="74072-104">Propage les modifications d’État qui se produisent à l’intérieur d’une passe active à l’appareil avant le rendu.</span><span class="sxs-lookup"><span data-stu-id="74072-104">Propagate state changes that occur inside of an active pass to the device before rendering.</span></span>

## <a name="syntax"></a><span data-ttu-id="74072-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="74072-105">Syntax</span></span>


```C++
HRESULT CommitChanges();
```



## <a name="parameters"></a><span data-ttu-id="74072-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="74072-106">Parameters</span></span>

<span data-ttu-id="74072-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="74072-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="74072-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="74072-108">Return value</span></span>

<span data-ttu-id="74072-109">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="74072-109">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="74072-110">Si la méthode est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="74072-110">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="74072-111">Si la méthode échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ INVALIDCALL, D3DXERR \_ sera déplacé.</span><span class="sxs-lookup"><span data-stu-id="74072-111">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="remarks"></a><span data-ttu-id="74072-112">Notes</span><span class="sxs-lookup"><span data-stu-id="74072-112">Remarks</span></span>

<span data-ttu-id="74072-113">Si l’application modifie un état d’effet à l’aide de l’une des méthodes [**ID3DXEffect :: setX**](id3dxeffect.md) à l’intérieur d’une paire de correspondances [**ID3DXEffect :: BeginPass**](id3dxeffect--beginpass.md) / [**ID3DXEffect :: EndPass**](id3dxeffect--endpass.md) , l’application doit appeler **ID3DXEffect :: CommitChanges** avant tout appel DrawxPrimitive pour propager les modifications d’État à l’appareil avant le rendu.</span><span class="sxs-lookup"><span data-stu-id="74072-113">If the application changes any effect state using any of the [**ID3DXEffect::Setx**](id3dxeffect.md) methods inside of an [**ID3DXEffect::BeginPass**](id3dxeffect--beginpass.md)/[**ID3DXEffect::EndPass**](id3dxeffect--endpass.md) matching pair, the application must call **ID3DXEffect::CommitChanges** before any DrawxPrimitive call to propagate state changes to the device before rendering.</span></span> <span data-ttu-id="74072-114">Si aucun changement d’État ne se produit dans une paire de correspondances **ID3DXEffect :: BeginPass** et **ID3DXEffect :: EndPass** , il n’est pas nécessaire d’appeler **ID3DXEffect :: CommitChanges**.</span><span class="sxs-lookup"><span data-stu-id="74072-114">If no state changes occur within a **ID3DXEffect::BeginPass** and **ID3DXEffect::EndPass** matching pair, it is not necessary to call **ID3DXEffect::CommitChanges**.</span></span>

<span data-ttu-id="74072-115">Cela est légèrement différent pour tous les paramètres partagés dans un effet cloné.</span><span class="sxs-lookup"><span data-stu-id="74072-115">This is slightly different for any shared parameters in a cloned effect.</span></span> <span data-ttu-id="74072-116">Quand une technique est active sur un effet cloné (autrement dit, quand [**ID3DXEffect :: Begin**](id3dxeffect--begin.md) a été appelé mais et que [**ID3DXEffect :: end**](id3dxeffect--end.md) n’a pas été appelé), **ID3DXEffect :: CommitChanges** met à jour les paramètres qui ne sont pas partagés comme prévu.</span><span class="sxs-lookup"><span data-stu-id="74072-116">When a technique is active on a cloned effect (that is, when [**ID3DXEffect::Begin**](id3dxeffect--begin.md) has been called but and [**ID3DXEffect::End**](id3dxeffect--end.md) has not been called), **ID3DXEffect::CommitChanges** updates parameters that are not shared as expected.</span></span> <span data-ttu-id="74072-117">Pour mettre à jour un paramètre partagé (uniquement pour un effet cloné dont la technique est active), appelez **ID3DXEffect :: end** pour désactiver la technique et **ID3DXEffect :: Begin** pour réactiver la technique avant d’appeler **ID3DXEffect :: CommitChanges**.</span><span class="sxs-lookup"><span data-stu-id="74072-117">To update a shared parameter (only for a cloned effect whose technique is active), call **ID3DXEffect::End** to deactivate the technique and **ID3DXEffect::Begin** to reactivate the technique before calling **ID3DXEffect::CommitChanges**.</span></span>

## <a name="requirements"></a><span data-ttu-id="74072-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="74072-118">Requirements</span></span>



| <span data-ttu-id="74072-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="74072-119">Requirement</span></span> | <span data-ttu-id="74072-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="74072-120">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="74072-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="74072-121">Header</span></span><br/>  | <dl> <span data-ttu-id="74072-122"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="74072-122"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="74072-123">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="74072-123">Library</span></span><br/> | <dl> <span data-ttu-id="74072-124"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="74072-124"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="74072-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="74072-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="74072-126">ID3DXEffect</span><span class="sxs-lookup"><span data-stu-id="74072-126">ID3DXEffect</span></span>](id3dxeffect.md)
</dt> </dl>

 

 




