---
title: Interface IWMPMedia2 (VB et C) (WMP. h)
description: Fournit l’accès à une propriété d’élément multimédia supplémentaire.
ms.assetid: 7d9f8304-ae26-4175-b9d4-9f272861ef87
keywords:
- IWMPMedia2 (VB et C) interface Windows Media Player
- Interface IWMPMedia2 (VB et C), le lecteur Windows Media, décrit
topic_type:
- apiref
api_name:
- IWMPMedia2 (VB and C )
api_location:
- wmp.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bb1a77322e0e6649d9a286c920ccd9ddc77890f3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106525343"
---
# <a name="iwmpmedia2-vb-and-c-interface"></a><span data-ttu-id="93c26-105">Interface IWMPMedia2 (VB et C#)</span><span class="sxs-lookup"><span data-stu-id="93c26-105">IWMPMedia2 (VB and C#) interface</span></span>

<span data-ttu-id="93c26-106">Fournit l’accès à une propriété d’élément multimédia supplémentaire.</span><span class="sxs-lookup"><span data-stu-id="93c26-106">Provides access to an additional media item property.</span></span>

<span data-ttu-id="93c26-107">En plus des propriétés et des méthodes héritées de **IWMPMedia**, l’interface **IWMPMedia2** expose la propriété suivante.</span><span class="sxs-lookup"><span data-stu-id="93c26-107">In addition to the properties and methods inherited from **IWMPMedia**, the **IWMPMedia2** interface exposes the following property.</span></span>



| <span data-ttu-id="93c26-108">Propriété</span><span class="sxs-lookup"><span data-stu-id="93c26-108">Property</span></span>                                                 | <span data-ttu-id="93c26-109">Description</span><span class="sxs-lookup"><span data-stu-id="93c26-109">Description</span></span>                                                                   |
|----------------------------------------------------------|-------------------------------------------------------------------------------|
| [<span data-ttu-id="93c26-110">Error</span><span class="sxs-lookup"><span data-stu-id="93c26-110">Error</span></span>](wmplibiwmpmedia2-iwmpmedia2-error--vb-and-c.md) | <span data-ttu-id="93c26-111">Obtient une interface **IWMPErrorItem** si l’élément multimédia a une condition d’erreur.</span><span class="sxs-lookup"><span data-stu-id="93c26-111">Gets an **IWMPErrorItem** interface if the media item has an error condition.</span></span> |



 

<span data-ttu-id="93c26-112">Obtient une interface **IWMPMedia2** en effectuant un cast de la valeur retournée par l’une des propriétés ou méthodes suivantes accessibles par le biais de l’objet ou de l’interface suivant.</span><span class="sxs-lookup"><span data-stu-id="93c26-112">Get an **IWMPMedia2** interface by casting the value returned by one of the following properties or methods accessed through the following object or interface.</span></span>



| <span data-ttu-id="93c26-113">Objet ou interface</span><span class="sxs-lookup"><span data-stu-id="93c26-113">Object or interface</span></span>                                               | <span data-ttu-id="93c26-114">Propriété ou méthode</span><span class="sxs-lookup"><span data-stu-id="93c26-114">Property or method</span></span>                                                                                                                |
|-------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="93c26-115">IWMPControls</span><span class="sxs-lookup"><span data-stu-id="93c26-115">IWMPControls</span></span>](iwmpcontrols--vb-and-c.md)                        | [<span data-ttu-id="93c26-116">currentItem</span><span class="sxs-lookup"><span data-stu-id="93c26-116">currentItem</span></span>](wmplibiwmpcontrols-iwmpcontrols-currentitem--vb-and-c.md)                                                          |
| [<span data-ttu-id="93c26-117">AxWindowsMediaPlayer</span><span class="sxs-lookup"><span data-stu-id="93c26-117">AxWindowsMediaPlayer</span></span>](axwindowsmediaplayer-object--vb-and-c.md) | <span data-ttu-id="93c26-118">[currentMedia](axwmplib-axwindowsmediaplayer-currentmedia--vb-and-c.md) , [newMedia](axwmplib-axwindowsmediaplayer-newmedia.md)</span><span class="sxs-lookup"><span data-stu-id="93c26-118">[currentMedia](axwmplib-axwindowsmediaplayer-currentmedia--vb-and-c.md) , [newMedia](axwmplib-axwindowsmediaplayer-newmedia.md)</span></span> |
| [<span data-ttu-id="93c26-119">IWMPPlaylist</span><span class="sxs-lookup"><span data-stu-id="93c26-119">IWMPPlaylist</span></span>](iwmpplaylist--vb-and-c.md)                        | <span data-ttu-id="93c26-120">[Item](iwmpplaylist-item--vb-and-c.md) ( **recevoir un \_ élément** en C#)</span><span class="sxs-lookup"><span data-stu-id="93c26-120">[Item](iwmpplaylist-item--vb-and-c.md) ( **get\_Item** in C#)</span></span>                                                                   |



 

## <a name="members"></a><span data-ttu-id="93c26-121">Membres</span><span class="sxs-lookup"><span data-stu-id="93c26-121">Members</span></span>

<span data-ttu-id="93c26-122">L’interface **IWMPMedia2 (VB et C#)** ne définit aucun membre.</span><span class="sxs-lookup"><span data-stu-id="93c26-122">The **IWMPMedia2 (VB and C#)** interface does not define any members.</span></span>

## <a name="requirements"></a><span data-ttu-id="93c26-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="93c26-123">Requirements</span></span>



| <span data-ttu-id="93c26-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="93c26-124">Requirement</span></span> | <span data-ttu-id="93c26-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="93c26-125">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="93c26-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="93c26-126">Header</span></span><br/> | <dl> <span data-ttu-id="93c26-127"><dt>WMP. h</dt></span><span class="sxs-lookup"><span data-stu-id="93c26-127"><dt>Wmp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="93c26-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="93c26-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="93c26-129">**Interfaces pour Visual Basic .NET et C #**</span><span class="sxs-lookup"><span data-stu-id="93c26-129">**Interfaces for Visual Basic .NET and C#**</span></span>](interfaces-for-visual-basic--net-and-c.md)
</dt> <dt>

[<span data-ttu-id="93c26-130">**IWMPErrorItem (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="93c26-130">**IWMPErrorItem (VB and C#)**</span></span>](iwmperroritem--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="93c26-131">**Interface IWMPMedia (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="93c26-131">**IWMPMedia Interface (VB and C#)**</span></span>](iwmpmedia--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="93c26-132">**Interface IWMPMedia3 (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="93c26-132">**IWMPMedia3 Interface (VB and C#)**</span></span>](iwmpmedia3--vb-and-c.md)
</dt> </dl>

 

 





