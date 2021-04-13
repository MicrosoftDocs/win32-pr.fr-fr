---
description: Met fin à une technique active.
ms.assetid: 7297aa67-5cd4-4557-b5ef-faa6c27eaeb5
title: 'ID3DXEffect :: end, méthode (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffect.End
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: baaccd7710845296497dcc7f16d3d71c7ceeb9bd
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104322982"
---
# <a name="id3dxeffectend-method"></a><span data-ttu-id="abc32-103">ID3DXEffect :: end, méthode</span><span class="sxs-lookup"><span data-stu-id="abc32-103">ID3DXEffect::End method</span></span>

<span data-ttu-id="abc32-104">Met fin à une technique active.</span><span class="sxs-lookup"><span data-stu-id="abc32-104">Ends an active technique.</span></span>

## <a name="syntax"></a><span data-ttu-id="abc32-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="abc32-105">Syntax</span></span>


```C++
HRESULT End();
```



## <a name="parameters"></a><span data-ttu-id="abc32-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="abc32-106">Parameters</span></span>

<span data-ttu-id="abc32-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="abc32-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="abc32-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="abc32-108">Return value</span></span>

<span data-ttu-id="abc32-109">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="abc32-109">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="abc32-110">Cette méthode retourne toujours la valeur \_ OK.</span><span class="sxs-lookup"><span data-stu-id="abc32-110">This method always returns the value S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="abc32-111">Notes</span><span class="sxs-lookup"><span data-stu-id="abc32-111">Remarks</span></span>

<span data-ttu-id="abc32-112">Tout rendu dans un effet est effectué dans une paire correspondante d’appels [**ID3DXEffect :: Begin**](id3dxeffect--begin.md) et **ID3DXEffect :: end** .</span><span class="sxs-lookup"><span data-stu-id="abc32-112">All rendering in an effect is done within a matching pair of [**ID3DXEffect::Begin**](id3dxeffect--begin.md) and **ID3DXEffect::End** calls.</span></span> <span data-ttu-id="abc32-113">Une fois toutes les passes rendues, **ID3DXEffect :: end** doit être appelé pour terminer la technique active.</span><span class="sxs-lookup"><span data-stu-id="abc32-113">After all passes are rendered, **ID3DXEffect::End** must be called to end the active technique.</span></span> <span data-ttu-id="abc32-114">Le système d’effet répond à l’aide du bloc d’état créé lors de l’appel de **ID3DXEffect :: Begin** , afin de restaurer automatiquement l’état du pipeline avant **ID3DXEffect :: Begin**.</span><span class="sxs-lookup"><span data-stu-id="abc32-114">The effect system responds by using the state block created when **ID3DXEffect::Begin** was called, to automatically restore the pipeline state before **ID3DXEffect::Begin**.</span></span>

<span data-ttu-id="abc32-115">Par défaut, le système d’effet prend en charge l’enregistrement de l’état avant une technique et la restauration de l’état après une technique.</span><span class="sxs-lookup"><span data-stu-id="abc32-115">By default, the effect system takes care of saving state prior to a technique, and restoring state after a technique.</span></span> <span data-ttu-id="abc32-116">Si vous choisissez de désactiver cette fonctionnalité d’enregistrement et de restauration, consultez [D3DXFX \_ DONOTSAVESAMPLERSTATE](d3dxfx.md).</span><span class="sxs-lookup"><span data-stu-id="abc32-116">If you choose to disable this save and restore functionality, see [D3DXFX\_DONOTSAVESAMPLERSTATE](d3dxfx.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="abc32-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="abc32-117">Requirements</span></span>



| <span data-ttu-id="abc32-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="abc32-118">Requirement</span></span> | <span data-ttu-id="abc32-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="abc32-119">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="abc32-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="abc32-120">Header</span></span><br/>  | <dl> <span data-ttu-id="abc32-121"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="abc32-121"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="abc32-122">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="abc32-122">Library</span></span><br/> | <dl> <span data-ttu-id="abc32-123"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="abc32-123"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="abc32-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="abc32-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="abc32-125">ID3DXEffect</span><span class="sxs-lookup"><span data-stu-id="abc32-125">ID3DXEffect</span></span>](id3dxeffect.md)
</dt> </dl>

 

 




