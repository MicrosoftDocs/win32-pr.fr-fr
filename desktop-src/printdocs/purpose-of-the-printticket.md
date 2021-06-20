---
description: L’objectif de PrintTicket est de définir une configuration spécifique qui est appliquée à l’objet de traitement en cours de traitement.
ms.assetid: 8a7dd185-0324-44a0-8405-59a2fdc1efcb
title: Objectif du PrintTicket
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5d0166e150beedf354e4fb2c99a84e94c519fd5
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112405332"
---
# <a name="purpose-of-the-printticket"></a><span data-ttu-id="cb010-103">Objectif du PrintTicket</span><span class="sxs-lookup"><span data-stu-id="cb010-103">Purpose of the PrintTicket</span></span>

<span data-ttu-id="cb010-104">Cette rubrique n’est pas à jour.</span><span class="sxs-lookup"><span data-stu-id="cb010-104">This topic is not current.</span></span> <span data-ttu-id="cb010-105">Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="cb010-105">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="cb010-106">L’objectif principal du PrintTicket est d’exprimer les configurations de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="cb010-106">The primary purpose of the PrintTicket is to express device configurations.</span></span> <span data-ttu-id="cb010-107">Contrairement au document PrintCapabilities, qui définit toutes les configurations possibles que l’appareil peut supposer (l’espace de configuration de l’appareil), l’objectif de l’PrintTicket est de définir une configuration spécifique qui est appliquée à l’objet de traitement (dans le cas présent, la page) qui est en cours de traitement.</span><span class="sxs-lookup"><span data-stu-id="cb010-107">In contrast to the PrintCapabilities document, which defines all possible configurations the device can assume (the device's configuration space), the PrintTicket's purpose is to define a single specific configuration that is applied to the job object (in this case the page) that is being processed.</span></span> <span data-ttu-id="cb010-108">Pour promouvoir la portabilité et la cohérence des configurations, les technologies et les mots clés spécifiques présentés dans la section Mots clés du schéma d’impression sont utilisés par les technologies PrintCapabilities et PrintTicket.</span><span class="sxs-lookup"><span data-stu-id="cb010-108">To promote portability and consistency of configurations, the specific keywords and hierarchy presented in the Print Schema Keywords section are used by both the PrintCapabilities and the PrintTicket technologies.</span></span> <span data-ttu-id="cb010-109">En outre, l' [infrastructure du schéma d’impression](print-schema-framework.md) définit les constructions de base des deux technologies, afin de promouvoir les communications non ambiguës, ouvertes et extensibles de la mise en forme des travaux et de PrintCapabilities.</span><span class="sxs-lookup"><span data-stu-id="cb010-109">In addition, the [Print Schema Framework](print-schema-framework.md) defines the basic constructs of both technologies, to promote unambiguous, open, and extensible communication of job formatting and PrintCapabilities.</span></span>

## <a name="related-topics"></a><span data-ttu-id="cb010-110">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="cb010-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cb010-111">Spécification du schéma d’impression</span><span class="sxs-lookup"><span data-stu-id="cb010-111">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



