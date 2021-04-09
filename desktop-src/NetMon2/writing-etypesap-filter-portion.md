---
description: La partie ETYPE/SAP du filtre de capture notifie au pilote Moniteur réseau d’accepter des frames qui ont une combinaison spécifique de ETYPE et de points d’accès de service (SAP).
ms.assetid: 57dcf1cd-f27f-4bd3-a5a8-9e978a2d213e
title: Écriture de la portion de filtre ETYPE/SAP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b072d123ca18d3aa2b3f2c91db4a8461473a854
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103952589"
---
# <a name="writing-etypesap-filter-portion"></a><span data-ttu-id="2a2fc-103">Écriture de la portion de filtre ETYPE/SAP</span><span class="sxs-lookup"><span data-stu-id="2a2fc-103">Writing Etype/SAP Filter Portion</span></span>

<span data-ttu-id="2a2fc-104">La partie ETYPE/SAP du filtre de capture notifie au pilote Moniteur réseau d’accepter des frames qui ont une combinaison spécifique de ETYPE et de [*points d’accès de service*](s.md) (SAP).</span><span class="sxs-lookup"><span data-stu-id="2a2fc-104">The Etype/SAP portion of the capture filter notifies the Network Monitor driver to accept frames that have a specific combination of Etypes and [*service access points*](s.md) (SAPs).</span></span> <span data-ttu-id="2a2fc-105">Les types ETYPE et SAP sont les deux façons dont les protocoles de bas niveau tels que Ethernet, LLC et Snap indiquent le protocole qui les suit.</span><span class="sxs-lookup"><span data-stu-id="2a2fc-105">Etypes and SAPs are both ways that low-level protocols such as Ethernet, LLC, and Snap indicate which protocol follows them.</span></span> <span data-ttu-id="2a2fc-106">Plus précisément :</span><span class="sxs-lookup"><span data-stu-id="2a2fc-106">Specifically:</span></span>

-   <span data-ttu-id="2a2fc-107">Ethernet spécifie un ETYPE</span><span class="sxs-lookup"><span data-stu-id="2a2fc-107">Ethernet specifies an Etype</span></span>
-   <span data-ttu-id="2a2fc-108">LLC spécifie un SAP</span><span class="sxs-lookup"><span data-stu-id="2a2fc-108">LLC specifies a SAP</span></span>
-   <span data-ttu-id="2a2fc-109">Le magnétisme spécifie un ETYPE</span><span class="sxs-lookup"><span data-stu-id="2a2fc-109">Snap specifies an Etype</span></span>

## <a name="etypesap-capture-filter-flags"></a><span data-ttu-id="2a2fc-110">Indicateurs de filtre de capture ETYPE/SAP</span><span class="sxs-lookup"><span data-stu-id="2a2fc-110">Etype/SAP Capture Filter Flags</span></span>

<span data-ttu-id="2a2fc-111">Utilisez les informations suivantes pour définir les indicateurs dans le membre **FilterFlags** de la structure [**capturefilter**](capturefilter.md) .</span><span class="sxs-lookup"><span data-stu-id="2a2fc-111">Use the following information to set the flags in the **FilterFlags** member of the [**CAPTUREFILTER**](capturefilter.md) structure.</span></span>



| <span data-ttu-id="2a2fc-112">Indicateur</span><span class="sxs-lookup"><span data-stu-id="2a2fc-112">Flag</span></span>                                         | <span data-ttu-id="2a2fc-113">Signification</span><span class="sxs-lookup"><span data-stu-id="2a2fc-113">Meaning</span></span>                                                                                                                                                                                                                                                     |
|----------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2a2fc-114">\_les indicateurs capturefilter \_ incluent \_ tous les \_ SAP</span><span class="sxs-lookup"><span data-stu-id="2a2fc-114">CAPTUREFILTER\_ FLAGS\_INCLUDE\_ ALL\_SAPS</span></span>   | <span data-ttu-id="2a2fc-115">Transmet toutes les valeurs SAP et notifie au pilote que toutes les valeurs SAP sont valides.</span><span class="sxs-lookup"><span data-stu-id="2a2fc-115">Passes all SAP values and notifies the driver that all SAP values are valid.</span></span> <span data-ttu-id="2a2fc-116">En cas de combinaison avec toutes les valeurs du membre **lpSapTable** , cet indicateur informe le pilote que toutes les valeurs SAP, à l’exception de celles du **lpSapTable** , sont valides.</span><span class="sxs-lookup"><span data-stu-id="2a2fc-116">If combined with any values in the **lpSapTable** member, this flag notifies the driver that all SAP values except those in the **lpSapTable** are valid.</span></span><br/>           |
| <span data-ttu-id="2a2fc-117">\_les indicateurs capturefilter \_ incluent \_ tous les \_ ETYPE</span><span class="sxs-lookup"><span data-stu-id="2a2fc-117">CAPTUREFILTER\_ FLAGS\_INCLUDE\_ ALL\_ETYPES</span></span> | <span data-ttu-id="2a2fc-118">Passe toutes les valeurs ETYPE et notifie au pilote que toutes les valeurs ETYPE sont valides.</span><span class="sxs-lookup"><span data-stu-id="2a2fc-118">Passes all Etype values and notifies the driver that all Etype values are valid.</span></span> <span data-ttu-id="2a2fc-119">En cas de combinaison avec toutes les valeurs du membre **lpEtypeTable** , cet indicateur informe le pilote que toutes les valeurs ETYPE, à l’exception de celles du **lpEtypeTable** , sont valides.</span><span class="sxs-lookup"><span data-stu-id="2a2fc-119">If combined with any values in the **lpEtypeTable** member, this flag notifies the driver that all Etype values except those in the **lpEtypeTable** are valid.</span></span><br/> |
| <span data-ttu-id="2a2fc-120">\_indicateurs capturefilter \_ locaux \_ uniquement</span><span class="sxs-lookup"><span data-stu-id="2a2fc-120">CAPTUREFILTER\_ FLAGS\_LOCAL\_ONLY</span></span>           | <span data-ttu-id="2a2fc-121">La définition de cet indicateur ne définit pas une carte réseau en mode P.</span><span class="sxs-lookup"><span data-stu-id="2a2fc-121">Setting this flag will not set a NIC to P-Mode.</span></span> <span data-ttu-id="2a2fc-122">Vous verrez uniquement le trafic local (tous les frames sur l’ordinateur local).</span><span class="sxs-lookup"><span data-stu-id="2a2fc-122">You will only see local traffic (any frames to the local machine).</span></span>                                                                                                                                          |
| <span data-ttu-id="2a2fc-123">les \_ indicateurs capturefilter \_ conservent \_ RAW</span><span class="sxs-lookup"><span data-stu-id="2a2fc-123">CAPTUREFILTER\_ FLAGS\_KEEP\_RAW</span></span>             | <span data-ttu-id="2a2fc-124">Conserve les trames de SMT et Token Ring MAC.</span><span class="sxs-lookup"><span data-stu-id="2a2fc-124">Keeps SMT and Token Ring MAC frames.</span></span>                                                                                                                                                                                                                        |



 

## <a name="etypesap-capture-filter-settings"></a><span data-ttu-id="2a2fc-125">Paramètres du filtre ETYPE/SAP capture</span><span class="sxs-lookup"><span data-stu-id="2a2fc-125">Etype/SAP Capture Filter Settings</span></span>

<span data-ttu-id="2a2fc-126">Utilisez les informations suivantes pour définir les membres **lpSapTable** et **lpEtypeTable** de la structure [**capturefilter**](capturefilter.md) .</span><span class="sxs-lookup"><span data-stu-id="2a2fc-126">Use the following information to set the **lpSapTable** and **lpEtypeTable** members of the [**CAPTUREFILTER**](capturefilter.md) structure.</span></span>



| <span data-ttu-id="2a2fc-127">Paramètre</span><span class="sxs-lookup"><span data-stu-id="2a2fc-127">Setting</span></span>          | <span data-ttu-id="2a2fc-128">Signification</span><span class="sxs-lookup"><span data-stu-id="2a2fc-128">Meaning</span></span>                                                                                                                                                                                                                                                              |
|------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2a2fc-129">**lpSapTable**</span><span class="sxs-lookup"><span data-stu-id="2a2fc-129">**lpSapTable**</span></span>   | <span data-ttu-id="2a2fc-130">Répertorie les valeurs SAP que le pilote doit passer.</span><span class="sxs-lookup"><span data-stu-id="2a2fc-130">Lists the SAP values that you want the driver to pass.</span></span> <span data-ttu-id="2a2fc-131">Cette liste indique au pilote Moniteur réseau de valider les frames qui contiennent une correspondance.</span><span class="sxs-lookup"><span data-stu-id="2a2fc-131">This list tells the Network Monitor driver to validate any frame that contains a match.</span></span> <span data-ttu-id="2a2fc-132">Si \_ les indicateurs capturefilter \_ incluent \_ tous les \_ SAP sont définis, cela devient une liste d’exceptions (si elle est trouvée, ne réussit pas).</span><span class="sxs-lookup"><span data-stu-id="2a2fc-132">If CAPTUREFILTER\_FLAGS\_INCLUDE\_ALL\_SAPS is set, this becomes an exception list (if found, do not pass).</span></span>           |
| <span data-ttu-id="2a2fc-133">**lpEtypeTable**</span><span class="sxs-lookup"><span data-stu-id="2a2fc-133">**lpEtypeTable**</span></span> | <span data-ttu-id="2a2fc-134">Répertorie les valeurs ETYPE que vous souhaitez que le pilote de Moniteur réseau passe.</span><span class="sxs-lookup"><span data-stu-id="2a2fc-134">Lists the Etype values that you want the Network Monitor driver to pass.</span></span> <span data-ttu-id="2a2fc-135">Cette liste indique uniquement au pilote de valider toute trame qui contient une correspondance.</span><span class="sxs-lookup"><span data-stu-id="2a2fc-135">This list alone tells the driver to validate any frame that contains a match.</span></span> <span data-ttu-id="2a2fc-136">Si \_ les indicateurs capturefilter \_ incluent \_ tous les \_ ETYPE sont définis, cela devient une liste d’exceptions (si elle est trouvée, ne passe pas).</span><span class="sxs-lookup"><span data-stu-id="2a2fc-136">If CAPTUREFILTER\_FLAGS\_INCLUDE\_ALL\_ETYPES is set, this becomes an exception list (if found, do not pass).</span></span> |



 

 

 




