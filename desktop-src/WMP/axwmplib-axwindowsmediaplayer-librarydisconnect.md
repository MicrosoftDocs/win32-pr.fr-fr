---
title: Événement LibraryDisconnect de l’objet AxWindowsMediaPlayer
description: L’événement LibraryDisconnect se produit lorsqu’une bibliothèque n’est plus disponible.
ms.assetid: 053d914a-dcd9-4fd6-a789-10c26147d08a
keywords:
- Événement LibraryDisconnect de l’objet AxWindowsMediaPlayer du lecteur Windows Media
topic_type:
- apiref
api_name:
- LibraryDisconnect Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 058c75ed0d1173661b16baa6e4b4394ba4d0c38f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106542719"
---
# <a name="librarydisconnect-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="d1061-104">Événement LibraryDisconnect de l’objet AxWindowsMediaPlayer</span><span class="sxs-lookup"><span data-stu-id="d1061-104">LibraryDisconnect Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="d1061-105">L’événement LibraryDisconnect se produit lorsqu’une bibliothèque n’est plus disponible.</span><span class="sxs-lookup"><span data-stu-id="d1061-105">The LibraryDisconnect event occurs when a library is no longer available.</span></span>

``` syntax
[C#]
private void player_LibraryDisconnect(
  object sender,
  _WMPOCXEvents_LibraryDisconnectEvent e
)

[Visual Basic]
Private Sub player_LibraryDisconnect(  
   sender As Object,  
   e As _WMPOCXEvents_LibraryDisconnectEvent
) Handles player.LibraryDisconnect
```

## <a name="event-data"></a><span data-ttu-id="d1061-106">Données d'événements</span><span class="sxs-lookup"><span data-stu-id="d1061-106">Event Data</span></span>

<span data-ttu-id="d1061-107">Le gestionnaire associé à cet événement est de type **AxWMPLib. \_ WMPOCXEvents \_ LibraryDisconnectEventHandler**.</span><span class="sxs-lookup"><span data-stu-id="d1061-107">The handler associated with this event is of type **AxWMPLib.\_WMPOCXEvents\_LibraryDisconnectEventHandler**.</span></span> <span data-ttu-id="d1061-108">Ce gestionnaire reçoit un argument de type **AxWMPLib. \_ WMPOCXEvents \_ LibraryDisconnectEvent**, qui contient la propriété suivante associée à cet événement.</span><span class="sxs-lookup"><span data-stu-id="d1061-108">This handler receives an argument of type **AxWMPLib.\_WMPOCXEvents\_LibraryDisconnectEvent**, which contains the following property related to this event.</span></span>



| <span data-ttu-id="d1061-109">Propriété</span><span class="sxs-lookup"><span data-stu-id="d1061-109">Property</span></span> | <span data-ttu-id="d1061-110">Description</span><span class="sxs-lookup"><span data-stu-id="d1061-110">Description</span></span>                                                                                   |
|----------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="d1061-111">pLibrary</span><span class="sxs-lookup"><span data-stu-id="d1061-111">pLibrary</span></span> | <span data-ttu-id="d1061-112">**Wmplib. IWMPLibrary** Interface qui représente la bibliothèque déconnectée.</span><span class="sxs-lookup"><span data-stu-id="d1061-112">**WMPLib.IWMPLibrary** The interface that represents the library that disconnected.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="d1061-113">Notes</span><span class="sxs-lookup"><span data-stu-id="d1061-113">Remarks</span></span>

<span data-ttu-id="d1061-114">Cet événement ne se produit pas pour la bibliothèque locale.</span><span class="sxs-lookup"><span data-stu-id="d1061-114">This event does not occur for the local library.</span></span>

## <a name="requirements"></a><span data-ttu-id="d1061-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d1061-115">Requirements</span></span>



| <span data-ttu-id="d1061-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d1061-116">Requirement</span></span> | <span data-ttu-id="d1061-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="d1061-117">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d1061-118">Version</span><span class="sxs-lookup"><span data-stu-id="d1061-118">Version</span></span><br/>   | <span data-ttu-id="d1061-119">Lecteur Windows Media 11</span><span class="sxs-lookup"><span data-stu-id="d1061-119">Windows Media Player 11</span></span><br/>                                                                                         |
| <span data-ttu-id="d1061-120">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="d1061-120">Namespace</span></span><br/> | <span data-ttu-id="d1061-121">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="d1061-121">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="d1061-122">Assembly</span><span class="sxs-lookup"><span data-stu-id="d1061-122">Assembly</span></span><br/>  | <dl> <span data-ttu-id="d1061-123"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="d1061-123"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d1061-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d1061-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d1061-125">**Objet AxWindowsMediaPlayer (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="d1061-125">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="d1061-126">**Interface IWMPLibrary (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="d1061-126">**IWMPLibrary Interface (VB and C#)**</span></span>](iwmplibrary--vb-and-c.md)
</dt> </dl>

 

 





