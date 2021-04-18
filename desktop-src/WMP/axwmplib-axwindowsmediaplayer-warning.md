---
title: Événement Warning de l’objet AxWindowsMediaPlayer
description: L’événement d’avertissement est réservé à une utilisation ultérieure.
ms.assetid: 3de63756-2726-4864-8988-fd614f23bcad
keywords:
- Événement d’avertissement de l’objet AxWindowsMediaPlayer lecteur Windows Media
topic_type:
- apiref
api_name:
- Warning Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2a868ba7f619287cd96929c62d89dee3555d908b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526802"
---
# <a name="warning-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="41cbb-104">Événement Warning de l’objet AxWindowsMediaPlayer</span><span class="sxs-lookup"><span data-stu-id="41cbb-104">Warning Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="41cbb-105">L’événement d’avertissement est réservé à une utilisation ultérieure.</span><span class="sxs-lookup"><span data-stu-id="41cbb-105">The Warning event is reserved for future use.</span></span>

``` syntax
[C#]
private void player_Warning(
  object sender,
  _WMPOCXEvents_WarningEvent e
)

[Visual Basic]
Private Sub player_Warning(
  sender As Object,
  e As _WMPOCXEvents_WarningEvent
) Handles player.Warning
```

## <a name="event-data"></a><span data-ttu-id="41cbb-106">Données d'événements</span><span class="sxs-lookup"><span data-stu-id="41cbb-106">Event Data</span></span>

<span data-ttu-id="41cbb-107">Le gestionnaire associé à cet événement est de type **AxWMPLib. \_ WMPOCXEvents \_ WarningEventHandler**.</span><span class="sxs-lookup"><span data-stu-id="41cbb-107">The handler associated with this event is of type **AxWMPLib.\_WMPOCXEvents\_WarningEventHandler**.</span></span> <span data-ttu-id="41cbb-108">Ce gestionnaire reçoit un argument de type **AxWMPLib. \_ WMPOCXEvents \_ WarningEvent**, qui contient les propriétés suivantes relatives à cet événement.</span><span class="sxs-lookup"><span data-stu-id="41cbb-108">This handler receives an argument of type **AxWMPLib.\_WMPOCXEvents\_WarningEvent**, which contains the following properties related to this event.</span></span>



| <span data-ttu-id="41cbb-109">Propriété</span><span class="sxs-lookup"><span data-stu-id="41cbb-109">Property</span></span>    | <span data-ttu-id="41cbb-110">Description</span><span class="sxs-lookup"><span data-stu-id="41cbb-110">Description</span></span>                                |
|-------------|--------------------------------------------|
| <span data-ttu-id="41cbb-111">warningType</span><span class="sxs-lookup"><span data-stu-id="41cbb-111">warningType</span></span> | <span data-ttu-id="41cbb-112">**System. Int32** Non pris en charge.</span><span class="sxs-lookup"><span data-stu-id="41cbb-112">**System.Int32** Not supported.</span></span><br/>  |
| <span data-ttu-id="41cbb-113">param</span><span class="sxs-lookup"><span data-stu-id="41cbb-113">param</span></span>       | <span data-ttu-id="41cbb-114">**System. Int32** Non pris en charge.</span><span class="sxs-lookup"><span data-stu-id="41cbb-114">**System.Int32** Not supported.</span></span><br/>  |
| <span data-ttu-id="41cbb-115">description</span><span class="sxs-lookup"><span data-stu-id="41cbb-115">description</span></span> | <span data-ttu-id="41cbb-116">**System. String** Non pris en charge.</span><span class="sxs-lookup"><span data-stu-id="41cbb-116">**System.String** Not supported.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="41cbb-117">Notes</span><span class="sxs-lookup"><span data-stu-id="41cbb-117">Remarks</span></span>

<span data-ttu-id="41cbb-118">Cet événement est réservé à une utilisation ultérieure.</span><span class="sxs-lookup"><span data-stu-id="41cbb-118">This event is reserved for future use.</span></span>

## <a name="requirements"></a><span data-ttu-id="41cbb-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="41cbb-119">Requirements</span></span>



| <span data-ttu-id="41cbb-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="41cbb-120">Requirement</span></span> | <span data-ttu-id="41cbb-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="41cbb-121">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="41cbb-122">Version</span><span class="sxs-lookup"><span data-stu-id="41cbb-122">Version</span></span><br/>   | <span data-ttu-id="41cbb-123">Lecteur Windows Media série 9 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="41cbb-123">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="41cbb-124">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="41cbb-124">Namespace</span></span><br/> | <span data-ttu-id="41cbb-125">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="41cbb-125">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="41cbb-126">Assembly</span><span class="sxs-lookup"><span data-stu-id="41cbb-126">Assembly</span></span><br/>  | <dl> <span data-ttu-id="41cbb-127"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="41cbb-127"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="41cbb-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="41cbb-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="41cbb-129">**Objet AxWindowsMediaPlayer (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="41cbb-129">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> </dl>

 

 





