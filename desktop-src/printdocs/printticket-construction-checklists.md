---
description: Cette rubrique n’est pas à jour. Pour obtenir les informations les plus récentes, consultez la spécification du schéma d’impression.
ms.assetid: ed53d1a8-d302-4855-9858-0f37dfbbd1d3
title: Listes de vérification de la construction PrintTicket
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e742bcd3b94c5016fda6f97e2fb5e20a2cf70f73
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2021
ms.locfileid: "106524782"
---
# <a name="printticket-construction-checklists"></a><span data-ttu-id="49192-104">Listes de vérification de la construction PrintTicket</span><span class="sxs-lookup"><span data-stu-id="49192-104">PrintTicket Construction Checklists</span></span>

<span data-ttu-id="49192-105">Cette rubrique n’est pas à jour.</span><span class="sxs-lookup"><span data-stu-id="49192-105">This topic is not current.</span></span> <span data-ttu-id="49192-106">Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="49192-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="49192-107">Cette section montre comment l’auteur d’un client PrintTicket peut utiliser les types d’éléments définis dans l’infrastructure du schéma d’impression pour créer un PrintTicket qui décrit les intentions d’un appareil.</span><span class="sxs-lookup"><span data-stu-id="49192-107">This section demonstrates how the author of a PrintTicket client can use the element types defined in the Print Schema Framework to create a PrintTicket that describes intents for a device.</span></span> <span data-ttu-id="49192-108">Le PrintTicket peut être générique (non lié à un appareil spécifique) ou il peut être spécifique à l’appareil.</span><span class="sxs-lookup"><span data-stu-id="49192-108">The PrintTicket can be generic (not tied to a specific device), or it can be device-specific.</span></span> <span data-ttu-id="49192-109">La sémantique du PrintTicket est présentée plus en détail.</span><span class="sxs-lookup"><span data-stu-id="49192-109">The semantics of the PrintTicket are presented in greater detail.</span></span> <span data-ttu-id="49192-110">En outre, cette section contient une vue d’ensemble des concepts et de la terminologie qui sont traités plus en détail dans les sections suivantes.</span><span class="sxs-lookup"><span data-stu-id="49192-110">In addition, this section contains an overview of concepts and terminology that are covered in more depth in subsequent sections.</span></span>

<span data-ttu-id="49192-111">Il existe deux approches fondamentalement différentes de la construction d’un PrintTicket.</span><span class="sxs-lookup"><span data-stu-id="49192-111">There are two fundamentally different approaches to constructing a PrintTicket.</span></span> <span data-ttu-id="49192-112">Vous pouvez utiliser l’une ou l’autre de ces approches.</span><span class="sxs-lookup"><span data-stu-id="49192-112">Either approach can be used.</span></span>

-   <span data-ttu-id="49192-113">Ciblez le PrintTicket sur un appareil inconnu ou générique en [créant un PrintTicket générique](creating-a-generic-printticket.md).</span><span class="sxs-lookup"><span data-stu-id="49192-113">Target the PrintTicket to an unknown or generic device by [Creating a Generic PrintTicket](creating-a-generic-printticket.md).</span></span>

    <span data-ttu-id="49192-114">Si votre objectif principal est de préserver l’intention de l’utilisateur final, vous souhaiterez peut-être adopter cette approche, en construisant et en stockant un PrintTicket générique non validé avec le document.</span><span class="sxs-lookup"><span data-stu-id="49192-114">If your primary objective is to preserve the end user's intent, you might want to take this approach, by constructing and storing an unvalidated generic PrintTicket with the document.</span></span>

-   <span data-ttu-id="49192-115">Ciblez le PrintTicket sur un appareil spécifique, en [créant un Device-Specific PrintTicket](creating-a-device-specific-printticket.md).</span><span class="sxs-lookup"><span data-stu-id="49192-115">Target the PrintTicket to a specific device, by [Creating a Device-Specific PrintTicket](creating-a-device-specific-printticket.md).</span></span>

    <span data-ttu-id="49192-116">Si vous souhaitez tirer parti de toutes les fonctionnalités offertes par un appareil particulier, vous souhaiterez peut-être adopter cette approche, en construisant un PrintTicket pour l’appareil spécifique et en stockant le PrintTicket validé avec le document.</span><span class="sxs-lookup"><span data-stu-id="49192-116">If you are more interested in taking advantage of all of the features offered by a particular device, you might want to take this approach, by constructing a PrintTicket for the specific device and storing the validated PrintTicket with the document.</span></span>

## <a name="related-topics"></a><span data-ttu-id="49192-117">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="49192-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="49192-118">Spécification du schéma d’impression</span><span class="sxs-lookup"><span data-stu-id="49192-118">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



