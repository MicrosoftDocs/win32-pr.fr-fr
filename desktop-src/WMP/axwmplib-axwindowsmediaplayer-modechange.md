---
title: Événement ModeChange de l’objet AxWindowsMediaPlayer
description: L’événement ModeChange se produit lorsqu’un mode du lecteur Windows Media est modifié. | Événement ModeChange de l’objet AxWindowsMediaPlayer
ms.assetid: 56308425-dce5-4691-8970-c0807744abef
keywords:
- Événement ModeChange de l’objet AxWindowsMediaPlayer du lecteur Windows Media
topic_type:
- apiref
api_name:
- ModeChange Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c06575fc986f4223056244964c2d070874c890b2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106534777"
---
# <a name="modechange-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="bac51-105">Événement ModeChange de l’objet AxWindowsMediaPlayer</span><span class="sxs-lookup"><span data-stu-id="bac51-105">ModeChange Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="bac51-106">L’événement ModeChange se produit lorsqu’un mode du lecteur Windows Media est modifié.</span><span class="sxs-lookup"><span data-stu-id="bac51-106">The ModeChange event occurs when a mode of Windows Media Player is changed.</span></span>

``` syntax
[C#]
private void player_ModeChange(
  object sender,
  _WMPOCXEvents_ModeChangeEvent e
)

[Visual Basic]
Private Sub player_ModeChange( 
  sender As Object,
  e As _WMPOCXEvents_ModeChangeEvent
) Handles player.ModeChange
```

## <a name="event-data"></a><span data-ttu-id="bac51-107">Données d'événements</span><span class="sxs-lookup"><span data-stu-id="bac51-107">Event Data</span></span>

<span data-ttu-id="bac51-108">Le gestionnaire associé à cet événement est de type **AxWMPLib. \_ WMPOCXEvents \_ ModeChangeEventHandler**.</span><span class="sxs-lookup"><span data-stu-id="bac51-108">The handler associated with this event is of type **AxWMPLib.\_WMPOCXEvents\_ModeChangeEventHandler**.</span></span> <span data-ttu-id="bac51-109">Ce gestionnaire reçoit un argument de type **AxWMPLib. \_ WMPOCXEvents \_ ModeChangeEvent**, qui contient les propriétés suivantes relatives à cet événement.</span><span class="sxs-lookup"><span data-stu-id="bac51-109">This handler receives an argument of type **AxWMPLib.\_WMPOCXEvents\_ModeChangeEvent**, which contains the following properties related to this event.</span></span>



| <span data-ttu-id="bac51-110">Propriété</span><span class="sxs-lookup"><span data-stu-id="bac51-110">Property</span></span> | <span data-ttu-id="bac51-111">Description</span><span class="sxs-lookup"><span data-stu-id="bac51-111">Description</span></span>                                                                                    |
|----------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bac51-112">modeName</span><span class="sxs-lookup"><span data-stu-id="bac51-112">modeName</span></span> | <span data-ttu-id="bac51-113">System. StringIndicates le mode qui a été modifié.</span><span class="sxs-lookup"><span data-stu-id="bac51-113">System.StringIndicates the mode that was changed.</span></span> <span data-ttu-id="bac51-114">Pour connaître les valeurs possibles, consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="bac51-114">For possible values, see Remarks.</span></span><br/> |
| <span data-ttu-id="bac51-115">newValue</span><span class="sxs-lookup"><span data-stu-id="bac51-115">newValue</span></span> | <span data-ttu-id="bac51-116">System. BooleanIndicates : nouvel État du mode spécifié.</span><span class="sxs-lookup"><span data-stu-id="bac51-116">System.BooleanIndicates the new state of the specified mode.</span></span><br/>                        |



 

## <a name="remarks"></a><span data-ttu-id="bac51-117">Notes</span><span class="sxs-lookup"><span data-stu-id="bac51-117">Remarks</span></span>

<span data-ttu-id="bac51-118">Le tableau suivant indique les valeurs possibles pour la propriété modeName.</span><span class="sxs-lookup"><span data-stu-id="bac51-118">The following table shows the possible values for the modeName property.</span></span>



| <span data-ttu-id="bac51-119">String</span><span class="sxs-lookup"><span data-stu-id="bac51-119">String</span></span>  | <span data-ttu-id="bac51-120">Description</span><span class="sxs-lookup"><span data-stu-id="bac51-120">Description</span></span>                                         |
|---------|-----------------------------------------------------|
| <span data-ttu-id="bac51-121">lecture aléatoire</span><span class="sxs-lookup"><span data-stu-id="bac51-121">shuffle</span></span> | <span data-ttu-id="bac51-122">Les pistes sont lues dans un ordre aléatoire.</span><span class="sxs-lookup"><span data-stu-id="bac51-122">Tracks are played in random order.</span></span>                  |
| <span data-ttu-id="bac51-123">loop</span><span class="sxs-lookup"><span data-stu-id="bac51-123">loop</span></span>    | <span data-ttu-id="bac51-124">L’intégralité de la séquence de pistes est lue à plusieurs reprises.</span><span class="sxs-lookup"><span data-stu-id="bac51-124">The entire sequence of tracks is played repeatedly.</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="bac51-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="bac51-125">Requirements</span></span>



| <span data-ttu-id="bac51-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="bac51-126">Requirement</span></span> | <span data-ttu-id="bac51-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="bac51-127">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bac51-128">Version</span><span class="sxs-lookup"><span data-stu-id="bac51-128">Version</span></span><br/>   | <span data-ttu-id="bac51-129">Lecteur Windows Media série 9 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="bac51-129">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="bac51-130">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="bac51-130">Namespace</span></span><br/> | <span data-ttu-id="bac51-131">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="bac51-131">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="bac51-132">Assembly</span><span class="sxs-lookup"><span data-stu-id="bac51-132">Assembly</span></span><br/>  | <dl> <span data-ttu-id="bac51-133"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="bac51-133"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bac51-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bac51-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bac51-135">**Objet AxWindowsMediaPlayer (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="bac51-135">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="bac51-136">**IWMPSettings. getMode (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="bac51-136">**IWMPSettings.getMode (VB and C#)**</span></span>](wmplibiwmpsettings-iwmpsettings-getmode--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="bac51-137">**IWMPSettings. setMode (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="bac51-137">**IWMPSettings.setMode (VB and C#)**</span></span>](wmplibiwmpsettings-iwmpsettings-setmode--vb-and-c.md)
</dt> </dl>

 

 





