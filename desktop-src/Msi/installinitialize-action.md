---
description: L’action InstallInitialize et l’action InstallFinalize marquent le début et la fin d’une séquence d’actions qui modifient le système.
ms.assetid: c2637070-3fd9-422c-9252-cf15045c6485
title: Action InstallInitialize
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80d500779ed018905edfc5347d85d21cc40e6175
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103752204"
---
# <a name="installinitialize-action"></a><span data-ttu-id="0bd90-103">Action InstallInitialize</span><span class="sxs-lookup"><span data-stu-id="0bd90-103">InstallInitialize Action</span></span>

<span data-ttu-id="0bd90-104">L’action InstallInitialize et l’action [InstallFinalize](installfinalize-action.md) marquent le début et la fin d’une séquence d’actions qui modifient le système.</span><span class="sxs-lookup"><span data-stu-id="0bd90-104">The InstallInitialize action and [InstallFinalize](installfinalize-action.md) action mark the beginning and end of a sequence of actions that change the system.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="0bd90-105">Restrictions de séquence</span><span class="sxs-lookup"><span data-stu-id="0bd90-105">Sequence Restrictions</span></span>

<span data-ttu-id="0bd90-106">L’action InstallInitialize doit être séquencée avant toute action qui modifie le système, telle que l’action [InstallFiles](installfiles-action.md) , l’action [WriteRegistryValues](writeregistryvalues-action.md) , l’action [SelfRegModules](selfregmodules-action.md) et l’action [ProcessComponents](processcomponents-action.md) .</span><span class="sxs-lookup"><span data-stu-id="0bd90-106">The InstallInitialize action must be sequenced before any actions that change the system, such as the [InstallFiles](installfiles-action.md) action, the [WriteRegistryValues](writeregistryvalues-action.md) action, the [SelfRegModules](selfregmodules-action.md) action, and the [ProcessComponents](processcomponents-action.md) action.</span></span> <span data-ttu-id="0bd90-107">L’action InstallInitialize doit donc être séquencée avant l’action [InstallFinalize](installfinalize-action.md) et l’action [InstallExecute](installexecute-action.md) .</span><span class="sxs-lookup"><span data-stu-id="0bd90-107">The InstallInitialize action must therefore be sequenced before the [InstallFinalize](installfinalize-action.md) action and the [InstallExecute](installexecute-action.md) action.</span></span>

<span data-ttu-id="0bd90-108">Les [actions personnalisées](custom-actions.md) qui modifient le package Windows Installer, par exemple en ajoutant des lignes à une table qui gère des ressources installables, telles que la table [du Registre](registry-table.md) ou la table [DuplicateFile](duplicatefile-table.md) , doivent être séquencées avant l’action InstallInitialize.</span><span class="sxs-lookup"><span data-stu-id="0bd90-108">[Custom actions](custom-actions.md) that modify the Windows Installer package, for example by adding rows to a table that handles installable resources, such as the [Registry](registry-table.md) table or [DuplicateFile](duplicatefile-table.md) table, must be sequenced before InstallInitialize action.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="0bd90-109">Messages ActionData</span><span class="sxs-lookup"><span data-stu-id="0bd90-109">ActionData Messages</span></span>

<span data-ttu-id="0bd90-110">Il n’y a aucun message ActionData.</span><span class="sxs-lookup"><span data-stu-id="0bd90-110">There are no ActionData messages.</span></span>

 

 



