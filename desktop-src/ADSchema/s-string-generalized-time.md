---
title: Syntaxe de chaîne (temps généralisé)
description: Format de chaîne d’heure défini par les normes ASN. 1. | Syntaxe de chaîne (temps généralisé)
ms.assetid: c69ab29b-5877-47d4-b58d-4f103758dfac
ms.tgt_platform: multiple
keywords:
- Schéma Active Directory de syntaxe de chaîne (temps généralisé)
topic_type:
- apiref
api_name:
- String(Generalized-Time)
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 81e754fe622d3ff6f010521b7bc9b9e4ff7a5f34
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104211449"
---
# <a name="stringgeneralized-time-syntax"></a><span data-ttu-id="fde6f-105">Syntaxe de chaîne (temps généralisé)</span><span class="sxs-lookup"><span data-stu-id="fde6f-105">String(Generalized-Time) syntax</span></span>

<span data-ttu-id="fde6f-106">Format de chaîne d’heure défini par les normes ASN. 1.</span><span class="sxs-lookup"><span data-stu-id="fde6f-106">A time string format defined by ASN.1 standards.</span></span> <span data-ttu-id="fde6f-107">Utilisez cette syntaxe pour stocker des valeurs d’heure au format Generalized-Time.</span><span class="sxs-lookup"><span data-stu-id="fde6f-107">Use this syntax for storing time values in Generalized-Time format.</span></span>

<span data-ttu-id="fde6f-108">Le format de la syntaxe de Generalized-Time est « AAAAMMJJHHMMSS. 0Z ».</span><span class="sxs-lookup"><span data-stu-id="fde6f-108">The format for the Generalized-Time syntax is "YYYYMMDDHHMMSS.0Z".</span></span> <span data-ttu-id="fde6f-109">« 20010928060000.0 Z » est un exemple de valeur acceptable.</span><span class="sxs-lookup"><span data-stu-id="fde6f-109">An example of an acceptable value is "20010928060000.0Z".</span></span> <span data-ttu-id="fde6f-110">Le « Z » indique qu’il n’y a pas de différence de temps.</span><span class="sxs-lookup"><span data-stu-id="fde6f-110">The "Z" indicates no time differential.</span></span> <span data-ttu-id="fde6f-111">Active Directory stocke la date/l’heure sur l’heure GMT (Greenwich Mean Time).</span><span class="sxs-lookup"><span data-stu-id="fde6f-111">Active Directory stores date/time as Greenwich Mean Time (GMT).</span></span> <span data-ttu-id="fde6f-112">Si aucune différence de temps n’est spécifiée, la valeur par défaut est GMT.</span><span class="sxs-lookup"><span data-stu-id="fde6f-112">If no time differential is specified, GMT is the default.</span></span>

<span data-ttu-id="fde6f-113">Si l’heure est spécifiée dans un fuseau horaire différent de GMT, la différence entre le fuseau horaire et l’heure GMT est ajoutée à la chaîne au lieu de « Z » sous la forme « AAAAMMJJHHMMSS. 0 \[ +/- \] hhmm ».</span><span class="sxs-lookup"><span data-stu-id="fde6f-113">If the time is specified in a time zone other than GMT, the differential between the time zone and GMT is appended to the string instead of "Z" in the form "YYYYMMDDHHMMSS.0\[+/-\]HHMM".</span></span> <span data-ttu-id="fde6f-114">« 20010928060000.0 + 0200 » est un exemple de valeur acceptable.</span><span class="sxs-lookup"><span data-stu-id="fde6f-114">An example of an acceptable value is "20010928060000.0+0200".</span></span> <span data-ttu-id="fde6f-115">La différence est basée sur la formule suivante : GMT = local + différentielle.</span><span class="sxs-lookup"><span data-stu-id="fde6f-115">The differential is based on the formula: GMT=Local+differential.</span></span>

<span data-ttu-id="fde6f-116">Pour plus d’informations, consultez ISO 8601 et X680.</span><span class="sxs-lookup"><span data-stu-id="fde6f-116">For more information, see ISO 8601 and X680.</span></span>



| <span data-ttu-id="fde6f-117">Entrée</span><span class="sxs-lookup"><span data-stu-id="fde6f-117">Entry</span></span> | <span data-ttu-id="fde6f-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="fde6f-118">Value</span></span> |
|--------------|----------------------------------------------------------------------------|
| <span data-ttu-id="fde6f-119">Nom</span><span class="sxs-lookup"><span data-stu-id="fde6f-119">Name</span></span>         | <span data-ttu-id="fde6f-120">String(Generalized-Time)</span><span class="sxs-lookup"><span data-stu-id="fde6f-120">String(Generalized-Time)</span></span>                                                   |
| <span data-ttu-id="fde6f-121">ID de syntaxe</span><span class="sxs-lookup"><span data-stu-id="fde6f-121">Syntax ID</span></span>    | <span data-ttu-id="fde6f-122">2.5.5.11</span><span class="sxs-lookup"><span data-stu-id="fde6f-122">2.5.5.11</span></span>                                                                   |
| <span data-ttu-id="fde6f-123">ID OM</span><span class="sxs-lookup"><span data-stu-id="fde6f-123">OM ID</span></span>        | <span data-ttu-id="fde6f-124">24</span><span class="sxs-lookup"><span data-stu-id="fde6f-124">24</span></span>                                                                         |
| <span data-ttu-id="fde6f-125">Type MAPI</span><span class="sxs-lookup"><span data-stu-id="fde6f-125">MAPI Type</span></span>    | <span data-ttu-id="fde6f-126">SYSTIME</span><span class="sxs-lookup"><span data-stu-id="fde6f-126">SYSTIME</span></span>                                                                    |
| <span data-ttu-id="fde6f-127">Type ADS</span><span class="sxs-lookup"><span data-stu-id="fde6f-127">ADS Type</span></span>     | <span data-ttu-id="fde6f-128">\_heure UTC \_ ADSTYPE</span><span class="sxs-lookup"><span data-stu-id="fde6f-128">ADSTYPE\_UTC\_TIME</span></span>                                                         |
| <span data-ttu-id="fde6f-129">Type de variante</span><span class="sxs-lookup"><span data-stu-id="fde6f-129">Variant Type</span></span> | <span data-ttu-id="fde6f-130">\_Date VT</span><span class="sxs-lookup"><span data-stu-id="fde6f-130">VT\_DATE</span></span>                                                                   |
| <span data-ttu-id="fde6f-131">SDS, type</span><span class="sxs-lookup"><span data-stu-id="fde6f-131">SDS Type</span></span>     | [<span data-ttu-id="fde6f-132">System.DateTime</span><span class="sxs-lookup"><span data-stu-id="fde6f-132">System.DateTime</span></span>](/dotnet/api/system.datetime) |



## <a name="see-also"></a><span data-ttu-id="fde6f-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fde6f-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fde6f-134">System.DateTime</span><span class="sxs-lookup"><span data-stu-id="fde6f-134">System.DateTime</span></span>](/dotnet/api/system.datetime)
</dt> </dl>

 

 
