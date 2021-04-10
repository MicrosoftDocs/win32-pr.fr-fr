---
description: Dans Moniteur réseau, le filtre de capture est défini par la structure CAPTUREFILTER.
ms.assetid: 03cd35f2-4da5-4ef6-b73f-0bf6e0e33135
title: Structure CAPTUREFILTER
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3962ef9828ce13a1d03c58e4d7744d2854624858
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103951259"
---
# <a name="the-capturefilter-structure"></a><span data-ttu-id="f63c8-103">Structure CAPTUREFILTER</span><span class="sxs-lookup"><span data-stu-id="f63c8-103">The CAPTUREFILTER Structure</span></span>

<span data-ttu-id="f63c8-104">Dans Moniteur réseau, le [filtre de capture](capture-filters.md) est défini par la structure [**capturefilter**](capturefilter.md) .</span><span class="sxs-lookup"><span data-stu-id="f63c8-104">In Network Monitor, the [capture filter](capture-filters.md) is defined by the [**CAPTUREFILTER**](capturefilter.md) structure.</span></span> <span data-ttu-id="f63c8-105">L’absence ou la combinaison d’indicateurs, de valeurs et d’expressions détermine les frames qui seront transmis ou supprimés par le pilote Moniteur réseau.</span><span class="sxs-lookup"><span data-stu-id="f63c8-105">The absence or combination of flags, values, and expressions determines which frames will be passed on or dropped by the Network Monitor driver.</span></span> <span data-ttu-id="f63c8-106">L’illustration suivante montre les trois zones de l’analyse de filtre de capture : ETYPE/SAP, adresse et correspondance de modèle.</span><span class="sxs-lookup"><span data-stu-id="f63c8-106">The following illustration shows the three areas of the capture filter analysis: Etype/SAP, address, and pattern match.</span></span>

![trois zones de l’analyse de filtre de capture](images/capfilter.png)

<span data-ttu-id="f63c8-108">Le tableau suivant répertorie la fonction de chaque élément de filtre de capture.</span><span class="sxs-lookup"><span data-stu-id="f63c8-108">The following table lists the function of each capture filter element.</span></span>



| <span data-ttu-id="f63c8-109">Filter, élément</span><span class="sxs-lookup"><span data-stu-id="f63c8-109">Filter element</span></span>                                       | <span data-ttu-id="f63c8-110">Action</span><span class="sxs-lookup"><span data-stu-id="f63c8-110">Action</span></span>                                                                                                                                                                                                       |
|------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f63c8-111">ETYPE/SAP</span><span class="sxs-lookup"><span data-stu-id="f63c8-111">Etype/SAP</span></span>](writing-etypesap-filter-portion.md)     | <span data-ttu-id="f63c8-112">Évalue les paramètres ETYPE/SAP.</span><span class="sxs-lookup"><span data-stu-id="f63c8-112">Evaluates Etype/SAP settings.</span></span> <span data-ttu-id="f63c8-113">La combinaison d’indicateurs détermine les types de paramètres ou les valeurs qui sont inclus ou exclus.</span><span class="sxs-lookup"><span data-stu-id="f63c8-113">The combination of flags determines which setting types or values are included or excluded.</span></span>                                                                                    |
| [<span data-ttu-id="f63c8-114">Adresse</span><span class="sxs-lookup"><span data-stu-id="f63c8-114">Address</span></span>](writing-addresstable-filter-portion.md)   | <span data-ttu-id="f63c8-115">Évalue les adresses source et de destination et les paires d’adresses.</span><span class="sxs-lookup"><span data-stu-id="f63c8-115">Evaluates source and destination addresses and address pairs.</span></span> <span data-ttu-id="f63c8-116">Différentes combinaisons d’indicateurs déterminent les valeurs individuelles ou les combinaisons de paires d’adresses qui sont incluses ou exclues.</span><span class="sxs-lookup"><span data-stu-id="f63c8-116">Different combinations of flags determine which individual values or combinations of address pairs are included or excluded.</span></span>                   |
| [<span data-ttu-id="f63c8-117">Correspondance de modèle</span><span class="sxs-lookup"><span data-stu-id="f63c8-117">Pattern Match</span></span>](writing-the-patternmatch-filter.md) | <span data-ttu-id="f63c8-118">Définit des correspondances de modèle complexes dans un frame.</span><span class="sxs-lookup"><span data-stu-id="f63c8-118">Defines complex pattern matches within a frame.</span></span> <span data-ttu-id="f63c8-119">Les indicateurs sont fournis pour différents types et décalages.</span><span class="sxs-lookup"><span data-stu-id="f63c8-119">Flags are provided for different types and offsets.</span></span> <span data-ttu-id="f63c8-120">Vous pouvez combiner des correspondances de modèle avec des instructions AND logiques AND ou Operator.</span><span class="sxs-lookup"><span data-stu-id="f63c8-120">You can combine pattern matches with logical AND or OR operator statements.</span></span>                              |
| [<span data-ttu-id="f63c8-121">Portion</span><span class="sxs-lookup"><span data-stu-id="f63c8-121">Clipping</span></span>](clipping-a-frame.md)                     | <span data-ttu-id="f63c8-122">Découpe les trames d’une manière spécifiée par différentes valeurs d’octets.</span><span class="sxs-lookup"><span data-stu-id="f63c8-122">Clips frames in a manner specified by various byte values.</span></span> <span data-ttu-id="f63c8-123">Vous pouvez utiliser uniquement cet élément pour découper tous les frames ou les utiliser avec d’autres éléments de filtre de capture. par exemple, pour rechercher, puis détourer une image unique.</span><span class="sxs-lookup"><span data-stu-id="f63c8-123">You can use only this element to clip all frames or use it with other capture filter elements; for example, to find and then clip a single frame.</span></span> |
| [<span data-ttu-id="f63c8-124">**Stead**</span><span class="sxs-lookup"><span data-stu-id="f63c8-124">**Trigger**</span></span>](trigger.md)                           | <span data-ttu-id="f63c8-125">Cet élément de filtre de capture est obsolète.</span><span class="sxs-lookup"><span data-stu-id="f63c8-125">This capture filter element is obsolete.</span></span> <span data-ttu-id="f63c8-126">Les déclencheurs ne font plus partie d’un filtre de capture ; elles sont maintenant contenues dans leurs propres balises d’objet BLOB, qui sont spécifiées séparément.</span><span class="sxs-lookup"><span data-stu-id="f63c8-126">Triggers are no longer part of a capture filter; they are now contained in their own BLOB tags, which are specified separately.</span></span>                                     |



 

<span data-ttu-id="f63c8-127">Un frame est évalué par rapport aux trois parties du filtre de capture.</span><span class="sxs-lookup"><span data-stu-id="f63c8-127">A frame is evaluated against all three portions of the capture filter.</span></span> <span data-ttu-id="f63c8-128">Par conséquent, une trame transmise avec succès doit passer chaque élément.</span><span class="sxs-lookup"><span data-stu-id="f63c8-128">Therefore, a successfully transmitted frame must pass each element.</span></span> <span data-ttu-id="f63c8-129">N’oubliez pas que le pilote Moniteur réseau évalue l’absence de l’un des trois éléments comme **vrai**.</span><span class="sxs-lookup"><span data-stu-id="f63c8-129">Be aware that the Network Monitor driver evaluates the absence of any of the three elements as **TRUE**.</span></span> <span data-ttu-id="f63c8-130">Par exemple, le pilote évalue l’absence d’une section ETYPE/SAP en tant que « toutes les trames avec la valeur ETYPE/SAP sont valides ».</span><span class="sxs-lookup"><span data-stu-id="f63c8-130">For example, the driver evaluates the absence of an Etype/SAP section as "ALL frames with the ANY Etype/SAP value are valid."</span></span>

 

 



