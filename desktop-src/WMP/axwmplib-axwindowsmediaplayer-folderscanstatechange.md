---
title: Événement FolderScanStateChange de l’objet AxWindowsMediaPlayer
description: L’événement FolderScanStateChange se produit lorsqu’une opération de surveillance des dossiers change d’État.
ms.assetid: f68829a3-00df-417a-ae78-49dff1e6f09b
keywords:
- Événement FolderScanStateChange de l’objet AxWindowsMediaPlayer du lecteur Windows Media
topic_type:
- apiref
api_name:
- FolderScanStateChange Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3672f16bee5251aa46e6a64a0da983e0f34ec54a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106545336"
---
# <a name="folderscanstatechange-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="13e3c-104">Événement FolderScanStateChange de l’objet AxWindowsMediaPlayer</span><span class="sxs-lookup"><span data-stu-id="13e3c-104">FolderScanStateChange Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="13e3c-105">L’événement FolderScanStateChange se produit lorsqu’une opération de surveillance des dossiers change d’État.</span><span class="sxs-lookup"><span data-stu-id="13e3c-105">The FolderScanStateChange event occurs when a folder monitoring operation changes state.</span></span>

``` syntax
[C#]
private void player_FolderScanStateChange(
  object sender,
  _WMPOCXEvents_FolderScanStateChangeEvent e
)

[Visual Basic]
Private Sub player_FolderScanStateChange( 
  sender As Object,  
  e As _WMPOCXEvents_FolderScanStateChangeEvent
) Handles player.FolderScanStateChange
```

## <a name="event-data"></a><span data-ttu-id="13e3c-106">Données d'événements</span><span class="sxs-lookup"><span data-stu-id="13e3c-106">Event Data</span></span>

<span data-ttu-id="13e3c-107">Le gestionnaire associé à cet événement est de type **AxWMPLib. \_ WMPOCXEvents \_ FolderScanStateChangeEventHandler**.</span><span class="sxs-lookup"><span data-stu-id="13e3c-107">The handler associated with this event is of type **AxWMPLib.\_WMPOCXEvents\_FolderScanStateChangeEventHandler**.</span></span> <span data-ttu-id="13e3c-108">Ce gestionnaire reçoit un argument de type **AxWMPLib. \_ WMPOCXEvents \_ FolderScanStateChangeEvent**, qui contient la propriété suivante associée à cet événement.</span><span class="sxs-lookup"><span data-stu-id="13e3c-108">This handler receives an argument of type **AxWMPLib.\_WMPOCXEvents\_FolderScanStateChangeEvent**, which contains the following property related to this event.</span></span>



| <span data-ttu-id="13e3c-109">Propriété</span><span class="sxs-lookup"><span data-stu-id="13e3c-109">Property</span></span> | <span data-ttu-id="13e3c-110">Description</span><span class="sxs-lookup"><span data-stu-id="13e3c-110">Description</span></span>                                                                             |
|----------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="13e3c-111">wmpfss</span><span class="sxs-lookup"><span data-stu-id="13e3c-111">wmpfss</span></span>   | <span data-ttu-id="13e3c-112">Valeur d’énumération WMPLib. WMPFolderScanStateThe qui indique le nouvel État.</span><span class="sxs-lookup"><span data-stu-id="13e3c-112">WMPLib.WMPFolderScanStateThe enumeration value that indicates the new state.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="13e3c-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="13e3c-113">Requirements</span></span>



| <span data-ttu-id="13e3c-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="13e3c-114">Requirement</span></span> | <span data-ttu-id="13e3c-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="13e3c-115">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="13e3c-116">Version</span><span class="sxs-lookup"><span data-stu-id="13e3c-116">Version</span></span><br/>   | <span data-ttu-id="13e3c-117">Lecteur Windows Media 11</span><span class="sxs-lookup"><span data-stu-id="13e3c-117">Windows Media Player 11</span></span><br/>                                                                                         |
| <span data-ttu-id="13e3c-118">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="13e3c-118">Namespace</span></span><br/> | <span data-ttu-id="13e3c-119">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="13e3c-119">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="13e3c-120">Assembly</span><span class="sxs-lookup"><span data-stu-id="13e3c-120">Assembly</span></span><br/>  | <dl> <span data-ttu-id="13e3c-121"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="13e3c-121"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="13e3c-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="13e3c-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="13e3c-123">**Objet AxWindowsMediaPlayer (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="13e3c-123">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="13e3c-124">**WMPFolderScanState**</span><span class="sxs-lookup"><span data-stu-id="13e3c-124">**WMPFolderScanState**</span></span>](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpfolderscanstate)
</dt> </dl>

 

 





