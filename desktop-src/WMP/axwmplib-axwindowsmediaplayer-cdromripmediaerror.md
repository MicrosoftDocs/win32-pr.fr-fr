---
title: Événement CdromRipMediaError de l’objet AxWindowsMediaPlayer
description: L’événement CdromRipMediaError se produit lorsqu’une erreur se produit lors de l’extraction d’une piste individuelle à partir d’un CD.
ms.assetid: 542d0184-d893-4b98-903e-339909276fd6
keywords:
- Événement CdromRipMediaError de l’objet AxWindowsMediaPlayer du lecteur Windows Media
topic_type:
- apiref
api_name:
- CdromRipMediaError Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 39b429505996cd5e85bc1e0e2e85c3f47103d244
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106525106"
---
# <a name="cdromripmediaerror-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="26aa0-104">Événement CdromRipMediaError de l’objet AxWindowsMediaPlayer</span><span class="sxs-lookup"><span data-stu-id="26aa0-104">CdromRipMediaError Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="26aa0-105">L’événement CdromRipMediaError se produit lorsqu’une erreur se produit lors de l’extraction d’une piste individuelle à partir d’un CD.</span><span class="sxs-lookup"><span data-stu-id="26aa0-105">The CdromRipMediaError event occurs when an error happens while ripping an individual track from a CD.</span></span>

``` syntax
[C#]
private void player_CdromRipMediaError(
  object sender,
  _WMPOCXEvents_CdromRipMediaErrorEvent e
)

[Visual Basic]
Private Sub player_CdromRipMediaError( 
  sender As Object,
  e As _WMPOCXEvents_CdromRipMediaErrorEvent
) Handles player.CdromRipMediaError
```

## <a name="event-data"></a><span data-ttu-id="26aa0-106">Données d'événements</span><span class="sxs-lookup"><span data-stu-id="26aa0-106">Event Data</span></span>

<span data-ttu-id="26aa0-107">Le gestionnaire associé à cet événement est de type **AxWMPLib. \_ WMPOCXEvents \_ CdromRipMediaErrorEventHandler**.</span><span class="sxs-lookup"><span data-stu-id="26aa0-107">The handler associated with this event is of type **AxWMPLib.\_WMPOCXEvents\_CdromRipMediaErrorEventHandler**.</span></span> <span data-ttu-id="26aa0-108">Ce gestionnaire reçoit un argument de type **AxWMPLib. \_ WMPOCXEvents \_ CdromRipMediaErrorEvent**, qui contient les propriétés suivantes relatives à cet événement.</span><span class="sxs-lookup"><span data-stu-id="26aa0-108">This handler receives an argument of type **AxWMPLib.\_WMPOCXEvents\_CdromRipMediaErrorEvent**, which contains the following properties related to this event.</span></span>



| <span data-ttu-id="26aa0-109">Propriété</span><span class="sxs-lookup"><span data-stu-id="26aa0-109">Property</span></span>  | <span data-ttu-id="26aa0-110">Description</span><span class="sxs-lookup"><span data-stu-id="26aa0-110">Description</span></span>                                                                                                             |
|-----------|-------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="26aa0-111">pCdromRip</span><span class="sxs-lookup"><span data-stu-id="26aa0-111">pCdromRip</span></span> | <span data-ttu-id="26aa0-112">Interface WMPLib. IWMPCdromRipThe qui représente l’opération d’extraction qui a déclenché l’erreur.</span><span class="sxs-lookup"><span data-stu-id="26aa0-112">WMPLib.IWMPCdromRipThe interface that represents the ripping operation that raised the error.</span></span><br/>                |
| <span data-ttu-id="26aa0-113">pMedia</span><span class="sxs-lookup"><span data-stu-id="26aa0-113">pMedia</span></span>    | <span data-ttu-id="26aa0-114">Élément multimédia System. ObjectThe qui a généré l’erreur.</span><span class="sxs-lookup"><span data-stu-id="26aa0-114">System.ObjectThe media item that raised the error.</span></span> <span data-ttu-id="26aa0-115">Vous pouvez effectuer un cast de ce en une interface IWMPMedia pour y accéder.</span><span class="sxs-lookup"><span data-stu-id="26aa0-115">You can cast this to an IWMPMedia interface to access it.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="26aa0-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="26aa0-116">Requirements</span></span>



| <span data-ttu-id="26aa0-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="26aa0-117">Requirement</span></span> | <span data-ttu-id="26aa0-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="26aa0-118">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="26aa0-119">Version</span><span class="sxs-lookup"><span data-stu-id="26aa0-119">Version</span></span><br/>   | <span data-ttu-id="26aa0-120">Lecteur Windows Media 11</span><span class="sxs-lookup"><span data-stu-id="26aa0-120">Windows Media Player 11</span></span><br/>                                                                                         |
| <span data-ttu-id="26aa0-121">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="26aa0-121">Namespace</span></span><br/> | <span data-ttu-id="26aa0-122">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="26aa0-122">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="26aa0-123">Assembly</span><span class="sxs-lookup"><span data-stu-id="26aa0-123">Assembly</span></span><br/>  | <dl> <span data-ttu-id="26aa0-124"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="26aa0-124"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="26aa0-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="26aa0-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="26aa0-126">**Objet AxWindowsMediaPlayer (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="26aa0-126">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="26aa0-127">**Interface IWMPCdromRip (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="26aa0-127">**IWMPCdromRip Interface (VB and C#)**</span></span>](iwmpcdromrip--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="26aa0-128">**Interface IWMPMedia (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="26aa0-128">**IWMPMedia Interface (VB and C#)**</span></span>](iwmpmedia--vb-and-c.md)
</dt> </dl>

 

 





