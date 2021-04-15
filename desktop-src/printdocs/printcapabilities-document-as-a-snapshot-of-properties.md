---
title: Document en tant qu’instantané des propriétés
description: Cette rubrique n’est pas à jour. Pour obtenir les informations les plus récentes, consultez la spécification du schéma d’impression.
ms.assetid: 476c98e6-face-42cf-874d-cfa7a54b0666
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d73fc190ed8c259e64fdd60cc291c6ae5b58f80
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2021
ms.locfileid: "104393883"
---
# <a name="printcapabilities-document-as-a-snapshot-of-properties"></a><span data-ttu-id="75b4e-104">Document PrintCapabilities comme un instantané des propriétés</span><span class="sxs-lookup"><span data-stu-id="75b4e-104">PrintCapabilities Document as a Snapshot of Properties</span></span>

<span data-ttu-id="75b4e-105">Cette rubrique n’est pas à jour.</span><span class="sxs-lookup"><span data-stu-id="75b4e-105">This topic is not current.</span></span> <span data-ttu-id="75b4e-106">Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="75b4e-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="75b4e-107">L’appareil décrit par le PrintCapabilities peut avoir des propriétés qui dépendent de l’État ou de la configuration de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="75b4e-107">The device described by the PrintCapabilities might have properties that depend on the state or configuration of the device.</span></span> <span data-ttu-id="75b4e-108">Alors que PrintCapabilities représente l’espace de configuration complet d’un appareil, le fournisseur PrintCapabilities produit une instance dépendante de la configuration du PrintCapabilities, appelée document PrintCapabilities.</span><span class="sxs-lookup"><span data-stu-id="75b4e-108">While the PrintCapabilities represents the full configuration space of a device, the PrintCapabilities provider produces a configuration-dependent instance of the PrintCapabilities called the PrintCapabilities document.</span></span> <span data-ttu-id="75b4e-109">Ce document PrintCapabilities dépendant de la configuration évite la charge du schéma PrintCapabilities avec la complexité de la représentation des données à valeurs multiples.</span><span class="sxs-lookup"><span data-stu-id="75b4e-109">This configuration-dependent PrintCapabilities document avoids burdening the PrintCapabilities Schema with the complexity of representing multivalued data.</span></span> <span data-ttu-id="75b4e-110">Plus important encore, pour soulager un consommateur du document PrintCapabilities du point de vue de l’extraction de la valeur appropriée d’une représentation de données à valeurs multiples, toutes les instances Property et ScoredProperty d’un document PrintCapabilities doivent être à valeur unique.</span><span class="sxs-lookup"><span data-stu-id="75b4e-110">More importantly, to relieve a consumer of the PrintCapabilities document from the burden of extracting the appropriate value from a multivalued data representation, all Property and ScoredProperty instances in a PrintCapabilities document are required to be single-valued.</span></span> <span data-ttu-id="75b4e-111">En d’autres termes, chaque propriété et instance ScoredProperty dans un document PrintCapabilities doit avoir une valeur fixe, relative à la configuration d’entrée.</span><span class="sxs-lookup"><span data-stu-id="75b4e-111">In other words, each Property and ScoredProperty instance in a PrintCapabilities document must have a fixed Value, relative to the input configuration.</span></span> <span data-ttu-id="75b4e-112">Chaque document PrintCapabilities peut être considéré comme un instantané des propriétés de l’appareil lorsque ce dernier est dans un état particulier.</span><span class="sxs-lookup"><span data-stu-id="75b4e-112">Each PrintCapabilities document can be thought of as a snapshot of the properties of the device when the device is in a particular state.</span></span> <span data-ttu-id="75b4e-113">Par conséquent, avant de pouvoir construire un document PrintCapabilities, vous devez fournir la configuration à utiliser.</span><span class="sxs-lookup"><span data-stu-id="75b4e-113">Consequently, before a PrintCapabilities document can be constructed, the configuration to be used must be provided.</span></span>

## <a name="related-topics"></a><span data-ttu-id="75b4e-114">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="75b4e-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="75b4e-115">Spécification du schéma d’impression</span><span class="sxs-lookup"><span data-stu-id="75b4e-115">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



