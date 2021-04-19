---
title: Interface IWMPMediaCollection2 (VB et C) (WMP. h)
description: Fournit des méthodes qui complètent l’interface IWMPMediaCollection.
ms.assetid: 204f336c-ea78-43d4-9686-bcab72362bc9
keywords:
- IWMPMediaCollection2 (VB et C) interface Windows Media Player
- Interface IWMPMediaCollection2 (VB et C), le lecteur Windows Media, décrit
topic_type:
- apiref
api_name:
- IWMPMediaCollection2 (VB and C )
api_location:
- wmp.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 58175e80fbf0f706a9ae6c6b3b69afbd26d52af3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106533110"
---
# <a name="iwmpmediacollection2-vb-and-c-interface"></a><span data-ttu-id="5d59e-105">Interface IWMPMediaCollection2 (VB et C#)</span><span class="sxs-lookup"><span data-stu-id="5d59e-105">IWMPMediaCollection2 (VB and C#) interface</span></span>

<span data-ttu-id="5d59e-106">Fournit des méthodes qui complètent l’interface **IWMPMediaCollection** .</span><span class="sxs-lookup"><span data-stu-id="5d59e-106">Provides methods that supplement the **IWMPMediaCollection** interface.</span></span>

## <a name="members"></a><span data-ttu-id="5d59e-107">Membres</span><span class="sxs-lookup"><span data-stu-id="5d59e-107">Members</span></span>

<span data-ttu-id="5d59e-108">L’interface **IWMPMediaCollection2 (VB et C#)** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="5d59e-108">The **IWMPMediaCollection2 (VB and C#)** interface has these types of members:</span></span>

-   [<span data-ttu-id="5d59e-109">Méthodes</span><span class="sxs-lookup"><span data-stu-id="5d59e-109">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="5d59e-110">Méthodes</span><span class="sxs-lookup"><span data-stu-id="5d59e-110">Methods</span></span>

<span data-ttu-id="5d59e-111">L’interface **IWMPMediaCollection2 (VB et C#)** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="5d59e-111">The **IWMPMediaCollection2 (VB and C#)** interface has these methods.</span></span>



| <span data-ttu-id="5d59e-112">Méthode</span><span class="sxs-lookup"><span data-stu-id="5d59e-112">Method</span></span>                                                                                                                     | <span data-ttu-id="5d59e-113">Description</span><span class="sxs-lookup"><span data-stu-id="5d59e-113">Description</span></span>                                                                                                                                                              |
|:---------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5d59e-114">**createQuery**</span><span class="sxs-lookup"><span data-stu-id="5d59e-114">**createQuery**</span></span>](wmplibiwmpmediacollection2-iwmpmediacollection2-createquery--vb-and-c.md)                               | <span data-ttu-id="5d59e-115">Retourne une interface **IWMPQuery** qui représente une nouvelle requête.</span><span class="sxs-lookup"><span data-stu-id="5d59e-115">Returns an **IWMPQuery** interface that represents a new query.</span></span><br/>                                                                                               |
| [<span data-ttu-id="5d59e-116">**getByAttributeAndMediaType**</span><span class="sxs-lookup"><span data-stu-id="5d59e-116">**getByAttributeAndMediaType**</span></span>](wmplibiwmpmediacollection2-iwmpmediacollection2-getbyattributeandmediatype--vb-and-c.md) | <span data-ttu-id="5d59e-117">Retourne une interface **IWMPPlaylist** qui fournit l’accès aux éléments multimédias qui ont un attribut et un type de média spécifiés.</span><span class="sxs-lookup"><span data-stu-id="5d59e-117">Returns an **IWMPPlaylist** interface that provides access to media items that have a specified attribute and media type.</span></span><br/>                                     |
| [<span data-ttu-id="5d59e-118">**getPlaylistByQuery**</span><span class="sxs-lookup"><span data-stu-id="5d59e-118">**getPlaylistByQuery**</span></span>](wmplibiwmpmediacollection2-iwmpmediacollection2-getplaylistbyquery--vb-and-c.md)                 | <span data-ttu-id="5d59e-119">Retourne une interface **IWMPPlaylist** qui fournit l’accès aux éléments multimédias qui correspondent aux conditions de requête.</span><span class="sxs-lookup"><span data-stu-id="5d59e-119">Returns an **IWMPPlaylist** interface that provides access to media items that match the query conditions.</span></span><br/>                                                    |
| [<span data-ttu-id="5d59e-120">**getStringCollectionByQuery**</span><span class="sxs-lookup"><span data-stu-id="5d59e-120">**getStringCollectionByQuery**</span></span>](wmplibiwmpmediacollection2-iwmpmediacollection2-getstringcollectionbyquery--vb-and-c.md) | <span data-ttu-id="5d59e-121">Retourne une interface **IWMPStringCollection** qui fournit l’accès à l’ensemble de toutes les valeurs de chaîne pour un attribut spécifié qui correspondent aux conditions de requête.</span><span class="sxs-lookup"><span data-stu-id="5d59e-121">Returns an **IWMPStringCollection** interface that provides access to the set of all string values for a specified attribute that match the query conditions.</span></span><br/> |



 

<span data-ttu-id="5d59e-122">Obtient une interface **IWMPMediaCollection2** en effectuant un cast de la valeur retournée par la propriété [**AxWindowsMediaPlayer. mediaCollection**](axwmplib-axwindowsmediaplayer-mediacollection--vb-and-c.md) ou de la valeur retournée par la propriété [**IWMPLibrary. mediaCollection**](wmplibiwmplibrary-iwmplibrary-mediacollection--vb-and-c.md) .</span><span class="sxs-lookup"><span data-stu-id="5d59e-122">Get an **IWMPMediaCollection2** interface by casting the value returned by the [**AxWindowsMediaPlayer.mediaCollection**](axwmplib-axwindowsmediaplayer-mediacollection--vb-and-c.md) property or the value returned by the [**IWMPLibrary.mediaCollection**](wmplibiwmplibrary-iwmplibrary-mediacollection--vb-and-c.md) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="5d59e-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5d59e-123">Requirements</span></span>



| <span data-ttu-id="5d59e-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5d59e-124">Requirement</span></span> | <span data-ttu-id="5d59e-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="5d59e-125">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="5d59e-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="5d59e-126">Header</span></span><br/> | <dl> <span data-ttu-id="5d59e-127"><dt>WMP. h</dt></span><span class="sxs-lookup"><span data-stu-id="5d59e-127"><dt>Wmp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5d59e-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5d59e-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5d59e-129">**Interfaces pour Visual Basic .NET et C #**</span><span class="sxs-lookup"><span data-stu-id="5d59e-129">**Interfaces for Visual Basic .NET and C#**</span></span>](interfaces-for-visual-basic--net-and-c.md)
</dt> <dt>

[<span data-ttu-id="5d59e-130">**Interface IWMPMediaCollection (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="5d59e-130">**IWMPMediaCollection Interface (VB and C#)**</span></span>](iwmpmediacollection--vb-and-c.md)
</dt> </dl>

 

 





