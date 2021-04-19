---
description: L’action RMCCPSearch utilise des signatures de fichiers pour vérifier que les produits éligibles sont installés sur un système avant l’exécution d’une mise à niveau.
ms.assetid: d37b2434-86eb-4c6e-b817-77c75dcebbf5
title: Action RMCCPSearch
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c273ccb03bb77e0346edf73177d938d6002878a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106517755"
---
# <a name="rmccpsearch-action"></a><span data-ttu-id="b8082-103">Action RMCCPSearch</span><span class="sxs-lookup"><span data-stu-id="b8082-103">RMCCPSearch Action</span></span>

<span data-ttu-id="b8082-104">L’action RMCCPSearch utilise des signatures de fichiers pour vérifier que les produits éligibles sont installés sur un système avant l’exécution d’une mise à niveau.</span><span class="sxs-lookup"><span data-stu-id="b8082-104">The RMCCPSearch action uses file signatures to validate that qualifying products are installed on a system before an upgrade installation is performed.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="b8082-105">Restrictions de séquence</span><span class="sxs-lookup"><span data-stu-id="b8082-105">Sequence Restrictions</span></span>

<span data-ttu-id="b8082-106">L’action RMCCPSearch doit être créée dans la [table InstallUISequence](installuisequence-table.md) et la [table InstallExecuteSequence](installexecutesequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="b8082-106">RMCCPSearch action should be authored into the [InstallUISequence table](installuisequence-table.md) and [InstallExecuteSequence table](installexecutesequence-table.md).</span></span> <span data-ttu-id="b8082-107">Le programme d’installation empêche RMCCPSearch de s’exécuter dans la séquence InstallExecuteSequence si l’action a déjà été exécutée dans la séquence InstallUISequence.</span><span class="sxs-lookup"><span data-stu-id="b8082-107">The installer prevents RMCCPSearch from running in the InstallExecuteSequence sequence if the action has already run in InstallUISequence sequence.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="b8082-108">Messages ActionData</span><span class="sxs-lookup"><span data-stu-id="b8082-108">ActionData Messages</span></span>

<span data-ttu-id="b8082-109">Il n’y a aucun message ActionData.</span><span class="sxs-lookup"><span data-stu-id="b8082-109">There are no ActionData messages.</span></span>

## <a name="remarks"></a><span data-ttu-id="b8082-110">Notes</span><span class="sxs-lookup"><span data-stu-id="b8082-110">Remarks</span></span>

<span data-ttu-id="b8082-111">L’action RMCCPSearch nécessite que la propriété [**\_ lecteur CCP**](ccp-drive.md) soit définie sur le chemin d’accès racine sur le [*volume*](v-gly.md) amovible qui a l’installation de l’un des produits éligibles.</span><span class="sxs-lookup"><span data-stu-id="b8082-111">The RMCCPSearch action requires the [**CCP\_DRIVE**](ccp-drive.md) property to be set to the root path on the removable [*volume*](v-gly.md) that has the installation for any of the qualifying products.</span></span>

<span data-ttu-id="b8082-112">Chaque signature de fichier de la table CCPSearch est recherchée dans le chemin d’accès référencé par la propriété [**\_ lecteur CCP**](ccp-drive.md) à l’aide de la table [DrLocator](drlocator-table.md) .</span><span class="sxs-lookup"><span data-stu-id="b8082-112">Each file signature in the CCPSearch table is searched for under the path referred to by the [**CCP\_DRIVE**](ccp-drive.md) property using the [DrLocator](drlocator-table.md) table.</span></span> <span data-ttu-id="b8082-113">L’absence de signature à partir de la table de [signature](signature-table.md) désigne un répertoire.</span><span class="sxs-lookup"><span data-stu-id="b8082-113">The absence of the signature from the [Signature](signature-table.md) table denotes a directory.</span></span> <span data-ttu-id="b8082-114">Si une signature est identifiée comme existante, l’action RMCCPSearch se termine.</span><span class="sxs-lookup"><span data-stu-id="b8082-114">If any signature is determined to exist, the RMCCPSearch action terminates.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b8082-115">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="b8082-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b8082-116">Table CCPSearch</span><span class="sxs-lookup"><span data-stu-id="b8082-116">CCPSearch table</span></span>](ccpsearch-table.md)
</dt> </dl>

 

 



