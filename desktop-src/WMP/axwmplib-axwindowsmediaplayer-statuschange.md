---
title: Événement StatusChange de l’objet AxWindowsMediaPlayer
description: L’événement StatusChange se produit lorsque la propriété Status change de valeur. | Événement StatusChange de l’objet AxWindowsMediaPlayer
ms.assetid: 5295fccb-7be0-46d3-85ba-b481e575d393
keywords:
- Événement StatusChange de l’objet AxWindowsMediaPlayer du lecteur Windows Media
topic_type:
- apiref
api_name:
- StatusChange Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d3ef3224afadb1f98a3067913a8beb095d4e46e5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106524022"
---
# <a name="statuschange-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="45fda-105">Événement StatusChange de l’objet AxWindowsMediaPlayer</span><span class="sxs-lookup"><span data-stu-id="45fda-105">StatusChange Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="45fda-106">L’événement **statuschange** se produit lorsque la propriété **Status** change de valeur.</span><span class="sxs-lookup"><span data-stu-id="45fda-106">The **StatusChange** event occurs when the **status** property changes value.</span></span>

``` syntax
[C#]
private void player_StatusChange(
  object sender,
  System.EventArgs e
)

[Visual Basic]
Private Sub player_StatusChange(
  sender As Object,
  e As System.EventArgs
) Handles player.StatusChange
```

## <a name="event-data"></a><span data-ttu-id="45fda-107">Données d'événements</span><span class="sxs-lookup"><span data-stu-id="45fda-107">Event Data</span></span>

<span data-ttu-id="45fda-108">Cet événement ne contient pas de données.</span><span class="sxs-lookup"><span data-stu-id="45fda-108">This event does not contain data.</span></span>

## <a name="requirements"></a><span data-ttu-id="45fda-109">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="45fda-109">Requirements</span></span>



| <span data-ttu-id="45fda-110">Condition requise</span><span class="sxs-lookup"><span data-stu-id="45fda-110">Requirement</span></span> | <span data-ttu-id="45fda-111">Valeur</span><span class="sxs-lookup"><span data-stu-id="45fda-111">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="45fda-112">Version</span><span class="sxs-lookup"><span data-stu-id="45fda-112">Version</span></span><br/>   | <span data-ttu-id="45fda-113">Lecteur Windows Media série 9 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="45fda-113">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="45fda-114">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="45fda-114">Namespace</span></span><br/> | <span data-ttu-id="45fda-115">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="45fda-115">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="45fda-116">Assembly</span><span class="sxs-lookup"><span data-stu-id="45fda-116">Assembly</span></span><br/>  | <dl> <span data-ttu-id="45fda-117"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="45fda-117"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="45fda-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="45fda-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="45fda-119">**Objet AxWindowsMediaPlayer (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="45fda-119">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="45fda-120">**AxWindowsMediaPlayer. Status (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="45fda-120">**AxWindowsMediaPlayer.status (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-status--vb-and-c.md)
</dt> </dl>

 

 





