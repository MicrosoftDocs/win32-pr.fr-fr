---
description: Chaque définition d’objet MIB contient une clause ACCESS (SNMPv1) ou MAX-ACCESS (SNMPv2C) qui définit les droits d’accès à l’objet.
ms.assetid: c3b8d65b-c1ca-4131-baf4-1aab54451180
ms.tgt_platform: multiple
title: Clauses Access et MAX-ACCESS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37084a25a48c874866774b990a70e1332e730103
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106523312"
---
# <a name="access-and-max-access-clauses"></a><span data-ttu-id="ac631-103">Clauses Access et MAX-ACCESS</span><span class="sxs-lookup"><span data-stu-id="ac631-103">ACCESS and MAX-ACCESS Clauses</span></span>

<span data-ttu-id="ac631-104">Chaque définition d’objet MIB contient une clause ACCESS (SNMPv1) ou MAX-ACCESS (SNMPv2C) qui définit les droits d’accès à l’objet.</span><span class="sxs-lookup"><span data-stu-id="ac631-104">Each MIB object definition contains either an ACCESS (SNMPv1) or MAX-ACCESS (SNMPv2C) clause that defines the access rights to the object.</span></span>

> [!Note]  
> <span data-ttu-id="ac631-105">Pour plus d’informations sur l’installation du fournisseur, consultez [configuration de l’environnement SNMP WMI](setting-up-the-wmi-snmp-environment.md).</span><span class="sxs-lookup"><span data-stu-id="ac631-105">For more information about installing the provider, see [Setting up the WMI SNMP Environment](setting-up-the-wmi-snmp-environment.md).</span></span>

 

<span data-ttu-id="ac631-106">Le tableau suivant répertorie le mappage de la clause d’accès SNMPv1.</span><span class="sxs-lookup"><span data-stu-id="ac631-106">The following table lists the mapping of the SNMPv1 ACCESS clause.</span></span>



| <span data-ttu-id="ac631-107">Clause d’accès MIB</span><span class="sxs-lookup"><span data-stu-id="ac631-107">MIB ACCESS clause</span></span> | <span data-ttu-id="ac631-108">Qualificateur CIM</span><span class="sxs-lookup"><span data-stu-id="ac631-108">CIM qualifier</span></span>       |
|-------------------|---------------------|
| <span data-ttu-id="ac631-109">en lecture seule</span><span class="sxs-lookup"><span data-stu-id="ac631-109">read-only</span></span>         | <span data-ttu-id="ac631-110">**Lire**</span><span class="sxs-lookup"><span data-stu-id="ac631-110">**Read**</span></span>            |
| <span data-ttu-id="ac631-111">lecture-écriture</span><span class="sxs-lookup"><span data-stu-id="ac631-111">read-write</span></span>        | <span data-ttu-id="ac631-112">**Lire**, **écrire**</span><span class="sxs-lookup"><span data-stu-id="ac631-112">**Read**, **Write**</span></span> |
| <span data-ttu-id="ac631-113">en écriture seule</span><span class="sxs-lookup"><span data-stu-id="ac631-113">write-only</span></span>        | <span data-ttu-id="ac631-114">**Écrire**</span><span class="sxs-lookup"><span data-stu-id="ac631-114">**Write**</span></span>           |
| <span data-ttu-id="ac631-115">non accessible</span><span class="sxs-lookup"><span data-stu-id="ac631-115">not-accessible</span></span>    | <span data-ttu-id="ac631-116">**Non \_ accessible**</span><span class="sxs-lookup"><span data-stu-id="ac631-116">**Not\_Accessible**</span></span> |



 

<span data-ttu-id="ac631-117">Le tableau suivant répertorie le mappage de la clause MAX-ACCESS SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="ac631-117">The following table lists the mapping of the SNMPv2C MAX-ACCESS clause.</span></span>



| <span data-ttu-id="ac631-118">MIB-clause d’accès</span><span class="sxs-lookup"><span data-stu-id="ac631-118">MIB-ACCESS clause</span></span>     | <span data-ttu-id="ac631-119">Qualificateur CIM</span><span class="sxs-lookup"><span data-stu-id="ac631-119">CIM qualifier</span></span>       |
|-----------------------|---------------------|
| <span data-ttu-id="ac631-120">en lecture seule</span><span class="sxs-lookup"><span data-stu-id="ac631-120">read-only</span></span>             | <span data-ttu-id="ac631-121">**Lire**</span><span class="sxs-lookup"><span data-stu-id="ac631-121">**Read**</span></span>            |
| <span data-ttu-id="ac631-122">lecture-écriture</span><span class="sxs-lookup"><span data-stu-id="ac631-122">read-write</span></span>            | <span data-ttu-id="ac631-123">**Lire**, **écrire**</span><span class="sxs-lookup"><span data-stu-id="ac631-123">**Read**, **Write**</span></span> |
| <span data-ttu-id="ac631-124">lecture-créer</span><span class="sxs-lookup"><span data-stu-id="ac631-124">read-create</span></span>           | <span data-ttu-id="ac631-125">**Lire**</span><span class="sxs-lookup"><span data-stu-id="ac631-125">**Read**</span></span>            |
| <span data-ttu-id="ac631-126">accessible-pour notification</span><span class="sxs-lookup"><span data-stu-id="ac631-126">accessible-for-notify</span></span> | <span data-ttu-id="ac631-127">**Non \_ accessible**</span><span class="sxs-lookup"><span data-stu-id="ac631-127">**Not\_Accessible**</span></span> |
| <span data-ttu-id="ac631-128">non accessible</span><span class="sxs-lookup"><span data-stu-id="ac631-128">not-accessible</span></span>        | <span data-ttu-id="ac631-129">**Non \_ accessible**</span><span class="sxs-lookup"><span data-stu-id="ac631-129">**Not\_Accessible**</span></span> |



 

<span data-ttu-id="ac631-130">Lorsqu’un objet MIB est mappé à not-accessible et n’est pas une propriété indexée de la classe, il n’existe aucun mappage de l’objet MIB lui-même.</span><span class="sxs-lookup"><span data-stu-id="ac631-130">When a MIB object maps to not-accessible and is not a keyed property of the class, there is no mapping of the MIB object itself.</span></span>

 

 



