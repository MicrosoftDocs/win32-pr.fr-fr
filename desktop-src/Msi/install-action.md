---
description: L’action d’installation est une action de niveau supérieur appelée pour installer ou supprimer des composants.
ms.assetid: bf290b59-1ecb-410f-b1f6-fdbeebebe3d3
title: Action d’installation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04279ba66f189ff83146fc2010e6843c20b404d7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104034348"
---
# <a name="install-action"></a><span data-ttu-id="1edfe-103">Action d’installation</span><span class="sxs-lookup"><span data-stu-id="1edfe-103">INSTALL Action</span></span>

<span data-ttu-id="1edfe-104">L’action d’installation est une action de niveau supérieur appelée pour installer ou supprimer des composants.</span><span class="sxs-lookup"><span data-stu-id="1edfe-104">The INSTALL action is a top-level action called to install or remove components.</span></span> <span data-ttu-id="1edfe-105">Cette action interroge la table [InstallUISequence](installuisequence-table.md) et la [table InstallExecuteSequence](installexecutesequence-table.md) pour l’action à exécuter, la condition d’exécution de l’action et la place de l’action dans la séquence :</span><span class="sxs-lookup"><span data-stu-id="1edfe-105">This action queries the [InstallUISequence Table](installuisequence-table.md) and [InstallExecuteSequence Table](installexecutesequence-table.md) for the action to execute, the condition for action execution, and the place of the action in the sequence:</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="1edfe-106">Restrictions de séquence</span><span class="sxs-lookup"><span data-stu-id="1edfe-106">Sequence Restrictions</span></span>

<span data-ttu-id="1edfe-107">Il n’existe aucune restriction de séquence.</span><span class="sxs-lookup"><span data-stu-id="1edfe-107">There are no sequence restrictions.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="1edfe-108">Messages ActionData</span><span class="sxs-lookup"><span data-stu-id="1edfe-108">ActionData Messages</span></span>

<span data-ttu-id="1edfe-109">Il n’y a aucun message ActionData.</span><span class="sxs-lookup"><span data-stu-id="1edfe-109">There are no ActionData messages.</span></span>

## <a name="remarks"></a><span data-ttu-id="1edfe-110">Notes</span><span class="sxs-lookup"><span data-stu-id="1edfe-110">Remarks</span></span>

<span data-ttu-id="1edfe-111">L’action d’installation n’est pas appelée à partir de la séquence de la table d’action, elle est passée à Windows Installer quand [**MsiInstallProduct**](/windows/desktop/api/Msi/nf-msi-msiinstallproducta) est appelé, ou l’exécutable de ligne de commande Msiexec.exe est appelé avec le commutateur de ligne de commande «**/i**», ou lorsqu’une fonction de programme d’installation est appelée et peut exécuter une tâche d’installation, telle que [**MsiConfigureFeature**](/windows/desktop/api/Msi/nf-msi-msiconfigurefeaturea), [**MsiProvideComponent**](/windows/desktop/api/Msi/nf-msi-msiprovidecomponenta)ou [**MsiInstallMissingFile**](/windows/desktop/api/Msi/nf-msi-msiinstallmissingfilea).</span><span class="sxs-lookup"><span data-stu-id="1edfe-111">The INSTALL action is not called from within the action table sequence, it is passed to Windows Installer when [**MsiInstallProduct**](/windows/desktop/api/Msi/nf-msi-msiinstallproducta) is called, or the command line executable Msiexec.exe is called with the '**/i**' command line switch, or when any installer function is called that may perform an installation task, such as [**MsiConfigureFeature**](/windows/desktop/api/Msi/nf-msi-msiconfigurefeaturea), [**MsiProvideComponent**](/windows/desktop/api/Msi/nf-msi-msiprovidecomponenta), or [**MsiInstallMissingFile**](/windows/desktop/api/Msi/nf-msi-msiinstallmissingfilea).</span></span>

 

 



