---
title: Événement PlaylistChange de l’objet AxWindowsMediaPlayer
description: L’événement PlaylistChange se produit lorsqu’une sélection est modifiée. | Événement PlaylistChange de l’objet AxWindowsMediaPlayer
ms.assetid: e4166d81-a205-401a-94c4-a1619e764647
keywords:
- Événement PlaylistChange de l’objet AxWindowsMediaPlayer du lecteur Windows Media
topic_type:
- apiref
api_name:
- PlaylistChange Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9989b303d8e9077c158fd844c93431100205d9f6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106543916"
---
# <a name="playlistchange-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="ad97e-105">Événement PlaylistChange de l’objet AxWindowsMediaPlayer</span><span class="sxs-lookup"><span data-stu-id="ad97e-105">PlaylistChange Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="ad97e-106">L’événement PlaylistChange se produit lorsqu’une sélection est modifiée.</span><span class="sxs-lookup"><span data-stu-id="ad97e-106">The PlaylistChange event occurs when a playlist changes.</span></span>

``` syntax
[C#]
private void player_PlaylistChange(
  object sender,
  _WMPOCXEvents_PlaylistChangeEvent e
)

[Visual Basic]
Private Sub player_PlaylistChange(
  sender As Object,
  e As _WMPOCXEvents_PlaylistChangeEvent
) Handles player.PlaylistChange
```

## <a name="event-data"></a><span data-ttu-id="ad97e-107">Données d'événements</span><span class="sxs-lookup"><span data-stu-id="ad97e-107">Event Data</span></span>

<span data-ttu-id="ad97e-108">Le gestionnaire associé à cet événement est de type **AxWMPLib. \_ WMPOCXEvents \_ PlaylistChangeEventHandler**.</span><span class="sxs-lookup"><span data-stu-id="ad97e-108">The handler associated with this event is of type **AxWMPLib.\_WMPOCXEvents\_PlaylistChangeEventHandler**.</span></span> <span data-ttu-id="ad97e-109">Ce gestionnaire reçoit un argument de type **AxWMPLib. \_ WMPOCXEvents \_ PlaylistChangeEvent**, qui contient les propriétés suivantes relatives à cet événement.</span><span class="sxs-lookup"><span data-stu-id="ad97e-109">This handler receives an argument of type **AxWMPLib.\_WMPOCXEvents\_PlaylistChangeEvent**, which contains the following properties related to this event.</span></span>



| <span data-ttu-id="ad97e-110">Propriété</span><span class="sxs-lookup"><span data-stu-id="ad97e-110">Property</span></span>     | <span data-ttu-id="ad97e-111">Description</span><span class="sxs-lookup"><span data-stu-id="ad97e-111">Description</span></span>                                                                                                                   |
|--------------|-------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ad97e-112">**playlist**</span><span class="sxs-lookup"><span data-stu-id="ad97e-112">**playlist**</span></span> | <span data-ttu-id="ad97e-113">Objet System. ObjectThe qui a été modifié.</span><span class="sxs-lookup"><span data-stu-id="ad97e-113">System.ObjectThe object which changed.</span></span> <span data-ttu-id="ad97e-114">Vous pouvez effectuer un cast de ce en une interface IWMPPlaylist pour y accéder.</span><span class="sxs-lookup"><span data-stu-id="ad97e-114">You can cast this to an IWMPPlaylist interface to access it.</span></span><br/>                |
| <span data-ttu-id="ad97e-115">**change**</span><span class="sxs-lookup"><span data-stu-id="ad97e-115">**change**</span></span>   | <span data-ttu-id="ad97e-116">Valeur d’énumération WMPLib. WMPPlaylistChangeEventTypeAn indiquant le type de modification qui s’est produite dans la sélection.</span><span class="sxs-lookup"><span data-stu-id="ad97e-116">WMPLib.WMPPlaylistChangeEventTypeAn enumeration value indicating the type of change that occurred to the playlist.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="ad97e-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ad97e-117">Requirements</span></span>



| <span data-ttu-id="ad97e-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ad97e-118">Requirement</span></span> | <span data-ttu-id="ad97e-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="ad97e-119">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ad97e-120">Version</span><span class="sxs-lookup"><span data-stu-id="ad97e-120">Version</span></span><br/>   | <span data-ttu-id="ad97e-121">Lecteur Windows Media série 9 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="ad97e-121">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="ad97e-122">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="ad97e-122">Namespace</span></span><br/> | <span data-ttu-id="ad97e-123">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="ad97e-123">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="ad97e-124">Assembly</span><span class="sxs-lookup"><span data-stu-id="ad97e-124">Assembly</span></span><br/>  | <dl> <span data-ttu-id="ad97e-125"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="ad97e-125"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ad97e-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ad97e-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ad97e-127">**Objet AxWindowsMediaPlayer (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="ad97e-127">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="ad97e-128">**Interface IWMPPlaylist (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="ad97e-128">**IWMPPlaylist Interface (VB and C#)**</span></span>](iwmpplaylist--vb-and-c.md)
</dt> </dl>

 

 





