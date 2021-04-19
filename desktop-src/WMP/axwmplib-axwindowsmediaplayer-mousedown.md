---
title: Événement MouseDown de l’objet AxWindowsMediaPlayer
description: L’événement MouseDown se produit lorsque l’utilisateur appuie sur un bouton de la souris. | Événement MouseDown de l’objet AxWindowsMediaPlayer
ms.assetid: 3dfbd034-67d4-4b7e-88d8-a77d301c5df7
keywords:
- Événement MouseDown de l’objet AxWindowsMediaPlayer Windows Media Player
topic_type:
- apiref
api_name:
- MouseDown Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0779df27f406691903a0362c9eb3a1df993f595f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541465"
---
# <a name="mousedown-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="4d2de-105">Événement MouseDown de l’objet AxWindowsMediaPlayer</span><span class="sxs-lookup"><span data-stu-id="4d2de-105">MouseDown Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="4d2de-106">L’événement MouseDown se produit lorsque l’utilisateur appuie sur un bouton de la souris.</span><span class="sxs-lookup"><span data-stu-id="4d2de-106">The MouseDown event occurs when the user presses a mouse button.</span></span>

``` syntax
[C#]
private void player_MouseDownEvent(
  object sender,
  _WMPOCXEvents_MouseDownEvent e
)

[Visual Basic]
Private Sub player_MouseDownEvent(  
  sender As Object,
  e As _WMPOCXEvents_MouseDownEvent
) Handles player.MouseDownEvent
```

## <a name="event-data"></a><span data-ttu-id="4d2de-107">Données d'événements</span><span class="sxs-lookup"><span data-stu-id="4d2de-107">Event Data</span></span>

<span data-ttu-id="4d2de-108">Le gestionnaire associé à cet événement est de type **AxWMPLib. \_ WMPOCXEvents \_ MouseDownEventHandler**.</span><span class="sxs-lookup"><span data-stu-id="4d2de-108">The handler associated with this event is of type **AxWMPLib.\_WMPOCXEvents\_MouseDownEventHandler**.</span></span> <span data-ttu-id="4d2de-109">Ce gestionnaire reçoit un argument de type **AxWMPLib. \_ WMPOCXEvents \_ MouseDownEvent**, qui contient les propriétés suivantes relatives à cet événement.</span><span class="sxs-lookup"><span data-stu-id="4d2de-109">This handler receives an argument of type **AxWMPLib.\_WMPOCXEvents\_MouseDownEvent**, which contains the following properties related to this event.</span></span>



| <span data-ttu-id="4d2de-110">Propriété</span><span class="sxs-lookup"><span data-stu-id="4d2de-110">Property</span></span>    | <span data-ttu-id="4d2de-111">Description</span><span class="sxs-lookup"><span data-stu-id="4d2de-111">Description</span></span>                                                                                                                                                                                                                                                                                                                    |
|-------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4d2de-112">Nbouton</span><span class="sxs-lookup"><span data-stu-id="4d2de-112">nButton</span></span>     | <span data-ttu-id="4d2de-113">Champ de bits System. Int16a avec bits correspondant au bouton gauche (bit 0), bouton droit (bit 1) et bouton central (bit 2).</span><span class="sxs-lookup"><span data-stu-id="4d2de-113">System.Int16A bitfield with bits corresponding to the left button (bit 0), right button (bit 1), and middle button (bit 2).</span></span> <span data-ttu-id="4d2de-114">Ces bits correspondent respectivement aux valeurs 1, 2 et 4.</span><span class="sxs-lookup"><span data-stu-id="4d2de-114">These bits correspond to the values 1, 2, and 4, respectively.</span></span> <span data-ttu-id="4d2de-115">Seul l’un des bits est défini, ce qui indique le bouton à l’origine de l’événement.</span><span class="sxs-lookup"><span data-stu-id="4d2de-115">Only one of the bits is set, indicating the button that caused the event.</span></span><br/>                                                |
| <span data-ttu-id="4d2de-116">nShiftState</span><span class="sxs-lookup"><span data-stu-id="4d2de-116">nShiftState</span></span> | <span data-ttu-id="4d2de-117">Champ de bits System. Int16a avec les bits les moins significatifs correspondant à la touche Maj (bit 0), la touche CTRL (bit 1) et la touche ALT (bit 2).</span><span class="sxs-lookup"><span data-stu-id="4d2de-117">System.Int16A bitfield with the least significant bits corresponding to the SHIFT key (bit 0), the CTRL key (bit 1), and the ALT key (bit 2).</span></span> <span data-ttu-id="4d2de-118">Ces bits correspondent respectivement aux valeurs 1, 2 et 4.</span><span class="sxs-lookup"><span data-stu-id="4d2de-118">These bits correspond to the values 1, 2, and 4, respectively.</span></span> <span data-ttu-id="4d2de-119">Certains, tous ou aucun des bits peuvent être définis, ce qui indique qu’une partie, la totalité ou aucune des touches est enfoncée.</span><span class="sxs-lookup"><span data-stu-id="4d2de-119">Some, all, or none of the bits can be set, indicating that some, all, or none of the keys are pressed.</span></span><br/> |
| <span data-ttu-id="4d2de-120">Rotation</span><span class="sxs-lookup"><span data-stu-id="4d2de-120">fX</span></span>          | <span data-ttu-id="4d2de-121">Coordonnée x de System. Int32The du pointeur de la souris par rapport au coin supérieur gauche du contrôle.</span><span class="sxs-lookup"><span data-stu-id="4d2de-121">System.Int32The x-coordinate of the mouse pointer relative to the upper-left corner of the control.</span></span><br/>                                                                                                                                                                                                                 |
| <span data-ttu-id="4d2de-122">Années</span><span class="sxs-lookup"><span data-stu-id="4d2de-122">fY</span></span>          | <span data-ttu-id="4d2de-123">Coordonnée y du pointeur de la souris par rapport au coin supérieur gauche du contrôle.</span><span class="sxs-lookup"><span data-stu-id="4d2de-123">System.Int32The y-coordinate of the mouse pointer relative to the upper-left corner of the control.</span></span><br/>                                                                                                                                                                                                                 |



 

## <a name="requirements"></a><span data-ttu-id="4d2de-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4d2de-124">Requirements</span></span>



| <span data-ttu-id="4d2de-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4d2de-125">Requirement</span></span> | <span data-ttu-id="4d2de-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="4d2de-126">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4d2de-127">Version</span><span class="sxs-lookup"><span data-stu-id="4d2de-127">Version</span></span><br/>   | <span data-ttu-id="4d2de-128">Lecteur Windows Media série 9 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="4d2de-128">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="4d2de-129">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="4d2de-129">Namespace</span></span><br/> | <span data-ttu-id="4d2de-130">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="4d2de-130">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="4d2de-131">Assembly</span><span class="sxs-lookup"><span data-stu-id="4d2de-131">Assembly</span></span><br/>  | <dl> <span data-ttu-id="4d2de-132"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="4d2de-132"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4d2de-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4d2de-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4d2de-134">**Objet AxWindowsMediaPlayer (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="4d2de-134">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> </dl>

 

 





