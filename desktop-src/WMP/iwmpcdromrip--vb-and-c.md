---
title: Interface IWMPCdromRip (VB et C) (WMP. h)
description: Fournit des propriétés et des méthodes pour gérer la copie ou l’extraction des pistes d’un CD audio. l’extraction d’un CD à l’aide de l’interface IWMPCdromRip a le même effet que l’extraction de musique à l’aide de l’interface utilisateur du lecteur Windows Media.
ms.assetid: d7fbfc68-61b5-45bf-8df5-e3125a51a4d8
keywords:
- IWMPCdromRip (VB et C) interface Windows Media Player
- Interface IWMPCdromRip (VB et C), le lecteur Windows Media, décrit
topic_type:
- apiref
api_name:
- IWMPCdromRip (VB and C )
api_location:
- wmp.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7d069fd8bd727d6a2a380c2ef29ce7c086db88d0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540471"
---
# <a name="iwmpcdromrip-vb-and-c-interface"></a><span data-ttu-id="b7baa-105">Interface IWMPCdromRip (VB et C#)</span><span class="sxs-lookup"><span data-stu-id="b7baa-105">IWMPCdromRip (VB and C#) interface</span></span>

<span data-ttu-id="b7baa-106">Fournit des propriétés et des méthodes pour gérer la copie, ou l' *extraction*, des pistes d’un CD audio.</span><span class="sxs-lookup"><span data-stu-id="b7baa-106">Provides properties and methods to manage copying, or *ripping*, tracks from an audio CD.</span></span>

<span data-ttu-id="b7baa-107">L’extraction d’un CD à l’aide de l’interface **IWMPCdromRip** a le même effet que l’extraction de musique à l’aide de l’interface utilisateur du lecteur Windows Media.</span><span class="sxs-lookup"><span data-stu-id="b7baa-107">Ripping a CD by using the **IWMPCdromRip** interface has the same effect as ripping music by using the Windows Media Player user interface.</span></span> <span data-ttu-id="b7baa-108">Le contenu extrait est automatiquement ajouté à la bibliothèque en fonction des préférences de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="b7baa-108">Ripped content is automatically added to the library according to the user's preferences.</span></span> <span data-ttu-id="b7baa-109">Pour plus d’informations sur les préférences de l’utilisateur pour l’extraction de CD, consultez « extraction de musique à partir de CD » dans l’aide du lecteur Windows Media.</span><span class="sxs-lookup"><span data-stu-id="b7baa-109">For more information about user preferences for CD ripping, see "Ripping music from CDs" in Windows Media Player Help.</span></span>

<span data-ttu-id="b7baa-110">L’interface **IWMPCdromRip** expose les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="b7baa-110">The **IWMPCdromRip** interface exposes the following properties.</span></span>

## <a name="members"></a><span data-ttu-id="b7baa-111">Membres</span><span class="sxs-lookup"><span data-stu-id="b7baa-111">Members</span></span>

<span data-ttu-id="b7baa-112">L’interface **IWMPCdromRip (VB et C#)** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="b7baa-112">The **IWMPCdromRip (VB and C#)** interface has these types of members:</span></span>

-   [<span data-ttu-id="b7baa-113">Méthodes</span><span class="sxs-lookup"><span data-stu-id="b7baa-113">Methods</span></span>](#methods)
-   [<span data-ttu-id="b7baa-114">Propriétés</span><span class="sxs-lookup"><span data-stu-id="b7baa-114">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="b7baa-115">Méthodes</span><span class="sxs-lookup"><span data-stu-id="b7baa-115">Methods</span></span>

<span data-ttu-id="b7baa-116">L’interface **IWMPCdromRip (VB et C#)** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="b7baa-116">The **IWMPCdromRip (VB and C#)** interface has these methods.</span></span>



| <span data-ttu-id="b7baa-117">Méthode</span><span class="sxs-lookup"><span data-stu-id="b7baa-117">Method</span></span>                                                                 | <span data-ttu-id="b7baa-118">Description</span><span class="sxs-lookup"><span data-stu-id="b7baa-118">Description</span></span>                              |
|:-----------------------------------------------------------------------|:-----------------------------------------|
| [<span data-ttu-id="b7baa-119">**startRip**</span><span class="sxs-lookup"><span data-stu-id="b7baa-119">**startRip**</span></span>](wmplibiwmpcdromrip-iwmpcdromrip-startrip--vb-and-c.md) | <span data-ttu-id="b7baa-120">Déchirure du CD.</span><span class="sxs-lookup"><span data-stu-id="b7baa-120">Rips the CD.</span></span><br/>                  |
| [<span data-ttu-id="b7baa-121">**stopRip**</span><span class="sxs-lookup"><span data-stu-id="b7baa-121">**stopRip**</span></span>](wmplibiwmpcdromrip-iwmpcdromrip-stoprip--vb-and-c.md)   | <span data-ttu-id="b7baa-122">Arrête le processus d’extraction de CD.</span><span class="sxs-lookup"><span data-stu-id="b7baa-122">Stops the CD ripping process.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="b7baa-123">Propriétés</span><span class="sxs-lookup"><span data-stu-id="b7baa-123">Properties</span></span>

<span data-ttu-id="b7baa-124">L’interface **IWMPCdromRip (VB et C#)** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="b7baa-124">The **IWMPCdromRip (VB and C#)** interface has these properties.</span></span>



| <span data-ttu-id="b7baa-125">Propriété</span><span class="sxs-lookup"><span data-stu-id="b7baa-125">Property</span></span>                                                                                | <span data-ttu-id="b7baa-126">Type d’accès</span><span class="sxs-lookup"><span data-stu-id="b7baa-126">Access type</span></span>          | <span data-ttu-id="b7baa-127">Description</span><span class="sxs-lookup"><span data-stu-id="b7baa-127">Description</span></span>                                                                                   |
|:----------------------------------------------------------------------------------------|:---------------------|:----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b7baa-128">**ripProgress**</span><span class="sxs-lookup"><span data-stu-id="b7baa-128">**ripProgress**</span></span>](wmplibiwmpcdromrip-iwmpcdromrip-ripprogress--vb-and-c.md)<br/> | <span data-ttu-id="b7baa-129">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b7baa-129">Read-only</span></span><br/> | <span data-ttu-id="b7baa-130">Obtient la progression de l’extraction de CD comme pourcentage effectué.</span><span class="sxs-lookup"><span data-stu-id="b7baa-130">Gets the CD ripping progress as percent complete.</span></span><br/>                                  |
| [<span data-ttu-id="b7baa-131">**ripState**</span><span class="sxs-lookup"><span data-stu-id="b7baa-131">**ripState**</span></span>](wmplibiwmpcdromrip-iwmpcdromrip-ripstate--vb-and-c.md)<br/>       | <span data-ttu-id="b7baa-132">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b7baa-132">Read-only</span></span><br/> | <span data-ttu-id="b7baa-133">Obtient une valeur d’énumération qui indique l’état actuel du processus d’extraction.</span><span class="sxs-lookup"><span data-stu-id="b7baa-133">Gets an enumeration value that indicates the current state of the ripping process.</span></span><br/> |



 

<span data-ttu-id="b7baa-134">Procurez-vous une interface **IWMPCdromRip** en effectuant un cast de l’interface **IWMPCdrom** du CD que vous souhaitez extraire.</span><span class="sxs-lookup"><span data-stu-id="b7baa-134">Get an **IWMPCdromRip** interface by casting the **IWMPCdrom** interface of the CD that you wish to rip.</span></span>

## <a name="requirements"></a><span data-ttu-id="b7baa-135">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b7baa-135">Requirements</span></span>



| <span data-ttu-id="b7baa-136">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b7baa-136">Requirement</span></span> | <span data-ttu-id="b7baa-137">Valeur</span><span class="sxs-lookup"><span data-stu-id="b7baa-137">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="b7baa-138">En-tête</span><span class="sxs-lookup"><span data-stu-id="b7baa-138">Header</span></span><br/> | <dl> <span data-ttu-id="b7baa-139"><dt>WMP. h</dt></span><span class="sxs-lookup"><span data-stu-id="b7baa-139"><dt>Wmp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b7baa-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b7baa-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b7baa-141">**Interfaces pour Visual Basic .NET et C #**</span><span class="sxs-lookup"><span data-stu-id="b7baa-141">**Interfaces for Visual Basic .NET and C#**</span></span>](interfaces-for-visual-basic--net-and-c.md)
</dt> <dt>

[<span data-ttu-id="b7baa-142">**Extraction d’un CD**</span><span class="sxs-lookup"><span data-stu-id="b7baa-142">**Ripping a CD**</span></span>](ripping-a-cd.md)
</dt> </dl>

 

 





