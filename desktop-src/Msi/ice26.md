---
description: ICE26 valide les tables de séquence dans une base de données Windows Installer.
ms.assetid: 7ea47452-3147-4d39-961d-a10eca8328c9
title: ICE26
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d7b110d0b15b37441170980d0fd3e96e2eb00d5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866293"
---
# <a name="ice26"></a><span data-ttu-id="fe4df-103">ICE26</span><span class="sxs-lookup"><span data-stu-id="fe4df-103">ICE26</span></span>

<span data-ttu-id="fe4df-104">ICE26 vérifie que chacune des [*tables de séquence*](s-gly.md) suivantes contient les actions requises par la table et qu’elle ne contient aucune action interdite dans la table :</span><span class="sxs-lookup"><span data-stu-id="fe4df-104">ICE26 validates that each of the following [*sequence tables*](s-gly.md) contain the actions that are required by the table and does not contain any actions disallowed in the table:</span></span>

-   [<span data-ttu-id="fe4df-105">Table AdminUISequence</span><span class="sxs-lookup"><span data-stu-id="fe4df-105">AdminUISequence table</span></span>](adminuisequence-table.md)
-   [<span data-ttu-id="fe4df-106">Table AdminExecuteSequence</span><span class="sxs-lookup"><span data-stu-id="fe4df-106">AdminExecuteSequence table</span></span>](adminexecutesequence-table.md)
-   [<span data-ttu-id="fe4df-107">Table InstallUISequence</span><span class="sxs-lookup"><span data-stu-id="fe4df-107">InstallUISequence table</span></span>](installuisequence-table.md)
-   [<span data-ttu-id="fe4df-108">Table InstallExecuteSequence</span><span class="sxs-lookup"><span data-stu-id="fe4df-108">InstallExecuteSequence table</span></span>](installexecutesequence-table.md)

## <a name="result"></a><span data-ttu-id="fe4df-109">Résultats</span><span class="sxs-lookup"><span data-stu-id="fe4df-109">Result</span></span>

<span data-ttu-id="fe4df-110">ICE26 publie un message d’erreur si le package d’installation a une table de séquences qui n’a pas d’action requise ou qui contient une action qui n’est pas autorisée pour la table.</span><span class="sxs-lookup"><span data-stu-id="fe4df-110">ICE26 posts an error message if the installation package has a sequence table that lacks a required action or that contains an action that is disallowed for the table.</span></span>

## <a name="example"></a><span data-ttu-id="fe4df-111">Exemple</span><span class="sxs-lookup"><span data-stu-id="fe4df-111">Example</span></span>



| <span data-ttu-id="fe4df-112">Erreur ICE26</span><span class="sxs-lookup"><span data-stu-id="fe4df-112">ICE26 error</span></span>                                                                   | <span data-ttu-id="fe4df-113">Description</span><span class="sxs-lookup"><span data-stu-id="fe4df-113">Description</span></span>                                                                                                                                                                    |
|-------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fe4df-114">Action : 'action1 'est obligatoire dans la table de séquences InstallExecuteSequence.</span><span class="sxs-lookup"><span data-stu-id="fe4df-114">Action: 'Action1' is required in the InstallExecuteSequence Sequence table.</span></span>   | <span data-ttu-id="fe4df-115">Une action requise est absente de la table de séquences indiquée.</span><span class="sxs-lookup"><span data-stu-id="fe4df-115">A required action is missing from the indicated sequence table.</span></span> <span data-ttu-id="fe4df-116">Consultez le template.msi ou les tables de séquence suggérées dans [à l’aide d’une table de séquences](using-a-sequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="fe4df-116">See the template.msi or the suggested sequence tables in [Using a Sequence Table](using-a-sequence-table.md).</span></span> |
| <span data-ttu-id="fe4df-117">Action : 'action2 'est interdit dans la table de séquences InstallExecuteSequence.</span><span class="sxs-lookup"><span data-stu-id="fe4df-117">Action: 'Action2' is prohibited in the InstallExecuteSequence Sequence table.</span></span> | <span data-ttu-id="fe4df-118">Cette action ne peut pas figurer dans la table de séquence indiquée.</span><span class="sxs-lookup"><span data-stu-id="fe4df-118">This action cannot be in the indicated sequence table.</span></span> <span data-ttu-id="fe4df-119">Supprimez cette action de la table Sequence.</span><span class="sxs-lookup"><span data-stu-id="fe4df-119">Remove this action from the sequence table.</span></span>                                                                             |



 

## <a name="related-topics"></a><span data-ttu-id="fe4df-120">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="fe4df-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fe4df-121">Référence ICE</span><span class="sxs-lookup"><span data-stu-id="fe4df-121">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



