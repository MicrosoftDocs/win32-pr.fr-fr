---
title: Schéma d’événement
ms.assetid: 36037697-b777-4e5c-99af-77964200a3e4
description: En savoir plus sur le schéma d’événement
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: bfb26f6c71d544e0c0a6a4d833b40a5d15ae5485
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864978"
---
# <a name="event-schema"></a><span data-ttu-id="a63da-103">Schéma d’événement</span><span class="sxs-lookup"><span data-stu-id="a63da-103">Event Schema</span></span>

<span data-ttu-id="a63da-104">Le schéma d’événement définit les éléments et types suivants qui identifient les éléments et les attributs d’un événement enregistré :</span><span class="sxs-lookup"><span data-stu-id="a63da-104">The Event schema defines the following elements and types that identify the elements and attributes of a logged event:</span></span>

-   [<span data-ttu-id="a63da-105">Éléments EventSchema</span><span class="sxs-lookup"><span data-stu-id="a63da-105">EventSchema Elements</span></span>](eventschema-elements.md)
-   [<span data-ttu-id="a63da-106">Types simples EventSchema</span><span class="sxs-lookup"><span data-stu-id="a63da-106">EventSchema Simple Types</span></span>](eventschema-simple-types.md)
-   [<span data-ttu-id="a63da-107">Types complexes EventSchema</span><span class="sxs-lookup"><span data-stu-id="a63da-107">EventSchema Complex Types</span></span>](eventschema-complex-types.md)

<span data-ttu-id="a63da-108">La section éléments contient les noms des éléments que vous trouverez dans les événements journalisés. Toutefois, pour obtenir les détails de chaque élément, consultez le type complexe qui contient l’élément.</span><span class="sxs-lookup"><span data-stu-id="a63da-108">The elements section contains the names of the elements that you would find in a logged events; however, to get the details for each element, see the complex type that contains the element.</span></span>

<span data-ttu-id="a63da-109">Le SDK Windows inclut le schéma dans le \\ fichier include \\ Event. xsd.</span><span class="sxs-lookup"><span data-stu-id="a63da-109">The Windows SDK includes the schema in the \\Include\\Event.xsd file.</span></span>

<span data-ttu-id="a63da-110">Vous pouvez utiliser ce schéma pour identifier les éléments et les attributs lors de l’appel de la fonction [**EvtRender**](/windows/desktop/api/WinEvt/nf-winevt-evtrender) pour afficher des sections ou des propriétés spécifiques de l’événement.</span><span class="sxs-lookup"><span data-stu-id="a63da-110">You can use this schema to identify the elements and attributes when calling the [**EvtRender**](/windows/desktop/api/WinEvt/nf-winevt-evtrender) function to render specific sections or properties of the event.</span></span> <span data-ttu-id="a63da-111">Pour obtenir un exemple qui montre comment utiliser ce schéma lors du rendu des événements, consultez [rendu des événements](rendering-events.md).</span><span class="sxs-lookup"><span data-stu-id="a63da-111">For an example that shows how to use this schema when rendering events, see [Rendering Events](rendering-events.md).</span></span>

<span data-ttu-id="a63da-112">Outre le schéma d’événement, le journal des événements Windows définit également les schémas suivants :</span><span class="sxs-lookup"><span data-stu-id="a63da-112">In addition to the Event schema, Windows Event Log also defines the following schemas:</span></span>

-   <span data-ttu-id="a63da-113">[Schéma EventManifest](eventmanifestschema-schema.md): définit les éléments et les types utilisés pour écrire un manifeste d’instrumentation.</span><span class="sxs-lookup"><span data-stu-id="a63da-113">[EventManifest Schema](eventmanifestschema-schema.md)—defines the elements and types used to write an instrumentation manifest.</span></span>
-   <span data-ttu-id="a63da-114">[Schéma de requête](queryschema-schema.md): définit les éléments et les types utilisés pour écrire une requête afin de récupérer des événements à partir d’un ou plusieurs canaux.</span><span class="sxs-lookup"><span data-stu-id="a63da-114">[Query Schema](queryschema-schema.md)—defines the elements and types used to write a query to retrieve events from one or more channels.</span></span>

 

 




