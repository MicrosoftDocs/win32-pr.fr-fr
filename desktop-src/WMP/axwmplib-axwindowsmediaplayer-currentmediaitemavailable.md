---
title: Événement CurrentMediaItemAvailable de l’objet AxWindowsMediaPlayer
description: L’événement CurrentMediaItemAvailable se produit lorsqu’un élément de métadonnées graphiques de l’élément multimédia actuel devient disponible. | Événement CurrentMediaItemAvailable de l’objet AxWindowsMediaPlayer
ms.assetid: 7db62e6a-5f20-441a-801f-147ac386c5f8
keywords:
- Événement CurrentMediaItemAvailable de l’objet AxWindowsMediaPlayer du lecteur Windows Media
topic_type:
- apiref
api_name:
- CurrentMediaItemAvailable Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 547622424194e63733cec6166d813d42ebf577ee
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106535347"
---
# <a name="currentmediaitemavailable-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="3521e-105">Événement CurrentMediaItemAvailable de l’objet AxWindowsMediaPlayer</span><span class="sxs-lookup"><span data-stu-id="3521e-105">CurrentMediaItemAvailable Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="3521e-106">L’événement CurrentMediaItemAvailable se produit lorsqu’un élément de métadonnées graphiques de l’élément multimédia actuel devient disponible.</span><span class="sxs-lookup"><span data-stu-id="3521e-106">The CurrentMediaItemAvailable event occurs when a graphic metadata item in the current media item becomes available.</span></span>

``` syntax
[C#]
private void player_CurrentMediaItemAvailable(
  object sender,
  _WMPOCXEvents_CurrentMediaItemAvailableEvent e
)

[Visual Basic]
Private Sub player_CurrentMediaItemAvailable(
  sender As Object,  
  e As _WMPOCXEvents_CurrentMediaItemAvailableEvent
) Handles player.CurrentMediaItemAvailable
```

## <a name="event-data"></a><span data-ttu-id="3521e-107">Données d'événements</span><span class="sxs-lookup"><span data-stu-id="3521e-107">Event Data</span></span>

<span data-ttu-id="3521e-108">Le gestionnaire associé à cet événement est de type **AxWMPLib. \_ WMPOCXEvents \_ CurrentMediaItemAvailableEventHandler**.</span><span class="sxs-lookup"><span data-stu-id="3521e-108">The handler associated with this event is of type **AxWMPLib.\_WMPOCXEvents\_CurrentMediaItemAvailableEventHandler**.</span></span> <span data-ttu-id="3521e-109">Ce gestionnaire reçoit un argument de type **AxWMPLib. \_ WMPOCXEvents \_ CurrentMediaItemAvailableEvent**, qui contient la propriété suivante associée à cet événement.</span><span class="sxs-lookup"><span data-stu-id="3521e-109">This handler receives an argument of type **AxWMPLib.\_WMPOCXEvents\_CurrentMediaItemAvailableEvent**, which contains the following property related to this event.</span></span>



| <span data-ttu-id="3521e-110">Propriété</span><span class="sxs-lookup"><span data-stu-id="3521e-110">Property</span></span>     | <span data-ttu-id="3521e-111">Description</span><span class="sxs-lookup"><span data-stu-id="3521e-111">Description</span></span>                                                 |
|--------------|-------------------------------------------------------------|
| <span data-ttu-id="3521e-112">bstrItemName</span><span class="sxs-lookup"><span data-stu-id="3521e-112">bstrItemName</span></span> | <span data-ttu-id="3521e-113">Nom System. StringThe de l’élément multimédia actuel.</span><span class="sxs-lookup"><span data-stu-id="3521e-113">System.StringThe name of the current media item.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="3521e-114">Notes</span><span class="sxs-lookup"><span data-stu-id="3521e-114">Remarks</span></span>

<span data-ttu-id="3521e-115">Dans la mesure où la lecture peut commencer avant le téléchargement complet d’un élément multimédia, les graphiques de métadonnées contenus dans l’élément multimédia (par exemple, les jaquettes de la couverture de l’album) peuvent ne pas être disponibles au début de la lecture.</span><span class="sxs-lookup"><span data-stu-id="3521e-115">Because playback can begin before a media item is fully downloaded, any metadata graphics contained in the media item (such as album cover art) may not be available when it starts to play.</span></span> <span data-ttu-id="3521e-116">Cet événement vous avertit à la fin du téléchargement d’un élément de graphique de métadonnées.</span><span class="sxs-lookup"><span data-stu-id="3521e-116">This event alerts you when a metadata graphic item is finished downloading.</span></span> <span data-ttu-id="3521e-117">Vous pouvez ensuite récupérer l’interface **IWMPMedia** en passant la valeur de **bstrItemName** au *IWMPMediaCollection*. méthode **GetByName** , après laquelle vous pouvez accéder à l’élément de graphique de métadonnées à l’aide de *IWMPMedia3*. **getItemInfoByType** et en spécifiant **WM/image** comme nom d’attribut.</span><span class="sxs-lookup"><span data-stu-id="3521e-117">You can then retrieve the **IWMPMedia** interface by passing the value of **bstrItemName** to the *IWMPMediaCollection*.**getByName** method, after which you can access the metadata graphic item by using *IWMPMedia3*.**getItemInfoByType** and specifying **WM/Picture** for the attribute name.</span></span>

## <a name="requirements"></a><span data-ttu-id="3521e-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3521e-118">Requirements</span></span>



| <span data-ttu-id="3521e-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3521e-119">Requirement</span></span> | <span data-ttu-id="3521e-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="3521e-120">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3521e-121">Version</span><span class="sxs-lookup"><span data-stu-id="3521e-121">Version</span></span><br/>   | <span data-ttu-id="3521e-122">Lecteur Windows Media série 9 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="3521e-122">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="3521e-123">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="3521e-123">Namespace</span></span><br/> | <span data-ttu-id="3521e-124">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="3521e-124">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="3521e-125">Assembly</span><span class="sxs-lookup"><span data-stu-id="3521e-125">Assembly</span></span><br/>  | <dl> <span data-ttu-id="3521e-126"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="3521e-126"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3521e-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3521e-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3521e-128">**Objet AxWindowsMediaPlayer (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="3521e-128">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="3521e-129">**Interface IWMPMedia (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="3521e-129">**IWMPMedia Interface (VB and C#)**</span></span>](iwmpmedia--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="3521e-130">**IWMPMedia3. getItemInfoByType (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="3521e-130">**IWMPMedia3.getItemInfoByType (VB and C#)**</span></span>](wmplibiwmpmedia3-iwmpmedia3-getiteminfobytype--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="3521e-131">**IWMPMediaCollection. getByName (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="3521e-131">**IWMPMediaCollection.getByName (VB and C#)**</span></span>](wmplibiwmpmediacollection-iwmpmediacollection-getbyname--vb-and-c.md)
</dt> </dl>

 

 





