---
description: Cette rubrique n’est pas à jour. Pour obtenir les informations les plus récentes, consultez la spécification du schéma d’impression.
ms.assetid: ea75a7ac-d4d7-42b6-91e9-e28607fd684c
title: Utilisations du PrintCapabilities
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63dda5b21d1472ec8d4162c8d7229ff47264fb55
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2021
ms.locfileid: "103953501"
---
# <a name="uses-of-the-printcapabilities"></a><span data-ttu-id="8ada6-104">Utilisations du PrintCapabilities</span><span class="sxs-lookup"><span data-stu-id="8ada6-104">Uses of the PrintCapabilities</span></span>

<span data-ttu-id="8ada6-105">Cette rubrique n’est pas à jour.</span><span class="sxs-lookup"><span data-stu-id="8ada6-105">This topic is not current.</span></span> <span data-ttu-id="8ada6-106">Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="8ada6-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="8ada6-107">Le PrintCapabilities est destiné à représenter des attributs d’appareil configurables comme des constructions de fonctionnalité/option ou des constructions de paramètres.</span><span class="sxs-lookup"><span data-stu-id="8ada6-107">The PrintCapabilities are intended to represent configurable device attributes as either Feature/Option constructs or parameter constructs.</span></span> <span data-ttu-id="8ada6-108">Ces informations définissent l’espace de configuration de l’appareil et peuvent être utilisées par un client de l’interface utilisateur pour construire une interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="8ada6-108">This information defines the configuration space of the device and can be used by a user interface (UI) client to construct a UI.</span></span> <span data-ttu-id="8ada6-109">Les mots clés du schéma d’impression définissent un ensemble d’instances de fonctionnalités standard, d’instances d’option pour les instances de fonctionnalités standard et d’instances ParameterDef.</span><span class="sxs-lookup"><span data-stu-id="8ada6-109">The Print Schema Keywords define a set of standard Feature instances, Option instances for the standard Feature instances, and ParameterDef instances.</span></span>

<span data-ttu-id="8ada6-110">Les constructions de fonctionnalité et d’option ou de paramètres dans PrintCapabilities sont destinées à contenir des instances de propriété ou de ScoredProperty qui décrivent un appareil et qui sont prises en charge par le sous-système de spouleur.</span><span class="sxs-lookup"><span data-stu-id="8ada6-110">The Feature/Option or parameter constructs in the PrintCapabilities are intended to hold Property or ScoredProperty instances that describe a device, and that are supported by the spooler subsystem.</span></span> <span data-ttu-id="8ada6-111">Ces instances de propriété et ScoredProperty présentent un intérêt général pour les clients de l’appareil, et contiennent les informations fournies par les fonctions Win32 DevCaps.</span><span class="sxs-lookup"><span data-stu-id="8ada6-111">These Property and ScoredProperty instances are of general interest to clients of the device, and contain the information that is provided by the Win32 DevCaps functions.</span></span> <span data-ttu-id="8ada6-112">Les mots clés du schéma d’impression définissent un ensemble de propriétés standard et d’instances ScoredProperty.</span><span class="sxs-lookup"><span data-stu-id="8ada6-112">The Print Schema Keywords define a set of standard Property and ScoredProperty instances.</span></span>

<span data-ttu-id="8ada6-113">Il convient de souligner que le document PrintCapabilities est destiné à représenter uniquement des données à valeur unique : les données qui ne dépendent pas d’une configuration particulière de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="8ada6-113">It should be emphasized that the PrintCapabilities document is intended to represent only single-valued data: data that does not depend on a particular configuration of the device.</span></span> <span data-ttu-id="8ada6-114">Le document PrintCapabilities fournit uniquement une capture instantanée de données dépendantes de la configuration.</span><span class="sxs-lookup"><span data-stu-id="8ada6-114">The PrintCapabilities document provides only a snapshot of configuration-dependent data.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8ada6-115">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="8ada6-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8ada6-116">Spécification du schéma d’impression</span><span class="sxs-lookup"><span data-stu-id="8ada6-116">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



