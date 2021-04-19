---
title: Événement DurationUnitChange de l’objet AxWindowsMediaPlayer
description: L’événement DurationUnitChange est réservé pour une utilisation ultérieure.
ms.assetid: d8d7da21-bc61-49f8-91bd-4c232295c1ac
keywords:
- Événement DurationUnitChange de l’objet AxWindowsMediaPlayer du lecteur Windows Media
topic_type:
- apiref
api_name:
- DurationUnitChange Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f90aa052c61893d83683d10f482cd05841a49fab
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528608"
---
# <a name="durationunitchange-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="3520b-104">Événement DurationUnitChange de l’objet AxWindowsMediaPlayer</span><span class="sxs-lookup"><span data-stu-id="3520b-104">DurationUnitChange Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="3520b-105">L’événement DurationUnitChange est réservé pour une utilisation ultérieure.</span><span class="sxs-lookup"><span data-stu-id="3520b-105">The DurationUnitChange event is reserved for future use.</span></span>

``` syntax
[C#]
private void player_DurationUnitChange(
  object sender,
  _WMPOCXEvents_DurationUnitChangeEvent e
)

[Visual Basic]
Private Sub player_DurationUnitChange(  
  sender As Object,  
  e As _WMPOCXEvents_DurationUnitChangeEvent
) Handles player.DurationUnitChange
```

## <a name="event-data"></a><span data-ttu-id="3520b-106">Données d'événements</span><span class="sxs-lookup"><span data-stu-id="3520b-106">Event Data</span></span>

<span data-ttu-id="3520b-107">Le gestionnaire associé à cet événement est de type **AxWMPLib. \_ WMPOCXEvents \_ DurationUnitChangeEventHandler**.</span><span class="sxs-lookup"><span data-stu-id="3520b-107">The handler associated with this event is of type **AxWMPLib.\_WMPOCXEvents\_DurationUnitChangeEventHandler**.</span></span> <span data-ttu-id="3520b-108">Ce gestionnaire reçoit un argument de type **AxWMPLib. \_ WMPOCXEvents \_ DurationUnitChangeEvent**, qui contient la propriété suivante associée à cet événement.</span><span class="sxs-lookup"><span data-stu-id="3520b-108">This handler receives an argument of type **AxWMPLib.\_WMPOCXEvents\_DurationUnitChangeEvent**, which contains the following property related to this event.</span></span>



| <span data-ttu-id="3520b-109">Propriété</span><span class="sxs-lookup"><span data-stu-id="3520b-109">Property</span></span>        | <span data-ttu-id="3520b-110">Description</span><span class="sxs-lookup"><span data-stu-id="3520b-110">Description</span></span>                               |
|-----------------|-------------------------------------------|
| <span data-ttu-id="3520b-111">newDurationUnit</span><span class="sxs-lookup"><span data-stu-id="3520b-111">newDurationUnit</span></span> | <span data-ttu-id="3520b-112">**System. Int32** Non pris en charge.</span><span class="sxs-lookup"><span data-stu-id="3520b-112">**System.Int32** Not supported.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="3520b-113">Notes</span><span class="sxs-lookup"><span data-stu-id="3520b-113">Remarks</span></span>

<span data-ttu-id="3520b-114">Cet événement est réservé à une utilisation ultérieure.</span><span class="sxs-lookup"><span data-stu-id="3520b-114">This event is reserved for future use.</span></span>

## <a name="requirements"></a><span data-ttu-id="3520b-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3520b-115">Requirements</span></span>



| <span data-ttu-id="3520b-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3520b-116">Requirement</span></span> | <span data-ttu-id="3520b-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="3520b-117">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3520b-118">Version</span><span class="sxs-lookup"><span data-stu-id="3520b-118">Version</span></span><br/>   | <span data-ttu-id="3520b-119">Lecteur Windows Media série 9 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="3520b-119">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="3520b-120">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="3520b-120">Namespace</span></span><br/> | <span data-ttu-id="3520b-121">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="3520b-121">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="3520b-122">Assembly</span><span class="sxs-lookup"><span data-stu-id="3520b-122">Assembly</span></span><br/>  | <dl> <span data-ttu-id="3520b-123"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="3520b-123"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3520b-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3520b-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3520b-125">**Objet AxWindowsMediaPlayer (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="3520b-125">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> </dl>

 

 





