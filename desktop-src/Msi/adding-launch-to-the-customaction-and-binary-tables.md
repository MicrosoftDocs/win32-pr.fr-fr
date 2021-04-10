---
description: Ajoutez un enregistrement à la table CustomAction pour l’action personnalisée Launch.
ms.assetid: 010ce7cd-010b-4fac-90ad-5745c6a38630
title: Ajout d’un lancement aux tables CustomAction et binaires
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3bbcd1b483505d7d33981d695ed0d29c3b72a3f9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104115390"
---
# <a name="adding-launch-to-the-customaction-and-binary-tables"></a><span data-ttu-id="1519e-103">Ajout d’un lancement aux tables CustomAction et binaires</span><span class="sxs-lookup"><span data-stu-id="1519e-103">Adding Launch to the CustomAction and Binary Tables</span></span>

<span data-ttu-id="1519e-104">Ajoutez un enregistrement à la [table CustomAction](customaction-table.md) pour l’action personnalisée Launch.</span><span class="sxs-lookup"><span data-stu-id="1519e-104">Add a record to the [CustomAction table](customaction-table.md) for the Launch custom action.</span></span> <span data-ttu-id="1519e-105">Entrez le nom de l’action personnalisée dans la colonne action de la table CustomAction.</span><span class="sxs-lookup"><span data-stu-id="1519e-105">Enter the custom action's name in the Action column of the CustomAction table.</span></span> <span data-ttu-id="1519e-106">Entrez le type numérique total pour Launch, 65, dans la colonne type de la table d’action personnalisée.</span><span class="sxs-lookup"><span data-stu-id="1519e-106">Enter the total numeric type for Launch, 65, into the Type column of the Custom action table.</span></span> <span data-ttu-id="1519e-107">La colonne source de la table CustomAction spécifie une clé dans l’enregistrement de la [table binaire](binary-table.md) qui contient les données binaires de la dll.</span><span class="sxs-lookup"><span data-stu-id="1519e-107">The Source column of the CustomAction table specifies a key into the record of the [Binary Table](binary-table.md) that contains the binary data for the DLL.</span></span> <span data-ttu-id="1519e-108">Entrez Tutorial.dll dans la colonne source de la table CustomAction.</span><span class="sxs-lookup"><span data-stu-id="1519e-108">Enter Tutorial.dll into the Source column of the CustomAction table.</span></span> <span data-ttu-id="1519e-109">Le point d’entrée spécifié dans le champ cible de la table CustomAction doit correspondre à celui exporté à partir de la DLL.</span><span class="sxs-lookup"><span data-stu-id="1519e-109">The entry point specified in the Target field of the CustomAction table must match that exported from the DLL.</span></span> <span data-ttu-id="1519e-110">Entrez LaunchTutorial dans la colonne cible de la table CustomAction.</span><span class="sxs-lookup"><span data-stu-id="1519e-110">Enter LaunchTutorial into the Target column of the CustomAction table.</span></span>

[<span data-ttu-id="1519e-111">Table CustomAction</span><span class="sxs-lookup"><span data-stu-id="1519e-111">CustomAction Table</span></span>](customaction-table.md)



| <span data-ttu-id="1519e-112">Action</span><span class="sxs-lookup"><span data-stu-id="1519e-112">Action</span></span> | <span data-ttu-id="1519e-113">Type</span><span class="sxs-lookup"><span data-stu-id="1519e-113">Type</span></span> | <span data-ttu-id="1519e-114">Source</span><span class="sxs-lookup"><span data-stu-id="1519e-114">Source</span></span>       | <span data-ttu-id="1519e-115">Cible</span><span class="sxs-lookup"><span data-stu-id="1519e-115">Target</span></span>         |
|--------|------|--------------|----------------|
| <span data-ttu-id="1519e-116">Lancer</span><span class="sxs-lookup"><span data-stu-id="1519e-116">Launch</span></span> | <span data-ttu-id="1519e-117">65</span><span class="sxs-lookup"><span data-stu-id="1519e-117">65</span></span>   | <span data-ttu-id="1519e-118">Tutorial.dll</span><span class="sxs-lookup"><span data-stu-id="1519e-118">Tutorial.dll</span></span> | <span data-ttu-id="1519e-119">LaunchTutorial</span><span class="sxs-lookup"><span data-stu-id="1519e-119">LaunchTutorial</span></span> |



 

<span data-ttu-id="1519e-120">Ajoutez la Tutorial.dll que vous avez créée à partir de Tutorial. cpp en tant que flux binaire à la table binaire.</span><span class="sxs-lookup"><span data-stu-id="1519e-120">Add the Tutorial.dll you created from Tutorial.cpp as a binary stream to the Binary table.</span></span>

[<span data-ttu-id="1519e-121">Table binaire</span><span class="sxs-lookup"><span data-stu-id="1519e-121">Binary Table</span></span>](binary-table.md)



| <span data-ttu-id="1519e-122">Nom</span><span class="sxs-lookup"><span data-stu-id="1519e-122">Name</span></span>         | <span data-ttu-id="1519e-123">Données</span><span class="sxs-lookup"><span data-stu-id="1519e-123">Data</span></span>                          |
|--------------|-------------------------------|
| <span data-ttu-id="1519e-124">Tutorial.dll</span><span class="sxs-lookup"><span data-stu-id="1519e-124">Tutorial.dll</span></span> | <span data-ttu-id="1519e-125">{*données binaires ajoutées pour la dll*}</span><span class="sxs-lookup"><span data-stu-id="1519e-125">{*binary data added for DLL*}</span></span> |



 

<span data-ttu-id="1519e-126">Continuez à [Ajouter un événement de contrôle à la fin de l’installation pour exécuter le lancement](adding-a-control-event-at-the-end-of-the-installation-to-run-launch.md).</span><span class="sxs-lookup"><span data-stu-id="1519e-126">Continue to [Adding a Control Event at the End of the Installation to Run Launch](adding-a-control-event-at-the-end-of-the-installation-to-run-launch.md).</span></span>

 

 



