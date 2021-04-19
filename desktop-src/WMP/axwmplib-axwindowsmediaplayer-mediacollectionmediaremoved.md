---
title: Événement MediaCollectionMediaRemoved de l’objet AxWindowsMediaPlayer
description: L’événement MediaCollectionMediaRemoved se produit lorsqu’un élément multimédia est supprimé de la bibliothèque locale. | Événement MediaCollectionMediaRemoved de l’objet AxWindowsMediaPlayer
ms.assetid: 66dae2be-2a71-4d53-b2e2-f106426d4eea
keywords:
- Événement MediaCollectionMediaRemoved de l’objet AxWindowsMediaPlayer du lecteur Windows Media
topic_type:
- apiref
api_name:
- MediaCollectionMediaRemoved Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cea15ff63fb913cd399a152913a27ffda1090d9a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106531078"
---
# <a name="mediacollectionmediaremoved-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="7683a-105">Événement MediaCollectionMediaRemoved de l’objet AxWindowsMediaPlayer</span><span class="sxs-lookup"><span data-stu-id="7683a-105">MediaCollectionMediaRemoved Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="7683a-106">L’événement MediaCollectionMediaRemoved se produit lorsqu’un élément multimédia est supprimé de la bibliothèque locale.</span><span class="sxs-lookup"><span data-stu-id="7683a-106">The MediaCollectionMediaRemoved event occurs when a media item is removed from the local library.</span></span>

``` syntax
[C#]
private void player_MediaCollectionMediaRemoved(
  object sender,
  _WMPOCXEvents_MediaCollectionMediaRemovedEvent e
)
        
[Visual Basic]
Private Sub player_MediaCollectionMediaRemoved(
  sender As Object,
  e As _WMPOCXEvents_MediaCollectionMediaRemovedEvent
) Handles player.MediaCollectionMediaRemoved
```

## <a name="event-data"></a><span data-ttu-id="7683a-107">Données d'événements</span><span class="sxs-lookup"><span data-stu-id="7683a-107">Event Data</span></span>

<span data-ttu-id="7683a-108">Le gestionnaire associé à cet événement est de type **AxWMPLib. \_ WMPOCXEvents \_ MediaCollectionMediaRemovedEventHandler**.</span><span class="sxs-lookup"><span data-stu-id="7683a-108">The handler associated with this event is of type **AxWMPLib.\_WMPOCXEvents\_MediaCollectionMediaRemovedEventHandler**.</span></span> <span data-ttu-id="7683a-109">Ce gestionnaire reçoit un argument de type **AxWMPLib. \_ WMPOCXEvents \_ MediaCollectionMediaRemovedEvent**, qui contient la propriété suivante associée à cet événement.</span><span class="sxs-lookup"><span data-stu-id="7683a-109">This handler receives an argument of type **AxWMPLib.\_WMPOCXEvents\_MediaCollectionMediaRemovedEvent**, which contains the following property related to this event.</span></span>



| <span data-ttu-id="7683a-110">Propriété</span><span class="sxs-lookup"><span data-stu-id="7683a-110">Property</span></span> | <span data-ttu-id="7683a-111">Description</span><span class="sxs-lookup"><span data-stu-id="7683a-111">Description</span></span>                                                                                                                      |
|----------|----------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7683a-112">pMedia</span><span class="sxs-lookup"><span data-stu-id="7683a-112">pMedia</span></span>   | <span data-ttu-id="7683a-113">Élément multimédia System. ObjectThe supprimé de la bibliothèque locale.</span><span class="sxs-lookup"><span data-stu-id="7683a-113">System.ObjectThe media item removed from the local library.</span></span> <span data-ttu-id="7683a-114">Vous pouvez effectuer un cast de ce en une interface IWMPMedia pour y accéder.</span><span class="sxs-lookup"><span data-stu-id="7683a-114">You can cast this to an IWMPMedia interface to access it.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="7683a-115">Notes</span><span class="sxs-lookup"><span data-stu-id="7683a-115">Remarks</span></span>

<span data-ttu-id="7683a-116">Cet événement se produit uniquement pour la bibliothèque locale.</span><span class="sxs-lookup"><span data-stu-id="7683a-116">This event occurs only for the local library.</span></span>

## <a name="requirements"></a><span data-ttu-id="7683a-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7683a-117">Requirements</span></span>



| <span data-ttu-id="7683a-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7683a-118">Requirement</span></span> | <span data-ttu-id="7683a-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="7683a-119">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7683a-120">Version</span><span class="sxs-lookup"><span data-stu-id="7683a-120">Version</span></span><br/>   | <span data-ttu-id="7683a-121">Lecteur Windows Media 11</span><span class="sxs-lookup"><span data-stu-id="7683a-121">Windows Media Player 11</span></span><br/>                                                                                         |
| <span data-ttu-id="7683a-122">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="7683a-122">Namespace</span></span><br/> | <span data-ttu-id="7683a-123">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="7683a-123">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="7683a-124">Assembly</span><span class="sxs-lookup"><span data-stu-id="7683a-124">Assembly</span></span><br/>  | <dl> <span data-ttu-id="7683a-125"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="7683a-125"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7683a-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7683a-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7683a-127">**Objet AxWindowsMediaPlayer (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="7683a-127">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="7683a-128">**Interface IWMPMedia (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="7683a-128">**IWMPMedia Interface (VB and C#)**</span></span>](iwmpmedia--vb-and-c.md)
</dt> </dl>

 

 





