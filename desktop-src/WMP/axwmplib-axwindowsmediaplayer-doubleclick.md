---
title: Événement DoubleClick de l’objet AxWindowsMediaPlayer
description: L’événement DoubleClick se produit lorsque l’utilisateur double-clique sur un bouton de la souris sur un contrôle du lecteur Windows Media.
ms.assetid: 4f116d8a-1ad5-443a-9c91-66214bbdebcf
keywords:
- Événement DoubleClick de l’objet AxWindowsMediaPlayer Windows Media Player
topic_type:
- apiref
api_name:
- DoubleClick Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1ac809e8ea61b3abbbc964f6dc9ee2976442fc31
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106525238"
---
# <a name="doubleclick-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="8bede-104">Événement DoubleClick de l’objet AxWindowsMediaPlayer</span><span class="sxs-lookup"><span data-stu-id="8bede-104">DoubleClick Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="8bede-105">L’événement DoubleClick se produit lorsque l’utilisateur double-clique sur un bouton de la souris sur un contrôle du lecteur Windows Media.</span><span class="sxs-lookup"><span data-stu-id="8bede-105">The DoubleClick event occurs when the user double-clicks a mouse button on a Windows Media Player control.</span></span>

``` syntax
[C#]
private void player_DoubleClickEvent(
  object sender,
  _WMPOCXEvents_DoubleClickEvent e
)

[Visual Basic]
Private Sub player_DoubleClickEvent(  
  sender As Object,  
  e As _WMPOCXEvents_DoubleClickEvent
) Handles player.DoubleClickEvent
```

## <a name="event-data"></a><span data-ttu-id="8bede-106">Données d'événements</span><span class="sxs-lookup"><span data-stu-id="8bede-106">Event Data</span></span>

<span data-ttu-id="8bede-107">Le gestionnaire associé à cet événement est de type **AxWMPLib. \_ WMPOCXEvents \_ DoubleClickEventHandler**.</span><span class="sxs-lookup"><span data-stu-id="8bede-107">The handler associated with this event is of type **AxWMPLib.\_WMPOCXEvents\_DoubleClickEventHandler**.</span></span> <span data-ttu-id="8bede-108">Ce gestionnaire reçoit un argument de type **AxWMPLib. \_ WMPOCXEvents \_ DoubleClickEvent**, qui contient les propriétés suivantes relatives à cet événement.</span><span class="sxs-lookup"><span data-stu-id="8bede-108">This handler receives an argument of type **AxWMPLib.\_WMPOCXEvents\_DoubleClickEvent**, which contains the following properties related to this event.</span></span>



| <span data-ttu-id="8bede-109">Propriété</span><span class="sxs-lookup"><span data-stu-id="8bede-109">Property</span></span>    | <span data-ttu-id="8bede-110">Description</span><span class="sxs-lookup"><span data-stu-id="8bede-110">Description</span></span>                                                                                                                                                                                                                                                                                                                    |
|-------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8bede-111">Nbouton</span><span class="sxs-lookup"><span data-stu-id="8bede-111">nButton</span></span>     | <span data-ttu-id="8bede-112">Champ de bits System. Int16a avec bits correspondant au bouton gauche (bit 0), bouton droit (bit 1) et bouton central (bit 2).</span><span class="sxs-lookup"><span data-stu-id="8bede-112">System.Int16A bitfield with bits corresponding to the left button (bit 0), right button (bit 1), and middle button (bit 2).</span></span> <span data-ttu-id="8bede-113">Ces bits correspondent respectivement aux valeurs 1, 2 et 4.</span><span class="sxs-lookup"><span data-stu-id="8bede-113">These bits correspond to the values 1, 2, and 4, respectively.</span></span> <span data-ttu-id="8bede-114">Seul l’un des bits est défini, ce qui indique le bouton à l’origine de l’événement.</span><span class="sxs-lookup"><span data-stu-id="8bede-114">Only one of the bits is set, indicating the button that caused the event.</span></span><br/>                                                |
| <span data-ttu-id="8bede-115">nShiftState</span><span class="sxs-lookup"><span data-stu-id="8bede-115">nShiftState</span></span> | <span data-ttu-id="8bede-116">Champ de bits System. Int16a avec les bits les moins significatifs correspondant à la touche Maj (bit 0), la touche CTRL (bit 1) et la touche ALT (bit 2).</span><span class="sxs-lookup"><span data-stu-id="8bede-116">System.Int16A bitfield with the least significant bits corresponding to the SHIFT key (bit 0), the CTRL key (bit 1), and the ALT key (bit 2).</span></span> <span data-ttu-id="8bede-117">Ces bits correspondent respectivement aux valeurs 1, 2 et 4.</span><span class="sxs-lookup"><span data-stu-id="8bede-117">These bits correspond to the values 1, 2, and 4, respectively.</span></span> <span data-ttu-id="8bede-118">Certains, tous ou aucun des bits peuvent être définis, ce qui indique qu’une partie, la totalité ou aucune des touches est enfoncée.</span><span class="sxs-lookup"><span data-stu-id="8bede-118">Some, all, or none of the bits can be set, indicating that some, all, or none of the keys are pressed.</span></span><br/> |
| <span data-ttu-id="8bede-119">Rotation</span><span class="sxs-lookup"><span data-stu-id="8bede-119">fX</span></span>          | <span data-ttu-id="8bede-120">Coordonnée x de System. Int32The du pointeur de la souris par rapport au coin supérieur gauche du contrôle.</span><span class="sxs-lookup"><span data-stu-id="8bede-120">System.Int32The x-coordinate of the mouse pointer relative to the upper-left corner of the control.</span></span><br/>                                                                                                                                                                                                                 |
| <span data-ttu-id="8bede-121">Années</span><span class="sxs-lookup"><span data-stu-id="8bede-121">fY</span></span>          | <span data-ttu-id="8bede-122">Coordonnée y du pointeur de la souris par rapport au coin supérieur gauche du contrôle.</span><span class="sxs-lookup"><span data-stu-id="8bede-122">System.Int32The y-coordinate of the mouse pointer relative to the upper-left corner of the control.</span></span><br/>                                                                                                                                                                                                                 |



 

## <a name="requirements"></a><span data-ttu-id="8bede-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8bede-123">Requirements</span></span>



| <span data-ttu-id="8bede-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8bede-124">Requirement</span></span> | <span data-ttu-id="8bede-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="8bede-125">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8bede-126">Version</span><span class="sxs-lookup"><span data-stu-id="8bede-126">Version</span></span><br/>   | <span data-ttu-id="8bede-127">Lecteur Windows Media série 9 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="8bede-127">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="8bede-128">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="8bede-128">Namespace</span></span><br/> | <span data-ttu-id="8bede-129">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="8bede-129">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="8bede-130">Assembly</span><span class="sxs-lookup"><span data-stu-id="8bede-130">Assembly</span></span><br/>  | <dl> <span data-ttu-id="8bede-131"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="8bede-131"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8bede-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8bede-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8bede-133">**Objet AxWindowsMediaPlayer (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="8bede-133">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> </dl>

 

 





