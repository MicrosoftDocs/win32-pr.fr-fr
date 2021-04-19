---
title: Événement CdromBurnStateChange de l’objet AxWindowsMediaPlayer
description: L’événement CdromBurnStateChange se produit lorsqu’une opération de gravure de CD change d’État.
ms.assetid: fec8a8e5-e282-454e-9713-fd9bb131df6a
keywords:
- Événement CdromBurnStateChange de l’objet AxWindowsMediaPlayer du lecteur Windows Media
topic_type:
- apiref
api_name:
- CdromBurnStateChange Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc679a96600bff5aa4ca805018d364a6aeea8174
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528590"
---
# <a name="cdromburnstatechange-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="4294a-104">Événement CdromBurnStateChange de l’objet AxWindowsMediaPlayer</span><span class="sxs-lookup"><span data-stu-id="4294a-104">CdromBurnStateChange Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="4294a-105">L’événement CdromBurnStateChange se produit lorsqu’une opération de gravure de CD change d’État.</span><span class="sxs-lookup"><span data-stu-id="4294a-105">The CdromBurnStateChange event occurs when a CD burning operation changes state.</span></span>

``` syntax
[C#]
private void player_CdromBurnStateChange(
  object sender,
  _WMPOCXEvents_CdromBurnStateChangeEvent e
)

[Visual Basic]
Private Sub player_CdromBurnStateChange(  
  sender As Object,
  e As _WMPOCXEvents_CdromBurnStateChangeEvent
) Handles player.CdromBurnStateChange
```

## <a name="event-data"></a><span data-ttu-id="4294a-106">Données d'événements</span><span class="sxs-lookup"><span data-stu-id="4294a-106">Event Data</span></span>

<span data-ttu-id="4294a-107">Le gestionnaire associé à cet événement est de type **AxWMPLib. \_ WMPOCXEvents \_ CdromBurnStateChangeEventHandler**.</span><span class="sxs-lookup"><span data-stu-id="4294a-107">The handler associated with this event is of type **AxWMPLib.\_WMPOCXEvents\_CdromBurnStateChangeEventHandler**.</span></span> <span data-ttu-id="4294a-108">Ce gestionnaire reçoit un argument de type **AxWMPLib. \_ WMPOCXEvents \_ CdromBurnStateChangeEvent**, qui contient les propriétés suivantes relatives à cet événement.</span><span class="sxs-lookup"><span data-stu-id="4294a-108">This handler receives an argument of type **AxWMPLib.\_WMPOCXEvents\_CdromBurnStateChangeEvent**, which contains the following properties related to this event.</span></span>



| <span data-ttu-id="4294a-109">Propriété</span><span class="sxs-lookup"><span data-stu-id="4294a-109">Property</span></span>   | <span data-ttu-id="4294a-110">Description</span><span class="sxs-lookup"><span data-stu-id="4294a-110">Description</span></span>                                                                                               |
|------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4294a-111">pCdromBurn</span><span class="sxs-lookup"><span data-stu-id="4294a-111">pCdromBurn</span></span> | <span data-ttu-id="4294a-112">Interface WMPLib. IWMPCdromBurnThe qui représente l’opération de gravure qui a déclenché l’erreur.</span><span class="sxs-lookup"><span data-stu-id="4294a-112">WMPLib.IWMPCdromBurnThe interface that represents the burning operation that raised the error.</span></span><br/> |
| <span data-ttu-id="4294a-113">wmpbs</span><span class="sxs-lookup"><span data-stu-id="4294a-113">wmpbs</span></span>      | <span data-ttu-id="4294a-114">Valeur d’énumération WMPLib. WMPBurnStateThe qui indique le nouvel État.</span><span class="sxs-lookup"><span data-stu-id="4294a-114">WMPLib.WMPBurnStateThe enumeration value that indicates the new state.</span></span><br/>                         |



 

## <a name="requirements"></a><span data-ttu-id="4294a-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4294a-115">Requirements</span></span>



| <span data-ttu-id="4294a-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4294a-116">Requirement</span></span> | <span data-ttu-id="4294a-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="4294a-117">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4294a-118">Version</span><span class="sxs-lookup"><span data-stu-id="4294a-118">Version</span></span><br/>   | <span data-ttu-id="4294a-119">Lecteur Windows Media 11</span><span class="sxs-lookup"><span data-stu-id="4294a-119">Windows Media Player 11</span></span><br/>                                                                                         |
| <span data-ttu-id="4294a-120">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="4294a-120">Namespace</span></span><br/> | <span data-ttu-id="4294a-121">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="4294a-121">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="4294a-122">Assembly</span><span class="sxs-lookup"><span data-stu-id="4294a-122">Assembly</span></span><br/>  | <dl> <span data-ttu-id="4294a-123"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="4294a-123"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4294a-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4294a-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4294a-125">**Objet AxWindowsMediaPlayer (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="4294a-125">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="4294a-126">**Interface IWMPCdromBurn (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="4294a-126">**IWMPCdromBurn Interface (VB and C#)**</span></span>](iwmpcdromburn--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="4294a-127">**WMPBurnState**</span><span class="sxs-lookup"><span data-stu-id="4294a-127">**WMPBurnState**</span></span>](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpburnstate)
</dt> </dl>

 

 





