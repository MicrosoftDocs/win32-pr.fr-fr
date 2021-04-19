---
title: Événement CdromBurnError de l’objet AxWindowsMediaPlayer
description: L’événement CdromBurnError se produit lorsqu’une erreur générique se produit pendant une opération de gravure de CD.
ms.assetid: 512a3417-c8f3-42c7-ab2e-bea35cadbd4e
keywords:
- Événement CdromBurnError de l’objet AxWindowsMediaPlayer du lecteur Windows Media
topic_type:
- apiref
api_name:
- CdromBurnError Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c27969ea83089b225ba92eb93854fc1dcde9bde
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106531386"
---
# <a name="cdromburnerror-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="4dd0a-104">Événement CdromBurnError de l’objet AxWindowsMediaPlayer</span><span class="sxs-lookup"><span data-stu-id="4dd0a-104">CdromBurnError Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="4dd0a-105">L’événement CdromBurnError se produit lorsqu’une erreur générique se produit pendant une opération de gravure de CD.</span><span class="sxs-lookup"><span data-stu-id="4dd0a-105">The CdromBurnError event occurs when a generic error happens during a CD burning operation.</span></span>

``` syntax
[C#]
private void player_CdromBurnError(
  object sender,
  _WMPOCXEvents_CdromBurnErrorEvent e
)

[Visual Basic]
Private Sub player_CdromBurnError(  
  sender As Object,
  e As _WMPOCXEvents_CdromBurnErrorEvent
) Handles player.CdromBurnError
```

## <a name="event-data"></a><span data-ttu-id="4dd0a-106">Données d'événements</span><span class="sxs-lookup"><span data-stu-id="4dd0a-106">Event Data</span></span>

<span data-ttu-id="4dd0a-107">Le gestionnaire associé à cet événement est de type **AxWMPLib. \_ WMPOCXEvents \_ CdromBurnErrorEventHandler**.</span><span class="sxs-lookup"><span data-stu-id="4dd0a-107">The handler associated with this event is of type **AxWMPLib.\_WMPOCXEvents\_CdromBurnErrorEventHandler**.</span></span> <span data-ttu-id="4dd0a-108">Ce gestionnaire reçoit un argument de type **AxWMPLib. \_ WMPOCXEvents \_ CdromBurnErrorEvent**, qui contient les propriétés suivantes relatives à cet événement.</span><span class="sxs-lookup"><span data-stu-id="4dd0a-108">This handler receives an argument of type **AxWMPLib.\_WMPOCXEvents\_CdromBurnErrorEvent**, which contains the following properties related to this event.</span></span>



| <span data-ttu-id="4dd0a-109">Propriété</span><span class="sxs-lookup"><span data-stu-id="4dd0a-109">Property</span></span>   | <span data-ttu-id="4dd0a-110">Description</span><span class="sxs-lookup"><span data-stu-id="4dd0a-110">Description</span></span>                                                                                               |
|------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4dd0a-111">hrError</span><span class="sxs-lookup"><span data-stu-id="4dd0a-111">hrError</span></span>    | <span data-ttu-id="4dd0a-112">**System. Int32** Erreur qui a déclenché l’événement.</span><span class="sxs-lookup"><span data-stu-id="4dd0a-112">**System.Int32** The error that raised the event.</span></span><br/>                                               |
| <span data-ttu-id="4dd0a-113">pCdromBurn</span><span class="sxs-lookup"><span data-stu-id="4dd0a-113">pCdromBurn</span></span> | <span data-ttu-id="4dd0a-114">Interface WMPLib. IWMPCdromBurnThe qui représente l’opération de gravure qui a déclenché l’erreur.</span><span class="sxs-lookup"><span data-stu-id="4dd0a-114">WMPLib.IWMPCdromBurnThe interface that represents the burning operation that raised the error.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="4dd0a-115">Notes</span><span class="sxs-lookup"><span data-stu-id="4dd0a-115">Remarks</span></span>

<span data-ttu-id="4dd0a-116">Pour capturer les erreurs spécifiques au support, gérez le AxWMPLib. \_ \_Événement WMPOCXEvents CdromBurnMediaError.</span><span class="sxs-lookup"><span data-stu-id="4dd0a-116">To capture media specific errors, handle the AxWMPLib.\_WMPOCXEvents\_CdromBurnMediaError event.</span></span>

## <a name="requirements"></a><span data-ttu-id="4dd0a-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4dd0a-117">Requirements</span></span>



| <span data-ttu-id="4dd0a-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4dd0a-118">Requirement</span></span> | <span data-ttu-id="4dd0a-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="4dd0a-119">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4dd0a-120">Version</span><span class="sxs-lookup"><span data-stu-id="4dd0a-120">Version</span></span><br/>   | <span data-ttu-id="4dd0a-121">Lecteur Windows Media 11</span><span class="sxs-lookup"><span data-stu-id="4dd0a-121">Windows Media Player 11</span></span><br/>                                                                                         |
| <span data-ttu-id="4dd0a-122">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="4dd0a-122">Namespace</span></span><br/> | <span data-ttu-id="4dd0a-123">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="4dd0a-123">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="4dd0a-124">Assembly</span><span class="sxs-lookup"><span data-stu-id="4dd0a-124">Assembly</span></span><br/>  | <dl> <span data-ttu-id="4dd0a-125"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="4dd0a-125"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4dd0a-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4dd0a-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4dd0a-127">**Objet AxWindowsMediaPlayer (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="4dd0a-127">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="4dd0a-128">**Événement AxWindowsMediaPlayer. CdromBurnMediaError (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="4dd0a-128">**AxWindowsMediaPlayer.CdromBurnMediaError Event (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-cdromburnmediaerror.md)
</dt> <dt>

[<span data-ttu-id="4dd0a-129">**Interface IWMPCdromBurn (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="4dd0a-129">**IWMPCdromBurn Interface (VB and C#)**</span></span>](iwmpcdromburn--vb-and-c.md)
</dt> </dl>

 

 





