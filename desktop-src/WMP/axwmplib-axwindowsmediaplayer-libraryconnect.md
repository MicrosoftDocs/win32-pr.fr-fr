---
title: Événement LibraryConnect de l’objet AxWindowsMediaPlayer
description: L’événement LibraryConnect se produit lorsqu’une bibliothèque devient disponible.
ms.assetid: f67243ce-0e25-43a7-b754-6b0e80d72055
keywords:
- Événement LibraryConnect de l’objet AxWindowsMediaPlayer du lecteur Windows Media
topic_type:
- apiref
api_name:
- LibraryConnect Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c33353b8438c61e28a3d52975fe90b06f14f03a4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526417"
---
# <a name="libraryconnect-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="7ff5a-104">Événement LibraryConnect de l’objet AxWindowsMediaPlayer</span><span class="sxs-lookup"><span data-stu-id="7ff5a-104">LibraryConnect Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="7ff5a-105">L’événement LibraryConnect se produit lorsqu’une bibliothèque devient disponible.</span><span class="sxs-lookup"><span data-stu-id="7ff5a-105">The LibraryConnect event occurs when a library becomes available.</span></span>

``` syntax
[C#]
private void player_LibraryConnect(
  object sender,
  _WMPOCXEvents_LibraryConnectEvent e
)

[Visual Basic]
Private Sub player_LibraryConnect(  
  sender As Object,
  e As _WMPOCXEvents_LibraryConnectEvent
) Handles player.LibraryConnect
```

## <a name="event-data"></a><span data-ttu-id="7ff5a-106">Données d'événements</span><span class="sxs-lookup"><span data-stu-id="7ff5a-106">Event Data</span></span>

<span data-ttu-id="7ff5a-107">Le gestionnaire associé à cet événement est de type **AxWMPLib. \_ WMPOCXEvents \_ LibraryConnectEventHandler**.</span><span class="sxs-lookup"><span data-stu-id="7ff5a-107">The handler associated with this event is of type **AxWMPLib.\_WMPOCXEvents\_LibraryConnectEventHandler**.</span></span> <span data-ttu-id="7ff5a-108">Ce gestionnaire reçoit un argument de type **AxWMPLib. \_ WMPOCXEvents \_ LibraryConnectEvent**, qui contient la propriété suivante associée à cet événement.</span><span class="sxs-lookup"><span data-stu-id="7ff5a-108">This handler receives an argument of type **AxWMPLib.\_WMPOCXEvents\_LibraryConnectEvent**, which contains the following property related to this event.</span></span>



| <span data-ttu-id="7ff5a-109">Propriété</span><span class="sxs-lookup"><span data-stu-id="7ff5a-109">Property</span></span> | <span data-ttu-id="7ff5a-110">Description</span><span class="sxs-lookup"><span data-stu-id="7ff5a-110">Description</span></span>                                                                                |
|----------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="7ff5a-111">pLibrary</span><span class="sxs-lookup"><span data-stu-id="7ff5a-111">pLibrary</span></span> | <span data-ttu-id="7ff5a-112">**Wmplib. IWMPLibrary** Interface qui représente la bibliothèque connectée.</span><span class="sxs-lookup"><span data-stu-id="7ff5a-112">**WMPLib.IWMPLibrary** The interface that represents the library that connected.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="7ff5a-113">Notes</span><span class="sxs-lookup"><span data-stu-id="7ff5a-113">Remarks</span></span>

<span data-ttu-id="7ff5a-114">Cet événement ne se produit pas pour la bibliothèque locale.</span><span class="sxs-lookup"><span data-stu-id="7ff5a-114">This event does not occur for the local library.</span></span>

## <a name="requirements"></a><span data-ttu-id="7ff5a-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7ff5a-115">Requirements</span></span>



| <span data-ttu-id="7ff5a-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7ff5a-116">Requirement</span></span> | <span data-ttu-id="7ff5a-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="7ff5a-117">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7ff5a-118">Version</span><span class="sxs-lookup"><span data-stu-id="7ff5a-118">Version</span></span><br/>   | <span data-ttu-id="7ff5a-119">Lecteur Windows Media 11</span><span class="sxs-lookup"><span data-stu-id="7ff5a-119">Windows Media Player 11</span></span><br/>                                                                                         |
| <span data-ttu-id="7ff5a-120">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="7ff5a-120">Namespace</span></span><br/> | <span data-ttu-id="7ff5a-121">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="7ff5a-121">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="7ff5a-122">Assembly</span><span class="sxs-lookup"><span data-stu-id="7ff5a-122">Assembly</span></span><br/>  | <dl> <span data-ttu-id="7ff5a-123"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="7ff5a-123"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7ff5a-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7ff5a-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7ff5a-125">**Objet AxWindowsMediaPlayer (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="7ff5a-125">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="7ff5a-126">**Interface IWMPLibrary (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="7ff5a-126">**IWMPLibrary Interface (VB and C#)**</span></span>](iwmplibrary--vb-and-c.md)
</dt> </dl>

 

 





