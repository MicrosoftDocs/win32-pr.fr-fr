---
description: En savoir plus sur les utilisations de PrintCapabilities. Cette rubrique n’est pas à jour. Pour obtenir les informations les plus récentes, consultez la spécification du schéma d’impression.
ms.assetid: ea75a7ac-d4d7-42b6-91e9-e28607fd684c
title: Utilisations du PrintCapabilities
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f09882d42814930ef5ba08e087f1df87e0d0e9bc
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/30/2021
ms.locfileid: "113119424"
---
# <a name="uses-of-the-printcapabilities"></a><span data-ttu-id="86ffb-105">Utilisations du PrintCapabilities</span><span class="sxs-lookup"><span data-stu-id="86ffb-105">Uses of the PrintCapabilities</span></span>

<span data-ttu-id="86ffb-106">Cette rubrique n’est pas à jour.</span><span class="sxs-lookup"><span data-stu-id="86ffb-106">This topic is not current.</span></span> <span data-ttu-id="86ffb-107">Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="86ffb-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="86ffb-108">Le PrintCapabilities est destiné à représenter des attributs d’appareil configurables comme des constructions de fonctionnalité/option ou des constructions de paramètres.</span><span class="sxs-lookup"><span data-stu-id="86ffb-108">The PrintCapabilities are intended to represent configurable device attributes as either Feature/Option constructs or parameter constructs.</span></span> <span data-ttu-id="86ffb-109">Ces informations définissent l’espace de configuration de l’appareil et peuvent être utilisées par un client de l’interface utilisateur pour construire une interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="86ffb-109">This information defines the configuration space of the device and can be used by a user interface (UI) client to construct a UI.</span></span> <span data-ttu-id="86ffb-110">Les mots clés du schéma d’impression définissent un ensemble d’instances de fonctionnalités standard, d’instances d’option pour les instances de fonctionnalités standard et d’instances ParameterDef.</span><span class="sxs-lookup"><span data-stu-id="86ffb-110">The Print Schema Keywords define a set of standard Feature instances, Option instances for the standard Feature instances, and ParameterDef instances.</span></span>

<span data-ttu-id="86ffb-111">Les constructions de fonctionnalité et d’option ou de paramètres dans PrintCapabilities sont destinées à contenir des instances de propriété ou de ScoredProperty qui décrivent un appareil et qui sont prises en charge par le sous-système de spouleur.</span><span class="sxs-lookup"><span data-stu-id="86ffb-111">The Feature/Option or parameter constructs in the PrintCapabilities are intended to hold Property or ScoredProperty instances that describe a device, and that are supported by the spooler subsystem.</span></span> <span data-ttu-id="86ffb-112">Ces instances de propriété et ScoredProperty présentent un intérêt général pour les clients de l’appareil, et contiennent les informations fournies par les fonctions Win32 DevCaps.</span><span class="sxs-lookup"><span data-stu-id="86ffb-112">These Property and ScoredProperty instances are of general interest to clients of the device, and contain the information that is provided by the Win32 DevCaps functions.</span></span> <span data-ttu-id="86ffb-113">Les mots clés du schéma d’impression définissent un ensemble de propriétés standard et d’instances ScoredProperty.</span><span class="sxs-lookup"><span data-stu-id="86ffb-113">The Print Schema Keywords define a set of standard Property and ScoredProperty instances.</span></span>

<span data-ttu-id="86ffb-114">Il convient de souligner que le document PrintCapabilities est destiné à représenter uniquement des données à valeur unique : les données qui ne dépendent pas d’une configuration particulière de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="86ffb-114">It should be emphasized that the PrintCapabilities document is intended to represent only single-valued data: data that does not depend on a particular configuration of the device.</span></span> <span data-ttu-id="86ffb-115">Le document PrintCapabilities fournit uniquement une capture instantanée de données dépendantes de la configuration.</span><span class="sxs-lookup"><span data-stu-id="86ffb-115">The PrintCapabilities document provides only a snapshot of configuration-dependent data.</span></span>

## <a name="related-topics"></a><span data-ttu-id="86ffb-116">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="86ffb-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="86ffb-117">Spécification du schéma d’impression</span><span class="sxs-lookup"><span data-stu-id="86ffb-117">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



