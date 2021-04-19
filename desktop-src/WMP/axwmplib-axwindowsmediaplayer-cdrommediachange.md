---
title: Événement CdromMediaChange de l’objet AxWindowsMediaPlayer
description: L’événement CdromMediaChange se produit lorsqu’un CD ou un DVD est inséré ou éjecté d’un lecteur de CD ou DVD. | Événement CdromMediaChange de l’objet AxWindowsMediaPlayer
ms.assetid: 0a6378c1-59e4-4be3-8764-d5c4ab478b6c
keywords:
- Événement CdromMediaChange de l’objet AxWindowsMediaPlayer du lecteur Windows Media
topic_type:
- apiref
api_name:
- CdromMediaChange Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 35385541f6bc91b6935f148fd8ae28df6a415f3d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106525917"
---
# <a name="cdrommediachange-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="b8602-105">Événement CdromMediaChange de l’objet AxWindowsMediaPlayer</span><span class="sxs-lookup"><span data-stu-id="b8602-105">CdromMediaChange Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="b8602-106">L’événement **CdromMediaChange** se produit lorsqu’un CD ou un DVD est inséré ou éjecté d’un lecteur de CD ou DVD.</span><span class="sxs-lookup"><span data-stu-id="b8602-106">The **CdromMediaChange** event occurs when a CD or DVD is inserted into or ejected from a CD or DVD drive.</span></span>

``` syntax
[C#]
private void player_CdromMediaChange(
  object sender,
  _WMPOCXEvents_CdromMediaChangeEvent e
)

[Visual Basic]
Private Sub player_CdromMediaChange(  
  sender As Object,
  e As _WMPOCXEvents_CdromMediaChangeEvent
) Handles player.CdromMediaChange
```

## <a name="event-data"></a><span data-ttu-id="b8602-107">Données d'événements</span><span class="sxs-lookup"><span data-stu-id="b8602-107">Event Data</span></span>

<span data-ttu-id="b8602-108">Le gestionnaire associé à cet événement est de type **AxWMPLib. \_ WMPOCXEvents \_ CdromMediaChangeEventHandler**.</span><span class="sxs-lookup"><span data-stu-id="b8602-108">The handler associated with this event is of type **AxWMPLib.\_WMPOCXEvents\_CdromMediaChangeEventHandler**.</span></span> <span data-ttu-id="b8602-109">Ce gestionnaire reçoit un argument de type **AxWMPLib. \_ WMPOCXEvents \_ CdromMediaChangeEvent**, qui contient la propriété suivante associée à cet événement.</span><span class="sxs-lookup"><span data-stu-id="b8602-109">This handler receives an argument of type **AxWMPLib.\_WMPOCXEvents\_CdromMediaChangeEvent**, which contains the following property related to this event.</span></span>



| <span data-ttu-id="b8602-110">Propriété</span><span class="sxs-lookup"><span data-stu-id="b8602-110">Property</span></span> | <span data-ttu-id="b8602-111">Description</span><span class="sxs-lookup"><span data-stu-id="b8602-111">Description</span></span>                                                        |
|----------|--------------------------------------------------------------------|
| <span data-ttu-id="b8602-112">CdromNum</span><span class="sxs-lookup"><span data-stu-id="b8602-112">CdromNum</span></span> | <span data-ttu-id="b8602-113">System. Int32Specifies l’index du lecteur de CD ou de DVD.</span><span class="sxs-lookup"><span data-stu-id="b8602-113">System.Int32Specifies the index of the CD or DVD drive.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="b8602-114">Notes</span><span class="sxs-lookup"><span data-stu-id="b8602-114">Remarks</span></span>

<span data-ttu-id="b8602-115">L’index du lecteur de CD correspond à l’index d’une interface IWMPCdrom accessible via l’interface IWMPCdromCollection.</span><span class="sxs-lookup"><span data-stu-id="b8602-115">The index of the CD drive corresponds to the index of an IWMPCdrom interface accessible through the IWMPCdromCollection interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="b8602-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b8602-116">Requirements</span></span>



| <span data-ttu-id="b8602-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b8602-117">Requirement</span></span> | <span data-ttu-id="b8602-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="b8602-118">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b8602-119">Version</span><span class="sxs-lookup"><span data-stu-id="b8602-119">Version</span></span><br/>   | <span data-ttu-id="b8602-120">Lecteur Windows Media série 9 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="b8602-120">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="b8602-121">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="b8602-121">Namespace</span></span><br/> | <span data-ttu-id="b8602-122">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="b8602-122">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="b8602-123">Assembly</span><span class="sxs-lookup"><span data-stu-id="b8602-123">Assembly</span></span><br/>  | <dl> <span data-ttu-id="b8602-124"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="b8602-124"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b8602-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b8602-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b8602-126">**Objet AxWindowsMediaPlayer (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="b8602-126">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="b8602-127">**Interface IWMPCdrom (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="b8602-127">**IWMPCdrom Interface (VB and C#)**</span></span>](iwmpcdrom--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="b8602-128">**Interface IWMPCdromCollection (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="b8602-128">**IWMPCdromCollection Interface (VB and C#)**</span></span>](iwmpcdromcollection--vb-and-c.md)
</dt> </dl>

 

 





