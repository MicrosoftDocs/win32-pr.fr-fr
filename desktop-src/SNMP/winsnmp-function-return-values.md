---
title: Valeurs de retour de la fonction WinSNMP
description: La valeur de retour d’un appel de fonction WinSNMP peut être un handle vers une ressource que l’implémentation de l’WinSNMP Microsoft alloue pour l’application WinSNMP.
ms.assetid: f0723cc7-fa3b-4a72-93a0-49d40a1fedd5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48a8e42e7d27b1079398efb2970b385bfc4e732c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104031734"
---
# <a name="winsnmp-function-return-values"></a><span data-ttu-id="a011b-103">Valeurs de retour de la fonction WinSNMP</span><span class="sxs-lookup"><span data-stu-id="a011b-103">WinSNMP Function Return Values</span></span>

<span data-ttu-id="a011b-104">\[SNMP peut être utilisé dans les systèmes d’exploitation spécifiés dans la section Configuration requise.</span><span class="sxs-lookup"><span data-stu-id="a011b-104">\[SNMP is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="a011b-105">Il sera peut-être modifié ou indisponible dans les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="a011b-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="a011b-106">Utilisez plutôt [Windows Remote Management](/windows/desktop/WinRM/portal), qui est l’implémentation Microsoft de WS-Man.\]</span><span class="sxs-lookup"><span data-stu-id="a011b-106">Instead, use [Windows Remote Management](/windows/desktop/WinRM/portal), which is the Microsoft implementation of WS-Man.\]</span></span>

<span data-ttu-id="a011b-107">La valeur de retour d’un appel de fonction WinSNMP peut être un handle vers une ressource que l’implémentation de l’WinSNMP Microsoft alloue pour l’application WinSNMP.</span><span class="sxs-lookup"><span data-stu-id="a011b-107">The return value from a WinSNMP function call can be a handle to a resource that the Microsoft WinSNMP implementation allocates for the WinSNMP application.</span></span>

<span data-ttu-id="a011b-108">Le tableau suivant répertorie les cinq types de descripteurs de ressources que l’implémentation alloue.</span><span class="sxs-lookup"><span data-stu-id="a011b-108">The following table lists the five types of resource handles that the implementation allocates.</span></span>



| <span data-ttu-id="a011b-109">Type de handle</span><span class="sxs-lookup"><span data-stu-id="a011b-109">Handle type</span></span>    | <span data-ttu-id="a011b-110">Description</span><span class="sxs-lookup"><span data-stu-id="a011b-110">Description</span></span>                       |
|----------------|-----------------------------------|
| <span data-ttu-id="a011b-111">\_session HSNMP</span><span class="sxs-lookup"><span data-stu-id="a011b-111">HSNMP\_SESSION</span></span> | <span data-ttu-id="a011b-112">Handle vers une session WinSNMP</span><span class="sxs-lookup"><span data-stu-id="a011b-112">Handle to a WinSNMP session</span></span>       |
| <span data-ttu-id="a011b-113">\_entité HSNMP</span><span class="sxs-lookup"><span data-stu-id="a011b-113">HSNMP\_ENTITY</span></span>  | <span data-ttu-id="a011b-114">Handle vers une entité SNMP</span><span class="sxs-lookup"><span data-stu-id="a011b-114">Handle to an SNMP entity</span></span>          |
| <span data-ttu-id="a011b-115">\_contexte HSNMP</span><span class="sxs-lookup"><span data-stu-id="a011b-115">HSNMP\_CONTEXT</span></span> | <span data-ttu-id="a011b-116">Handle vers un contexte SNMP</span><span class="sxs-lookup"><span data-stu-id="a011b-116">Handle to an SNMP context</span></span>         |
| <span data-ttu-id="a011b-117">\_PDU HSNMP</span><span class="sxs-lookup"><span data-stu-id="a011b-117">HSNMP\_PDU</span></span>     | <span data-ttu-id="a011b-118">Handle vers une unité de données de protocole</span><span class="sxs-lookup"><span data-stu-id="a011b-118">Handle to a protocol data unit</span></span>    |
| <span data-ttu-id="a011b-119">HSNMP \_ VBL</span><span class="sxs-lookup"><span data-stu-id="a011b-119">HSNMP\_VBL</span></span>     | <span data-ttu-id="a011b-120">Handle vers une liste de liaisons de variables</span><span class="sxs-lookup"><span data-stu-id="a011b-120">Handle to a variable binding list</span></span> |



 

<span data-ttu-id="a011b-121">Pour plus d’informations, consultez [objets descripteur de ressource](resource-handle-objects.md).</span><span class="sxs-lookup"><span data-stu-id="a011b-121">For more information, see [Resource Handle Objects](resource-handle-objects.md).</span></span>

<span data-ttu-id="a011b-122">La valeur de retour peut également être une valeur d’entier long non signé du type **smiUINT32** qui représente une \_ valeur d’État SNMPAPI.</span><span class="sxs-lookup"><span data-stu-id="a011b-122">The return value can also be an unsigned long integer value of the **smiUINT32** type that represents an SNMPAPI\_STATUS value.</span></span>

<span data-ttu-id="a011b-123">Le tableau suivant répertorie les valeurs d’État WinSNMP et leur signification.</span><span class="sxs-lookup"><span data-stu-id="a011b-123">The following table lists the WinSNMP status values and their meaning.</span></span>



| <span data-ttu-id="a011b-124">Statut</span><span class="sxs-lookup"><span data-stu-id="a011b-124">Status</span></span>           | <span data-ttu-id="a011b-125">Description</span><span class="sxs-lookup"><span data-stu-id="a011b-125">Description</span></span>                                                                      |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="a011b-126">échec de SNMPAPI \_</span><span class="sxs-lookup"><span data-stu-id="a011b-126">SNMPAPI\_FAILURE</span></span> | <span data-ttu-id="a011b-127">Indique une erreur.</span><span class="sxs-lookup"><span data-stu-id="a011b-127">Indicates an error.</span></span> <span data-ttu-id="a011b-128">Équivaut à 0 ou **null**.</span><span class="sxs-lookup"><span data-stu-id="a011b-128">Equates to 0 or **NULL**.</span></span>                                    |
| <span data-ttu-id="a011b-129">réussite de SNMPAPI \_</span><span class="sxs-lookup"><span data-stu-id="a011b-129">SNMPAPI\_SUCCESS</span></span> | <span data-ttu-id="a011b-130">Indique que la fonction s’est terminée avec succès.</span><span class="sxs-lookup"><span data-stu-id="a011b-130">Indicates the function completed successfully.</span></span> <span data-ttu-id="a011b-131">Équivaut à 1 ou à un nombre positif.</span><span class="sxs-lookup"><span data-stu-id="a011b-131">Equates to 1 or a positive count.</span></span> |



 

 

 