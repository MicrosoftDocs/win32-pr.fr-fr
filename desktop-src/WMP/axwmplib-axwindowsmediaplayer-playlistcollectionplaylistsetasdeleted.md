---
title: Événement PlaylistCollectionPlaylistSetAsDeleted de l’objet AxWindowsMediaPlayer
description: L’événement PlaylistCollectionPlaylistSetAsDeleted est réservé pour une utilisation ultérieure.
ms.assetid: 6c0a4d2c-e965-4a88-acd4-2a2a12265e36
keywords:
- Événement PlaylistCollectionPlaylistSetAsDeleted de l’objet AxWindowsMediaPlayer du lecteur Windows Media
topic_type:
- apiref
api_name:
- PlaylistCollectionPlaylistSetAsDeleted Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bf432ede40298abed98cdf0c5b02b0a192f7b3a9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106530353"
---
# <a name="playlistcollectionplaylistsetasdeleted-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="826b3-104">Événement PlaylistCollectionPlaylistSetAsDeleted de l’objet AxWindowsMediaPlayer</span><span class="sxs-lookup"><span data-stu-id="826b3-104">PlaylistCollectionPlaylistSetAsDeleted Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="826b3-105">L’événement PlaylistCollectionPlaylistSetAsDeleted est réservé pour une utilisation ultérieure.</span><span class="sxs-lookup"><span data-stu-id="826b3-105">The PlaylistCollectionPlaylistSetAsDeleted event is reserved for future use.</span></span>

``` syntax
[C#]
private void player_PlaylistCollectionPlaylistSetAsDeleted(
  object sender,
  _WMPOCXEvents_PlaylistCollectionPlaylistSetAsDeletedEvent e
)

[Visual Basic]
Private Sub player_PlaylistCollectionPlaylistSetAsDeleted(
  sender As Object,
  e As _WMPOCXEvents_PlaylistCollectionPlaylistSetAsDeletedEvent
) Handles player.PlaylistCollectionPlaylistSetAsDeleted
```

## <a name="event-data"></a><span data-ttu-id="826b3-106">Données d'événements</span><span class="sxs-lookup"><span data-stu-id="826b3-106">Event Data</span></span>

<span data-ttu-id="826b3-107">Le gestionnaire associé à cet événement est de type **AxWMPLib. \_ WMPOCXEvents \_ PlaylistCollectionPlaylistSetAsDeletedEventHandler**.</span><span class="sxs-lookup"><span data-stu-id="826b3-107">The handler associated with this event is of type **AxWMPLib.\_WMPOCXEvents\_PlaylistCollectionPlaylistSetAsDeletedEventHandler**.</span></span> <span data-ttu-id="826b3-108">Ce gestionnaire reçoit un argument de type **AxWMPLib. \_ WMPOCXEvents \_ PlaylistCollectionPlaylistSetAsDeletedEvent**, qui contient les propriétés suivantes relatives à cet événement.</span><span class="sxs-lookup"><span data-stu-id="826b3-108">This handler receives an argument of type **AxWMPLib.\_WMPOCXEvents\_PlaylistCollectionPlaylistSetAsDeletedEvent**, which contains the following properties related to this event.</span></span>



| <span data-ttu-id="826b3-109">Propriété</span><span class="sxs-lookup"><span data-stu-id="826b3-109">Property</span></span>         | <span data-ttu-id="826b3-110">Description</span><span class="sxs-lookup"><span data-stu-id="826b3-110">Description</span></span>                                 |
|------------------|---------------------------------------------|
| <span data-ttu-id="826b3-111">bstrPlaylistName</span><span class="sxs-lookup"><span data-stu-id="826b3-111">bstrPlaylistName</span></span> | <span data-ttu-id="826b3-112">**System. String** Non pris en charge.</span><span class="sxs-lookup"><span data-stu-id="826b3-112">**System.String** Not supported.</span></span><br/>  |
| <span data-ttu-id="826b3-113">varfIsDeleted</span><span class="sxs-lookup"><span data-stu-id="826b3-113">varfIsDeleted</span></span>    | <span data-ttu-id="826b3-114">**System. Boolean** Non pris en charge.</span><span class="sxs-lookup"><span data-stu-id="826b3-114">**System.Boolean** Not supported.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="826b3-115">Notes</span><span class="sxs-lookup"><span data-stu-id="826b3-115">Remarks</span></span>

<span data-ttu-id="826b3-116">Cet événement est réservé à une utilisation ultérieure.</span><span class="sxs-lookup"><span data-stu-id="826b3-116">This event is reserved for future use.</span></span>

## <a name="requirements"></a><span data-ttu-id="826b3-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="826b3-117">Requirements</span></span>



| <span data-ttu-id="826b3-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="826b3-118">Requirement</span></span> | <span data-ttu-id="826b3-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="826b3-119">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="826b3-120">Version</span><span class="sxs-lookup"><span data-stu-id="826b3-120">Version</span></span><br/>   | <span data-ttu-id="826b3-121">Lecteur Windows Media série 9 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="826b3-121">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="826b3-122">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="826b3-122">Namespace</span></span><br/> | <span data-ttu-id="826b3-123">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="826b3-123">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="826b3-124">Assembly</span><span class="sxs-lookup"><span data-stu-id="826b3-124">Assembly</span></span><br/>  | <dl> <span data-ttu-id="826b3-125"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="826b3-125"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="826b3-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="826b3-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="826b3-127">**Objet AxWindowsMediaPlayer (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="826b3-127">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> </dl>

 

 





