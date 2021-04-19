---
description: Cette rubrique n’est pas à jour. Pour obtenir les informations les plus récentes, consultez la spécification du schéma d’impression.
ms.assetid: 87a897cd-d3aa-488a-b129-9837d3500d0d
title: Ce qu’est un document PrintCapabilities
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd6e18082a5e551f3997dad8b9688d84ff2f824a
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2021
ms.locfileid: "106535117"
---
# <a name="what-a-printcapabilities-document-is-not"></a><span data-ttu-id="dc13b-104">Ce qu’est un document PrintCapabilities</span><span class="sxs-lookup"><span data-stu-id="dc13b-104">What a PrintCapabilities Document Is Not</span></span>

<span data-ttu-id="dc13b-105">Cette rubrique n’est pas à jour.</span><span class="sxs-lookup"><span data-stu-id="dc13b-105">This topic is not current.</span></span> <span data-ttu-id="dc13b-106">Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="dc13b-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="dc13b-107">Il est utile de répertorier certaines des fonctionnalités et informations que le document PrintCapabilities n’est pas destiné à fournir.</span><span class="sxs-lookup"><span data-stu-id="dc13b-107">It is worthwhile to list some of the functionality and information the PrintCapabilities document is not intended to provide.</span></span>

<span data-ttu-id="dc13b-108">Un document PrintCapabilities :</span><span class="sxs-lookup"><span data-stu-id="dc13b-108">A PrintCapabilities document:</span></span>

-   <span data-ttu-id="dc13b-109">Ne représente pas des données à valeurs multiples (dépendantes de la configuration).</span><span class="sxs-lookup"><span data-stu-id="dc13b-109">Does not represent multivalued (configuration-dependent) data.</span></span>

    <span data-ttu-id="dc13b-110">Chaque document PrintCapabilities est construit pour une configuration spécifique.</span><span class="sxs-lookup"><span data-stu-id="dc13b-110">Each PrintCapabilities document is constructed for a specific configuration.</span></span> <span data-ttu-id="dc13b-111">Aucune propriété ou ScoredProperty dans le document ne peut avoir une valeur qui dépend de la configuration particulière.</span><span class="sxs-lookup"><span data-stu-id="dc13b-111">No Property or ScoredProperty in the document can have a Value that depends on the particular configuration.</span></span> <span data-ttu-id="dc13b-112">Dans la version de schéma initiale, le fournisseur PrintCapabilities doit traiter l’entrée PrintTicket et créer un document PrintCapabilities qui contient les valeurs de propriété appropriées pour la configuration spécifiée dans PrintTicket.</span><span class="sxs-lookup"><span data-stu-id="dc13b-112">In the initial schema version, the PrintCapabilities provider must process the input PrintTicket and create a PrintCapabilities document that contains Property values appropriate for the configuration specified in the PrintTicket.</span></span>

-   <span data-ttu-id="dc13b-113">Ne contient pas d’informations de contrainte.</span><span class="sxs-lookup"><span data-stu-id="dc13b-113">Does not contain constraint information.</span></span>

    <span data-ttu-id="dc13b-114">Le document PrintCapabilities n’indique pas quelles configurations sont autorisées et qui ne sont pas autorisées.</span><span class="sxs-lookup"><span data-stu-id="dc13b-114">The PrintCapabilities document does not indicate which configurations are allowed and which are not allowed.</span></span> <span data-ttu-id="dc13b-115">Dans la version de schéma initiale, le fournisseur PrintCapabilities doit stocker toutes les informations nécessaires pour valider les configurations, fournir une méthode qui valide l’entrée PrintTicket et retourner un PrintTicket corrigé dans le cas où le PrintTicket spécifié viole une ou plusieurs contraintes.</span><span class="sxs-lookup"><span data-stu-id="dc13b-115">In the initial schema version, the PrintCapabilities provider must store any information needed to validate configurations, supply a method that validates the input PrintTicket, and return a corrected PrintTicket in the event that the specified PrintTicket violates one or more constraints.</span></span>

-   <span data-ttu-id="dc13b-116">Ne contient pas d’informations sur l’appareil dynamique.</span><span class="sxs-lookup"><span data-stu-id="dc13b-116">Does not contain dynamic device information.</span></span>

    <span data-ttu-id="dc13b-117">Il y a trop de surcharge impliquée dans la construction du document PrintCapabilities pour qu’il soit utilisé pour conserver rapidement les informations d’État, telles que les niveaux d’encre, le papier restant dans chaque plateau ou l’état du bourrage papier.</span><span class="sxs-lookup"><span data-stu-id="dc13b-117">There is too much overhead involved in constructing the PrintCapabilities document for it to be used to hold rapidly changing status information, such as ink levels, paper remaining in each tray, or paper jam status.</span></span>

## <a name="related-topics"></a><span data-ttu-id="dc13b-118">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="dc13b-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dc13b-119">Spécification du schéma d’impression</span><span class="sxs-lookup"><span data-stu-id="dc13b-119">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



