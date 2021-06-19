---
description: Découvrez quelques-unes des fonctionnalités et des informations que le document PrintCapabilities n’est pas destiné à fournir.
ms.assetid: 87a897cd-d3aa-488a-b129-9837d3500d0d
title: Ce qu’est un document PrintCapabilities
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8bcd5dbedf6ee3a7e2713bd3591b182c606cfb0c
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112409892"
---
# <a name="what-a-printcapabilities-document-is-not"></a><span data-ttu-id="2dbc9-103">Ce qu’est un document PrintCapabilities</span><span class="sxs-lookup"><span data-stu-id="2dbc9-103">What a PrintCapabilities Document Is Not</span></span>

<span data-ttu-id="2dbc9-104">Cette rubrique n’est pas à jour.</span><span class="sxs-lookup"><span data-stu-id="2dbc9-104">This topic is not current.</span></span> <span data-ttu-id="2dbc9-105">Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="2dbc9-105">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="2dbc9-106">Il est utile de répertorier certaines des fonctionnalités et informations que le document PrintCapabilities n’est pas destiné à fournir.</span><span class="sxs-lookup"><span data-stu-id="2dbc9-106">It is worthwhile to list some of the functionality and information the PrintCapabilities document is not intended to provide.</span></span>

<span data-ttu-id="2dbc9-107">Un document PrintCapabilities :</span><span class="sxs-lookup"><span data-stu-id="2dbc9-107">A PrintCapabilities document:</span></span>

-   <span data-ttu-id="2dbc9-108">Ne représente pas des données à valeurs multiples (dépendantes de la configuration).</span><span class="sxs-lookup"><span data-stu-id="2dbc9-108">Does not represent multivalued (configuration-dependent) data.</span></span>

    <span data-ttu-id="2dbc9-109">Chaque document PrintCapabilities est construit pour une configuration spécifique.</span><span class="sxs-lookup"><span data-stu-id="2dbc9-109">Each PrintCapabilities document is constructed for a specific configuration.</span></span> <span data-ttu-id="2dbc9-110">Aucune propriété ou ScoredProperty dans le document ne peut avoir une valeur qui dépend de la configuration particulière.</span><span class="sxs-lookup"><span data-stu-id="2dbc9-110">No Property or ScoredProperty in the document can have a Value that depends on the particular configuration.</span></span> <span data-ttu-id="2dbc9-111">Dans la version de schéma initiale, le fournisseur PrintCapabilities doit traiter l’entrée PrintTicket et créer un document PrintCapabilities qui contient les valeurs de propriété appropriées pour la configuration spécifiée dans PrintTicket.</span><span class="sxs-lookup"><span data-stu-id="2dbc9-111">In the initial schema version, the PrintCapabilities provider must process the input PrintTicket and create a PrintCapabilities document that contains Property values appropriate for the configuration specified in the PrintTicket.</span></span>

-   <span data-ttu-id="2dbc9-112">Ne contient pas d’informations de contrainte.</span><span class="sxs-lookup"><span data-stu-id="2dbc9-112">Does not contain constraint information.</span></span>

    <span data-ttu-id="2dbc9-113">Le document PrintCapabilities n’indique pas quelles configurations sont autorisées et qui ne sont pas autorisées.</span><span class="sxs-lookup"><span data-stu-id="2dbc9-113">The PrintCapabilities document does not indicate which configurations are allowed and which are not allowed.</span></span> <span data-ttu-id="2dbc9-114">Dans la version de schéma initiale, le fournisseur PrintCapabilities doit stocker toutes les informations nécessaires pour valider les configurations, fournir une méthode qui valide l’entrée PrintTicket et retourner un PrintTicket corrigé dans le cas où le PrintTicket spécifié viole une ou plusieurs contraintes.</span><span class="sxs-lookup"><span data-stu-id="2dbc9-114">In the initial schema version, the PrintCapabilities provider must store any information needed to validate configurations, supply a method that validates the input PrintTicket, and return a corrected PrintTicket in the event that the specified PrintTicket violates one or more constraints.</span></span>

-   <span data-ttu-id="2dbc9-115">Ne contient pas d’informations sur l’appareil dynamique.</span><span class="sxs-lookup"><span data-stu-id="2dbc9-115">Does not contain dynamic device information.</span></span>

    <span data-ttu-id="2dbc9-116">Il y a trop de surcharge impliquée dans la construction du document PrintCapabilities pour qu’il soit utilisé pour conserver rapidement les informations d’État, telles que les niveaux d’encre, le papier restant dans chaque plateau ou l’état du bourrage papier.</span><span class="sxs-lookup"><span data-stu-id="2dbc9-116">There is too much overhead involved in constructing the PrintCapabilities document for it to be used to hold rapidly changing status information, such as ink levels, paper remaining in each tray, or paper jam status.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2dbc9-117">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="2dbc9-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2dbc9-118">Spécification du schéma d’impression</span><span class="sxs-lookup"><span data-stu-id="2dbc9-118">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



