---
description: En savoir plus sur les limitations imposées par le schéma PrintCapabilities. Le fournisseur PrintCapabilities doit détecter les configurations non valides et les résoudre.
ms.assetid: 420c5c84-abb8-495a-9b74-dc19a16034fb
title: Limitations de Schema-Imposed
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0ee2911d4b90ebc194aa245f398f71575496c877
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112404922"
---
# <a name="schema-imposed-limitations"></a><span data-ttu-id="5811d-104">Limitations de Schema-Imposed</span><span class="sxs-lookup"><span data-stu-id="5811d-104">Schema-Imposed Limitations</span></span>

<span data-ttu-id="5811d-105">Cette rubrique n’est pas à jour.</span><span class="sxs-lookup"><span data-stu-id="5811d-105">This topic is not current.</span></span> <span data-ttu-id="5811d-106">Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="5811d-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="5811d-107">Le schéma PrintCapabilities fournit aux auteurs PrintCapabilities un degré élevé de flexibilité et d’expressivité qui peuvent être utilisés dans les descriptions des appareils.</span><span class="sxs-lookup"><span data-stu-id="5811d-107">The PrintCapabilities Schema provides PrintCapabilities authors with a substantial amount of flexibility and expressiveness that can be utilized in device descriptions.</span></span> <span data-ttu-id="5811d-108">Toutefois, les dépendances de configuration imposent une limitation à cette flexibilité et à l’expressivité.</span><span class="sxs-lookup"><span data-stu-id="5811d-108">However, configuration dependencies impose a limitation on this flexibility and expressiveness.</span></span> <span data-ttu-id="5811d-109">Les instances ParameterDef, la liste des éléments de fonctionnalité, la liste des instances d’option dans chaque fonctionnalité et les instances ScoredProperty dans chaque option ne doivent pas contenir de dépendances de configuration.</span><span class="sxs-lookup"><span data-stu-id="5811d-109">ParameterDef instances, the list of Feature elements, the list of Option instances within each Feature, and the ScoredProperty instances within each Option must not contain configuration dependencies.</span></span> <span data-ttu-id="5811d-110">Le fournisseur de documents PrintCapabilities doit détecter les combinaisons de configurations non valides et doit les résoudre.</span><span class="sxs-lookup"><span data-stu-id="5811d-110">The PrintCapabilities document provider must detect invalid combinations of configurations and must resolve them.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5811d-111">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="5811d-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5811d-112">Spécification du schéma d’impression</span><span class="sxs-lookup"><span data-stu-id="5811d-112">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



