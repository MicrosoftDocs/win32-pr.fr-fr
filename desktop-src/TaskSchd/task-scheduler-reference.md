---
title: Référence Planificateur de tâches
description: Cette section décrit les API, les objets de script et le schéma XML fournis par le Planificateur de tâches.
ms.assetid: e3b5a1e1-4d18-44b7-aaa6-ebec11892bec
keywords:
- Planificateur de tâches Planificateur de tâches, référence
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb22306266054b8ec19a90f188c43e5eb7e4393b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103673238"
---
# <a name="task-scheduler-reference"></a><span data-ttu-id="2edbc-104">Référence Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="2edbc-104">Task Scheduler Reference</span></span>

<span data-ttu-id="2edbc-105">Cette section décrit les API, les objets de script et le schéma XML fournis par le Planificateur de tâches.</span><span class="sxs-lookup"><span data-stu-id="2edbc-105">This section describes the APIs, scripting objects, and XML schema that are provided by the Task Scheduler.</span></span>

<span data-ttu-id="2edbc-106">Les rubriques de l’API incluent une description de l’API, la syntaxe de déclaration de l’API, des notes qui décrivent des conditions spéciales pour l’API et un bloc d’impératifs qui décrit la plateforme, les fichiers d’en-tête et les bibliothèques nécessaires.</span><span class="sxs-lookup"><span data-stu-id="2edbc-106">API topics include a description of the API, the declaration syntax of the API, remarks that describe special conditions for the API, and a requirements block that describes what platform, header files, and libraries are required.</span></span>

<span data-ttu-id="2edbc-107">Les rubriques relatives aux objets de script incluent une description de l’objet, la syntaxe de déclaration de l’objet, des notes qui décrivent des conditions spéciales pour l’objet et un bloc de spécifications qui décrit quelles plateformes et bibliothèques de types sont requises.</span><span class="sxs-lookup"><span data-stu-id="2edbc-107">Scripting object topics include a description of the object, the declaration syntax of the object, remarks that describe special conditions for the object, and a requirements block that describes what platform and type libraries are required.</span></span>

<span data-ttu-id="2edbc-108">Les rubriques relatives aux schémas XML incluent une description de l’élément, du parent, de l’enfant et des informations d’attribut, ainsi que des remarques qui décrivent des conditions spéciales.</span><span class="sxs-lookup"><span data-stu-id="2edbc-108">XML schema topics include a description of the element, parent, child, and attribute information, and remarks that describe special conditions.</span></span>



| <span data-ttu-id="2edbc-109">Consultez</span><span class="sxs-lookup"><span data-stu-id="2edbc-109">See</span></span>                                                                                          | <span data-ttu-id="2edbc-110">Pour plus d’informations sur</span><span class="sxs-lookup"><span data-stu-id="2edbc-110">For information on</span></span>                                                                                                                            |
|----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2edbc-111">Objets Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="2edbc-111">Task Scheduler Objects</span></span>](task-scheduler-objects.md)                                         | <span data-ttu-id="2edbc-112">Les objets de script et leurs méthodes et propriétés.</span><span class="sxs-lookup"><span data-stu-id="2edbc-112">Scripting objects and their methods and properties.</span></span>                                                                                           |
| [<span data-ttu-id="2edbc-113">Interfaces Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="2edbc-113">Task Scheduler Interfaces</span></span>](task-scheduler-interfaces.md)                                   | <span data-ttu-id="2edbc-114">Interfaces et leurs méthodes et propriétés.</span><span class="sxs-lookup"><span data-stu-id="2edbc-114">Interfaces and their methods and properties.</span></span>                                                                                                  |
| [<span data-ttu-id="2edbc-115">Structures et unions de Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="2edbc-115">Task Scheduler Structures and Unions</span></span>](task-scheduler-structures-and-unions.md)             | <span data-ttu-id="2edbc-116">Structures et unions.</span><span class="sxs-lookup"><span data-stu-id="2edbc-116">Structures and unions.</span></span>                                                                                                                        |
| [<span data-ttu-id="2edbc-117">Types énumérés Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="2edbc-117">Task Scheduler Enumerated Types</span></span>](task-scheduler-enumerated-types.md)                       | <span data-ttu-id="2edbc-118">Constantes définies par des énumérateurs.</span><span class="sxs-lookup"><span data-stu-id="2edbc-118">Constants defined by enumerators.</span></span>                                                                                                             |
| [<span data-ttu-id="2edbc-119">Schéma Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="2edbc-119">Task Scheduler Schema</span></span>](task-scheduler-schema.md)                                           | <span data-ttu-id="2edbc-120">Éléments, types simples, types complexes et groupes d’attributs définis par le schéma.</span><span class="sxs-lookup"><span data-stu-id="2edbc-120">Elements, simple types, complex types, and attribute groups defined by the schema.</span></span>                                                            |
| [<span data-ttu-id="2edbc-121">Planificateur de tâches les constantes d’erreur et de réussite</span><span class="sxs-lookup"><span data-stu-id="2edbc-121">Task Scheduler Error and Success Constants</span></span>](task-scheduler-error-and-success-constants.md) | <span data-ttu-id="2edbc-122">Constantes d’erreur et de réussite retournées par les API Planificateur de tâches.</span><span class="sxs-lookup"><span data-stu-id="2edbc-122">Error and success constants returned by Task Scheduler APIs.</span></span>                                                                                  |
| [<span data-ttu-id="2edbc-123">**Schtasks.exe**</span><span class="sxs-lookup"><span data-stu-id="2edbc-123">**Schtasks.exe**</span></span>](schtasks.md)                                                             | <span data-ttu-id="2edbc-124">L’outil en ligne de commande Schtasks.exe utilisé pour créer, supprimer, interroger, modifier, exécuter et terminer des tâches planifiées sur un ordinateur local ou distant.</span><span class="sxs-lookup"><span data-stu-id="2edbc-124">The Schtasks.exe command line tool that is used to create, delete, query, change, run, and end scheduled tasks on a local or remote computer.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="2edbc-125">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="2edbc-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2edbc-126">Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="2edbc-126">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 




