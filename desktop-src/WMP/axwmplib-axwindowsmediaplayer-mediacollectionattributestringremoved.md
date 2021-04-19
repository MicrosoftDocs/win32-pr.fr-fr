---
title: Événement MediaCollectionAttributeStringRemoved de l’objet AxWindowsMediaPlayer
description: L’événement MediaCollectionAttributeStringRemoved se produit lorsqu’une valeur d’attribut est supprimée de la bibliothèque. | Événement MediaCollectionAttributeStringRemoved de l’objet AxWindowsMediaPlayer
ms.assetid: 2f264416-0bc5-41d0-8863-32c284393082
keywords:
- Événement MediaCollectionAttributeStringRemoved de l’objet AxWindowsMediaPlayer du lecteur Windows Media
topic_type:
- apiref
api_name:
- MediaCollectionAttributeStringRemoved Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a11b6b028a2a47585b06159ed46b986124583950
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537367"
---
# <a name="mediacollectionattributestringremoved-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="52e95-105">Événement MediaCollectionAttributeStringRemoved de l’objet AxWindowsMediaPlayer</span><span class="sxs-lookup"><span data-stu-id="52e95-105">MediaCollectionAttributeStringRemoved Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="52e95-106">L’événement MediaCollectionAttributeStringRemoved se produit lorsqu’une valeur d’attribut est supprimée de la bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="52e95-106">The MediaCollectionAttributeStringRemoved event occurs when an attribute value is removed from the library.</span></span>

``` syntax
[C#]
private void player_MediaCollectionAttributeStringRemoved(
  object sender,
  _WMPOCXEvents_MediaCollectionAttributeStringRemovedEvent e
)

[Visual Basic]
Private Sub player_MediaCollectionAttributeStringRemoved(
  sender As Object,
  e As _WMPOCXEvents_MediaCollectionAttributeStringRemovedEvent
) Handles player.MediaCollectionAttributeStringRemoved
```

## <a name="event-data"></a><span data-ttu-id="52e95-107">Données d'événements</span><span class="sxs-lookup"><span data-stu-id="52e95-107">Event Data</span></span>

<span data-ttu-id="52e95-108">Le gestionnaire associé à cet événement est de type **AxWMPLib. \_ WMPOCXEvents \_ MediaCollectionAttributeStringRemovedEventHandler**.</span><span class="sxs-lookup"><span data-stu-id="52e95-108">The handler associated with this event is of type **AxWMPLib.\_WMPOCXEvents\_MediaCollectionAttributeStringRemovedEventHandler**.</span></span> <span data-ttu-id="52e95-109">Ce gestionnaire reçoit un argument de type **AxWMPLib. \_ WMPOCXEvents \_ MediaCollectionAttributeStringRemovedEvent**, qui contient les propriétés suivantes relatives à cet événement.</span><span class="sxs-lookup"><span data-stu-id="52e95-109">This handler receives an argument of type **AxWMPLib.\_WMPOCXEvents\_MediaCollectionAttributeStringRemovedEvent**, which contains the following properties related to this event.</span></span>



| <span data-ttu-id="52e95-110">Propriété</span><span class="sxs-lookup"><span data-stu-id="52e95-110">Property</span></span>           | <span data-ttu-id="52e95-111">Description</span><span class="sxs-lookup"><span data-stu-id="52e95-111">Description</span></span>                                                                                                                                                                                  |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="52e95-112">**bstrAttribName**</span><span class="sxs-lookup"><span data-stu-id="52e95-112">**bstrAttribName**</span></span> | <span data-ttu-id="52e95-113">System. StringSpecifies nom de l’attribut.</span><span class="sxs-lookup"><span data-stu-id="52e95-113">System.StringSpecifies the name of the attribute.</span></span> <span data-ttu-id="52e95-114">Pour plus d’informations sur les attributs pris en charge par le lecteur Windows Media, consultez la [référence d’attribut](attribute-reference.md).</span><span class="sxs-lookup"><span data-stu-id="52e95-114">For information about the attributes supported by Windows Media Player, see the [Attribute Reference](attribute-reference.md).</span></span><br/> |
| <span data-ttu-id="52e95-115">bstrAttribVal</span><span class="sxs-lookup"><span data-stu-id="52e95-115">bstrAttribVal</span></span>      | <span data-ttu-id="52e95-116">System. StringSpecifies valeur de l’attribut.</span><span class="sxs-lookup"><span data-stu-id="52e95-116">System.StringSpecifies the value of the attribute.</span></span><br/>                                                                                                                                |



 

## <a name="remarks"></a><span data-ttu-id="52e95-117">Notes</span><span class="sxs-lookup"><span data-stu-id="52e95-117">Remarks</span></span>

<span data-ttu-id="52e95-118">Lorsqu’un élément multimédia est supprimé de la bibliothèque, ses métadonnées sont supprimées du **MediaCollection** et cet événement est déclenché pour chaque attribut supprimé.</span><span class="sxs-lookup"><span data-stu-id="52e95-118">When a media item is removed from the library, its metadata is removed from the **MediaCollection** and this event is fired for each attribute removed.</span></span>

## <a name="requirements"></a><span data-ttu-id="52e95-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="52e95-119">Requirements</span></span>



| <span data-ttu-id="52e95-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="52e95-120">Requirement</span></span> | <span data-ttu-id="52e95-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="52e95-121">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="52e95-122">Version</span><span class="sxs-lookup"><span data-stu-id="52e95-122">Version</span></span><br/>   | <span data-ttu-id="52e95-123">Lecteur Windows Media série 9 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="52e95-123">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="52e95-124">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="52e95-124">Namespace</span></span><br/> | <span data-ttu-id="52e95-125">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="52e95-125">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="52e95-126">Assembly</span><span class="sxs-lookup"><span data-stu-id="52e95-126">Assembly</span></span><br/>  | <dl> <span data-ttu-id="52e95-127"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="52e95-127"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="52e95-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="52e95-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="52e95-129">**Objet AxWindowsMediaPlayer (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="52e95-129">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="52e95-130">**AxWindowsMediaPlayer. mediaCollection (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="52e95-130">**AxWindowsMediaPlayer.mediaCollection (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-mediacollection--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="52e95-131">**Interface IWMPMediaCollection (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="52e95-131">**IWMPMediaCollection Interface (VB and C#)**</span></span>](iwmpmediacollection--vb-and-c.md)
</dt> </dl>

 

 





