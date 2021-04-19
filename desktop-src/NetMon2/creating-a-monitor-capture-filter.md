---
description: La création d’un filtre de capture qui fonctionne avec Moniteur réseau est un processus en cinq étapes.
ms.assetid: 04be791c-43c5-44c2-8ab0-799a99974bf6
title: Création d’un filtre de capture d’analyse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 097a8276bd6a1f311b343787b3f06175d9b7091f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106527214"
---
# <a name="creating-a-monitor-capture-filter"></a><span data-ttu-id="a4651-103">Création d’un filtre de capture d’analyse</span><span class="sxs-lookup"><span data-stu-id="a4651-103">Creating a Monitor Capture Filter</span></span>

<span data-ttu-id="a4651-104">La création d’un filtre de capture qui fonctionne avec Moniteur réseau est un processus en cinq étapes :</span><span class="sxs-lookup"><span data-stu-id="a4651-104">Creating a capture filter that works with Network Monitor is a five-step process:</span></span>

-   [<span data-ttu-id="a4651-105">Définition du filtre ETYPE ou SAP</span><span class="sxs-lookup"><span data-stu-id="a4651-105">Setting the Etype or SAP Filter</span></span>](writing-etypesap-filter-portion.md)
-   [<span data-ttu-id="a4651-106">Écriture du filtre ADDRESSTABLE</span><span class="sxs-lookup"><span data-stu-id="a4651-106">Writing ADDRESSTABLE Filter</span></span>](writing-addresstable-filter-portion.md)
-   [<span data-ttu-id="a4651-107">Écriture du filtre PATTERNMATCH</span><span class="sxs-lookup"><span data-stu-id="a4651-107">Writing the PATTERNMATCH Filter</span></span>](writing-the-patternmatch-filter.md)
-   [<span data-ttu-id="a4651-108">Découpage d’un frame</span><span class="sxs-lookup"><span data-stu-id="a4651-108">Clipping a Frame</span></span>](clipping-a-frame.md)
-   [<span data-ttu-id="a4651-109">Implémentation du code de filtre de capture</span><span class="sxs-lookup"><span data-stu-id="a4651-109">Implementing the Capture Filter Code</span></span>](implementing-the-capture-filter-code.md)

<span data-ttu-id="a4651-110">Un [*filtre de capture*](c.md) est une série d’ajouts à l’objet BLOB NPP qui sélectionne les frames qui sont renvoyés à l’analyse.</span><span class="sxs-lookup"><span data-stu-id="a4651-110">A [*capture filter*](c.md) is a series of additions to the NPP BLOB that selects which frames are passed back to the monitor.</span></span> <span data-ttu-id="a4651-111">Si une analyse ne modifie pas l’objet BLOB NPP, le NPP passe en mode promiscuité et envoie tout le trafic réseau à l’analyse.</span><span class="sxs-lookup"><span data-stu-id="a4651-111">If a monitor does not alter the NPP BLOB, then the NPP will go into promiscuous mode and send all network traffic to the monitor.</span></span> <span data-ttu-id="a4651-112">Le NPP est plus efficace s’il peut réduire les données transmises à un pilote, de sorte qu’une analyse doit créer un filtre de capture.</span><span class="sxs-lookup"><span data-stu-id="a4651-112">The NPP is most efficient if it can reduce the data handed up to a driver, so a monitor should create a capture filter.</span></span> <span data-ttu-id="a4651-113">Une analyse définit son filtre de capture en écrivant dans l’objet BLOB NPP dans l’appel à la fonction [configure](imonitor-doconfigure.md) .</span><span class="sxs-lookup"><span data-stu-id="a4651-113">A monitor sets its capture filter by writing to the NPP BLOB in the call to the [DoConfigure](imonitor-doconfigure.md) function.</span></span> <span data-ttu-id="a4651-114">Le MCSVC appelle ensuite le NPP avec l’objet BLOB NPP.</span><span class="sxs-lookup"><span data-stu-id="a4651-114">The MCSVC then calls the NPP with the NPP BLOB.</span></span> <span data-ttu-id="a4651-115">Pour plus d’informations sur le filtre de capture, les [fournisseurs de paquets réseau](network-packet-providers.md) sur NPPs et les [objets BLOB Moniteur réseau](network-monitor-blobs.md) sur les fonctions BLOB, consultez filtres de [capture](capture-filters.md) .</span><span class="sxs-lookup"><span data-stu-id="a4651-115">See [Capture Filters](capture-filters.md) for more details on the capture filter, [Network Packet Providers](network-packet-providers.md) on NPPs, and [Network Monitor Blobs](network-monitor-blobs.md) on BLOB functions.</span></span>

 

 



