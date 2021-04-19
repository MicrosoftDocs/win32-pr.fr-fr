---
title: Événement CurrentPlaylistItemAvailable de l’objet AxWindowsMediaPlayer
description: L’événement CurrentPlaylistItemAvailable se produit lorsque la sélection actuelle est disponible. | Événement CurrentPlaylistItemAvailable de l’objet AxWindowsMediaPlayer
ms.assetid: 101807c9-b00f-4351-a9a3-5413a52496f4
keywords:
- Événement CurrentPlaylistItemAvailable de l’objet AxWindowsMediaPlayer du lecteur Windows Media
topic_type:
- apiref
api_name:
- CurrentPlaylistItemAvailable Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: be9362a569fe8296284d92204628627c74ae3b44
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106539493"
---
# <a name="currentplaylistitemavailable-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="4f21f-105">Événement CurrentPlaylistItemAvailable de l’objet AxWindowsMediaPlayer</span><span class="sxs-lookup"><span data-stu-id="4f21f-105">CurrentPlaylistItemAvailable Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="4f21f-106">L’événement CurrentPlaylistItemAvailable se produit lorsque la sélection actuelle est disponible.</span><span class="sxs-lookup"><span data-stu-id="4f21f-106">The CurrentPlaylistItemAvailable event occurs when the current playlist becomes available.</span></span>

``` syntax
[C#]
private void player_CurrentPlaylistItemAvailable(
  object sender,
  _WMPOCXEvents_CurrentPlaylistItemAvailableEvent e
)

[Visual Basic]
Private Sub player_CurrentPlaylistItemAvailable(  
  sender As Object,
  e As _WMPOCXEvents_CurrentPlaylistItemAvailableEvent
) Handles player.CurrentPlaylistItemAvailable
```

## <a name="event-data"></a><span data-ttu-id="4f21f-107">Données d'événements</span><span class="sxs-lookup"><span data-stu-id="4f21f-107">Event Data</span></span>

<span data-ttu-id="4f21f-108">Le gestionnaire associé à cet événement est de type **AxWMPLib. \_ WMPOCXEvents \_ CurrentPlaylistItemAvailableEventHandler**.</span><span class="sxs-lookup"><span data-stu-id="4f21f-108">The handler associated with this event is of type **AxWMPLib.\_WMPOCXEvents\_CurrentPlaylistItemAvailableEventHandler**.</span></span> <span data-ttu-id="4f21f-109">Ce gestionnaire reçoit un argument de type **AxWMPLib. \_ WMPOCXEvents \_ CurrentPlaylistItemAvailableEvent**, qui contient la propriété suivante associée à cet événement.</span><span class="sxs-lookup"><span data-stu-id="4f21f-109">This handler receives an argument of type **AxWMPLib.\_WMPOCXEvents\_CurrentPlaylistItemAvailableEvent**, which contains the following property related to this event.</span></span>



| <span data-ttu-id="4f21f-110">Propriété</span><span class="sxs-lookup"><span data-stu-id="4f21f-110">Property</span></span>         | <span data-ttu-id="4f21f-111">Description</span><span class="sxs-lookup"><span data-stu-id="4f21f-111">Description</span></span>                                                    |
|------------------|----------------------------------------------------------------|
| <span data-ttu-id="4f21f-112">**bstrItemName**</span><span class="sxs-lookup"><span data-stu-id="4f21f-112">**bstrItemName**</span></span> | <span data-ttu-id="4f21f-113">Nom System. StringThe de l’élément de sélection en cours.</span><span class="sxs-lookup"><span data-stu-id="4f21f-113">System.StringThe name of the current playlist item.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="4f21f-114">Notes</span><span class="sxs-lookup"><span data-stu-id="4f21f-114">Remarks</span></span>

<span data-ttu-id="4f21f-115">Le nom de la sélection actuelle peut être utilisé pour récupérer l’interface **IWMPPlaylist** correspondante à partir de l’interface IWMPPlaylistArray qui est retournée à partir de la méthode IWMPPlaylistCollection. GetByName.</span><span class="sxs-lookup"><span data-stu-id="4f21f-115">The name of the current playlist can be used to retrieve the corresponding **IWMPPlaylist** interface from the IWMPPlaylistArray interface that is returned from the IWMPPlaylistCollection.getByName method.</span></span>

## <a name="requirements"></a><span data-ttu-id="4f21f-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4f21f-116">Requirements</span></span>



| <span data-ttu-id="4f21f-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4f21f-117">Requirement</span></span> | <span data-ttu-id="4f21f-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="4f21f-118">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4f21f-119">Version</span><span class="sxs-lookup"><span data-stu-id="4f21f-119">Version</span></span><br/>   | <span data-ttu-id="4f21f-120">Lecteur Windows Media série 9 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="4f21f-120">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="4f21f-121">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="4f21f-121">Namespace</span></span><br/> | <span data-ttu-id="4f21f-122">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="4f21f-122">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="4f21f-123">Assembly</span><span class="sxs-lookup"><span data-stu-id="4f21f-123">Assembly</span></span><br/>  | <dl> <span data-ttu-id="4f21f-124"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="4f21f-124"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4f21f-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4f21f-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4f21f-126">**Objet AxWindowsMediaPlayer (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="4f21f-126">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="4f21f-127">**Interface IWMPPlaylist (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="4f21f-127">**IWMPPlaylist Interface (VB and C#)**</span></span>](iwmpplaylist--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="4f21f-128">**Interface IWMPPlaylistArray (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="4f21f-128">**IWMPPlaylistArray Interface (VB and C#)**</span></span>](iwmpplaylistarray--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="4f21f-129">**IWMPPlaylistCollection. getByName (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="4f21f-129">**IWMPPlaylistCollection.getByName (VB and C#)**</span></span>](wmplibiwmpplaylistcollection-iwmpplaylistcollection-getbyname--vb-and-c.md)
</dt> </dl>

 

 





