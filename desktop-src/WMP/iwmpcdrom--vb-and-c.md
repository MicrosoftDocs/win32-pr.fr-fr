---
title: Interface IWMPCdrom (VB et C) (WMP. h)
description: Offre un moyen d’accéder à un CD ou un DVD dans son lecteur. L’interface IWMPCdrom expose les propriétés suivantes.
ms.assetid: 2748e64b-b9b7-489a-a6b5-21154aabd312
keywords:
- IWMPCdrom (VB et C) interface Windows Media Player
- Interface IWMPCdrom (VB et C), le lecteur Windows Media, décrit
topic_type:
- apiref
api_name:
- IWMPCdrom (VB and C )
api_location:
- wmp.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 036411c96b278023d87c37ad48f81e986b9dadcb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528132"
---
# <a name="iwmpcdrom-vb-and-c-interface"></a><span data-ttu-id="df57c-105">Interface IWMPCdrom (VB et C#)</span><span class="sxs-lookup"><span data-stu-id="df57c-105">IWMPCdrom (VB and C#) interface</span></span>

<span data-ttu-id="df57c-106">Offre un moyen d’accéder à un CD ou un DVD dans son lecteur.</span><span class="sxs-lookup"><span data-stu-id="df57c-106">Provides a way to access a CD or DVD in its drive.</span></span>

<span data-ttu-id="df57c-107">L’interface **IWMPCdrom** expose les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="df57c-107">The **IWMPCdrom** interface exposes the following properties.</span></span>

## <a name="members"></a><span data-ttu-id="df57c-108">Membres</span><span class="sxs-lookup"><span data-stu-id="df57c-108">Members</span></span>

<span data-ttu-id="df57c-109">L’interface **IWMPCdrom (VB et C#)** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="df57c-109">The **IWMPCdrom (VB and C#)** interface has these types of members:</span></span>

-   [<span data-ttu-id="df57c-110">Méthodes</span><span class="sxs-lookup"><span data-stu-id="df57c-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="df57c-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="df57c-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="df57c-112">Méthodes</span><span class="sxs-lookup"><span data-stu-id="df57c-112">Methods</span></span>

<span data-ttu-id="df57c-113">L’interface **IWMPCdrom (VB et C#)** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="df57c-113">The **IWMPCdrom (VB and C#)** interface has these methods.</span></span>



| <span data-ttu-id="df57c-114">Méthode</span><span class="sxs-lookup"><span data-stu-id="df57c-114">Method</span></span>                                                     | <span data-ttu-id="df57c-115">Description</span><span class="sxs-lookup"><span data-stu-id="df57c-115">Description</span></span>                                     |
|:-----------------------------------------------------------|:------------------------------------------------|
| [<span data-ttu-id="df57c-116">**émission**</span><span class="sxs-lookup"><span data-stu-id="df57c-116">**eject**</span></span>](wmplibiwmpcdrom-iwmpcdrom-eject--vb-and-c.md) | <span data-ttu-id="df57c-117">Éjecte le CD ou DVD du lecteur.</span><span class="sxs-lookup"><span data-stu-id="df57c-117">Ejects the CD or DVD from the drive.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="df57c-118">Propriétés</span><span class="sxs-lookup"><span data-stu-id="df57c-118">Properties</span></span>

<span data-ttu-id="df57c-119">L’interface **IWMPCdrom (VB et C#)** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="df57c-119">The **IWMPCdrom (VB and C#)** interface has these properties.</span></span>



| <span data-ttu-id="df57c-120">Propriété</span><span class="sxs-lookup"><span data-stu-id="df57c-120">Property</span></span>                                                                                | <span data-ttu-id="df57c-121">Type d’accès</span><span class="sxs-lookup"><span data-stu-id="df57c-121">Access type</span></span>          | <span data-ttu-id="df57c-122">Description</span><span class="sxs-lookup"><span data-stu-id="df57c-122">Description</span></span>                                                                                                                                  |
|:----------------------------------------------------------------------------------------|:---------------------|:---------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="df57c-123">**driveSpecifier**</span><span class="sxs-lookup"><span data-stu-id="df57c-123">**driveSpecifier**</span></span>](wmplibiwmpcdrom-iwmpcdrom-drivespecifier--vb-and-c.md)<br/> | <span data-ttu-id="df57c-124">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="df57c-124">Read-only</span></span><br/> | <span data-ttu-id="df57c-125">Obtient la lettre du lecteur de CD ou de DVD.</span><span class="sxs-lookup"><span data-stu-id="df57c-125">Gets the CD or DVD drive letter.</span></span><br/>                                                                                                  |
| [<span data-ttu-id="df57c-126">**Playlist**</span><span class="sxs-lookup"><span data-stu-id="df57c-126">**Playlist**</span></span>](wmplibiwmpcdrom-iwmpcdrom-playlist--vb-and-c.md)<br/>             | <span data-ttu-id="df57c-127">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="df57c-127">Read-only</span></span><br/> | <span data-ttu-id="df57c-128">Obtient une interface [**IWMPPlaylist**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplaylist) représentant les pistes sur un CD ou les entrées de titre au niveau de la racine d’un DVD.</span><span class="sxs-lookup"><span data-stu-id="df57c-128">Gets an [**IWMPPlaylist**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplaylist) interface representing the tracks on a CD or the root-level title entries for a DVD.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="df57c-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="df57c-129">Requirements</span></span>



| <span data-ttu-id="df57c-130">Condition requise</span><span class="sxs-lookup"><span data-stu-id="df57c-130">Requirement</span></span> | <span data-ttu-id="df57c-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="df57c-131">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="df57c-132">En-tête</span><span class="sxs-lookup"><span data-stu-id="df57c-132">Header</span></span><br/> | <dl> <span data-ttu-id="df57c-133"><dt>WMP. h</dt></span><span class="sxs-lookup"><span data-stu-id="df57c-133"><dt>Wmp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="df57c-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="df57c-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="df57c-135">**Interfaces pour Visual Basic .NET et C #**</span><span class="sxs-lookup"><span data-stu-id="df57c-135">**Interfaces for Visual Basic .NET and C#**</span></span>](interfaces-for-visual-basic--net-and-c.md)
</dt> <dt>

[<span data-ttu-id="df57c-136">**Interface IWMPPlaylist (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="df57c-136">**IWMPPlaylist Interface (VB and C#)**</span></span>](iwmpplaylist--vb-and-c.md)
</dt> </dl>

 

 





