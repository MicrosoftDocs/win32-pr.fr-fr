---
title: Événement MarkerHit de l’objet AxWindowsMediaPlayer
description: L’événement MarkerHit se produit lorsqu’un marqueur est atteint. | Événement MarkerHit de l’objet AxWindowsMediaPlayer
ms.assetid: 247fc22c-18c4-46b6-b42c-4882209a47f4
keywords:
- Événement MarkerHit de l’objet AxWindowsMediaPlayer du lecteur Windows Media
topic_type:
- apiref
api_name:
- MarkerHit Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 03bad8d9d64b4711937cd984bbd9d335acebfe67
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540639"
---
# <a name="markerhit-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="9ed9d-105">Événement MarkerHit de l’objet AxWindowsMediaPlayer</span><span class="sxs-lookup"><span data-stu-id="9ed9d-105">MarkerHit Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="9ed9d-106">L’événement MarkerHit se produit lorsqu’un marqueur est atteint.</span><span class="sxs-lookup"><span data-stu-id="9ed9d-106">The MarkerHit event occurs when a marker is reached.</span></span>

``` syntax
[C#]
private void player_MarkerHit(
  object sender,
  _WMPOCXEvents_MarkerHitEvent e
)

[Visual Basic]
Private Sub player_MarkerHit(  
  sender As Object,  
  e As _WMPOCXEvents_MarkerHitEvent
) Handles player.MarkerHit
```

## <a name="event-data"></a><span data-ttu-id="9ed9d-107">Données d'événements</span><span class="sxs-lookup"><span data-stu-id="9ed9d-107">Event Data</span></span>

<span data-ttu-id="9ed9d-108">Le gestionnaire associé à cet événement est de type **AxWMPLib. \_ WMPOCXEvents \_ MarkerHitEventHandler**.</span><span class="sxs-lookup"><span data-stu-id="9ed9d-108">The handler associated with this event is of type **AxWMPLib.\_WMPOCXEvents\_MarkerHitEventHandler**.</span></span> <span data-ttu-id="9ed9d-109">Ce gestionnaire reçoit un argument de type **AxWMPLib. \_ WMPOCXEvents \_ MarkerHitEvent**, qui contient la propriété suivante associée à cet événement.</span><span class="sxs-lookup"><span data-stu-id="9ed9d-109">This handler receives an argument of type **AxWMPLib.\_WMPOCXEvents\_MarkerHitEvent**, which contains the following property related to this event.</span></span>



| <span data-ttu-id="9ed9d-110">Propriété</span><span class="sxs-lookup"><span data-stu-id="9ed9d-110">Property</span></span>      | <span data-ttu-id="9ed9d-111">Description</span><span class="sxs-lookup"><span data-stu-id="9ed9d-111">Description</span></span>                                                             |
|---------------|-------------------------------------------------------------------------|
| <span data-ttu-id="9ed9d-112">**MarkerNum**</span><span class="sxs-lookup"><span data-stu-id="9ed9d-112">**MarkerNum**</span></span> | <span data-ttu-id="9ed9d-113">System. Int32Indicates numéro du marqueur qui a été atteint.</span><span class="sxs-lookup"><span data-stu-id="9ed9d-113">System.Int32Indicates the number of the marker that was hit.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="9ed9d-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9ed9d-114">Requirements</span></span>



| <span data-ttu-id="9ed9d-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9ed9d-115">Requirement</span></span> | <span data-ttu-id="9ed9d-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="9ed9d-116">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9ed9d-117">Version</span><span class="sxs-lookup"><span data-stu-id="9ed9d-117">Version</span></span><br/>   | <span data-ttu-id="9ed9d-118">Lecteur Windows Media série 9 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="9ed9d-118">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="9ed9d-119">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="9ed9d-119">Namespace</span></span><br/> | <span data-ttu-id="9ed9d-120">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="9ed9d-120">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="9ed9d-121">Assembly</span><span class="sxs-lookup"><span data-stu-id="9ed9d-121">Assembly</span></span><br/>  | <dl> <span data-ttu-id="9ed9d-122"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="9ed9d-122"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9ed9d-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9ed9d-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9ed9d-124">**Objet AxWindowsMediaPlayer (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="9ed9d-124">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> </dl>

 

 





