---
description: Après avoir sélectionné le CIEM approprié pour la validation, un développeur doit rassembler les actions personnalisées dans une base de données ICE.
ms.assetid: 69151d5a-be6e-4947-862d-cea65306c536
title: Génération d’une base de données ICE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f51043aa9b3c1591fa3262492c117aba35f23d92
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864426"
---
# <a name="building-an-ice-database"></a><span data-ttu-id="1f28c-103">Génération d’une base de données ICE</span><span class="sxs-lookup"><span data-stu-id="1f28c-103">Building an ICE Database</span></span>

<span data-ttu-id="1f28c-104">Après avoir sélectionné le [CIEM](internal-consistency-evaluators-ices.md) approprié pour la validation, un développeur doit rassembler les actions personnalisées dans une base de données Ice.</span><span class="sxs-lookup"><span data-stu-id="1f28c-104">After selecting the appropriate [ICEs](internal-consistency-evaluators-ices.md) for validation, a developer must collect the custom actions together into an ICE database.</span></span> <span data-ttu-id="1f28c-105">Un fichier. CUB est une base de données. msi standard qui contient uniquement le CIEM et les tables requises.</span><span class="sxs-lookup"><span data-stu-id="1f28c-105">A .cub file is a standard .msi database that contains only ICEs and their required tables.</span></span> <span data-ttu-id="1f28c-106">Un fichier. CUB ne peut pas être installé et est utilisé uniquement pour stocker et fournir l’accès aux actions personnalisées ICE.</span><span class="sxs-lookup"><span data-stu-id="1f28c-106">A .cub file cannot be installed and is used only to store and provide access to ICE custom actions.</span></span>

<span data-ttu-id="1f28c-107">Un fichier. CUB contient les tables de base de données suivantes.</span><span class="sxs-lookup"><span data-stu-id="1f28c-107">A .cub file contains the following database tables.</span></span>



| <span data-ttu-id="1f28c-108">Table de charge de travail</span><span class="sxs-lookup"><span data-stu-id="1f28c-108">Table</span></span>                                  | <span data-ttu-id="1f28c-109">Description</span><span class="sxs-lookup"><span data-stu-id="1f28c-109">Description</span></span>                                                                                                                                                                                                                                                                |
|----------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1f28c-110">Binaire</span><span class="sxs-lookup"><span data-stu-id="1f28c-110">Binary</span></span>](binary-table.md)             | <span data-ttu-id="1f28c-111">Fichiers de script, dll et exe des actions en douane ICE qui sont référencées dans la table CustomAction.</span><span class="sxs-lookup"><span data-stu-id="1f28c-111">The script files, DLLs, and EXEs of the ICE customs actions that are referenced in the CustomAction table.</span></span>                                                                                                                                                                 |
| [<span data-ttu-id="1f28c-112">CustomAction</span><span class="sxs-lookup"><span data-stu-id="1f28c-112">CustomAction</span></span>](customaction-table.md) | <span data-ttu-id="1f28c-113">Chaque enregistrement dans cette table correspond à une action personnalisée ICE incluse dans le fichier. CUB.</span><span class="sxs-lookup"><span data-stu-id="1f28c-113">Each record in this table corresponds to an ICE custom action included in the .cub file.</span></span>                                                                                                                                                                                   |
| <span data-ttu-id="1f28c-114">\_ICESequence</span><span class="sxs-lookup"><span data-stu-id="1f28c-114">\_ICESequence</span></span>                          | <span data-ttu-id="1f28c-115">Ce tableau répertorie les actions de la glace en douane incluses dans le fichier. CUB dans leur séquence d’exécution.</span><span class="sxs-lookup"><span data-stu-id="1f28c-115">This table lists the ICE customs actions included in the .cub file in their execution sequence.</span></span> <span data-ttu-id="1f28c-116">Les actions personnalisées ICE répertoriées dans ce tableau sont exécutées en appelant [**MsiSequence**](/windows/desktop/api/Msiquery/nf-msiquery-msisequencea), ou exécutées individuellement à l’aide de [**MsiDoAction**](/windows/desktop/api/Msiquery/nf-msiquery-msidoactiona).</span><span class="sxs-lookup"><span data-stu-id="1f28c-116">The ICE custom actions listed in this table are executed by calling [**MsiSequence**](/windows/desktop/api/Msiquery/nf-msiquery-msisequencea), or individually executed using [**MsiDoAction**](/windows/desktop/api/Msiquery/nf-msiquery-msidoactiona).</span></span> |
| [<span data-ttu-id="1f28c-117">\_Validation</span><span class="sxs-lookup"><span data-stu-id="1f28c-117">\_Validation</span></span>](-validation-table.md)  | <span data-ttu-id="1f28c-118">Cette table contient les entrées du fichier. CUB qui doivent être fusionnées dans la \_ table de validation.</span><span class="sxs-lookup"><span data-stu-id="1f28c-118">This table contains the .cub file entries that are to be merged into the \_Validation table.</span></span>                                                                                                                                                                               |
| <span data-ttu-id="1f28c-119">\_Spécial</span><span class="sxs-lookup"><span data-stu-id="1f28c-119">\_Special</span></span>                              | <span data-ttu-id="1f28c-120">Toutes les tables de traitement spéciales requises par certaines actions personnalisées ICE doivent être incluses dans le fichier. CUB.</span><span class="sxs-lookup"><span data-stu-id="1f28c-120">Any special processing tables required by particular ICE custom actions must be included in the .cub file.</span></span> <span data-ttu-id="1f28c-121">Le nom de ces tables doit avoir un trait de soulignement de début.</span><span class="sxs-lookup"><span data-stu-id="1f28c-121">The name of these tables must have a leading underscore.</span></span>                                                                                                        |



 

<span data-ttu-id="1f28c-122">Consultez [exemple de fichier. CUB](sample--cub-file.md).</span><span class="sxs-lookup"><span data-stu-id="1f28c-122">See [Sample .cub File](sample--cub-file.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="1f28c-123">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="1f28c-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1f28c-124">Génération d’une glace</span><span class="sxs-lookup"><span data-stu-id="1f28c-124">Building An ICE</span></span>](building-an-ice.md)
</dt> </dl>

 

 



