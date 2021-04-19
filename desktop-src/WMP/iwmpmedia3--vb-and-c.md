---
title: Interface IWMPMedia3 (VB et C) (WMP. h)
description: Fournit des méthodes supplémentaires pour accéder aux propriétés d’un élément multimédia.
ms.assetid: e16aa5e2-ae44-41c2-8c61-fb688c2e89e2
keywords:
- IWMPMedia3 (VB et C) interface Windows Media Player
- Interface IWMPMedia3 (VB et C), le lecteur Windows Media, décrit
topic_type:
- apiref
api_name:
- IWMPMedia3 (VB and C )
api_location:
- wmp.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: edb5438ad4d80031d5b45c738c6b6cc9335018af
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106527989"
---
# <a name="iwmpmedia3-vb-and-c-interface"></a><span data-ttu-id="487ca-105">Interface IWMPMedia3 (VB et C#)</span><span class="sxs-lookup"><span data-stu-id="487ca-105">IWMPMedia3 (VB and C#) interface</span></span>

<span data-ttu-id="487ca-106">Fournit des méthodes supplémentaires pour accéder aux propriétés d’un élément multimédia.</span><span class="sxs-lookup"><span data-stu-id="487ca-106">Provides additional methods to access the properties of a media item.</span></span>

## <a name="members"></a><span data-ttu-id="487ca-107">Membres</span><span class="sxs-lookup"><span data-stu-id="487ca-107">Members</span></span>

<span data-ttu-id="487ca-108">L’interface **IWMPMedia3 (VB et C#)** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="487ca-108">The **IWMPMedia3 (VB and C#)** interface has these types of members:</span></span>

-   [<span data-ttu-id="487ca-109">Méthodes</span><span class="sxs-lookup"><span data-stu-id="487ca-109">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="487ca-110">Méthodes</span><span class="sxs-lookup"><span data-stu-id="487ca-110">Methods</span></span>

<span data-ttu-id="487ca-111">L’interface **IWMPMedia3 (VB et C#)** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="487ca-111">The **IWMPMedia3 (VB and C#)** interface has these methods.</span></span>



| <span data-ttu-id="487ca-112">Méthode</span><span class="sxs-lookup"><span data-stu-id="487ca-112">Method</span></span>                                                                                           | <span data-ttu-id="487ca-113">Description</span><span class="sxs-lookup"><span data-stu-id="487ca-113">Description</span></span>                                                                                            |
|:-------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="487ca-114">**getAttributeCountByType**</span><span class="sxs-lookup"><span data-stu-id="487ca-114">**getAttributeCountByType**</span></span>](wmplibiwmpmedia3-iwmpmedia3-getattributecountbytype--vb-and-c.md) | <span data-ttu-id="487ca-115">Retourne le nombre d’attributs associés au type d’attribut spécifié.</span><span class="sxs-lookup"><span data-stu-id="487ca-115">Returns the number of attributes associated with the specified attribute type.</span></span><br/>              |
| [<span data-ttu-id="487ca-116">**getItemInfoByType**</span><span class="sxs-lookup"><span data-stu-id="487ca-116">**getItemInfoByType**</span></span>](wmplibiwmpmedia3-iwmpmedia3-getiteminfobytype--vb-and-c.md)             | <span data-ttu-id="487ca-117">Retourne la valeur de l’attribut correspondant au type d’attribut et à l’index spécifiés.</span><span class="sxs-lookup"><span data-stu-id="487ca-117">Returns the value of the attribute corresponding to the specified attribute type and index.</span></span><br/> |



 

<span data-ttu-id="487ca-118">Obtient une interface **IWMPMedia3** en effectuant un cast de la valeur retournée par l’une des propriétés ou méthodes suivantes accessibles par le biais de l’objet ou de l’interface suivant.</span><span class="sxs-lookup"><span data-stu-id="487ca-118">Get an **IWMPMedia3** interface by casting the value returned by one of the following properties or methods accessed through the following object or interface.</span></span>



| <span data-ttu-id="487ca-119">Objet ou interface</span><span class="sxs-lookup"><span data-stu-id="487ca-119">Object or interface</span></span>                                               | <span data-ttu-id="487ca-120">Propriété ou méthode</span><span class="sxs-lookup"><span data-stu-id="487ca-120">Property or method</span></span>                                                                                                                |
|-------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="487ca-121">IWMPControls</span><span class="sxs-lookup"><span data-stu-id="487ca-121">IWMPControls</span></span>](iwmpcontrols--vb-and-c.md)                        | [<span data-ttu-id="487ca-122">currentItem</span><span class="sxs-lookup"><span data-stu-id="487ca-122">currentItem</span></span>](wmplibiwmpcontrols-iwmpcontrols-currentitem--vb-and-c.md)                                                          |
| [<span data-ttu-id="487ca-123">AxWindowsMediaPlayer</span><span class="sxs-lookup"><span data-stu-id="487ca-123">AxWindowsMediaPlayer</span></span>](axwindowsmediaplayer-object--vb-and-c.md) | <span data-ttu-id="487ca-124">[currentMedia](axwmplib-axwindowsmediaplayer-currentmedia--vb-and-c.md) , [newMedia](axwmplib-axwindowsmediaplayer-newmedia.md)</span><span class="sxs-lookup"><span data-stu-id="487ca-124">[currentMedia](axwmplib-axwindowsmediaplayer-currentmedia--vb-and-c.md) , [newMedia](axwmplib-axwindowsmediaplayer-newmedia.md)</span></span> |
| [<span data-ttu-id="487ca-125">IWMPPlaylist</span><span class="sxs-lookup"><span data-stu-id="487ca-125">IWMPPlaylist</span></span>](iwmpplaylist--vb-and-c.md)                        | <span data-ttu-id="487ca-126">[Item](iwmpplaylist-item--vb-and-c.md) ( **recevoir un \_ élément** en C#)</span><span class="sxs-lookup"><span data-stu-id="487ca-126">[Item](iwmpplaylist-item--vb-and-c.md) ( **get\_Item** in C#)</span></span>                                                                   |



 

## <a name="requirements"></a><span data-ttu-id="487ca-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="487ca-127">Requirements</span></span>



| <span data-ttu-id="487ca-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="487ca-128">Requirement</span></span> | <span data-ttu-id="487ca-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="487ca-129">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="487ca-130">En-tête</span><span class="sxs-lookup"><span data-stu-id="487ca-130">Header</span></span><br/> | <dl> <span data-ttu-id="487ca-131"><dt>WMP. h</dt></span><span class="sxs-lookup"><span data-stu-id="487ca-131"><dt>Wmp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="487ca-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="487ca-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="487ca-133">**Interfaces pour Visual Basic .NET et C #**</span><span class="sxs-lookup"><span data-stu-id="487ca-133">**Interfaces for Visual Basic .NET and C#**</span></span>](interfaces-for-visual-basic--net-and-c.md)
</dt> <dt>

[<span data-ttu-id="487ca-134">**Interface IWMPMedia (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="487ca-134">**IWMPMedia Interface (VB and C#)**</span></span>](iwmpmedia--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="487ca-135">**Interface IWMPMedia2 (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="487ca-135">**IWMPMedia2 Interface (VB and C#)**</span></span>](iwmpmedia2--vb-and-c.md)
</dt> </dl>

 

 





