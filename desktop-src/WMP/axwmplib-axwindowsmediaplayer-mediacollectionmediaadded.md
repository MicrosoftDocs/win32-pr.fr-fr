---
title: Événement MediaCollectionMediaAdded de l’objet AxWindowsMediaPlayer
description: L’événement MediaCollectionMediaAdded se produit lorsqu’un élément multimédia est ajouté à la bibliothèque locale. | Événement MediaCollectionMediaAdded de l’objet AxWindowsMediaPlayer
ms.assetid: ba1779f6-a212-44f4-b52a-c88e22aebcce
keywords:
- Événement MediaCollectionMediaAdded de l’objet AxWindowsMediaPlayer du lecteur Windows Media
topic_type:
- apiref
api_name:
- MediaCollectionMediaAdded Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bbb839fccf9a5048b5647480eca36fcfcaeb904e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526830"
---
# <a name="mediacollectionmediaadded-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="5dba1-105">Événement MediaCollectionMediaAdded de l’objet AxWindowsMediaPlayer</span><span class="sxs-lookup"><span data-stu-id="5dba1-105">MediaCollectionMediaAdded Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="5dba1-106">L’événement MediaCollectionMediaAdded se produit lorsqu’un élément multimédia est ajouté à la bibliothèque locale.</span><span class="sxs-lookup"><span data-stu-id="5dba1-106">The MediaCollectionMediaAdded event occurs when a media item is added to the local library.</span></span>

``` syntax
[C#]
private void player_MediaCollectionMediaAdded(
  object sender,
  _WMPOCXEvents_MediaCollectionMediaAddedEvent e
)

[Visual Basic]
Private Sub player_MediaCollectionMediaAdded(
  sender As Object,
  e As _WMPOCXEvents_MediaCollectionMediaAddedEvent
) Handles player.MediaCollectionMediaAdded
```

## <a name="event-data"></a><span data-ttu-id="5dba1-107">Données d'événements</span><span class="sxs-lookup"><span data-stu-id="5dba1-107">Event Data</span></span>

<span data-ttu-id="5dba1-108">Le gestionnaire associé à cet événement est de type **AxWMPLib. \_ WMPOCXEvents \_ MediaCollectionMediaAddedEventHandler**.</span><span class="sxs-lookup"><span data-stu-id="5dba1-108">The handler associated with this event is of type **AxWMPLib.\_WMPOCXEvents\_MediaCollectionMediaAddedEventHandler**.</span></span> <span data-ttu-id="5dba1-109">Ce gestionnaire reçoit un argument de type **AxWMPLib. \_ WMPOCXEvents \_ MediaCollectionMediaAddedEvent**, qui contient la propriété suivante associée à cet événement.</span><span class="sxs-lookup"><span data-stu-id="5dba1-109">This handler receives an argument of type **AxWMPLib.\_WMPOCXEvents\_MediaCollectionMediaAddedEvent**, which contains the following property related to this event.</span></span>



| <span data-ttu-id="5dba1-110">Propriété</span><span class="sxs-lookup"><span data-stu-id="5dba1-110">Property</span></span> | <span data-ttu-id="5dba1-111">Description</span><span class="sxs-lookup"><span data-stu-id="5dba1-111">Description</span></span>                                                                                                                  |
|----------|------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5dba1-112">pMedia</span><span class="sxs-lookup"><span data-stu-id="5dba1-112">pMedia</span></span>   | <span data-ttu-id="5dba1-113">Élément multimédia System. ObjectThe ajouté à la bibliothèque locale.</span><span class="sxs-lookup"><span data-stu-id="5dba1-113">System.ObjectThe media item added to the local library.</span></span> <span data-ttu-id="5dba1-114">Vous pouvez effectuer un cast de ce en une interface IWMPMedia pour y accéder.</span><span class="sxs-lookup"><span data-stu-id="5dba1-114">You can cast this to an IWMPMedia interface to access it.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="5dba1-115">Notes</span><span class="sxs-lookup"><span data-stu-id="5dba1-115">Remarks</span></span>

<span data-ttu-id="5dba1-116">Cet événement se produit uniquement pour la bibliothèque locale.</span><span class="sxs-lookup"><span data-stu-id="5dba1-116">This event occurs only for the local library.</span></span>

## <a name="requirements"></a><span data-ttu-id="5dba1-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5dba1-117">Requirements</span></span>



| <span data-ttu-id="5dba1-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5dba1-118">Requirement</span></span> | <span data-ttu-id="5dba1-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="5dba1-119">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5dba1-120">Version</span><span class="sxs-lookup"><span data-stu-id="5dba1-120">Version</span></span><br/>   | <span data-ttu-id="5dba1-121">Lecteur Windows Media 11</span><span class="sxs-lookup"><span data-stu-id="5dba1-121">Windows Media Player 11</span></span><br/>                                                                                         |
| <span data-ttu-id="5dba1-122">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="5dba1-122">Namespace</span></span><br/> | <span data-ttu-id="5dba1-123">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="5dba1-123">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="5dba1-124">Assembly</span><span class="sxs-lookup"><span data-stu-id="5dba1-124">Assembly</span></span><br/>  | <dl> <span data-ttu-id="5dba1-125"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="5dba1-125"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5dba1-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5dba1-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5dba1-127">**Objet AxWindowsMediaPlayer (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="5dba1-127">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="5dba1-128">**AxWindowsMediaPlayer. mediaCollection (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="5dba1-128">**AxWindowsMediaPlayer.mediaCollection (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-mediacollection--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="5dba1-129">**Interface IWMPMedia (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="5dba1-129">**IWMPMedia Interface (VB and C#)**</span></span>](iwmpmedia--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="5dba1-130">**Interface IWMPMediaCollection (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="5dba1-130">**IWMPMediaCollection Interface (VB and C#)**</span></span>](iwmpmediacollection--vb-and-c.md)
</dt> </dl>

 

 





