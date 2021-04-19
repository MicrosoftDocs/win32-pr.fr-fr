---
title: Événement PositionChange de l’objet AxWindowsMediaPlayer
description: L’événement PositionChange se produit lorsque la position de lecture actuelle dans l’élément multimédia a été modifiée.
ms.assetid: 92d469b9-813a-4148-be68-0fcef2e41491
keywords:
- Événement PositionChange de l’objet AxWindowsMediaPlayer lecteur Windows Media
topic_type:
- apiref
api_name:
- PositionChange Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 552b748121668e71ee4d2ffb54feed441620a1cb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106544079"
---
# <a name="positionchange-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="9fc0c-104">Événement PositionChange de l’objet AxWindowsMediaPlayer</span><span class="sxs-lookup"><span data-stu-id="9fc0c-104">PositionChange Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="9fc0c-105">L’événement PositionChange se produit lorsque la position de lecture actuelle dans l’élément multimédia a été modifiée.</span><span class="sxs-lookup"><span data-stu-id="9fc0c-105">The PositionChange event occurs when the current playback position within the media item has been changed.</span></span>

``` syntax
[C#]
private void player_PositionChange(
  object sender,
  _WMPOCXEvents_PositionChangeEvent e
)

[Visual Basic]
Private Sub player_PositionChange(  
  sender As Object,
  e As _WMPOCXEvents_PositionChangeEvent
) Handles player.PositionChange
```

## <a name="event-data"></a><span data-ttu-id="9fc0c-106">Données d'événements</span><span class="sxs-lookup"><span data-stu-id="9fc0c-106">Event Data</span></span>

<span data-ttu-id="9fc0c-107">Le gestionnaire associé à cet événement est de type **AxWMPLib. \_ WMPOCXEvents \_ PositionChangeEventHandler**.</span><span class="sxs-lookup"><span data-stu-id="9fc0c-107">The handler associated with this event is of type **AxWMPLib.\_WMPOCXEvents\_PositionChangeEventHandler**.</span></span> <span data-ttu-id="9fc0c-108">Ce gestionnaire reçoit un argument de type **AxWMPLib. \_ WMPOCXEvents \_ PositionChangeEvent**, qui contient les propriétés suivantes relatives à cet événement.</span><span class="sxs-lookup"><span data-stu-id="9fc0c-108">This handler receives an argument of type **AxWMPLib.\_WMPOCXEvents\_PositionChangeEvent**, which contains the following properties related to this event.</span></span>



| <span data-ttu-id="9fc0c-109">Propriété</span><span class="sxs-lookup"><span data-stu-id="9fc0c-109">Property</span></span>    | <span data-ttu-id="9fc0c-110">Description</span><span class="sxs-lookup"><span data-stu-id="9fc0c-110">Description</span></span>                                         |
|-------------|-----------------------------------------------------|
| <span data-ttu-id="9fc0c-111">oldPosition</span><span class="sxs-lookup"><span data-stu-id="9fc0c-111">oldPosition</span></span> | <span data-ttu-id="9fc0c-112">System. DoubleSpecifies l’ancienne position.</span><span class="sxs-lookup"><span data-stu-id="9fc0c-112">System.DoubleSpecifies the old position.</span></span><br/> |
| <span data-ttu-id="9fc0c-113">newPosition</span><span class="sxs-lookup"><span data-stu-id="9fc0c-113">newPosition</span></span> | <span data-ttu-id="9fc0c-114">System. DoubleSpecifies la nouvelle position.</span><span class="sxs-lookup"><span data-stu-id="9fc0c-114">System.DoubleSpecifies the new position.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="9fc0c-115">Notes</span><span class="sxs-lookup"><span data-stu-id="9fc0c-115">Remarks</span></span>

<span data-ttu-id="9fc0c-116">Cet événement n’est pas déclenché régulièrement pendant la lecture.</span><span class="sxs-lookup"><span data-stu-id="9fc0c-116">This event is not raised routinely during playback.</span></span> <span data-ttu-id="9fc0c-117">Il se produit uniquement quand une modification active la position actuelle de l’élément multimédia en cours de exécution, par exemple lorsque l’utilisateur déplace la poignée de recherche ou lorsque le code est exécuté et spécifie une valeur pour IWMPControls. **CurrentPosition**.</span><span class="sxs-lookup"><span data-stu-id="9fc0c-117">It only occurs when something actively changes the current position of the playing media item, such as when the user moves the seek handle or when code is executed that specifies a value for IWMPControls.**currentPosition**.</span></span>

## <a name="requirements"></a><span data-ttu-id="9fc0c-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9fc0c-118">Requirements</span></span>



| <span data-ttu-id="9fc0c-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9fc0c-119">Requirement</span></span> | <span data-ttu-id="9fc0c-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="9fc0c-120">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9fc0c-121">Version</span><span class="sxs-lookup"><span data-stu-id="9fc0c-121">Version</span></span><br/>   | <span data-ttu-id="9fc0c-122">Lecteur Windows Media série 9 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="9fc0c-122">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="9fc0c-123">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="9fc0c-123">Namespace</span></span><br/> | <span data-ttu-id="9fc0c-124">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="9fc0c-124">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="9fc0c-125">Assembly</span><span class="sxs-lookup"><span data-stu-id="9fc0c-125">Assembly</span></span><br/>  | <dl> <span data-ttu-id="9fc0c-126"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="9fc0c-126"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9fc0c-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9fc0c-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9fc0c-128">**Objet AxWindowsMediaPlayer (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="9fc0c-128">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="9fc0c-129">**IWMPControls. currentPosition (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="9fc0c-129">**IWMPControls.currentPosition (VB and C#)**</span></span>](wmplibiwmpcontrols-iwmpcontrols-currentposition--vb-and-c.md)
</dt> </dl>

 

 





