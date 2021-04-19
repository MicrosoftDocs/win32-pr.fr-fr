---
description: L’action CCPSearch utilise des signatures de fichiers pour vérifier que les produits éligibles sont installés sur un système avant l’exécution d’une mise à niveau.
ms.assetid: 0aa7bf8b-de76-464d-8e7b-3aa4f609fe19
title: Action CCPSearch
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a8b1f01462ac0ba9dcf8838b9a043d95aef8cefe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106534474"
---
# <a name="ccpsearch-action"></a><span data-ttu-id="e49ed-103">Action CCPSearch</span><span class="sxs-lookup"><span data-stu-id="e49ed-103">CCPSearch Action</span></span>

<span data-ttu-id="e49ed-104">L’action CCPSearch utilise des signatures de fichiers pour vérifier que les produits éligibles sont installés sur un système avant l’exécution d’une mise à niveau.</span><span class="sxs-lookup"><span data-stu-id="e49ed-104">The CCPSearch action uses file signatures to validate that qualifying products are installed on a system before an upgrade installation is performed.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="e49ed-105">Restrictions de séquence</span><span class="sxs-lookup"><span data-stu-id="e49ed-105">Sequence Restrictions</span></span>

<span data-ttu-id="e49ed-106">L’action CCPSearch doit être créée dans la [table InstallUISequence](installuisequence-table.md) et la [table InstallExecuteSequence](installexecutesequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="e49ed-106">CCPSearch action should be authored into the [InstallUISequence table](installuisequence-table.md) and [InstallExecuteSequence table](installexecutesequence-table.md).</span></span> <span data-ttu-id="e49ed-107">Le programme d’installation empêche l’action CCPSearch de s’exécuter dans la séquence InstallExecuteSequence si l’action a déjà été exécutée dans la séquence InstallUISequence.</span><span class="sxs-lookup"><span data-stu-id="e49ed-107">The installer prevents the CCPSearch action from running in the InstallExecuteSequence sequence if the action has already run in InstallUISequence sequence.</span></span> <span data-ttu-id="e49ed-108">L’action CCPSearch doit précéder l’action [RMCCPSearch](rmccpsearch-action.md) .</span><span class="sxs-lookup"><span data-stu-id="e49ed-108">The CCPSearch action must come before the [RMCCPSearch](rmccpsearch-action.md) action.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="e49ed-109">Messages ActionData</span><span class="sxs-lookup"><span data-stu-id="e49ed-109">ActionData Messages</span></span>

<span data-ttu-id="e49ed-110">Il n’y a aucun message ActionData.</span><span class="sxs-lookup"><span data-stu-id="e49ed-110">There are no ActionData messages.</span></span>

## <a name="remarks"></a><span data-ttu-id="e49ed-111">Notes</span><span class="sxs-lookup"><span data-stu-id="e49ed-111">Remarks</span></span>

<span data-ttu-id="e49ed-112">L’action CCPSearch recherche des signatures de fichiers listées dans la table CCPSearch sur le système en utilisant les tables suivantes dans l’ordre : signature, CompLocator, RegLocator, IniLocator et DrLocator.</span><span class="sxs-lookup"><span data-stu-id="e49ed-112">The CCPSearch action searches for file signatures listed in the CCPSearch table on the system using the following tables in order: Signature, CompLocator, RegLocator, IniLocator, and DrLocator.</span></span>

<span data-ttu-id="e49ed-113">Si une signature est identifiée comme existante, la propriété **CCP \_ Success** a la valeur 1 et l’action CCPSearch se termine.</span><span class="sxs-lookup"><span data-stu-id="e49ed-113">If any signature is determined to exist, the **CCP\_Success** property is set to 1 and the CCPSearch action terminates.</span></span>

<span data-ttu-id="e49ed-114">L’absence de signature à partir de la table de signature désigne un répertoire.</span><span class="sxs-lookup"><span data-stu-id="e49ed-114">The absence of the signature from the Signature table denotes a directory.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e49ed-115">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="e49ed-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e49ed-116">CCPSearch</span><span class="sxs-lookup"><span data-stu-id="e49ed-116">CCPSearch</span></span>](ccpsearch-table.md)
</dt> <dt>

[<span data-ttu-id="e49ed-117">Signature</span><span class="sxs-lookup"><span data-stu-id="e49ed-117">Signature</span></span>](signature-table.md)
</dt> <dt>

[<span data-ttu-id="e49ed-118">CompLocator</span><span class="sxs-lookup"><span data-stu-id="e49ed-118">CompLocator</span></span>](complocator-table.md)
</dt> <dt>

[<span data-ttu-id="e49ed-119">RegLocator</span><span class="sxs-lookup"><span data-stu-id="e49ed-119">RegLocator</span></span>](reglocator-table.md)
</dt> <dt>

[<span data-ttu-id="e49ed-120">IniLocator</span><span class="sxs-lookup"><span data-stu-id="e49ed-120">IniLocator</span></span>](inilocator-table.md)
</dt> <dt>

[<span data-ttu-id="e49ed-121">DrLocator</span><span class="sxs-lookup"><span data-stu-id="e49ed-121">DrLocator</span></span>](drlocator-table.md)
</dt> </dl>

 

 



