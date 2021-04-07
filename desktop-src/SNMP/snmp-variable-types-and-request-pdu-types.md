---
title: Types de variables SNMP et types de PDU de demande
description: Les définitions de certains types de variable SNMP et les types de PDU de demande ont changé. Le fichier SNMP. h mappe les anciens types aux nouveaux types correspondants.
ms.assetid: 2d87aeee-6fcb-4837-b091-6a9def8a9acb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d656add1b177b50e24b30a11d9fe008dcdfdf9bc
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103728956"
---
# <a name="snmp-variable-types-and-request-pdu-types"></a><span data-ttu-id="c7ac6-104">Types de variables SNMP et types de PDU de demande</span><span class="sxs-lookup"><span data-stu-id="c7ac6-104">SNMP Variable Types and Request PDU Types</span></span>

<span data-ttu-id="c7ac6-105">\[SNMP peut être utilisé dans les systèmes d’exploitation spécifiés dans la section Configuration requise.</span><span class="sxs-lookup"><span data-stu-id="c7ac6-105">\[SNMP is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="c7ac6-106">Il sera peut-être modifié ou indisponible dans les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="c7ac6-106">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="c7ac6-107">Utilisez plutôt [Windows Remote Management](/windows/desktop/WinRM/portal), qui est l’implémentation Microsoft de WS-Man.\]</span><span class="sxs-lookup"><span data-stu-id="c7ac6-107">Instead, use [Windows Remote Management](/windows/desktop/WinRM/portal), which is the Microsoft implementation of WS-Man.\]</span></span>

<span data-ttu-id="c7ac6-108">Les définitions de certains types de variable SNMP et les types de PDU de demande ont changé.</span><span class="sxs-lookup"><span data-stu-id="c7ac6-108">The definitions for some SNMP variable types and request PDU types have changed.</span></span> <span data-ttu-id="c7ac6-109">Le fichier SNMP. h mappe les anciens types aux nouveaux types correspondants.</span><span class="sxs-lookup"><span data-stu-id="c7ac6-109">The Snmp.h file maps old types to the corresponding new types.</span></span>

## <a name="modified-snmp-variable-types"></a><span data-ttu-id="c7ac6-110">Types de variable SNMP modifiés</span><span class="sxs-lookup"><span data-stu-id="c7ac6-110">Modified SNMP Variable Types</span></span>

<span data-ttu-id="c7ac6-111">Vous devez utiliser les nouveaux types de variables SNMP listés dans le tableau ci-dessous lorsque vous développez des applications de gestionnaire qui utilisent l’API de gestion SNMP de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="c7ac6-111">You should use the new SNMP variable types listed in the following table when you develop manager applications that use the Microsoft SNMP Management API.</span></span> <span data-ttu-id="c7ac6-112">Le tableau répertorie les anciens types de variable SNMP avec les nouveaux types de variables correspondants.</span><span class="sxs-lookup"><span data-stu-id="c7ac6-112">The table lists the old SNMP variable types with the corresponding new variable types.</span></span>

| <span data-ttu-id="c7ac6-113">Ancien type de variable</span><span class="sxs-lookup"><span data-stu-id="c7ac6-113">Old variable type</span></span>        | <span data-ttu-id="c7ac6-114">Nouveau type de variable</span><span class="sxs-lookup"><span data-stu-id="c7ac6-114">New variable type</span></span> |
|--------------------------|-------------------|
| <span data-ttu-id="c7ac6-115">\_ \_ Adresse IP ASN RFC1155</span><span class="sxs-lookup"><span data-stu-id="c7ac6-115">ASN\_RFC1155\_IPADDRESS</span></span>  | <span data-ttu-id="c7ac6-116">\_adresse IP ASN</span><span class="sxs-lookup"><span data-stu-id="c7ac6-116">ASN\_IPADDRESS</span></span>    |
| <span data-ttu-id="c7ac6-117">\_Compteur RFC1155 \_ ASN</span><span class="sxs-lookup"><span data-stu-id="c7ac6-117">ASN\_RFC1155\_COUNTER</span></span>    | <span data-ttu-id="c7ac6-118">\_COUNTER32 ASN</span><span class="sxs-lookup"><span data-stu-id="c7ac6-118">ASN\_COUNTER32</span></span>    |
| <span data-ttu-id="c7ac6-119">\_Jauge ASN RFC1155 \_</span><span class="sxs-lookup"><span data-stu-id="c7ac6-119">ASN\_RFC1155\_GAUGE</span></span>      | <span data-ttu-id="c7ac6-120">\_Gauge32 ASN</span><span class="sxs-lookup"><span data-stu-id="c7ac6-120">ASN\_GAUGE32</span></span>      |
| <span data-ttu-id="c7ac6-121">ASN \_ RFC1155 \_ graduations</span><span class="sxs-lookup"><span data-stu-id="c7ac6-121">ASN\_RFC1155\_TIMETICKS</span></span>  | <span data-ttu-id="c7ac6-122">\_graduations ASN</span><span class="sxs-lookup"><span data-stu-id="c7ac6-122">ASN\_TIMETICKS</span></span>    |
| <span data-ttu-id="c7ac6-123">\_RFC1155 ASN \_ opaque</span><span class="sxs-lookup"><span data-stu-id="c7ac6-123">ASN\_RFC1155\_OPAQUE</span></span>     | <span data-ttu-id="c7ac6-124">ASN \_ opaque</span><span class="sxs-lookup"><span data-stu-id="c7ac6-124">ASN\_OPAQUE</span></span>       |
| <span data-ttu-id="c7ac6-125">ASN \_ RFC1213 \_ DISPSTRING</span><span class="sxs-lookup"><span data-stu-id="c7ac6-125">ASN\_RFC1213\_DISPSTRING</span></span> | <span data-ttu-id="c7ac6-126">\_OCTETSTRING ASN</span><span class="sxs-lookup"><span data-stu-id="c7ac6-126">ASN\_OCTETSTRING</span></span>  |



 

## <a name="modified-snmp-pdu-request-types"></a><span data-ttu-id="c7ac6-127">Types de demandes PDU SNMP modifiés</span><span class="sxs-lookup"><span data-stu-id="c7ac6-127">Modified SNMP PDU Request Types</span></span>

<span data-ttu-id="c7ac6-128">Vous devez utiliser les nouveaux types de PDU SNMP figurant dans le tableau ci-dessous lorsque vous développez des applications de gestionnaire qui utilisent l’API de gestion SNMP de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="c7ac6-128">You should use the new SNMP PDU types listed in the following table when you develop manager applications that use the Microsoft SNMP Management API.</span></span> <span data-ttu-id="c7ac6-129">Le tableau répertorie les anciens types de PDU SNMP avec les nouveaux types de PDU correspondants.</span><span class="sxs-lookup"><span data-stu-id="c7ac6-129">The table lists the old SNMP PDU types with the corresponding new PDU types.</span></span>

| <span data-ttu-id="c7ac6-130">Ancien type d’unité d’alimentation</span><span class="sxs-lookup"><span data-stu-id="c7ac6-130">Old PDU type</span></span>                 | <span data-ttu-id="c7ac6-131">Nouveau type de PDU</span><span class="sxs-lookup"><span data-stu-id="c7ac6-131">New PDU type</span></span>        |
|------------------------------|---------------------|
| <span data-ttu-id="c7ac6-132">ASN \_ RFC1157 \_ GETREQUEST</span><span class="sxs-lookup"><span data-stu-id="c7ac6-132">ASN\_RFC1157\_GETREQUEST</span></span>     | <span data-ttu-id="c7ac6-133">\_récupération du PDU SNMP \_</span><span class="sxs-lookup"><span data-stu-id="c7ac6-133">SNMP\_PDU\_GET</span></span>      |
| <span data-ttu-id="c7ac6-134">ASN \_ RFC1157 \_ GETNEXTREQUEST</span><span class="sxs-lookup"><span data-stu-id="c7ac6-134">ASN\_RFC1157\_GETNEXTREQUEST</span></span> | <span data-ttu-id="c7ac6-135">\_PDU SNMP \_ GetNext</span><span class="sxs-lookup"><span data-stu-id="c7ac6-135">SNMP\_PDU\_GETNEXT</span></span>  |
| <span data-ttu-id="c7ac6-136">ASN \_ RFC1157 \_ GETRESPONSE</span><span class="sxs-lookup"><span data-stu-id="c7ac6-136">ASN\_RFC1157\_GETRESPONSE</span></span>    | <span data-ttu-id="c7ac6-137">\_réponse PDU \_ SNMP</span><span class="sxs-lookup"><span data-stu-id="c7ac6-137">SNMP\_PDU\_RESPONSE</span></span> |
| <span data-ttu-id="c7ac6-138">ASN \_ RFC1157 \_ SETREQUEST</span><span class="sxs-lookup"><span data-stu-id="c7ac6-138">ASN\_RFC1157\_SETREQUEST</span></span>     | <span data-ttu-id="c7ac6-139">\_ensemble d’PDU SNMP \_</span><span class="sxs-lookup"><span data-stu-id="c7ac6-139">SNMP\_PDU\_SET</span></span>      |
| <span data-ttu-id="c7ac6-140">\_Interruption ASN RFC1157 \_</span><span class="sxs-lookup"><span data-stu-id="c7ac6-140">ASN\_RFC1157\_TRAP</span></span>           | <span data-ttu-id="c7ac6-141">\_V1TRAP PDU \_ SNMP</span><span class="sxs-lookup"><span data-stu-id="c7ac6-141">SNMP\_PDU\_V1TRAP</span></span>   |



 

 

 