---
description: L’action InstallSFPCatalogFile installe les catalogues utilisés par Windows me pour la protection des fichiers Windows.
ms.assetid: 1c8253f1-ac7d-4346-a16e-887d16f521d9
title: Action InstallSFPCatalogFile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ddc4192f8ee0062c51833292a98c28ea27c12531
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106513359"
---
# <a name="installsfpcatalogfile-action"></a><span data-ttu-id="cb329-103">Action InstallSFPCatalogFile</span><span class="sxs-lookup"><span data-stu-id="cb329-103">InstallSFPCatalogFile Action</span></span>

<span data-ttu-id="cb329-104">L’action InstallSFPCatalogFile installe les catalogues utilisés par Windows me pour la protection des fichiers Windows.</span><span class="sxs-lookup"><span data-stu-id="cb329-104">The InstallSFPCatalogFile action installs the catalogs used by Windows Me for Windows File Protection.</span></span> <span data-ttu-id="cb329-105">InstallSFPCatalogFile interroge la table de [composants](component-table.md), la [table de fichiers](file-table.md), la table [FileSFPCatalog](filesfpcatalog-table.md) et la [table SFPCatalog](sfpcatalog-table.md).</span><span class="sxs-lookup"><span data-stu-id="cb329-105">InstallSFPCatalogFile queries the [Component table](component-table.md), [File table](file-table.md), [FileSFPCatalog table](filesfpcatalog-table.md) and [SFPCatalog table](sfpcatalog-table.md).</span></span> <span data-ttu-id="cb329-106">Les catalogues sont installés s’ils sont associés à un fichier dans un composant qui est défini pour une installation locale ou s’ils sont associés à un fichier en cours de réparation dans un composant installé localement.</span><span class="sxs-lookup"><span data-stu-id="cb329-106">Catalogs are installed if they are associated with a file in a component that is set for local installation or if they are associated with a file being repaired in a locally installed component.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="cb329-107">Restrictions de séquence</span><span class="sxs-lookup"><span data-stu-id="cb329-107">Sequence Restrictions</span></span>

<span data-ttu-id="cb329-108">L’action InstallSFPCatalogFile doit être séquencée avant [InstallFiles](installfiles-action.md) et après [CostFinalize](costfinalize-action.md).</span><span class="sxs-lookup"><span data-stu-id="cb329-108">The InstallSFPCatalogFile action must be sequenced before [InstallFiles](installfiles-action.md) and after [CostFinalize](costfinalize-action.md).</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="cb329-109">Messages ActionData</span><span class="sxs-lookup"><span data-stu-id="cb329-109">ActionData Messages</span></span>



| <span data-ttu-id="cb329-110">Champ</span><span class="sxs-lookup"><span data-stu-id="cb329-110">Field</span></span> | <span data-ttu-id="cb329-111">Description des données d’action</span><span class="sxs-lookup"><span data-stu-id="cb329-111">Description of action data</span></span>                                    |
|-------|---------------------------------------------------------------|
| <span data-ttu-id="cb329-112">\[1\]</span><span class="sxs-lookup"><span data-stu-id="cb329-112">\[1\]</span></span> | <span data-ttu-id="cb329-113">Nom du catalogue en cours d’installation.</span><span class="sxs-lookup"><span data-stu-id="cb329-113">Name of the catalog being installed.</span></span>                          |
| <span data-ttu-id="cb329-114">\[2\]</span><span class="sxs-lookup"><span data-stu-id="cb329-114">\[2\]</span></span> | <span data-ttu-id="cb329-115">Nom du catalogue dont l’installation du catalogue dépend.</span><span class="sxs-lookup"><span data-stu-id="cb329-115">Name of the catalog this catalog's installation depends upon.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="cb329-116">Notes</span><span class="sxs-lookup"><span data-stu-id="cb329-116">Remarks</span></span>

<span data-ttu-id="cb329-117">Catalogue dépendant d’un autre catalogue installé après le catalogue parent.</span><span class="sxs-lookup"><span data-stu-id="cb329-117">A catalog that is dependent on another catalog installed after the parent catalog.</span></span>

 

 



