---
description: Après avoir créé un document HTML source de page de référence des événements (ERP), vous devez le nommer pour que Moniteur réseau puisse l’afficher dans le observateur d’événements.
ms.assetid: 0c668a8b-94a5-4996-8214-4629a24a8337
title: Attribution d’un nom à une page de référence d’événement
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f9c82b153ce2c7086af3883bcf3c4b34a0e68a6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106524743"
---
# <a name="naming-an-event-reference-page"></a><span data-ttu-id="eac6b-103">Attribution d’un nom à une page de référence d’événement</span><span class="sxs-lookup"><span data-stu-id="eac6b-103">Naming an Event Reference Page</span></span>

<span data-ttu-id="eac6b-104">Après avoir créé un document HTML source de page de référence des événements (ERP), vous devez le nommer pour que Moniteur réseau puisse l’afficher dans le observateur d’événements.</span><span class="sxs-lookup"><span data-stu-id="eac6b-104">After you author an event reference page (ERP) source HTML document, you must name it before Network Monitor can display it in the Event Viewer.</span></span>

<span data-ttu-id="eac6b-105">Analyse de nom et fichiers ERP expert au format suivant :</span><span class="sxs-lookup"><span data-stu-id="eac6b-105">Name monitor and expert ERP files with this format:</span></span>

``` syntax
<ExpertName><EventIdent>.htm (or <MonitorName><EventIdent>.htm)
```

<dl> <dt>

<span data-ttu-id="eac6b-106"><span id="ExpertName"></span><span id="expertname"></span><span id="EXPERTNAME"></span>**ExpertName**</span><span class="sxs-lookup"><span data-stu-id="eac6b-106"><span id="ExpertName"></span><span id="expertname"></span><span id="EXPERTNAME"></span>**ExpertName**</span></span>
</dt> <dd>

<span data-ttu-id="eac6b-107">Nom du fichier DLL, à l’exclusion de l’extension de nom de fichier.</span><span class="sxs-lookup"><span data-stu-id="eac6b-107">DLL file name, excluding the file name extension.</span></span>

</dd> <dt>

<span data-ttu-id="eac6b-108"><span id="EventIdent"></span><span id="eventident"></span><span id="EVENTIDENT"></span>**EventIdent**</span><span class="sxs-lookup"><span data-stu-id="eac6b-108"><span id="EventIdent"></span><span id="eventident"></span><span id="EVENTIDENT"></span>**EventIdent**</span></span>
</dt> <dd>

<span data-ttu-id="eac6b-109">Identificateur d’événement de l’expert ERP.</span><span class="sxs-lookup"><span data-stu-id="eac6b-109">Event identifier of the expert ERP.</span></span>

<span data-ttu-id="eac6b-110">L’identificateur d’événement se trouve également dans le membre **EventIdent** de la structure **NMEVENTDATA** .</span><span class="sxs-lookup"><span data-stu-id="eac6b-110">The event identifier is also found in the **EventIdent** member of the **NMEVENTDATA** structure.</span></span>

</dd> </dl>

<span data-ttu-id="eac6b-111">Pour plus d’informations sur la création d’une ERP, consultez les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="eac6b-111">For more information about creating an ERP, see the following topics:</span></span>

-   [<span data-ttu-id="eac6b-112">Création d’un expert et surveillance des pages de référence des événements</span><span class="sxs-lookup"><span data-stu-id="eac6b-112">Creating Expert and Monitor Event Reference Pages</span></span>](creating-expert-and-monitor-event-reference-pages.md)
-   [<span data-ttu-id="eac6b-113">Écriture d’une page de référence d’événement</span><span class="sxs-lookup"><span data-stu-id="eac6b-113">Writing an Event Reference Page</span></span>](writing-an-event-reference-page.md)
-   [<span data-ttu-id="eac6b-114">Test d’une page de référence d’événement</span><span class="sxs-lookup"><span data-stu-id="eac6b-114">Testing an Event Reference Page</span></span>](testing-an-event-reference-page.md)

 

 



