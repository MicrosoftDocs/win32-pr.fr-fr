---
description: Cette rubrique n’est pas à jour. Pour obtenir les informations les plus récentes, consultez la spécification du schéma d’impression.
ms.assetid: 2377763b-9b3b-49ec-ab6c-476b8009ddcb
title: Responsabilités des consommateurs du document PrintCapabilities
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b74cfc1885ecc5599365bc6eadcef30ef4c4ae3
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2021
ms.locfileid: "106522899"
---
# <a name="responsibilities-of-consumers-of-the-printcapabilities-document"></a><span data-ttu-id="9b08c-104">Responsabilités des consommateurs du document PrintCapabilities</span><span class="sxs-lookup"><span data-stu-id="9b08c-104">Responsibilities of Consumers of the PrintCapabilities Document</span></span>

<span data-ttu-id="9b08c-105">Cette rubrique n’est pas à jour.</span><span class="sxs-lookup"><span data-stu-id="9b08c-105">This topic is not current.</span></span> <span data-ttu-id="9b08c-106">Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="9b08c-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="9b08c-107">Les consommateurs de documents PrintCapabilities présentent certaines obligations qu’ils doivent respecter avant de pouvoir utiliser un document PrintCapabilities.</span><span class="sxs-lookup"><span data-stu-id="9b08c-107">Consumers of PrintCapabilities documents have certain obligations they must uphold before they can use a PrintCapabilities document.</span></span> <span data-ttu-id="9b08c-108">Les exigences suivantes s’appliquent aux clients d’un document PrintCapabilities.</span><span class="sxs-lookup"><span data-stu-id="9b08c-108">The following requirements apply to clients of a PrintCapabilities document.</span></span>

-   <span data-ttu-id="9b08c-109">Ils ne doivent pas rejeter ou échouer le traitement d’un PrintCapabilities valide syntaxiquement ; autrement dit, tout document PrintCapabilities conforme au schéma PrintCapabilities.</span><span class="sxs-lookup"><span data-stu-id="9b08c-109">They must not reject or fail to process any syntactically valid PrintCapabilities; that is, any PrintCapabilities document that conforms to the PrintCapabilities Schema.</span></span>

-   <span data-ttu-id="9b08c-110">Ils doivent être en mesure de contourner la présence inattendue ou l’absence de contenu défini en privé.</span><span class="sxs-lookup"><span data-stu-id="9b08c-110">They must be able to work around the unexpected presence or absence of privately-defined content.</span></span> <span data-ttu-id="9b08c-111">Cela comprend le contenu privé défini qui apparaît dans les instances d’éléments définis par le schéma d’impression.</span><span class="sxs-lookup"><span data-stu-id="9b08c-111">This includes privately-defined content that appears within instances of Print Schema-defined elements.</span></span>

-   <span data-ttu-id="9b08c-112">Ils doivent être en mesure de contourner le contenu facultatif du schéma d’impression absent.</span><span class="sxs-lookup"><span data-stu-id="9b08c-112">They must be able to work around optional Print Schema content that is absent.</span></span>

-   <span data-ttu-id="9b08c-113">Ils doivent savoir quand demander un nouveau document.</span><span class="sxs-lookup"><span data-stu-id="9b08c-113">They must be aware of when to request a new document.</span></span>

    -   <span data-ttu-id="9b08c-114">Les valeurs des instances de propriété sont dépendantes de la configuration (par conséquent, en fonction de l’instantané).</span><span class="sxs-lookup"><span data-stu-id="9b08c-114">Values of Property instances are configuration-dependent (hence, snapshot-dependent).</span></span> <span data-ttu-id="9b08c-115">Vous devez mettre à jour l’instantané lorsque vous accédez à une instance de propriété.</span><span class="sxs-lookup"><span data-stu-id="9b08c-115">You must update the snapshot when you access a Property instance.</span></span>

    -   <span data-ttu-id="9b08c-116">Les instances Feature, option et ScoredProperty qui doivent être copiées dans un PrintTicket sont par définition statiques.</span><span class="sxs-lookup"><span data-stu-id="9b08c-116">Feature, Option and ScoredProperty instances that are to be copied to a PrintTicket are by definition static.</span></span> <span data-ttu-id="9b08c-117">Autrement dit, ils ne sont pas (et ne doivent pas être) dépendants de la configuration de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="9b08c-117">That is, they are not (and must not be) dependent on the device configuration.</span></span> <span data-ttu-id="9b08c-118">Si vous accédez à n’importe quelle instance de ces types, vous n’avez pas besoin d’obtenir un nouveau document PrintCapabilities lorsque la configuration est modifiée.</span><span class="sxs-lookup"><span data-stu-id="9b08c-118">If you access any instances of these types, you do not need to obtain a new PrintCapabilities document when the configuration changes.</span></span>

-   <span data-ttu-id="9b08c-119">Les consommateurs de PrintCapabilities qui sont des clients de l’interface utilisateur doivent être en mesure d’utiliser des informations dans un document PrintCapabilities pour construire une interface utilisateur et construire un PrintTicket valide à partir des sélections de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="9b08c-119">Consumers of PrintCapabilities that are user interface (UI) clients must be able to use information in a PrintCapabilities document to construct a user interface and to construct a valid PrintTicket from the user selections.</span></span> <span data-ttu-id="9b08c-120">Cela implique de savoir quelles instances ParameterInit doivent être spécifiées et de valider les instances spécifiées.</span><span class="sxs-lookup"><span data-stu-id="9b08c-120">This includes knowing which ParameterInit instances must be specified, and validating those instances that are specified.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9b08c-121">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="9b08c-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9b08c-122">Spécification du schéma d’impression</span><span class="sxs-lookup"><span data-stu-id="9b08c-122">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



