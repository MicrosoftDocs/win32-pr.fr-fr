---
title: Événement KeyUp de l’objet AxWindowsMediaPlayer
description: L’événement KeyUp se produit lorsqu’une touche est relâchée. | Événement KeyUp de l’objet AxWindowsMediaPlayer
ms.assetid: db814481-6099-4dbd-8ab1-808e1875ae35
keywords:
- Événement KeyUp de l’objet AxWindowsMediaPlayer lecteur Windows Media
topic_type:
- apiref
api_name:
- KeyUp Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 509f520ff7624b0b29302d7bf5cd825cd45b4254
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540553"
---
# <a name="keyup-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="0c73a-105">Événement KeyUp de l’objet AxWindowsMediaPlayer</span><span class="sxs-lookup"><span data-stu-id="0c73a-105">KeyUp Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="0c73a-106">L’événement KeyUp se produit lorsqu’une touche est relâchée.</span><span class="sxs-lookup"><span data-stu-id="0c73a-106">The KeyUp event occurs when a key is released.</span></span>

``` syntax
[C#]
private void player_KeyUpEvent(
  object sender,
  _WMPOCXEvents_KeyUpEvent e
)

[Visual Basic]
Private Sub player_KeyUpEvent(
    sender As Object,
    e As _WMPOCXEvents_KeyUpEvent
) Handles player.KeyUpEvent
```

## <a name="event-data"></a><span data-ttu-id="0c73a-107">Données d'événements</span><span class="sxs-lookup"><span data-stu-id="0c73a-107">Event Data</span></span>

<span data-ttu-id="0c73a-108">Le gestionnaire associé à cet événement est de type **AxWMPLib. \_ WMPOCXEvents \_ KeyUpEventHandler**.</span><span class="sxs-lookup"><span data-stu-id="0c73a-108">The handler associated with this event is of type **AxWMPLib.\_WMPOCXEvents\_KeyUpEventHandler**.</span></span> <span data-ttu-id="0c73a-109">Ce gestionnaire reçoit un argument de type **AxWMPLib. \_ WMPOCXEvents \_ KeyUpEvent**, qui contient les propriétés suivantes relatives à cet événement.</span><span class="sxs-lookup"><span data-stu-id="0c73a-109">This handler receives an argument of type **AxWMPLib.\_WMPOCXEvents\_KeyUpEvent**, which contains the following properties related to this event.</span></span>



| <span data-ttu-id="0c73a-110">Propriété</span><span class="sxs-lookup"><span data-stu-id="0c73a-110">Property</span></span>    | <span data-ttu-id="0c73a-111">Description</span><span class="sxs-lookup"><span data-stu-id="0c73a-111">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                          |
|-------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0c73a-112">nKeyCode</span><span class="sxs-lookup"><span data-stu-id="0c73a-112">nKeyCode</span></span>    | <span data-ttu-id="0c73a-113">System. Int16Specifies quelle touche physique est enfoncée.</span><span class="sxs-lookup"><span data-stu-id="0c73a-113">System.Int16Specifies which physical key is pressed.</span></span> <span data-ttu-id="0c73a-114">Pour connaître les valeurs possibles, consultez la section Notes de l’événement KeyOut.</span><span class="sxs-lookup"><span data-stu-id="0c73a-114">For possible values, see the Remarks section of the KeyDown event.</span></span><br/>                                                                                                                                                                                                                                                   |
| <span data-ttu-id="0c73a-115">nShiftState</span><span class="sxs-lookup"><span data-stu-id="0c73a-115">nShiftState</span></span> | <span data-ttu-id="0c73a-116">Champ de bits System. Int16a avec les bits les moins significatifs correspondant à la touche Maj (bit 0), la touche CTRL (bit 1) et la touche ALT (bit 2).</span><span class="sxs-lookup"><span data-stu-id="0c73a-116">System.Int16A bitfield with the least significant bits corresponding to the SHIFT key (bit 0), the CTRL key (bit 1), and the ALT key (bit 2).</span></span> <span data-ttu-id="0c73a-117">Ces bits correspondent respectivement aux valeurs 1, 2 et 4.</span><span class="sxs-lookup"><span data-stu-id="0c73a-117">These bits correspond to the values 1, 2, and 4, respectively.</span></span> <span data-ttu-id="0c73a-118">L’argument Shift indique l’état de ces clés.</span><span class="sxs-lookup"><span data-stu-id="0c73a-118">The shift argument indicates the state of these keys.</span></span> <span data-ttu-id="0c73a-119">Certains, tous ou aucun des bits peuvent être définis, ce qui indique qu’une partie, la totalité ou aucune des touches est enfoncée.</span><span class="sxs-lookup"><span data-stu-id="0c73a-119">Some, all, or none of the bits can be set, indicating that some, all, or none of the keys are pressed.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="0c73a-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0c73a-120">Requirements</span></span>



| <span data-ttu-id="0c73a-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0c73a-121">Requirement</span></span> | <span data-ttu-id="0c73a-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="0c73a-122">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0c73a-123">Version</span><span class="sxs-lookup"><span data-stu-id="0c73a-123">Version</span></span><br/>   | <span data-ttu-id="0c73a-124">Lecteur Windows Media série 9 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="0c73a-124">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="0c73a-125">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="0c73a-125">Namespace</span></span><br/> | <span data-ttu-id="0c73a-126">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="0c73a-126">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="0c73a-127">Assembly</span><span class="sxs-lookup"><span data-stu-id="0c73a-127">Assembly</span></span><br/>  | <dl> <span data-ttu-id="0c73a-128"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="0c73a-128"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0c73a-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0c73a-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0c73a-130">**Objet AxWindowsMediaPlayer (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="0c73a-130">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> </dl>

 

 





