---
description: Cette vue d’ensemble de la fonctionnalité PrintTicket décrit le format permettant d’exprimer les informations de configuration de l’appareil et l’utilisation d’un PrintTicket.
ms.assetid: c48b9821-9194-47d9-a3ec-b10dbbdf14cc
title: Vue d’ensemble de la fonctionnalité PrintTicket
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e90aa6f967f5fce25977b52a4d0bec7e9e1ea705
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112408542"
---
# <a name="overview-of-printticket-functionality"></a><span data-ttu-id="7fe62-103">Vue d’ensemble de la fonctionnalité PrintTicket</span><span class="sxs-lookup"><span data-stu-id="7fe62-103">Overview of PrintTicket Functionality</span></span>

<span data-ttu-id="7fe62-104">Cette rubrique n’est pas à jour.</span><span class="sxs-lookup"><span data-stu-id="7fe62-104">This topic is not current.</span></span> <span data-ttu-id="7fe62-105">Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="7fe62-105">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="7fe62-106">Le PrintTicket utilise un format XML pour exprimer les informations de configuration de l’appareil à l’aide de la fonctionnalité/option et des constructions de paramètre de l’infrastructure du schéma d’impression.</span><span class="sxs-lookup"><span data-stu-id="7fe62-106">The PrintTicket utilizes an XML-based format for expressing device configuration information using the Feature/Option and parameter constructs of the Print Schema Framework.</span></span> <span data-ttu-id="7fe62-107">Cela comprend tous les types d’éléments standard, ainsi que les fonctionnalités d’extensibilité de l’infrastructure de schéma d’impression.</span><span class="sxs-lookup"><span data-stu-id="7fe62-107">This includes all of the standard element types as well as the extensibility capabilities of the Print Schema Framework.</span></span> <span data-ttu-id="7fe62-108">Un PrintTicket est supposé être une description autonome de la façon dont une seule page doit être traitée.</span><span class="sxs-lookup"><span data-stu-id="7fe62-108">A PrintTicket is assumed to be a self-contained description of how a single page is to be processed.</span></span> <span data-ttu-id="7fe62-109">Les étapes impliquées dans l’extraction et la construction d’un tel PrintTicket à partir d’un format de document particulier ne sont pas abordées ici.</span><span class="sxs-lookup"><span data-stu-id="7fe62-109">The steps involved in extracting and constructing such a PrintTicket from a particular document format are not covered here.</span></span>

<span data-ttu-id="7fe62-110">Un PrintTicket peut être utilisé pour obtenir un document PrintCapabilities décrivant les caractéristiques de l’appareil pour une configuration particulière.</span><span class="sxs-lookup"><span data-stu-id="7fe62-110">A PrintTicket can be used to obtain a PrintCapabilities document describing the characteristics of the device for a particular configuration.</span></span> <span data-ttu-id="7fe62-111">L’PrintTicket peut également être envoyé avec un ensemble d’instructions de rendu pour produire une page de sortie rendue et traitée en fonction de la configuration spécifiée dans PrintTicket.</span><span class="sxs-lookup"><span data-stu-id="7fe62-111">Alternatively, the PrintTicket can be submitted with a set of rendering instructions to produce a page of output rendered and processed according to the configuration specified in the PrintTicket.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7fe62-112">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="7fe62-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7fe62-113">Spécification du schéma d’impression</span><span class="sxs-lookup"><span data-stu-id="7fe62-113">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



