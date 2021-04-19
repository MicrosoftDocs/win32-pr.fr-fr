---
title: Événement de mise en mémoire tampon de l’objet AxWindowsMediaPlayer
description: L’événement de mise en mémoire tampon se produit lorsque le contrôle du lecteur Windows Media démarre ou termine la mise en mémoire tampon ou le téléchargement. | Événement de mise en mémoire tampon de l’objet AxWindowsMediaPlayer
ms.assetid: ad152c4d-1c91-4da1-bec0-46f89f3b8c79
keywords:
- Événement de mise en mémoire tampon de l’objet AxWindowsMediaPlayer lecteur Windows Media
topic_type:
- apiref
api_name:
- Buffering Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: af595443d78a311510df6a7e06b2e716da22ecae
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106530940"
---
# <a name="buffering-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="caf2e-105">Événement de mise en mémoire tampon de l’objet AxWindowsMediaPlayer</span><span class="sxs-lookup"><span data-stu-id="caf2e-105">Buffering Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="caf2e-106">L’événement de mise en mémoire tampon se produit lorsque le contrôle du lecteur Windows Media démarre ou termine la mise en mémoire tampon ou le téléchargement.</span><span class="sxs-lookup"><span data-stu-id="caf2e-106">The Buffering event occurs when the Windows Media Player control begins or ends buffering or downloading.</span></span>

``` syntax
[C#]
private void player_Buffering(
  object sender,
  _WMPOCXEvents_BufferingEvent e
)

[Visual Basic]
Private Sub player_Buffering(
  sender As Object,
  e As _WMPOCXEvents_BufferingEvent
) Handles player.Buffering
```

## <a name="event-data"></a><span data-ttu-id="caf2e-107">Données d'événements</span><span class="sxs-lookup"><span data-stu-id="caf2e-107">Event Data</span></span>

<span data-ttu-id="caf2e-108">Le gestionnaire associé à cet événement est de type **AxWMPLib. \_ WMPOCXEvents \_ BufferingEventHandler**.</span><span class="sxs-lookup"><span data-stu-id="caf2e-108">The handler associated with this event is of type **AxWMPLib.\_WMPOCXEvents\_BufferingEventHandler**.</span></span> <span data-ttu-id="caf2e-109">Ce gestionnaire reçoit un argument de type **AxWMPLib. \_ WMPOCXEvents \_ BufferingEvent**, qui contient la propriété suivante associée à cet événement.</span><span class="sxs-lookup"><span data-stu-id="caf2e-109">This handler receives an argument of type **AxWMPLib.\_WMPOCXEvents\_BufferingEvent**, which contains the following property related to this event.</span></span>



| <span data-ttu-id="caf2e-110">Propriété</span><span class="sxs-lookup"><span data-stu-id="caf2e-110">Property</span></span> | <span data-ttu-id="caf2e-111">Description</span><span class="sxs-lookup"><span data-stu-id="caf2e-111">Description</span></span>                                                                                                                                                         |
|----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="caf2e-112">Démarrer</span><span class="sxs-lookup"><span data-stu-id="caf2e-112">Start</span></span>    | <span data-ttu-id="caf2e-113">System. BooleanSpecifies indique si la mise en mémoire tampon a commencé ou s’est terminée.</span><span class="sxs-lookup"><span data-stu-id="caf2e-113">System.BooleanSpecifies whether buffering has begun or ended.</span></span> <span data-ttu-id="caf2e-114">La valeur true indique qu’elle a commencé ; la valeur false indique qu’elle est terminée.</span><span class="sxs-lookup"><span data-stu-id="caf2e-114">A value of true indicates that it has begun; a value of false indicates that it has ended.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="caf2e-115">Notes</span><span class="sxs-lookup"><span data-stu-id="caf2e-115">Remarks</span></span>

<span data-ttu-id="caf2e-116">Utilisez cet événement pour déterminer quand la mise en mémoire tampon ou le téléchargement démarre ou s’arrête.</span><span class="sxs-lookup"><span data-stu-id="caf2e-116">Use this event to determine when buffering or downloading starts or stops.</span></span> <span data-ttu-id="caf2e-117">Vous pouvez utiliser le même bloc d’événements pour les cas et les *IWMPNetwork* de test. **bufferingProgress** et *IWMPNetwork*. **downloadProgress** pour déterminer si le lecteur Windows Media met actuellement en mémoire tampon ou télécharge le contenu.</span><span class="sxs-lookup"><span data-stu-id="caf2e-117">You can use the same event block for both cases and test *IWMPNetwork*.**bufferingProgress** and *IWMPNetwork*.**downloadProgress** to determine whether Windows Media Player is currently buffering or downloading content.</span></span>

## <a name="requirements"></a><span data-ttu-id="caf2e-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="caf2e-118">Requirements</span></span>



| <span data-ttu-id="caf2e-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="caf2e-119">Requirement</span></span> | <span data-ttu-id="caf2e-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="caf2e-120">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="caf2e-121">Version</span><span class="sxs-lookup"><span data-stu-id="caf2e-121">Version</span></span><br/>   | <span data-ttu-id="caf2e-122">Lecteur Windows Media série 9 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="caf2e-122">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="caf2e-123">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="caf2e-123">Namespace</span></span><br/> | <span data-ttu-id="caf2e-124">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="caf2e-124">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="caf2e-125">Assembly</span><span class="sxs-lookup"><span data-stu-id="caf2e-125">Assembly</span></span><br/>  | <dl> <span data-ttu-id="caf2e-126"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="caf2e-126"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="caf2e-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="caf2e-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="caf2e-128">**Objet AxWindowsMediaPlayer (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="caf2e-128">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="caf2e-129">**IWMPNetwork. bufferingProgress (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="caf2e-129">**IWMPNetwork.bufferingProgress (VB and C#)**</span></span>](wmplibiwmpnetwork-iwmpnetwork-bufferingprogress--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="caf2e-130">**IWMPNetwork. downloadProgress (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="caf2e-130">**IWMPNetwork.downloadProgress (VB and C#)**</span></span>](wmplibiwmpnetwork-iwmpnetwork-downloadprogress--vb-and-c.md)
</dt> </dl>

 

 





