---
title: Document en tant qu’instantané des propriétés
description: Examinez le document PrintCapabilities comme un instantané des propriétés. Cette rubrique n’est pas à jour. Pour obtenir les informations les plus récentes, consultez la spécification du schéma d’impression.
ms.assetid: 476c98e6-face-42cf-874d-cfa7a54b0666
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b399c82211c268a72ad2b67082c144c64e46a879
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/30/2021
ms.locfileid: "113118644"
---
# <a name="printcapabilities-document-as-a-snapshot-of-properties"></a><span data-ttu-id="b3e7d-105">Document PrintCapabilities comme un instantané des propriétés</span><span class="sxs-lookup"><span data-stu-id="b3e7d-105">PrintCapabilities Document as a Snapshot of Properties</span></span>

<span data-ttu-id="b3e7d-106">Cette rubrique n’est pas à jour.</span><span class="sxs-lookup"><span data-stu-id="b3e7d-106">This topic is not current.</span></span> <span data-ttu-id="b3e7d-107">Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="b3e7d-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="b3e7d-108">L’appareil décrit par le PrintCapabilities peut avoir des propriétés qui dépendent de l’État ou de la configuration de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="b3e7d-108">The device described by the PrintCapabilities might have properties that depend on the state or configuration of the device.</span></span> <span data-ttu-id="b3e7d-109">Alors que PrintCapabilities représente l’espace de configuration complet d’un appareil, le fournisseur PrintCapabilities produit une instance dépendante de la configuration du PrintCapabilities, appelée document PrintCapabilities.</span><span class="sxs-lookup"><span data-stu-id="b3e7d-109">While the PrintCapabilities represents the full configuration space of a device, the PrintCapabilities provider produces a configuration-dependent instance of the PrintCapabilities called the PrintCapabilities document.</span></span> <span data-ttu-id="b3e7d-110">Ce document PrintCapabilities dépendant de la configuration évite la charge du schéma PrintCapabilities avec la complexité de la représentation des données à valeurs multiples.</span><span class="sxs-lookup"><span data-stu-id="b3e7d-110">This configuration-dependent PrintCapabilities document avoids burdening the PrintCapabilities Schema with the complexity of representing multivalued data.</span></span> <span data-ttu-id="b3e7d-111">Plus important encore, pour soulager un consommateur du document PrintCapabilities du point de vue de l’extraction de la valeur appropriée d’une représentation de données à valeurs multiples, toutes les instances Property et ScoredProperty d’un document PrintCapabilities doivent être à valeur unique.</span><span class="sxs-lookup"><span data-stu-id="b3e7d-111">More importantly, to relieve a consumer of the PrintCapabilities document from the burden of extracting the appropriate value from a multivalued data representation, all Property and ScoredProperty instances in a PrintCapabilities document are required to be single-valued.</span></span> <span data-ttu-id="b3e7d-112">En d’autres termes, chaque propriété et instance ScoredProperty dans un document PrintCapabilities doit avoir une valeur fixe, relative à la configuration d’entrée.</span><span class="sxs-lookup"><span data-stu-id="b3e7d-112">In other words, each Property and ScoredProperty instance in a PrintCapabilities document must have a fixed Value, relative to the input configuration.</span></span> <span data-ttu-id="b3e7d-113">Chaque document PrintCapabilities peut être considéré comme un instantané des propriétés de l’appareil lorsque ce dernier est dans un état particulier.</span><span class="sxs-lookup"><span data-stu-id="b3e7d-113">Each PrintCapabilities document can be thought of as a snapshot of the properties of the device when the device is in a particular state.</span></span> <span data-ttu-id="b3e7d-114">Par conséquent, avant de pouvoir construire un document PrintCapabilities, vous devez fournir la configuration à utiliser.</span><span class="sxs-lookup"><span data-stu-id="b3e7d-114">Consequently, before a PrintCapabilities document can be constructed, the configuration to be used must be provided.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b3e7d-115">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="b3e7d-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b3e7d-116">Spécification du schéma d’impression</span><span class="sxs-lookup"><span data-stu-id="b3e7d-116">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



