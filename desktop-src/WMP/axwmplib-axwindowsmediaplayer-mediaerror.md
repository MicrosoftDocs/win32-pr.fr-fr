---
title: Événement MediaError de l’objet AxWindowsMediaPlayer
description: L’événement MediaError se produit lorsqu’un objet multimédia a une condition d’erreur.
ms.assetid: a1fb3422-85c4-4856-951a-332517599984
keywords:
- Événement MediaError de l’objet AxWindowsMediaPlayer du lecteur Windows Media
topic_type:
- apiref
api_name:
- MediaError Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 874b9297846a8f25f25c68545df234aa1be70594
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106531077"
---
# <a name="mediaerror-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="2791f-104">Événement MediaError de l’objet AxWindowsMediaPlayer</span><span class="sxs-lookup"><span data-stu-id="2791f-104">MediaError Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="2791f-105">L’événement MediaError se produit lorsqu’un objet multimédia a une condition d’erreur.</span><span class="sxs-lookup"><span data-stu-id="2791f-105">The MediaError event occurs when a media object has an error condition.</span></span>

``` syntax
[C#]
private void player_MediaError(
  object sender,
  _WMPOCXEvents_MediaErrorEvent e
)

[Visual Basic]
Private Sub player_MediaError(
  sender As Object,
  e As _WMPOCXEvents_MediaErrorEvent
) Handles player.MediaError
```

## <a name="event-data"></a><span data-ttu-id="2791f-106">Données d'événements</span><span class="sxs-lookup"><span data-stu-id="2791f-106">Event Data</span></span>

<span data-ttu-id="2791f-107">Le gestionnaire associé à cet événement est de type **AxWMPLib. \_ WMPOCXEvents \_ MediaErrorEventHandler**.</span><span class="sxs-lookup"><span data-stu-id="2791f-107">The handler associated with this event is of type **AxWMPLib.\_WMPOCXEvents\_MediaErrorEventHandler**.</span></span> <span data-ttu-id="2791f-108">Ce gestionnaire reçoit un argument de type **AxWMPLib. \_ WMPOCXEvents \_ MediaErrorEvent**, qui contient la propriété suivante associée à cet événement.</span><span class="sxs-lookup"><span data-stu-id="2791f-108">This handler receives an argument of type **AxWMPLib.\_WMPOCXEvents\_MediaErrorEvent**, which contains the following property related to this event.</span></span>



| <span data-ttu-id="2791f-109">Propriété</span><span class="sxs-lookup"><span data-stu-id="2791f-109">Property</span></span>     | <span data-ttu-id="2791f-110">Description</span><span class="sxs-lookup"><span data-stu-id="2791f-110">Description</span></span>                                                                                                           |
|--------------|-----------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2791f-111">pMediaObject</span><span class="sxs-lookup"><span data-stu-id="2791f-111">pMediaObject</span></span> | <span data-ttu-id="2791f-112">System. ObjectObject qui a une condition d’erreur.</span><span class="sxs-lookup"><span data-stu-id="2791f-112">System.ObjectObject that has an error condition.</span></span> <span data-ttu-id="2791f-113">Vous pouvez effectuer un cast de ce en une interface IWMPMedia pour y accéder.</span><span class="sxs-lookup"><span data-stu-id="2791f-113">You can cast this to an IWMPMedia interface to access it.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="2791f-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2791f-114">Requirements</span></span>



| <span data-ttu-id="2791f-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2791f-115">Requirement</span></span> | <span data-ttu-id="2791f-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="2791f-116">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2791f-117">Version</span><span class="sxs-lookup"><span data-stu-id="2791f-117">Version</span></span><br/>   | <span data-ttu-id="2791f-118">Lecteur Windows Media série 9 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="2791f-118">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="2791f-119">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="2791f-119">Namespace</span></span><br/> | <span data-ttu-id="2791f-120">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="2791f-120">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="2791f-121">Assembly</span><span class="sxs-lookup"><span data-stu-id="2791f-121">Assembly</span></span><br/>  | <dl> <span data-ttu-id="2791f-122"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="2791f-122"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2791f-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2791f-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2791f-124">**Objet AxWindowsMediaPlayer (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="2791f-124">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="2791f-125">**Interface IWMPMedia (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="2791f-125">**IWMPMedia Interface (VB and C#)**</span></span>](iwmpmedia--vb-and-c.md)
</dt> </dl>

 

 





