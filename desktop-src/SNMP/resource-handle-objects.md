---
title: Objets de descripteur de ressource
description: La structure d’un objet de ressource est limitée à l’implémentation de l’WinSNMP Microsoft. Une application WinSNMP peut accéder à un objet de ressource avec un descripteur.
ms.assetid: c70a03b1-afac-4f1a-81e7-7f31430f5655
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef1afe5e6488190f95961bff7ce37f7b719d076d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103674906"
---
# <a name="resource-handle-objects"></a><span data-ttu-id="f8fff-104">Objets de descripteur de ressource</span><span class="sxs-lookup"><span data-stu-id="f8fff-104">Resource Handle Objects</span></span>

<span data-ttu-id="f8fff-105">La structure d’un objet de ressource est limitée à l’implémentation de l’WinSNMP Microsoft.</span><span class="sxs-lookup"><span data-stu-id="f8fff-105">The structure of a resource object is restricted to the Microsoft WinSNMP implementation.</span></span> <span data-ttu-id="f8fff-106">Une application WinSNMP peut accéder à un objet de ressource avec un descripteur.</span><span class="sxs-lookup"><span data-stu-id="f8fff-106">A WinSNMP application can access a resource object with a handle.</span></span>

<span data-ttu-id="f8fff-107">L’implémentation peut allouer l’un des types de descripteurs de ressources suivants pour une application WinSNMP.</span><span class="sxs-lookup"><span data-stu-id="f8fff-107">The implementation can allocate one of the following types of resource handles for a WinSNMP application.</span></span>

| <span data-ttu-id="f8fff-108">Type de handle</span><span class="sxs-lookup"><span data-stu-id="f8fff-108">Handle type</span></span>        | <span data-ttu-id="f8fff-109">Description</span><span class="sxs-lookup"><span data-stu-id="f8fff-109">Description</span></span>                       |
|--------------------|-----------------------------------|
| <span data-ttu-id="f8fff-110">**\_session HSNMP**</span><span class="sxs-lookup"><span data-stu-id="f8fff-110">**HSNMP\_SESSION**</span></span> | <span data-ttu-id="f8fff-111">Handle vers une session WinSNMP</span><span class="sxs-lookup"><span data-stu-id="f8fff-111">Handle to a WinSNMP session</span></span>       |
| <span data-ttu-id="f8fff-112">**\_entité HSNMP**</span><span class="sxs-lookup"><span data-stu-id="f8fff-112">**HSNMP\_ENTITY**</span></span>  | <span data-ttu-id="f8fff-113">Handle vers une entité SNMP</span><span class="sxs-lookup"><span data-stu-id="f8fff-113">Handle to an SNMP entity</span></span>          |
| <span data-ttu-id="f8fff-114">**\_contexte HSNMP**</span><span class="sxs-lookup"><span data-stu-id="f8fff-114">**HSNMP\_CONTEXT**</span></span> | <span data-ttu-id="f8fff-115">Handle vers un contexte WinSNMP</span><span class="sxs-lookup"><span data-stu-id="f8fff-115">Handle to a WinSNMP context</span></span>       |
| <span data-ttu-id="f8fff-116">**\_PDU HSNMP**</span><span class="sxs-lookup"><span data-stu-id="f8fff-116">**HSNMP\_PDU**</span></span>     | <span data-ttu-id="f8fff-117">Handle vers une unité de données de protocole</span><span class="sxs-lookup"><span data-stu-id="f8fff-117">Handle to a protocol data unit</span></span>    |
| <span data-ttu-id="f8fff-118">**HSNMP \_ VBL**</span><span class="sxs-lookup"><span data-stu-id="f8fff-118">**HSNMP\_VBL**</span></span>     | <span data-ttu-id="f8fff-119">Handle vers une liste de liaisons de variables</span><span class="sxs-lookup"><span data-stu-id="f8fff-119">Handle to a variable binding list</span></span> |



 

<span data-ttu-id="f8fff-120">Une application WinSNMP peut demander que l’implémentation crée ou supprime des handles de ressource, mais que l’implémentation effectue l’opération.</span><span class="sxs-lookup"><span data-stu-id="f8fff-120">A WinSNMP application can request that the implementation create or delete resource handles, but the implementation performs the operation.</span></span> <span data-ttu-id="f8fff-121">Pour plus d’informations sur la libération de ressources individuelles, consultez les fonctions [**SnmpFreeDescriptor**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreedescriptor), [**SnmpFreeVbl**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreevbl), [**SnmpFreePdu**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreepdu), [**SnmpFreeEntity**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreeentity)et [**SnmpFreeContext**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreecontext) .</span><span class="sxs-lookup"><span data-stu-id="f8fff-121">For additional information about freeing individual resources, see the [**SnmpFreeDescriptor**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreedescriptor), [**SnmpFreeVbl**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreevbl), [**SnmpFreePdu**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreepdu), [**SnmpFreeEntity**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreeentity), and [**SnmpFreeContext**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreecontext) functions.</span></span>

 

 




