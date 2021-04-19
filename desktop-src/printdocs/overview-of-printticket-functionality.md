---
description: Cette rubrique n’est pas à jour. Pour obtenir les informations les plus récentes, consultez la spécification du schéma d’impression.
ms.assetid: c48b9821-9194-47d9-a3ec-b10dbbdf14cc
title: Vue d’ensemble de la fonctionnalité PrintTicket
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a70945fcc18e08615a9674a90a023f4ee12a76e
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2021
ms.locfileid: "106535756"
---
# <a name="overview-of-printticket-functionality"></a><span data-ttu-id="1d5cb-104">Vue d’ensemble de la fonctionnalité PrintTicket</span><span class="sxs-lookup"><span data-stu-id="1d5cb-104">Overview of PrintTicket Functionality</span></span>

<span data-ttu-id="1d5cb-105">Cette rubrique n’est pas à jour.</span><span class="sxs-lookup"><span data-stu-id="1d5cb-105">This topic is not current.</span></span> <span data-ttu-id="1d5cb-106">Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="1d5cb-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="1d5cb-107">Le PrintTicket utilise un format XML pour exprimer les informations de configuration de l’appareil à l’aide de la fonctionnalité/option et des constructions de paramètre de l’infrastructure du schéma d’impression.</span><span class="sxs-lookup"><span data-stu-id="1d5cb-107">The PrintTicket utilizes an XML-based format for expressing device configuration information using the Feature/Option and parameter constructs of the Print Schema Framework.</span></span> <span data-ttu-id="1d5cb-108">Cela comprend tous les types d’éléments standard, ainsi que les fonctionnalités d’extensibilité de l’infrastructure de schéma d’impression.</span><span class="sxs-lookup"><span data-stu-id="1d5cb-108">This includes all of the standard element types as well as the extensibility capabilities of the Print Schema Framework.</span></span> <span data-ttu-id="1d5cb-109">Un PrintTicket est supposé être une description autonome de la façon dont une seule page doit être traitée.</span><span class="sxs-lookup"><span data-stu-id="1d5cb-109">A PrintTicket is assumed to be a self-contained description of how a single page is to be processed.</span></span> <span data-ttu-id="1d5cb-110">Les étapes impliquées dans l’extraction et la construction d’un tel PrintTicket à partir d’un format de document particulier ne sont pas abordées ici.</span><span class="sxs-lookup"><span data-stu-id="1d5cb-110">The steps involved in extracting and constructing such a PrintTicket from a particular document format are not covered here.</span></span>

<span data-ttu-id="1d5cb-111">Un PrintTicket peut être utilisé pour obtenir un document PrintCapabilities décrivant les caractéristiques de l’appareil pour une configuration particulière.</span><span class="sxs-lookup"><span data-stu-id="1d5cb-111">A PrintTicket can be used to obtain a PrintCapabilities document describing the characteristics of the device for a particular configuration.</span></span> <span data-ttu-id="1d5cb-112">L’PrintTicket peut également être envoyé avec un ensemble d’instructions de rendu pour produire une page de sortie rendue et traitée en fonction de la configuration spécifiée dans PrintTicket.</span><span class="sxs-lookup"><span data-stu-id="1d5cb-112">Alternatively, the PrintTicket can be submitted with a set of rendering instructions to produce a page of output rendered and processed according to the configuration specified in the PrintTicket.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1d5cb-113">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="1d5cb-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1d5cb-114">Spécification du schéma d’impression</span><span class="sxs-lookup"><span data-stu-id="1d5cb-114">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



