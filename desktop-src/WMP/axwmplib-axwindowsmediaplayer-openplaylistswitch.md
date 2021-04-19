---
title: Événement OpenPlaylistSwitch de l’objet AxWindowsMediaPlayer
description: L’événement OpenPlaylistSwitch se produit lorsqu’un titre sur un DVD commence à être lu. | Événement OpenPlaylistSwitch de l’objet AxWindowsMediaPlayer
ms.assetid: 0b9c37a3-1349-48bd-8e1a-aba286c82abf
keywords:
- Événement OpenPlaylistSwitch de l’objet AxWindowsMediaPlayer du lecteur Windows Media
topic_type:
- apiref
api_name:
- OpenPlaylistSwitch Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 338d360944b46555be53d5e212561cf906dd33c9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106542493"
---
# <a name="openplaylistswitch-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="df46e-105">Événement OpenPlaylistSwitch de l’objet AxWindowsMediaPlayer</span><span class="sxs-lookup"><span data-stu-id="df46e-105">OpenPlaylistSwitch Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="df46e-106">L’événement OpenPlaylistSwitch se produit lorsqu’un titre sur un DVD commence à être lu.</span><span class="sxs-lookup"><span data-stu-id="df46e-106">The OpenPlaylistSwitch event occurs when a title on a DVD begins playing.</span></span>

``` syntax
[C#]
private void player_OpenPlaylistSwitch(
  object sender,
  _WMPOCXEvents_OpenPlaylistSwitchEvent e
)

[Visual Basic]
Private Sub player_OpenPlaylistSwitch(
  sender As Object,
  e As _WMPOCXEvents_OpenPlaylistSwitchEvent
) Handles player.OpenPlaylistSwitch
```

## <a name="event-data"></a><span data-ttu-id="df46e-107">Données d'événements</span><span class="sxs-lookup"><span data-stu-id="df46e-107">Event Data</span></span>

<span data-ttu-id="df46e-108">Le gestionnaire associé à cet événement est de type **AxWMPLib. \_ WMPOCXEvents \_ OpenPlaylistSwitchEventHandler**.</span><span class="sxs-lookup"><span data-stu-id="df46e-108">The handler associated with this event is of type **AxWMPLib.\_WMPOCXEvents\_OpenPlaylistSwitchEventHandler**.</span></span> <span data-ttu-id="df46e-109">Ce gestionnaire reçoit un argument de type **AxWMPLib. \_ WMPOCXEvents \_ OpenPlaylistSwitchEvent**, qui contient la propriété suivante associée à cet événement.</span><span class="sxs-lookup"><span data-stu-id="df46e-109">This handler receives an argument of type **AxWMPLib.\_WMPOCXEvents\_OpenPlaylistSwitchEvent**, which contains the following property related to this event.</span></span>



| <span data-ttu-id="df46e-110">Propriété</span><span class="sxs-lookup"><span data-stu-id="df46e-110">Property</span></span>  | <span data-ttu-id="df46e-111">Description</span><span class="sxs-lookup"><span data-stu-id="df46e-111">Description</span></span>                                                                                                         |
|-----------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="df46e-112">**pItem**</span><span class="sxs-lookup"><span data-stu-id="df46e-112">**pItem**</span></span> | <span data-ttu-id="df46e-113">System. ObjectObject représentant le titre.</span><span class="sxs-lookup"><span data-stu-id="df46e-113">System.ObjectObject representing the title.</span></span> <span data-ttu-id="df46e-114">Vous pouvez effectuer un cast de ce en une interface IWMPPlaylist pour y accéder.</span><span class="sxs-lookup"><span data-stu-id="df46e-114">You can cast this to an IWMPPlaylist interface to access it.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="df46e-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="df46e-115">Requirements</span></span>



| <span data-ttu-id="df46e-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="df46e-116">Requirement</span></span> | <span data-ttu-id="df46e-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="df46e-117">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="df46e-118">Version</span><span class="sxs-lookup"><span data-stu-id="df46e-118">Version</span></span><br/>   | <span data-ttu-id="df46e-119">Lecteur Windows Media série 9 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="df46e-119">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="df46e-120">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="df46e-120">Namespace</span></span><br/> | <span data-ttu-id="df46e-121">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="df46e-121">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="df46e-122">Assembly</span><span class="sxs-lookup"><span data-stu-id="df46e-122">Assembly</span></span><br/>  | <dl> <span data-ttu-id="df46e-123"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="df46e-123"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="df46e-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="df46e-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="df46e-125">**Objet AxWindowsMediaPlayer (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="df46e-125">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="df46e-126">**Interface IWMPPlaylist (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="df46e-126">**IWMPPlaylist Interface (VB and C#)**</span></span>](iwmpplaylist--vb-and-c.md)
</dt> </dl>

 

 





