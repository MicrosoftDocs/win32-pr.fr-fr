---
title: Événement Disconnect de l’objet AxWindowsMediaPlayer
description: L’événement Disconnect est réservé pour une utilisation ultérieure.
ms.assetid: 3baecc6c-e772-4269-96c1-900be270543e
keywords:
- Événement Disconnect de l’objet AxWindowsMediaPlayer lecteur Windows Media
topic_type:
- apiref
api_name:
- Disconnect Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 89dffe3191efeddba74eb22c7c5c72b8c52bc095
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106523912"
---
# <a name="disconnect-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="a7549-104">Événement Disconnect de l’objet AxWindowsMediaPlayer</span><span class="sxs-lookup"><span data-stu-id="a7549-104">Disconnect Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="a7549-105">L’événement Disconnect est réservé pour une utilisation ultérieure.</span><span class="sxs-lookup"><span data-stu-id="a7549-105">The Disconnect event is reserved for future use.</span></span>

``` syntax
[C#]
private void player_Disconnect(
  object sender,
  _WMPOCXEvents_DisconnectEvent e
)

[Visual Basic]
Private Sub player_Disconnect(  
  sender As Object,
  e As _WMPOCXEvents_DisconnectEvent
) Handles player.Disconnect
```

## <a name="event-data"></a><span data-ttu-id="a7549-106">Données d'événements</span><span class="sxs-lookup"><span data-stu-id="a7549-106">Event Data</span></span>

<span data-ttu-id="a7549-107">Le gestionnaire associé à cet événement est de type **AxWMPLib. \_ WMPOCXEvents \_ DisconnectEventHandler**.</span><span class="sxs-lookup"><span data-stu-id="a7549-107">The handler associated with this event is of type **AxWMPLib.\_WMPOCXEvents\_DisconnectEventHandler**.</span></span> <span data-ttu-id="a7549-108">Ce gestionnaire reçoit un argument de type **AxWMPLib. \_ WMPOCXEvents \_ DisconnectEvent**, qui contient la propriété suivante associée à cet événement.</span><span class="sxs-lookup"><span data-stu-id="a7549-108">This handler receives an argument of type **AxWMPLib.\_WMPOCXEvents\_DisconnectEvent**, which contains the following property related to this event.</span></span>



| <span data-ttu-id="a7549-109">Propriété</span><span class="sxs-lookup"><span data-stu-id="a7549-109">Property</span></span> | <span data-ttu-id="a7549-110">Description</span><span class="sxs-lookup"><span data-stu-id="a7549-110">Description</span></span>                               |
|----------|-------------------------------------------|
| <span data-ttu-id="a7549-111">result</span><span class="sxs-lookup"><span data-stu-id="a7549-111">result</span></span>   | <span data-ttu-id="a7549-112">**System. Int32** Non pris en charge.</span><span class="sxs-lookup"><span data-stu-id="a7549-112">**System.Int32** Not supported.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="a7549-113">Notes</span><span class="sxs-lookup"><span data-stu-id="a7549-113">Remarks</span></span>

<span data-ttu-id="a7549-114">Cet événement est réservé à une utilisation ultérieure.</span><span class="sxs-lookup"><span data-stu-id="a7549-114">This event is reserved for future use.</span></span>

## <a name="requirements"></a><span data-ttu-id="a7549-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a7549-115">Requirements</span></span>



| <span data-ttu-id="a7549-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a7549-116">Requirement</span></span> | <span data-ttu-id="a7549-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="a7549-117">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a7549-118">Version</span><span class="sxs-lookup"><span data-stu-id="a7549-118">Version</span></span><br/>   | <span data-ttu-id="a7549-119">Lecteur Windows Media série 9 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="a7549-119">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="a7549-120">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="a7549-120">Namespace</span></span><br/> | <span data-ttu-id="a7549-121">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="a7549-121">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="a7549-122">Assembly</span><span class="sxs-lookup"><span data-stu-id="a7549-122">Assembly</span></span><br/>  | <dl> <span data-ttu-id="a7549-123"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="a7549-123"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a7549-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a7549-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a7549-125">**Objet AxWindowsMediaPlayer (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="a7549-125">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> </dl>

 

 





