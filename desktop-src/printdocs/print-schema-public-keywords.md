---
description: Cette rubrique n’est pas à jour. Pour obtenir les informations les plus récentes, consultez la spécification du schéma d’impression.
ms.assetid: ff966475-626d-4a48-9349-e60454d47c57
title: Mots clés publics du schéma d’impression
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e3e8fb9a46bbed2b135f4e81456dd65e79be830
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2021
ms.locfileid: "106538273"
---
# <a name="print-schema-public-keywords"></a><span data-ttu-id="090d1-104">Mots clés publics du schéma d’impression</span><span class="sxs-lookup"><span data-stu-id="090d1-104">Print Schema Public Keywords</span></span>

<span data-ttu-id="090d1-105">Cette rubrique n’est pas à jour.</span><span class="sxs-lookup"><span data-stu-id="090d1-105">This topic is not current.</span></span> <span data-ttu-id="090d1-106">Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="090d1-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="090d1-107">La section suivante spécifie les mots clés publics qui sont définis pour le schéma d’impression.</span><span class="sxs-lookup"><span data-stu-id="090d1-107">The following section specifies the public keywords which are defined for the Print Schema.</span></span>

## <a name="print-schema-public-keywords-usage-for-print-capabilities"></a><span data-ttu-id="090d1-108">Utilisation des mots clés publics du schéma d’impression pour les fonctionnalités d’impression</span><span class="sxs-lookup"><span data-stu-id="090d1-108">Print Schema Public Keywords Usage for Print Capabilities</span></span>

<span data-ttu-id="090d1-109">Les mots clés spécifiés sous les mots clés publics PrintCapabilities peuvent apparaître dans un document de fonctionnalités d’impression.</span><span class="sxs-lookup"><span data-stu-id="090d1-109">Keywords specified under PrintCapabilities Public Keywords MAY appear in a Print Capabilities document.</span></span> <span data-ttu-id="090d1-110">Pour plus d’informations sur la façon dont ces mots clés interagissent avec la technologie PrintCapabilities, consultez [vue d’ensemble de la section PrintCapabilities](overview-of-the-printcapabilities.md) .</span><span class="sxs-lookup"><span data-stu-id="090d1-110">For more information on how these keywords interact with PrintCapabilities technology, please refer to [Overview of the PrintCapabilities](overview-of-the-printcapabilities.md) section.</span></span>

<span data-ttu-id="090d1-111">Les mots clés publics spécifiques à PrintTicket ne doivent pas apparaître dans un document PrintCapabilities.</span><span class="sxs-lookup"><span data-stu-id="090d1-111">Public keywords specific to PrintTicket SHOULD NOT appear in a PrintCapabilities document.</span></span>

## <a name="print-schema-public-keywords-usage-for-printticket"></a><span data-ttu-id="090d1-112">Utilisation des mots clés publics du schéma d’impression pour PrintTicket</span><span class="sxs-lookup"><span data-stu-id="090d1-112">Print Schema Public Keywords Usage for PrintTicket</span></span>

<span data-ttu-id="090d1-113">Les mots clés spécifiés sous les mots clés publics PrintTicket peuvent apparaître dans un PrintTicket.</span><span class="sxs-lookup"><span data-stu-id="090d1-113">Keywords specified under PrintTicket Public Keywords MAY appear in a PrintTicket.</span></span> <span data-ttu-id="090d1-114">Les mots clés PrintTicket sont implémentés en tant que type d’élément de propriété.</span><span class="sxs-lookup"><span data-stu-id="090d1-114">PrintTicket keywords are implemented as a Property element type.</span></span> <span data-ttu-id="090d1-115">Pour plus d’informations sur la façon dont ces mots clés interagissent avec la technologie PrintTicket, consultez les [informations de configuration non liées à](configuration-information-not-related-to-printcapabilities.md) la section PrintCapabilities.</span><span class="sxs-lookup"><span data-stu-id="090d1-115">For more information on how these keywords interact with PrintTicket technology, please refer to [Configuration Information Not Related to PrintCapabilities](configuration-information-not-related-to-printcapabilities.md) section.</span></span>

<span data-ttu-id="090d1-116">Les mots clés spécifiés sous les mots clés publics PrintCapabilities peuvent apparaître dans un PrintTicket en fonction de l’implémentation de PrintTicket dans une application et/ou un pilote.</span><span class="sxs-lookup"><span data-stu-id="090d1-116">Keywords specified under PrintCapabilities Public Keywords MAY appear in a PrintTicket depending on the implementation of the PrintTicket in an application and/or driver.</span></span> <span data-ttu-id="090d1-117">Cela permet de sélectionner les attributs d’appareil définis dans le document PrintCapabilities.</span><span class="sxs-lookup"><span data-stu-id="090d1-117">This provides selections for device attributes defined in the PrintCapabilities document.</span></span> <span data-ttu-id="090d1-118">Pour plus d’informations sur l’interaction entre les mots clés PrintCapabilities et PrintTicket, reportez-vous à [l’objectif de la section PrintTicket](purpose-of-the-printticket.md) .</span><span class="sxs-lookup"><span data-stu-id="090d1-118">For more information on the interaction between PrintCapabilities keywords and the PrintTicket, please refer to [Purpose of the PrintTicket](purpose-of-the-printticket.md) section.</span></span>

## <a name="related-topics"></a><span data-ttu-id="090d1-119">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="090d1-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="090d1-120">Spécification du schéma d’impression</span><span class="sxs-lookup"><span data-stu-id="090d1-120">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



