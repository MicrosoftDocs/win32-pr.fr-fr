---
title: Codes d’erreur WinSNMP
description: Codes d’erreur WinSNMP
ms.assetid: 03b13b82-a31c-47e2-8b4d-17dcc4d19e56
keywords:
- Codes d’erreur WinSNMP SNMP
- Codes d’erreur SNMP, WinSNMP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6d3cff7bd1e534f5f9c1fb0ae2ea2687d2ba99a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104463570"
---
# <a name="winsnmp-error-codes"></a><span data-ttu-id="81ff7-105">Codes d’erreur WinSNMP</span><span class="sxs-lookup"><span data-stu-id="81ff7-105">WinSNMP Error Codes</span></span>

<span data-ttu-id="81ff7-106">\[SNMP peut être utilisé dans les systèmes d’exploitation spécifiés dans la section Configuration requise.</span><span class="sxs-lookup"><span data-stu-id="81ff7-106">\[SNMP is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="81ff7-107">Il sera peut-être modifié ou indisponible dans les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="81ff7-107">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="81ff7-108">Utilisez plutôt [Windows Remote Management](/windows/desktop/WinRM/portal), qui est l’implémentation Microsoft de WS-Man.\]</span><span class="sxs-lookup"><span data-stu-id="81ff7-108">Instead, use [Windows Remote Management](/windows/desktop/WinRM/portal), which is the Microsoft implementation of WS-Man.\]</span></span>

> [!Note]  
> <span data-ttu-id="81ff7-109">Les erreurs décrites dans cette rubrique sont distinctes des codes d’erreur SNMP définis par les RFC pertinentes.</span><span class="sxs-lookup"><span data-stu-id="81ff7-109">The errors described in this topic are distinct from the SNMP error codes defined by the relevant RFCs.</span></span>

 

<span data-ttu-id="81ff7-110">Toutes les fonctions WinSNMP retournent la valeur **SNMPAPI \_ Failure** si la fonction échoue.</span><span class="sxs-lookup"><span data-stu-id="81ff7-110">All WinSNMP functions return the value **SNMPAPI\_FAILURE** if the function fails.</span></span> <span data-ttu-id="81ff7-111">L’application WinSNMP doit immédiatement appeler la fonction [**SnmpGetLastError**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetlasterror) pour récupérer les informations d’erreur étendues lorsqu’une fonction WinSNMP échoue.</span><span class="sxs-lookup"><span data-stu-id="81ff7-111">The WinSNMP application must immediately call the [**SnmpGetLastError**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetlasterror) function to retrieve extended error information when a WinSNMP function fails.</span></span> <span data-ttu-id="81ff7-112">Le tableau suivant répertorie les rubriques qui traitent des codes d’erreur étendus retournés par les fonctions WinSNMP.</span><span class="sxs-lookup"><span data-stu-id="81ff7-112">The following table lists topics that discuss extended error codes returned by WinSNMP functions.</span></span>



| <span data-ttu-id="81ff7-113">Rubrique</span><span class="sxs-lookup"><span data-stu-id="81ff7-113">Topic</span></span>                                                        | <span data-ttu-id="81ff7-114">Description</span><span class="sxs-lookup"><span data-stu-id="81ff7-114">Description</span></span>                                             |
|--------------------------------------------------------------|---------------------------------------------------------|
| [<span data-ttu-id="81ff7-115">Codes d’erreur courants WinSNMP</span><span class="sxs-lookup"><span data-stu-id="81ff7-115">WinSNMP Common Error Codes</span></span>](winsnmp-common-error-codes.md) | <span data-ttu-id="81ff7-116">Décrit les codes d’erreur courants pour l’API WinSNMP.</span><span class="sxs-lookup"><span data-stu-id="81ff7-116">Describes common error codes for the WinSNMP API.</span></span>       |
| [<span data-ttu-id="81ff7-117">Erreurs de transport réseau</span><span class="sxs-lookup"><span data-stu-id="81ff7-117">Network Transport Errors</span></span>](network-transport-errors.md)     | <span data-ttu-id="81ff7-118">Décrit les erreurs de transport réseau pour l’API WinSNMP.</span><span class="sxs-lookup"><span data-stu-id="81ff7-118">Describes network transport errors for the WinSNMP API.</span></span> |



 

<span data-ttu-id="81ff7-119">Les erreurs WinSNMP qui transmettent des informations spécifiques au contexte sont incluses dans la page de référence de la fonction.</span><span class="sxs-lookup"><span data-stu-id="81ff7-119">The WinSNMP errors that convey context-specific information are included in the function reference page.</span></span>

 

 