---
description: ICE82 vérifie que l’action RegisterProduct, l’action RegisterUser, l’action PublishProduct et l’action PublishFeatures sont toutes présentes dans la table InstallExecuteSequence. Le package est validé si toutes les actions sont présentes.
ms.assetid: b41a56f9-b57e-4133-ae7d-c51b36bab44f
title: ICE82
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8aa6ba2e0bd07af06bf90c604c333966b5581ba3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103758415"
---
# <a name="ice82"></a><span data-ttu-id="6c09b-104">ICE82</span><span class="sxs-lookup"><span data-stu-id="6c09b-104">ICE82</span></span>

<span data-ttu-id="6c09b-105">ICE82 vérifie que l’action [RegisterProduct](registerproduct-action.md), l' [action RegisterUser](registeruser-action.md), l’action [PublishProduct](publishproduct-action.md)et l' [action PublishFeatures](publishfeatures-action.md) sont toutes présentes dans la [table InstallExecuteSequence](installexecutesequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="6c09b-105">ICE82 validates that the [RegisterProduct Action](registerproduct-action.md), [RegisterUser Action](registeruser-action.md), [PublishProduct Action](publishproduct-action.md), and [PublishFeatures Action](publishfeatures-action.md) are all present in the [InstallExecuteSequence table](installexecutesequence-table.md).</span></span> <span data-ttu-id="6c09b-106">Le package est validé si toutes les actions sont présentes.</span><span class="sxs-lookup"><span data-stu-id="6c09b-106">The package is validated if all the actions are present.</span></span>

<span data-ttu-id="6c09b-107">ICE82 publie un avertissement s’il y a deux actions avec le même numéro de séquence répertorié dans les tables InstallExecuteSequence, InstallUISequence, AdminExecuteSequence, AdminUISequence ou AdvtExecuteSequence.</span><span class="sxs-lookup"><span data-stu-id="6c09b-107">ICE82 posts a warning if there are two actions with the same sequence number listed in the InstallExecuteSequence, InstallUISequence, AdminExecuteSequence, AdminUISequence, or AdvtExecuteSequence tables .</span></span>

## <a name="result"></a><span data-ttu-id="6c09b-108">Résultats</span><span class="sxs-lookup"><span data-stu-id="6c09b-108">Result</span></span>

<span data-ttu-id="6c09b-109">ICE82 publie les avertissements suivants.</span><span class="sxs-lookup"><span data-stu-id="6c09b-109">ICE82 posts the following warnings.</span></span>



| <span data-ttu-id="6c09b-110">AVERTISSEMENT ICE82</span><span class="sxs-lookup"><span data-stu-id="6c09b-110">ICE82 warning</span></span>                                                                                                                                                                                                                 | <span data-ttu-id="6c09b-111">Description</span><span class="sxs-lookup"><span data-stu-id="6c09b-111">Description</span></span>                                                                                                                                                                                                 |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6c09b-112">La table InstallExecuteSequence ne contient pas l’ensemble des actions mentionnées ci-dessous : actions manquantes :</span><span class="sxs-lookup"><span data-stu-id="6c09b-112">The InstallExecuteSequence table does not contain the set of actions mentioned below: Actions Missing:</span></span><br/> <span data-ttu-id="6c09b-113">Publier les fonctionnalités</span><span class="sxs-lookup"><span data-stu-id="6c09b-113">Publish Features</span></span><br/> <span data-ttu-id="6c09b-114">Publier le produit</span><span class="sxs-lookup"><span data-stu-id="6c09b-114">Publish Product</span></span><br/> <span data-ttu-id="6c09b-115">Inscrire le produit</span><span class="sxs-lookup"><span data-stu-id="6c09b-115">Register Product</span></span><br/> <span data-ttu-id="6c09b-116">Inscrire un utilisateur</span><span class="sxs-lookup"><span data-stu-id="6c09b-116">Register User</span></span><br/> | <span data-ttu-id="6c09b-117">L’action personnalisée ICE82 publie un avertissement si les quatre actions sont absentes.</span><span class="sxs-lookup"><span data-stu-id="6c09b-117">ICE82 custom action posts a warning if all four actions are absent.</span></span>                                                                                                                                         |
| <span data-ttu-id="6c09b-118">\[ \] Le numéro de séquence 2 de l’action 1 est dupliqué \[ \] dans le tableau \[ 3 \] .</span><span class="sxs-lookup"><span data-stu-id="6c09b-118">This action \[1\] has duplicate sequence number \[2\] in the table \[3\].</span></span>                                                                                                                                                     | <span data-ttu-id="6c09b-119">ICE82 publie un avertissement s’il y a deux actions avec le même numéro de séquence répertorié dans les tables InstallExecuteSequence, InstallUISequence, AdminExecuteSequence, AdminUISequence ou AdvtExecuteSequence.</span><span class="sxs-lookup"><span data-stu-id="6c09b-119">ICE82 posts a warning if there are two actions with the same sequence number listed in the InstallExecuteSequence, InstallUISequence, AdminExecuteSequence, AdminUISequence, or AdvtExecuteSequence tables.</span></span> |



 

<span data-ttu-id="6c09b-120">ICE82 publie les erreurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="6c09b-120">ICE82 posts the following errors.</span></span>



| <span data-ttu-id="6c09b-121">Erreur ICE82</span><span class="sxs-lookup"><span data-stu-id="6c09b-121">ICE82 error</span></span>                                                                                                                                                                                                                                        | <span data-ttu-id="6c09b-122">Description</span><span class="sxs-lookup"><span data-stu-id="6c09b-122">Description</span></span>                                                                         |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="6c09b-123">Le InstallExecuteSequence doit contenir toutes les actions mentionnées ci-dessous ou aucune des actions présentes</span><span class="sxs-lookup"><span data-stu-id="6c09b-123">The InstallExecuteSequence should either contain all of the actions mentioned below or none of them Actions Present</span></span><br/> <List of actions present> <br/> <span data-ttu-id="6c09b-124">Actions manquantes :</span><span class="sxs-lookup"><span data-stu-id="6c09b-124">Actions Missing:</span></span><br/> <List of actions missing> <br/> | <span data-ttu-id="6c09b-125">ICE82 publie une erreur si certaines des quatre actions sont présentes et que d’autres sont absentes.</span><span class="sxs-lookup"><span data-stu-id="6c09b-125">ICE82 posts an error if some of the four actions are present and others are absent.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="6c09b-126">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="6c09b-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6c09b-127">Référence ICE</span><span class="sxs-lookup"><span data-stu-id="6c09b-127">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 




