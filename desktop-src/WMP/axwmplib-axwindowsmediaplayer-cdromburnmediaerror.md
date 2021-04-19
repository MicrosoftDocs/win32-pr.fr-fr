---
title: Événement CdromBurnMediaError de l’objet AxWindowsMediaPlayer
description: L’événement CdromBurnMediaError se produit lorsqu’une erreur se produit lors de la gravure d’un élément multimédia individuel sur un CD.
ms.assetid: 0847a8a2-1fef-41a0-affb-9fa6bd10b925
keywords:
- Événement CdromBurnMediaError de l’objet AxWindowsMediaPlayer du lecteur Windows Media
topic_type:
- apiref
api_name:
- CdromBurnMediaError Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9d9fac8902fe8700171d2c909e8140c74c8cc3c8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106522409"
---
# <a name="cdromburnmediaerror-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="ed5d7-104">Événement CdromBurnMediaError de l’objet AxWindowsMediaPlayer</span><span class="sxs-lookup"><span data-stu-id="ed5d7-104">CdromBurnMediaError Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="ed5d7-105">L’événement CdromBurnMediaError se produit lorsqu’une erreur se produit lors de la gravure d’un élément multimédia individuel sur un CD.</span><span class="sxs-lookup"><span data-stu-id="ed5d7-105">The CdromBurnMediaError event occurs when an error happens while burning an individual media item to a CD.</span></span>

``` syntax
[C#]
private void player_CdromBurnMediaError(
  object sender,
  _WMPOCXEvents_CdromBurnMediaErrorEvent e
)

[Visual Basic]
Private Sub player_CdromBurnMediaError(
  sender As Object,
  e As _WMPOCXEvents_CdromBurnMediaErrorEvent
) Handles player.CdromBurnMediaError
```

## <a name="event-data"></a><span data-ttu-id="ed5d7-106">Données d'événements</span><span class="sxs-lookup"><span data-stu-id="ed5d7-106">Event Data</span></span>

<span data-ttu-id="ed5d7-107">Le gestionnaire associé à cet événement est de type **AxWMPLib. \_ WMPOCXEvents \_ CdromBurnMediaErrorEventHandler**.</span><span class="sxs-lookup"><span data-stu-id="ed5d7-107">The handler associated with this event is of type **AxWMPLib.\_WMPOCXEvents\_CdromBurnMediaErrorEventHandler**.</span></span> <span data-ttu-id="ed5d7-108">Ce gestionnaire reçoit un argument de type **AxWMPLib. \_ WMPOCXEvents \_ CdromBurnMediaErrorEvent**, qui contient les propriétés suivantes relatives à cet événement.</span><span class="sxs-lookup"><span data-stu-id="ed5d7-108">This handler receives an argument of type **AxWMPLib.\_WMPOCXEvents\_CdromBurnMediaErrorEvent**, which contains the following properties related to this event.</span></span>



| <span data-ttu-id="ed5d7-109">Propriété</span><span class="sxs-lookup"><span data-stu-id="ed5d7-109">Property</span></span>   | <span data-ttu-id="ed5d7-110">Description</span><span class="sxs-lookup"><span data-stu-id="ed5d7-110">Description</span></span>                                                                                                             |
|------------|-------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ed5d7-111">pCdromBurn</span><span class="sxs-lookup"><span data-stu-id="ed5d7-111">pCdromBurn</span></span> | <span data-ttu-id="ed5d7-112">Interface WMPLib. IWMPCdromBurnThe qui représente l’opération de gravure qui a déclenché l’erreur.</span><span class="sxs-lookup"><span data-stu-id="ed5d7-112">WMPLib.IWMPCdromBurnThe interface that represents the burning operation that raised the error.</span></span><br/>               |
| <span data-ttu-id="ed5d7-113">pMedia</span><span class="sxs-lookup"><span data-stu-id="ed5d7-113">pMedia</span></span>     | <span data-ttu-id="ed5d7-114">Élément multimédia System. ObjectThe qui a généré l’erreur.</span><span class="sxs-lookup"><span data-stu-id="ed5d7-114">System.ObjectThe media item that raised the error.</span></span> <span data-ttu-id="ed5d7-115">Vous pouvez effectuer un cast de ce en une interface IWMPMedia pour y accéder.</span><span class="sxs-lookup"><span data-stu-id="ed5d7-115">You can cast this to an IWMPMedia interface to access it.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="ed5d7-116">Notes</span><span class="sxs-lookup"><span data-stu-id="ed5d7-116">Remarks</span></span>

<span data-ttu-id="ed5d7-117">Pour capturer des erreurs génériques, gérez AxWMPLib. \_ \_Événement WMPOCXEvents CdromBurnError.</span><span class="sxs-lookup"><span data-stu-id="ed5d7-117">To capture generic errors, handle the AxWMPLib.\_WMPOCXEvents\_CdromBurnError event.</span></span>

## <a name="requirements"></a><span data-ttu-id="ed5d7-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ed5d7-118">Requirements</span></span>



| <span data-ttu-id="ed5d7-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ed5d7-119">Requirement</span></span> | <span data-ttu-id="ed5d7-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="ed5d7-120">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ed5d7-121">Version</span><span class="sxs-lookup"><span data-stu-id="ed5d7-121">Version</span></span><br/>   | <span data-ttu-id="ed5d7-122">Lecteur Windows Media 11</span><span class="sxs-lookup"><span data-stu-id="ed5d7-122">Windows Media Player 11</span></span><br/>                                                                                         |
| <span data-ttu-id="ed5d7-123">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="ed5d7-123">Namespace</span></span><br/> | <span data-ttu-id="ed5d7-124">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="ed5d7-124">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="ed5d7-125">Assembly</span><span class="sxs-lookup"><span data-stu-id="ed5d7-125">Assembly</span></span><br/>  | <dl> <span data-ttu-id="ed5d7-126"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="ed5d7-126"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ed5d7-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ed5d7-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ed5d7-128">**Objet AxWindowsMediaPlayer (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="ed5d7-128">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="ed5d7-129">**Événement AxWindowsMediaPlayer. CdromBurnError (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="ed5d7-129">**AxWindowsMediaPlayer.CdromBurnError Event (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-cdromburnerror.md)
</dt> <dt>

[<span data-ttu-id="ed5d7-130">**Interface IWMPCdromBurn (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="ed5d7-130">**IWMPCdromBurn Interface (VB and C#)**</span></span>](iwmpcdromburn--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="ed5d7-131">**Interface IWMPMedia (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="ed5d7-131">**IWMPMedia Interface (VB and C#)**</span></span>](iwmpmedia--vb-and-c.md)
</dt> </dl>

 

 





