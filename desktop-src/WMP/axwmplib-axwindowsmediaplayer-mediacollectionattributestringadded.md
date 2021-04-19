---
title: Événement MediaCollectionAttributeStringAdded de l’objet AxWindowsMediaPlayer
description: L’événement MediaCollectionAttributeStringAdded se produit lorsqu’une valeur d’attribut est ajoutée à la bibliothèque. | Événement MediaCollectionAttributeStringAdded de l’objet AxWindowsMediaPlayer
ms.assetid: b14db0ce-bd78-4e28-a42c-1a231c29da2b
keywords:
- Événement MediaCollectionAttributeStringAdded de l’objet AxWindowsMediaPlayer du lecteur Windows Media
topic_type:
- apiref
api_name:
- MediaCollectionAttributeStringAdded Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6712b6caa8f014ec75bf2b031e2d3f6db429dbd2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106523892"
---
# <a name="mediacollectionattributestringadded-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="a39a5-105">Événement MediaCollectionAttributeStringAdded de l’objet AxWindowsMediaPlayer</span><span class="sxs-lookup"><span data-stu-id="a39a5-105">MediaCollectionAttributeStringAdded Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="a39a5-106">L’événement MediaCollectionAttributeStringAdded se produit lorsqu’une valeur d’attribut est ajoutée à la bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="a39a5-106">The MediaCollectionAttributeStringAdded event occurs when an attribute value is added to the library.</span></span>

``` syntax
[C#]
private void player_MediaCollectionAttributeStringAdded(
  object sender,
  _WMPOCXEvents_MediaCollectionAttributeStringAddedEvent e
)

[Visual Basic]
Private Sub player_MediaCollectionAttributeStringAdded(
  sender As Object,
  e As _WMPOCXEvents_MediaCollectionAttributeStringAddedEvent
) Handles player.MediaCollectionAttributeStringAdded
```

## <a name="event-data"></a><span data-ttu-id="a39a5-107">Données d'événements</span><span class="sxs-lookup"><span data-stu-id="a39a5-107">Event Data</span></span>

<span data-ttu-id="a39a5-108">Le gestionnaire associé à cet événement est de type **AxWMPLib. \_ WMPOCXEvents \_ MediaCollectionAttributeStringAddedEventHandler**.</span><span class="sxs-lookup"><span data-stu-id="a39a5-108">The handler associated with this event is of type **AxWMPLib.\_WMPOCXEvents\_MediaCollectionAttributeStringAddedEventHandler**.</span></span> <span data-ttu-id="a39a5-109">Ce gestionnaire reçoit un argument de type **AxWMPLib. \_ WMPOCXEvents \_ MediaCollectionAttributeStringAddedEvent**, qui contient les propriétés suivantes relatives à cet événement.</span><span class="sxs-lookup"><span data-stu-id="a39a5-109">This handler receives an argument of type **AxWMPLib.\_WMPOCXEvents\_MediaCollectionAttributeStringAddedEvent**, which contains the following properties related to this event.</span></span>



| <span data-ttu-id="a39a5-110">Propriété</span><span class="sxs-lookup"><span data-stu-id="a39a5-110">Property</span></span>           | <span data-ttu-id="a39a5-111">Description</span><span class="sxs-lookup"><span data-stu-id="a39a5-111">Description</span></span>                                                                                                                                                                                  |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a39a5-112">**bstrAttribName**</span><span class="sxs-lookup"><span data-stu-id="a39a5-112">**bstrAttribName**</span></span> | <span data-ttu-id="a39a5-113">System. StringSpecifies nom de l’attribut.</span><span class="sxs-lookup"><span data-stu-id="a39a5-113">System.StringSpecifies the name of the attribute.</span></span> <span data-ttu-id="a39a5-114">Pour plus d’informations sur les attributs pris en charge par le lecteur Windows Media, consultez la [référence d’attribut](attribute-reference.md).</span><span class="sxs-lookup"><span data-stu-id="a39a5-114">For information about the attributes supported by Windows Media Player, see the [Attribute Reference](attribute-reference.md).</span></span><br/> |
| <span data-ttu-id="a39a5-115">bstrAttribVal</span><span class="sxs-lookup"><span data-stu-id="a39a5-115">bstrAttribVal</span></span>      | <span data-ttu-id="a39a5-116">System. StringSpecifies valeur de l’attribut.</span><span class="sxs-lookup"><span data-stu-id="a39a5-116">System.StringSpecifies the value of the attribute.</span></span><br/>                                                                                                                                |



 

## <a name="remarks"></a><span data-ttu-id="a39a5-117">Notes</span><span class="sxs-lookup"><span data-stu-id="a39a5-117">Remarks</span></span>

<span data-ttu-id="a39a5-118">Lorsqu’un élément multimédia est ajouté à la bibliothèque, ses métadonnées sont ajoutées à la collection de supports et cet événement est déclenché pour chaque attribut ajouté.</span><span class="sxs-lookup"><span data-stu-id="a39a5-118">When a media item is added to the library, its metadata is added to the media collection and this event is fired for each attribute added.</span></span>

## <a name="requirements"></a><span data-ttu-id="a39a5-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a39a5-119">Requirements</span></span>



| <span data-ttu-id="a39a5-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a39a5-120">Requirement</span></span> | <span data-ttu-id="a39a5-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="a39a5-121">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a39a5-122">Version</span><span class="sxs-lookup"><span data-stu-id="a39a5-122">Version</span></span><br/>   | <span data-ttu-id="a39a5-123">Lecteur Windows Media série 9 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="a39a5-123">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="a39a5-124">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="a39a5-124">Namespace</span></span><br/> | <span data-ttu-id="a39a5-125">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="a39a5-125">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="a39a5-126">Assembly</span><span class="sxs-lookup"><span data-stu-id="a39a5-126">Assembly</span></span><br/>  | <dl> <span data-ttu-id="a39a5-127"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="a39a5-127"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a39a5-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a39a5-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a39a5-129">**Objet AxWindowsMediaPlayer (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="a39a5-129">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="a39a5-130">**AxWindowsMediaPlayer. mediaCollection (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="a39a5-130">**AxWindowsMediaPlayer.mediaCollection (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-mediacollection--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="a39a5-131">**Interface IWMPMediaCollection (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="a39a5-131">**IWMPMediaCollection Interface (VB and C#)**</span></span>](iwmpmediacollection--vb-and-c.md)
</dt> </dl>

 

 





