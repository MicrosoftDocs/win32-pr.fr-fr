---
description: Supprime tous les événements d’une piste d’animation spécifiée.
ms.assetid: 25c4d04a-0d75-4113-ad90-db84aa937098
title: 'ID3DXAnimationController :: UnkeyAllTrackEvents, méthode (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.UnkeyAllTrackEvents
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 5904e9e09c8a821cdc532f9046217ae64bbf3de5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106543778"
---
# <a name="id3dxanimationcontrollerunkeyalltrackevents-method"></a><span data-ttu-id="6c373-103">ID3DXAnimationController :: UnkeyAllTrackEvents, méthode</span><span class="sxs-lookup"><span data-stu-id="6c373-103">ID3DXAnimationController::UnkeyAllTrackEvents method</span></span>

<span data-ttu-id="6c373-104">Supprime tous les événements d’une piste d’animation spécifiée.</span><span class="sxs-lookup"><span data-stu-id="6c373-104">Removes all events from a specified animation track.</span></span>

## <a name="syntax"></a><span data-ttu-id="6c373-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6c373-105">Syntax</span></span>


```C++
HRESULT UnkeyAllTrackEvents(
  [in] UINT Track
);
```



## <a name="parameters"></a><span data-ttu-id="6c373-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6c373-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6c373-107">*Suivre* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="6c373-107">*Track* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6c373-108">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6c373-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="6c373-109">Identificateur de la piste sur laquelle tous les événements doivent être supprimés.</span><span class="sxs-lookup"><span data-stu-id="6c373-109">Identifier of the track on which all events should be removed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6c373-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="6c373-110">Return value</span></span>

<span data-ttu-id="6c373-111">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="6c373-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="6c373-112">Si la méthode est réussie, la valeur de retour est S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="6c373-112">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="6c373-113">Si la méthode échoue, la valeur suivante est retournée : D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="6c373-113">If the method fails, the following value will be returned: D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="6c373-114">Notes</span><span class="sxs-lookup"><span data-stu-id="6c373-114">Remarks</span></span>

<span data-ttu-id="6c373-115">Cette méthode empêche l’exécution de tous les événements précédemment planifiés sur la piste et ignore toutes les données associées à ces événements.</span><span class="sxs-lookup"><span data-stu-id="6c373-115">This method prevents the execution of all events previously scheduled on the track, and discards all data associated with those events.</span></span>

## <a name="requirements"></a><span data-ttu-id="6c373-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6c373-116">Requirements</span></span>



| <span data-ttu-id="6c373-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6c373-117">Requirement</span></span> | <span data-ttu-id="6c373-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="6c373-118">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6c373-119">En-tête</span><span class="sxs-lookup"><span data-stu-id="6c373-119">Header</span></span><br/>  | <dl> <span data-ttu-id="6c373-120"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="6c373-120"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="6c373-121">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="6c373-121">Library</span></span><br/> | <dl> <span data-ttu-id="6c373-122"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6c373-122"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="6c373-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6c373-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6c373-124">ID3DXAnimationController</span><span class="sxs-lookup"><span data-stu-id="6c373-124">ID3DXAnimationController</span></span>](id3dxanimationcontroller.md)
</dt> </dl>

 

 
