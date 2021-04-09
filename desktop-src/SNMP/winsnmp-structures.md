---
title: Structures WinSNMP
description: Les fonctions de l’API WinSNMP utilisent les structures suivantes.
ms.assetid: ec74217e-8d02-4bda-b365-7b8f6c14cffb
keywords:
- SNMP structures WinSNMP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b263f6078171c096eb7208ae4c7ef29847aead9c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103842489"
---
# <a name="winsnmp-structures"></a><span data-ttu-id="36c8d-104">Structures WinSNMP</span><span class="sxs-lookup"><span data-stu-id="36c8d-104">WinSNMP Structures</span></span>

<span data-ttu-id="36c8d-105">\[SNMP peut être utilisé dans les systèmes d’exploitation spécifiés dans la section Configuration requise.</span><span class="sxs-lookup"><span data-stu-id="36c8d-105">\[SNMP is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="36c8d-106">Il sera peut-être modifié ou indisponible dans les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="36c8d-106">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="36c8d-107">Utilisez plutôt [Windows Remote Management](/windows/desktop/WinRM/portal), qui est l’implémentation Microsoft de WS-Man.\]</span><span class="sxs-lookup"><span data-stu-id="36c8d-107">Instead, use [Windows Remote Management](/windows/desktop/WinRM/portal), which is the Microsoft implementation of WS-Man.\]</span></span>

<span data-ttu-id="36c8d-108">Les fonctions de l’API WinSNMP utilisent les structures suivantes.</span><span class="sxs-lookup"><span data-stu-id="36c8d-108">The WinSNMP API functions use the following structures.</span></span>



| <span data-ttu-id="36c8d-109">Structure</span><span class="sxs-lookup"><span data-stu-id="36c8d-109">Structure</span></span>                                  | <span data-ttu-id="36c8d-110">Description</span><span class="sxs-lookup"><span data-stu-id="36c8d-110">Description</span></span>                                                                                                            |
|--------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="36c8d-111">**smiCNTR64**</span><span class="sxs-lookup"><span data-stu-id="36c8d-111">**smiCNTR64**</span></span>](/windows/desktop/api/Winsnmp/ns-winsnmp-smicntr64)         | <span data-ttu-id="36c8d-112">Contient une valeur d’entier non signé 64 bits qui représente un compteur.</span><span class="sxs-lookup"><span data-stu-id="36c8d-112">Contains a 64-bit unsigned integer value that represents a counter.</span></span>                                                    |
| [<span data-ttu-id="36c8d-113">**smiOCTETS**</span><span class="sxs-lookup"><span data-stu-id="36c8d-113">**smiOCTETS**</span></span>](/windows/desktop/api/Winsnmp/ns-winsnmp-smioctets)         | <span data-ttu-id="36c8d-114">Contient un pointeur vers une chaîne d’octets SNMP de longueur variable.</span><span class="sxs-lookup"><span data-stu-id="36c8d-114">Contains a pointer to an SNMP octet string of variable length.</span></span>                                                         |
| [<span data-ttu-id="36c8d-115">**smiOID**</span><span class="sxs-lookup"><span data-stu-id="36c8d-115">**smiOID**</span></span>](/windows/desktop/api/Winsnmp/ns-winsnmp-smioid)               | <span data-ttu-id="36c8d-116">Contient un pointeur vers un tableau de longueur variable des sous-identificateurs associés à un objet nommé spécifié.</span><span class="sxs-lookup"><span data-stu-id="36c8d-116">Contains a pointer to a variable length array of the subidentifiers that are associated with a specified named object.</span></span> |
| [<span data-ttu-id="36c8d-117">**smiVALUE**</span><span class="sxs-lookup"><span data-stu-id="36c8d-117">**smiVALUE**</span></span>](/windows/desktop/api/Winsnmp/ns-winsnmp-smivalue)           | <span data-ttu-id="36c8d-118">Représente la valeur associée à un nom de variable dans une entrée de liaison de variable.</span><span class="sxs-lookup"><span data-stu-id="36c8d-118">Represents the value that is associated with a variable name in a variable binding entry.</span></span>                              |
| [<span data-ttu-id="36c8d-119">**smiVENDORINFO**</span><span class="sxs-lookup"><span data-stu-id="36c8d-119">**smiVENDORINFO**</span></span>](/windows/desktop/api/Winsnmp/ns-winsnmp-smivendorinfo) | <span data-ttu-id="36c8d-120">Contient des informations sur l’implémentation Microsoft de WinSNMP.</span><span class="sxs-lookup"><span data-stu-id="36c8d-120">Contains information about the Microsoft implementation of WinSNMP.</span></span>                                                    |



 

 

 