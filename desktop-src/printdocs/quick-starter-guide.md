---
description: Cet article vous propose un démarrage rapide pour implémenter PrintTicket et PrintCapabilities pour votre application ou pilote de périphérique.
ms.assetid: 2c1d912e-464e-48d2-ba4f-c0b9a811b25e
title: Guide de démarrage rapide
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6060de551d3fb663e148cf80f661c4d517a51b93
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112405312"
---
# <a name="quick-starter-guide"></a><span data-ttu-id="0eaba-103">Guide de démarrage rapide</span><span class="sxs-lookup"><span data-stu-id="0eaba-103">Quick Starter Guide</span></span>

<span data-ttu-id="0eaba-104">Cette rubrique n’est pas à jour.</span><span class="sxs-lookup"><span data-stu-id="0eaba-104">This topic is not current.</span></span> <span data-ttu-id="0eaba-105">Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="0eaba-105">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="0eaba-106">Cette page est conçue pour vous permettre de commencer rapidement à implémenter PrintTicket et PrintCapabilities pour votre application ou pilote de périphérique.</span><span class="sxs-lookup"><span data-stu-id="0eaba-106">This page is designed to give you a quick start to implement PrintTicket and PrintCapabilities for your application or device driver.</span></span> <span data-ttu-id="0eaba-107">Nous vous encourageons à lire la spécification du schéma d’impression dans son intégralité, mais cette page vous permettra de commencer à vous lancer dans les domaines clés auxquels vous devez être attentif.</span><span class="sxs-lookup"><span data-stu-id="0eaba-107">Although we encourage that you read the Print Schema specification in full, this page will help give you a jump start in key areas you should pay attention to.</span></span>

1) <span data-ttu-id="0eaba-108">Lisez les [technologies d' Schema-Related d’impression](print-schema-related-technologies.md) pour obtenir une vue d’ensemble des technologies de fonctionnalités d’impression et PrintTicket</span><span class="sxs-lookup"><span data-stu-id="0eaba-108">Read the [Print Schema-Related Technologies](print-schema-related-technologies.md) to give you an overview of PrintTicket and Print Capabilities technologies</span></span>

2) <span data-ttu-id="0eaba-109">Veillez à bien comprendre le [Résumé des types d’éléments](summary-of-element-types.md) utilisés pour exprimer les technologies liées au schéma d’impression.</span><span class="sxs-lookup"><span data-stu-id="0eaba-109">Ensure that you have a grasp on the [Summary of Element Types](summary-of-element-types.md) which are used to express Print Schema related technologies.</span></span>

3) <span data-ttu-id="0eaba-110">Les documents PrintCapabilities et les des PrintTicket sont définis selon trois niveaux de [préfixe d’étendue](scoping-prefix.md) , travail, document et page.</span><span class="sxs-lookup"><span data-stu-id="0eaba-110">PrintCapabilities documents and PrintTickets are defined at three [Scoping Prefix](scoping-prefix.md) levels, Job, Document and Page.</span></span>

4) <span data-ttu-id="0eaba-111">Lire les différents [attributs XML](xml-attributes.md) utilisés dans différents types d’éléments de schéma d’impression</span><span class="sxs-lookup"><span data-stu-id="0eaba-111">Read over the different [XML Attributes](xml-attributes.md) which are used within different Print Schema element types</span></span>

5) <span data-ttu-id="0eaba-112">Consultez la [liste de vérification de la construction de document PrintCapabilities](printcapabilities-document-construction-checklist.md) et l' [exemple de document PrintCapabilities](printcapabilities-document-example.md) fourni</span><span class="sxs-lookup"><span data-stu-id="0eaba-112">Review the [PrintCapabilities Document Construction Checklist](printcapabilities-document-construction-checklist.md) and also the provided [PrintCapabilities Document Example](printcapabilities-document-example.md)</span></span>

6) <span data-ttu-id="0eaba-113">Examiner les [listes de vérification de construction PrintTicket](printticket-construction-checklists.md) et l' [exemple PrintTicket](printticket-example.md) fourni</span><span class="sxs-lookup"><span data-stu-id="0eaba-113">Review the [PrintTicket Construction Checklists](printticket-construction-checklists.md) and also the provided [PrintTicket Example](printticket-example.md)</span></span>

7) <span data-ttu-id="0eaba-114">Les fournisseurs PrintTicket doivent également consulter la [liste de vérification de validation PrintTicket](printticket-validation-checklist.md) pour garantir la conformité avec la spécification PrintSchema</span><span class="sxs-lookup"><span data-stu-id="0eaba-114">PrintTicket providers should also review the [PrintTicket Validation Checklist](printticket-validation-checklist.md) to ensure conformance with the PrintSchema specification</span></span>

8) <span data-ttu-id="0eaba-115">Passez en revue les [éléments configurables](user-configurable-elements.md) par l’utilisateur et les [définitions de paramètres](parameter-definitions.md) Mots clés du schéma d’impression public qui peuvent apparaître dans un document PrintCapabilities</span><span class="sxs-lookup"><span data-stu-id="0eaba-115">Review both [User Configurable Elements](user-configurable-elements.md) and [Parameter Definitions](parameter-definitions.md) public Print Schema keywords which may appear in a PrintCapabilities document</span></span>

## <a name="related-topics"></a><span data-ttu-id="0eaba-116">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="0eaba-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0eaba-117">Spécification du schéma d’impression</span><span class="sxs-lookup"><span data-stu-id="0eaba-117">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



