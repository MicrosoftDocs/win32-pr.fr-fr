---
title: Événement CdromRipStateChange de l’objet AxWindowsMediaPlayer
description: L’événement CdromRipStateChange se produit lorsqu’une opération d’extraction de CD change d’État.
ms.assetid: 0a0bd11f-a685-4c4e-8704-8eabe80d6f86
keywords:
- Événement CdromRipStateChange de l’objet AxWindowsMediaPlayer du lecteur Windows Media
topic_type:
- apiref
api_name:
- CdromRipStateChange Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 20fae9eb1fa6d5f65876e3f6758a7594f0bdbb19
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106542209"
---
# <a name="cdromripstatechange-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="44069-104">Événement CdromRipStateChange de l’objet AxWindowsMediaPlayer</span><span class="sxs-lookup"><span data-stu-id="44069-104">CdromRipStateChange Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="44069-105">L’événement CdromRipStateChange se produit lorsqu’une opération d’extraction de CD change d’État.</span><span class="sxs-lookup"><span data-stu-id="44069-105">The CdromRipStateChange event occurs when a CD ripping operation changes state.</span></span>

``` syntax
[C#]
private void player_CdromRipStateChange(
  object sender,
  _WMPOCXEvents_CdromRipStateChangeEvent e
)

[Visual Basic]
Private Sub player_CdromRipStateChange(  
  sender As Object,
  e As _WMPOCXEvents_CdromRipStateChangeEvent
) Handles player.CdromRipStateChange
```

## <a name="event-data"></a><span data-ttu-id="44069-106">Données d'événements</span><span class="sxs-lookup"><span data-stu-id="44069-106">Event Data</span></span>

<span data-ttu-id="44069-107">Le gestionnaire associé à cet événement est de type **AxWMPLib. \_ WMPOCXEvents \_ CdromRipStateChangeEventHandler**.</span><span class="sxs-lookup"><span data-stu-id="44069-107">The handler associated with this event is of type **AxWMPLib.\_WMPOCXEvents\_CdromRipStateChangeEventHandler**.</span></span> <span data-ttu-id="44069-108">Ce gestionnaire reçoit un argument de type **AxWMPLib. \_ WMPOCXEvents \_ CdromRipStateChangeEvent**, qui contient les propriétés suivantes relatives à cet événement.</span><span class="sxs-lookup"><span data-stu-id="44069-108">This handler receives an argument of type **AxWMPLib.\_WMPOCXEvents\_CdromRipStateChangeEvent**, which contains the following properties related to this event.</span></span>



| <span data-ttu-id="44069-109">Propriété</span><span class="sxs-lookup"><span data-stu-id="44069-109">Property</span></span>  | <span data-ttu-id="44069-110">Description</span><span class="sxs-lookup"><span data-stu-id="44069-110">Description</span></span>                                                                                              |
|-----------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="44069-111">pCdromRip</span><span class="sxs-lookup"><span data-stu-id="44069-111">pCdromRip</span></span> | <span data-ttu-id="44069-112">Interface WMPLib. IWMPCdromRipThe qui représente l’opération d’extraction qui a déclenché l’erreur.</span><span class="sxs-lookup"><span data-stu-id="44069-112">WMPLib.IWMPCdromRipThe interface that represents the ripping operation that raised the error.</span></span><br/> |
| <span data-ttu-id="44069-113">wmprs</span><span class="sxs-lookup"><span data-stu-id="44069-113">wmprs</span></span>     | <span data-ttu-id="44069-114">Valeur d’énumération WMPLib. WMPRipStateThe qui indique le nouvel État.</span><span class="sxs-lookup"><span data-stu-id="44069-114">WMPLib.WMPRipStateThe enumeration value that indicates the new state.</span></span><br/>                         |



 

## <a name="requirements"></a><span data-ttu-id="44069-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="44069-115">Requirements</span></span>



| <span data-ttu-id="44069-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="44069-116">Requirement</span></span> | <span data-ttu-id="44069-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="44069-117">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="44069-118">Version</span><span class="sxs-lookup"><span data-stu-id="44069-118">Version</span></span><br/>   | <span data-ttu-id="44069-119">Lecteur Windows Media 11</span><span class="sxs-lookup"><span data-stu-id="44069-119">Windows Media Player 11</span></span><br/>                                                                                         |
| <span data-ttu-id="44069-120">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="44069-120">Namespace</span></span><br/> | <span data-ttu-id="44069-121">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="44069-121">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="44069-122">Assembly</span><span class="sxs-lookup"><span data-stu-id="44069-122">Assembly</span></span><br/>  | <dl> <span data-ttu-id="44069-123"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="44069-123"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="44069-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="44069-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="44069-125">**Objet AxWindowsMediaPlayer (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="44069-125">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="44069-126">**Interface IWMPCdromRip (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="44069-126">**IWMPCdromRip Interface (VB and C#)**</span></span>](iwmpcdromrip--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="44069-127">**WMPRipState**</span><span class="sxs-lookup"><span data-stu-id="44069-127">**WMPRipState**</span></span>](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpripstate)
</dt> </dl>

 

 





