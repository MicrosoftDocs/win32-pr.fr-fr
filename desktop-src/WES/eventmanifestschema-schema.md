---
title: Schéma EventManifest
ms.assetid: 89acbc43-739b-4e89-a96a-cc3438ec8ecc
description: 'En savoir plus sur : schéma EventManifest'
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 67e1c2e9b769cd26e81a71853037655220a27d1b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106527461"
---
# <a name="eventmanifest-schema"></a><span data-ttu-id="affe0-103">Schéma EventManifest</span><span class="sxs-lookup"><span data-stu-id="affe0-103">EventManifest Schema</span></span>

<span data-ttu-id="affe0-104">Le schéma EventManifest définit les éléments et types suivants que vous utilisez pour écrire un manifeste d’Instrumentation :</span><span class="sxs-lookup"><span data-stu-id="affe0-104">The EventManifest schema defines the following elements and types that you use to write an instrumentation manifest:</span></span>

-   [<span data-ttu-id="affe0-105">Éléments EventManifestSchema</span><span class="sxs-lookup"><span data-stu-id="affe0-105">EventManifestSchema Elements</span></span>](eventmanifestschema-elements.md)
-   [<span data-ttu-id="affe0-106">Types simples EventManifestSchema</span><span class="sxs-lookup"><span data-stu-id="affe0-106">EventManifestSchema Simple Types</span></span>](eventmanifestschema-simple-types.md)
-   [<span data-ttu-id="affe0-107">Types complexes EventManifestSchema</span><span class="sxs-lookup"><span data-stu-id="affe0-107">EventManifestSchema Complex Types</span></span>](eventmanifestschema-complex-types.md)

<span data-ttu-id="affe0-108">La section éléments contient les noms des éléments que vous utilisez dans votre manifeste ; Toutefois, pour obtenir les détails de chaque élément, consultez le type complexe qui contient l’élément.</span><span class="sxs-lookup"><span data-stu-id="affe0-108">The elements section contains the names of the elements that you use in your manifest; however, to get the details for each element, see the complex type that contains the element.</span></span>

<span data-ttu-id="affe0-109">Un manifeste d’instrumentation est un fichier XML qui définit un fournisseur d’événements, les canaux sur lesquels les événements sont écrits, les événements eux-mêmes, les critères de filtrage des événements tels que les niveaux, les tâches et les OpCodes, ainsi que les chaînes localisées utilisées lors du rendu des événements.</span><span class="sxs-lookup"><span data-stu-id="affe0-109">An instrumentation manifest is an XML file that defines an event provider, the channels to which the events are written, the events themselves, the event filtering criteria such as levels, tasks, and opcodes, and the localized strings used when rendering the events.</span></span> <span data-ttu-id="affe0-110">La Convention consiste à utiliser. Man comme extension pour les fichiers manifeste.</span><span class="sxs-lookup"><span data-stu-id="affe0-110">The convention is to use .man as the extension for manifest files.</span></span> <span data-ttu-id="affe0-111">Pour plus d’informations sur l’écriture d’un manifeste, consultez [écriture d’un manifeste d’instrumentation](writing-an-instrumentation-manifest.md).</span><span class="sxs-lookup"><span data-stu-id="affe0-111">For details on writing a manifest, see [Writing an Instrumentation Manifest](writing-an-instrumentation-manifest.md).</span></span>

<span data-ttu-id="affe0-112">Le SDK Windows inclut le schéma dans le \\ fichier include \\ eventic. xsd.</span><span class="sxs-lookup"><span data-stu-id="affe0-112">The Windows SDK includes the schema in the \\Include\\Eventman.xsd file.</span></span> <span data-ttu-id="affe0-113">Vous pouvez utiliser le XSD pour valider votre manifeste.</span><span class="sxs-lookup"><span data-stu-id="affe0-113">You can use the XSD to validate your manifest.</span></span>

<span data-ttu-id="affe0-114">Outre le schéma EventManifest, le journal des événements Windows définit également les schémas suivants :</span><span class="sxs-lookup"><span data-stu-id="affe0-114">In addition to the EventManifest schema, Windows Event Log also defines the following schemas:</span></span>

-   <span data-ttu-id="affe0-115">[Schéma d’événement](eventschema-schema.md): définit les éléments et les types utilisés pour le rendu d’un événement.</span><span class="sxs-lookup"><span data-stu-id="affe0-115">[Event Schema](eventschema-schema.md)—defines the elements and types used to render an event.</span></span>
-   <span data-ttu-id="affe0-116">[Schéma de requête](queryschema-schema.md): définit les éléments et les types utilisés pour écrire une requête afin de récupérer des événements à partir d’un ou plusieurs canaux.</span><span class="sxs-lookup"><span data-stu-id="affe0-116">[Query Schema](queryschema-schema.md)—defines the elements and types used to write a query to retrieve events from one or more channels.</span></span>

 

 




