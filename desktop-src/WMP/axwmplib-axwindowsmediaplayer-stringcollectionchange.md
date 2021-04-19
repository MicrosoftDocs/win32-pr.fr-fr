---
title: Événement StringCollectionChange de l’objet AxWindowsMediaPlayer
description: L’événement StringCollectionChange se produit lorsqu’une collection de chaînes change. | Événement StringCollectionChange de l’objet AxWindowsMediaPlayer
ms.assetid: 21b66882-bff9-4482-b56c-32c9df0bc02f
keywords:
- Événement StringCollectionChange de l’objet AxWindowsMediaPlayer du lecteur Windows Media
topic_type:
- apiref
api_name:
- StringCollectionChange Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5182352f7f18727a1c11e9a0ef49e8141000d299
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540968"
---
# <a name="stringcollectionchange-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="18e2b-105">Événement StringCollectionChange de l’objet AxWindowsMediaPlayer</span><span class="sxs-lookup"><span data-stu-id="18e2b-105">StringCollectionChange Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="18e2b-106">L’événement StringCollectionChange se produit lorsqu’une collection de chaînes change.</span><span class="sxs-lookup"><span data-stu-id="18e2b-106">The StringCollectionChange event occurs when a string collection changes.</span></span>

``` syntax
[C#]
private void player_StringCollectionChange(
  object sender,
  _WMPOCXEvents_StringCollectionChangeEvent e
)

[Visual Basic]
Private Sub player_StringCollectionChange(
  sender As Object,
  e As _WMPOCXEvents_StringCollectionChangeEvent
) Handles player.StringCollectionChange
```

## <a name="event-data"></a><span data-ttu-id="18e2b-107">Données d'événements</span><span class="sxs-lookup"><span data-stu-id="18e2b-107">Event Data</span></span>

<span data-ttu-id="18e2b-108">Le gestionnaire associé à cet événement est de type **AxWMPLib. \_ WMPOCXEvents \_ StringCollectionChangeEventHandler**.</span><span class="sxs-lookup"><span data-stu-id="18e2b-108">The handler associated with this event is of type **AxWMPLib.\_WMPOCXEvents\_StringCollectionChangeEventHandler**.</span></span> <span data-ttu-id="18e2b-109">Ce gestionnaire reçoit un argument de type **AxWMPLib. \_ WMPOCXEvents \_ StringCollectionChangeEvent**, qui contient les propriétés suivantes relatives à cet événement.</span><span class="sxs-lookup"><span data-stu-id="18e2b-109">This handler receives an argument of type **AxWMPLib.\_WMPOCXEvents\_StringCollectionChangeEvent**, which contains the following properties related to this event.</span></span>



| <span data-ttu-id="18e2b-110">Propriété</span><span class="sxs-lookup"><span data-stu-id="18e2b-110">Property</span></span>              | <span data-ttu-id="18e2b-111">Description</span><span class="sxs-lookup"><span data-stu-id="18e2b-111">Description</span></span>                                                                                                                           |
|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="18e2b-112">pdispStringCollection</span><span class="sxs-lookup"><span data-stu-id="18e2b-112">pdispStringCollection</span></span> | <span data-ttu-id="18e2b-113">Élément de collection de chaînes System. ObjectThe modifié.</span><span class="sxs-lookup"><span data-stu-id="18e2b-113">System.ObjectThe string collection item that changed.</span></span> <span data-ttu-id="18e2b-114">Vous pouvez effectuer un cast de ce en une interface IWMPStringCollection pour y accéder.</span><span class="sxs-lookup"><span data-stu-id="18e2b-114">You can cast this to an IWMPStringCollection interface to access it.</span></span><br/> |
| <span data-ttu-id="18e2b-115">lCollectionIndex</span><span class="sxs-lookup"><span data-stu-id="18e2b-115">lCollectionIndex</span></span>      | <span data-ttu-id="18e2b-116">Index System. Int32The de l’élément de collection de chaînes qui a changé.</span><span class="sxs-lookup"><span data-stu-id="18e2b-116">System.Int32The index of the string collection item that changed.</span></span><br/>                                                          |
| <span data-ttu-id="18e2b-117">Modifier</span><span class="sxs-lookup"><span data-stu-id="18e2b-117">change</span></span>                | <span data-ttu-id="18e2b-118">Valeur d’énumération WMPLib. WMPStringCollectionChangeEventTypeAn indiquant le type de modification qui s’est produite.</span><span class="sxs-lookup"><span data-stu-id="18e2b-118">WMPLib.WMPStringCollectionChangeEventTypeAn enumeration value indicating the type of change that occurred.</span></span><br/>                 |



 

## <a name="requirements"></a><span data-ttu-id="18e2b-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="18e2b-119">Requirements</span></span>



| <span data-ttu-id="18e2b-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="18e2b-120">Requirement</span></span> | <span data-ttu-id="18e2b-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="18e2b-121">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="18e2b-122">Version</span><span class="sxs-lookup"><span data-stu-id="18e2b-122">Version</span></span><br/>   | <span data-ttu-id="18e2b-123">Lecteur Windows Media série 9 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="18e2b-123">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="18e2b-124">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="18e2b-124">Namespace</span></span><br/> | <span data-ttu-id="18e2b-125">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="18e2b-125">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="18e2b-126">Assembly</span><span class="sxs-lookup"><span data-stu-id="18e2b-126">Assembly</span></span><br/>  | <dl> <span data-ttu-id="18e2b-127"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="18e2b-127"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="18e2b-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="18e2b-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="18e2b-129">**Objet AxWindowsMediaPlayer (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="18e2b-129">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="18e2b-130">**Interface IWMPStringCollection (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="18e2b-130">**IWMPStringCollection Interface (VB and C#)**</span></span>](iwmpstringcollection--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="18e2b-131">**WMPStringCollectionChangeEventType**</span><span class="sxs-lookup"><span data-stu-id="18e2b-131">**WMPStringCollectionChangeEventType**</span></span>](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpstringcollectionchangeeventtype)
</dt> </dl>

 

 





