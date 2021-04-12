---
description: L’action AppSearch utilise des signatures de fichiers pour rechercher les versions existantes des produits.
ms.assetid: 56665876-2c74-476b-aa1a-158c6e86418d
title: Action AppSearch
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04187fb146af80839e135c99986dea1902ccb6b9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104202556"
---
# <a name="appsearch-action"></a><span data-ttu-id="c48c8-103">Action AppSearch</span><span class="sxs-lookup"><span data-stu-id="c48c8-103">AppSearch Action</span></span>

<span data-ttu-id="c48c8-104">L’action AppSearch utilise des signatures de fichiers pour rechercher les versions existantes des produits.</span><span class="sxs-lookup"><span data-stu-id="c48c8-104">The AppSearch action uses file signatures to search for existing versions of products.</span></span> <span data-ttu-id="c48c8-105">L’action AppSearch peut utiliser ces informations pour déterminer où les mises à niveau doivent être installées.</span><span class="sxs-lookup"><span data-stu-id="c48c8-105">The AppSearch action may use this information to determine where upgrades are to be installed.</span></span> <span data-ttu-id="c48c8-106">L’action AppSearch peut également être utilisée pour affecter à une propriété la valeur existante d’une entrée de registre ou de fichier. ini.</span><span class="sxs-lookup"><span data-stu-id="c48c8-106">The AppSearch action can also be used to set a property to the existing value of an registry or .ini file entry.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="c48c8-107">Restrictions de séquence</span><span class="sxs-lookup"><span data-stu-id="c48c8-107">Sequence Restrictions</span></span>

<span data-ttu-id="c48c8-108">AppSearch doit être créé dans la [table InstallUISequence](installuisequence-table.md) et la [table InstallExecuteSequence](installexecutesequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="c48c8-108">AppSearch should be authored into the [InstallUISequence table](installuisequence-table.md) and [InstallExecuteSequence table](installexecutesequence-table.md).</span></span> <span data-ttu-id="c48c8-109">Le programme d’installation empêche l’action AppSearch de s’exécuter dans la séquence InstallExecuteSequence si l’action a déjà été exécutée dans la séquence InstallUISequence.</span><span class="sxs-lookup"><span data-stu-id="c48c8-109">The installer prevents the AppSearch action from running in the InstallExecuteSequence sequence if the action has already run in InstallUISequence sequence.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="c48c8-110">Messages ActionData</span><span class="sxs-lookup"><span data-stu-id="c48c8-110">ActionData Messages</span></span>



| <span data-ttu-id="c48c8-111">Champ</span><span class="sxs-lookup"><span data-stu-id="c48c8-111">Field</span></span> | <span data-ttu-id="c48c8-112">Description des données d’action</span><span class="sxs-lookup"><span data-stu-id="c48c8-112">Description of action data</span></span>      |
|-------|---------------------------------|
| <span data-ttu-id="c48c8-113">\[1\]</span><span class="sxs-lookup"><span data-stu-id="c48c8-113">\[1\]</span></span> | <span data-ttu-id="c48c8-114">Propriété contenant l’emplacement du fichier.</span><span class="sxs-lookup"><span data-stu-id="c48c8-114">Property holding file location.</span></span> |
| <span data-ttu-id="c48c8-115">\[2\]</span><span class="sxs-lookup"><span data-stu-id="c48c8-115">\[2\]</span></span> | <span data-ttu-id="c48c8-116">Signature de fichier.</span><span class="sxs-lookup"><span data-stu-id="c48c8-116">File signature.</span></span>                 |



 

## <a name="remarks"></a><span data-ttu-id="c48c8-117">Notes</span><span class="sxs-lookup"><span data-stu-id="c48c8-117">Remarks</span></span>

<span data-ttu-id="c48c8-118">L’action AppSearch requiert que la table de [signatures](signature-table.md) soit présente dans le package d’installation.</span><span class="sxs-lookup"><span data-stu-id="c48c8-118">The AppSearch action requires that the [Signature](signature-table.md) table be present in the installation package.</span></span> <span data-ttu-id="c48c8-119">Les signatures de fichiers sont répertoriées dans la table de signature.</span><span class="sxs-lookup"><span data-stu-id="c48c8-119">File signatures are listed in the Signature table.</span></span> <span data-ttu-id="c48c8-120">Une signature qui ne figure pas dans la table de signature désigne un répertoire et l’action définit la propriété sur le chemin d’accès au répertoire de cette signature.</span><span class="sxs-lookup"><span data-stu-id="c48c8-120">A signature that is not in the Signature table denotes a directory and the action sets the property to the directory path for that signature.</span></span>

<span data-ttu-id="c48c8-121">L’action AppSearch recherche d’abord des signatures de fichier à l’aide de la table [CompLocator](complocator-table.md) , la table [RegLocator](reglocator-table.md) , puis la table [IniLocator](inilocator-table.md) et enfin la table [DrLocator](drlocator-table.md) .</span><span class="sxs-lookup"><span data-stu-id="c48c8-121">The AppSearch action searches for file signatures using the [CompLocator](complocator-table.md) table first, the [RegLocator](reglocator-table.md) table next, then the [IniLocator](inilocator-table.md) table, and finally the [DrLocator](drlocator-table.md) table.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c48c8-122">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="c48c8-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c48c8-123">AppSearch</span><span class="sxs-lookup"><span data-stu-id="c48c8-123">AppSearch</span></span>](appsearch-table.md)
</dt> <dt>

[<span data-ttu-id="c48c8-124">CompLocator</span><span class="sxs-lookup"><span data-stu-id="c48c8-124">CompLocator</span></span>](complocator-table.md)
</dt> <dt>

[<span data-ttu-id="c48c8-125">IniLocator</span><span class="sxs-lookup"><span data-stu-id="c48c8-125">IniLocator</span></span>](inilocator-table.md)
</dt> <dt>

[<span data-ttu-id="c48c8-126">RegLocator</span><span class="sxs-lookup"><span data-stu-id="c48c8-126">RegLocator</span></span>](reglocator-table.md)
</dt> <dt>

[<span data-ttu-id="c48c8-127">DrLocator</span><span class="sxs-lookup"><span data-stu-id="c48c8-127">DrLocator</span></span>](drlocator-table.md)
</dt> </dl>

 

 



