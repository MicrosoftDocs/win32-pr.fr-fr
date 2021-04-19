---
title: Événement MediaCollectionAttributeStringChanged de l’objet AxWindowsMediaPlayer
description: L’événement MediaCollectionAttributeStringChanged se produit lorsqu’une valeur d’attribut de la bibliothèque est modifiée. | Événement MediaCollectionAttributeStringChanged de l’objet AxWindowsMediaPlayer
ms.assetid: f5b91399-42b7-4202-9b65-caa9b15847b9
keywords:
- Événement MediaCollectionAttributeStringChanged de l’objet AxWindowsMediaPlayer du lecteur Windows Media
topic_type:
- apiref
api_name:
- MediaCollectionAttributeStringChanged Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c8b83d8036ca0dca7f79e2a9ba721830447f9c5a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526831"
---
# <a name="mediacollectionattributestringchanged-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="69a71-105">Événement MediaCollectionAttributeStringChanged de l’objet AxWindowsMediaPlayer</span><span class="sxs-lookup"><span data-stu-id="69a71-105">MediaCollectionAttributeStringChanged Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="69a71-106">L’événement MediaCollectionAttributeStringChanged se produit lorsqu’une valeur d’attribut de la bibliothèque est modifiée.</span><span class="sxs-lookup"><span data-stu-id="69a71-106">The MediaCollectionAttributeStringChanged event occurs when an attribute value in the library is changed.</span></span>

``` syntax
[C#]
private void player_MediaCollectionAttributeStringChanged(
  object sender,
  _WMPOCXEvents_MediaCollectionAttributeStringChangedEvent e
)

[Visual Basic]
Private Sub player_MediaCollectionAttributeStringChanged(
  sender As Object,
  e As _WMPOCXEvents_MediaCollectionAttributeStringChangedEvent
) Handles player.MediaCollectionAttributeStringChanged
```

## <a name="event-data"></a><span data-ttu-id="69a71-107">Données d'événements</span><span class="sxs-lookup"><span data-stu-id="69a71-107">Event Data</span></span>

<span data-ttu-id="69a71-108">Le gestionnaire associé à cet événement est de type **AxWMPLib. \_ WMPOCXEvents \_ MediaCollectionAttributeStringChangedEventHandler**.</span><span class="sxs-lookup"><span data-stu-id="69a71-108">The handler associated with this event is of type **AxWMPLib.\_WMPOCXEvents\_MediaCollectionAttributeStringChangedEventHandler**.</span></span> <span data-ttu-id="69a71-109">Ce gestionnaire reçoit un argument de type **AxWMPLib. \_ WMPOCXEvents \_ MediaCollectionAttributeStringChangedEvent**, qui contient les propriétés suivantes relatives à cet événement.</span><span class="sxs-lookup"><span data-stu-id="69a71-109">This handler receives an argument of type **AxWMPLib.\_WMPOCXEvents\_MediaCollectionAttributeStringChangedEvent**, which contains the following properties related to this event.</span></span>



| <span data-ttu-id="69a71-110">Propriété</span><span class="sxs-lookup"><span data-stu-id="69a71-110">Property</span></span>         | <span data-ttu-id="69a71-111">Description</span><span class="sxs-lookup"><span data-stu-id="69a71-111">Description</span></span>                                                                                                                                                                                  |
|------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="69a71-112">bstrAttribName</span><span class="sxs-lookup"><span data-stu-id="69a71-112">bstrAttribName</span></span>   | <span data-ttu-id="69a71-113">System. StringSpecifies nom de l’attribut.</span><span class="sxs-lookup"><span data-stu-id="69a71-113">System.StringSpecifies the name of the attribute.</span></span> <span data-ttu-id="69a71-114">Pour plus d’informations sur les attributs pris en charge par le lecteur Windows Media, consultez la [référence d’attribut](attribute-reference.md).</span><span class="sxs-lookup"><span data-stu-id="69a71-114">For information about the attributes supported by Windows Media Player, see the [Attribute Reference](attribute-reference.md).</span></span><br/> |
| <span data-ttu-id="69a71-115">bstrOldAttribVal</span><span class="sxs-lookup"><span data-stu-id="69a71-115">bstrOldAttribVal</span></span> | <span data-ttu-id="69a71-116">System. StringSpecifies l’ancienne valeur de l’attribut.</span><span class="sxs-lookup"><span data-stu-id="69a71-116">System.StringSpecifies the old value of the attribute.</span></span><br/>                                                                                                                            |
| <span data-ttu-id="69a71-117">bstrNewAttribVal</span><span class="sxs-lookup"><span data-stu-id="69a71-117">bstrNewAttribVal</span></span> | <span data-ttu-id="69a71-118">System. StringSpecifies nouvelle valeur de l’attribut.</span><span class="sxs-lookup"><span data-stu-id="69a71-118">System.StringSpecifies the new value of the attribute.</span></span><br/>                                                                                                                            |



 

## <a name="remarks"></a><span data-ttu-id="69a71-119">Notes</span><span class="sxs-lookup"><span data-stu-id="69a71-119">Remarks</span></span>

<span data-ttu-id="69a71-120">Quand un utilisateur modifie des métadonnées de bibliothèque, la collection de supports est mise à jour et cet événement se déclenche pour chaque attribut modifié.</span><span class="sxs-lookup"><span data-stu-id="69a71-120">When a user modifies library metadata, the media collection is updated and this event fires for each attribute changed.</span></span>

## <a name="requirements"></a><span data-ttu-id="69a71-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="69a71-121">Requirements</span></span>



| <span data-ttu-id="69a71-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="69a71-122">Requirement</span></span> | <span data-ttu-id="69a71-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="69a71-123">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="69a71-124">Version</span><span class="sxs-lookup"><span data-stu-id="69a71-124">Version</span></span><br/>   | <span data-ttu-id="69a71-125">Lecteur Windows Media série 9 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="69a71-125">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="69a71-126">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="69a71-126">Namespace</span></span><br/> | <span data-ttu-id="69a71-127">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="69a71-127">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="69a71-128">Assembly</span><span class="sxs-lookup"><span data-stu-id="69a71-128">Assembly</span></span><br/>  | <dl> <span data-ttu-id="69a71-129"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="69a71-129"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="69a71-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="69a71-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="69a71-131">**Objet AxWindowsMediaPlayer (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="69a71-131">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="69a71-132">**AxWindowsMediaPlayer. mediaCollection (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="69a71-132">**AxWindowsMediaPlayer.mediaCollection (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-mediacollection--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="69a71-133">**Interface IWMPMediaCollection (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="69a71-133">**IWMPMediaCollection Interface (VB and C#)**</span></span>](iwmpmediacollection--vb-and-c.md)
</dt> </dl>

 

 





