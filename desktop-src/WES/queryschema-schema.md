---
title: Schéma de requête
ms.assetid: 5710231b-5195-413e-8953-e47a411897a6
description: 'En savoir plus sur : schéma de requête'
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: aa9b6c842ff7acd874e8e467d07c31e298a63564
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104209664"
---
# <a name="query-schema"></a><span data-ttu-id="e8619-103">Schéma de requête</span><span class="sxs-lookup"><span data-stu-id="e8619-103">Query Schema</span></span>

<span data-ttu-id="e8619-104">Le schéma de requête définit les éléments et types suivants que vous pouvez utiliser pour écrire une requête XML structurée afin de récupérer des événements à partir d’un canal ou d’un fichier journal :</span><span class="sxs-lookup"><span data-stu-id="e8619-104">The Query Schema defines the following elements and types that you can use to write a structured XML query to retrieve events from a channel or log file:</span></span>

-   [<span data-ttu-id="e8619-105">Éléments QuerySchema</span><span class="sxs-lookup"><span data-stu-id="e8619-105">QuerySchema Elements</span></span>](queryschema-elements.md)
-   [<span data-ttu-id="e8619-106">Types complexes QuerySchema</span><span class="sxs-lookup"><span data-stu-id="e8619-106">QuerySchema Complex Types</span></span>](queryschema-complex-types.md)

<span data-ttu-id="e8619-107">La section éléments contient les noms des éléments que vous utilisez dans votre requête ; Toutefois, pour obtenir les détails de chaque élément, consultez le type complexe qui contient l’élément.</span><span class="sxs-lookup"><span data-stu-id="e8619-107">The elements section contains the names of the elements that you use in your query; however, to get the details for each element, see the complex type that contains the element.</span></span>

<span data-ttu-id="e8619-108">Une requête peut contenir une ou plusieurs expressions XPath utilisées pour inclure ou exclure un événement dans le jeu de résultats de la requête.</span><span class="sxs-lookup"><span data-stu-id="e8619-108">A query can contain one or more XPath expressions that are used to include or exclude event in the query result set.</span></span> <span data-ttu-id="e8619-109">Vous pouvez rechercher des événements à partir de plusieurs canaux ou fichiers journaux, mais vous ne pouvez pas mélanger des canaux et des fichiers journaux.</span><span class="sxs-lookup"><span data-stu-id="e8619-109">You can query for events from multiple channels or log files but you cannot mix channels and log files.</span></span> <span data-ttu-id="e8619-110">Vous pouvez utiliser une requête dans toute fonction qui accepte un XPath (par exemple, les fonctions [**EvtQuery**](/windows/desktop/api/WinEvt/nf-winevt-evtquery) ou [**EvtSubscribe**](/windows/desktop/api/WinEvt/nf-winevt-evtsubscribe) ).</span><span class="sxs-lookup"><span data-stu-id="e8619-110">You can use a query in any function that takes an XPath (for example, the [**EvtQuery**](/windows/desktop/api/WinEvt/nf-winevt-evtquery) or [**EvtSubscribe**](/windows/desktop/api/WinEvt/nf-winevt-evtsubscribe) functions).</span></span> <span data-ttu-id="e8619-111">Chaque XPath que vous spécifiez est limité à 32 expressions.</span><span class="sxs-lookup"><span data-stu-id="e8619-111">Each XPath that you specify is limited to 32 expressions.</span></span> <span data-ttu-id="e8619-112">Pour obtenir un exemple, consultez [consommation d’événements](consuming-events.md).</span><span class="sxs-lookup"><span data-stu-id="e8619-112">For an example, see [Consuming Events](consuming-events.md).</span></span>

<span data-ttu-id="e8619-113">Le SDK Windows inclut le schéma dans le \\ fichier include \\ query. xsd.</span><span class="sxs-lookup"><span data-stu-id="e8619-113">The Windows SDK includes the schema in the \\Include\\Query.xsd file.</span></span>

<span data-ttu-id="e8619-114">Outre le schéma de requête, le journal des événements Windows définit également les schémas suivants :</span><span class="sxs-lookup"><span data-stu-id="e8619-114">In addition to the Query schema, Windows Event Log also defines the following schemas:</span></span>

-   <span data-ttu-id="e8619-115">[Schéma EventManifest](eventmanifestschema-schema.md): définit les éléments et les types utilisés pour écrire un manifeste d’instrumentation.</span><span class="sxs-lookup"><span data-stu-id="e8619-115">[EventManifest Schema](eventmanifestschema-schema.md)—defines the elements and types used to write an instrumentation manifest.</span></span>
-   <span data-ttu-id="e8619-116">[Schéma d’événement](eventschema-schema.md): définit les éléments et les types utilisés pour le rendu d’un événement.</span><span class="sxs-lookup"><span data-stu-id="e8619-116">[Event Schema](eventschema-schema.md)—defines the elements and types used to render an event.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e8619-117">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="e8619-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e8619-118">Événements de consommation</span><span class="sxs-lookup"><span data-stu-id="e8619-118">Consuming Events</span></span>](consuming-events.md)
</dt> </dl>

 

 




