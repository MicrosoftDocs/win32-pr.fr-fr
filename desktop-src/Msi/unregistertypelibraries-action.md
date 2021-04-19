---
description: L’action UnregisterTypeLibraries annule l’inscription des bibliothèques de types à partir du système. Cette action s’applique à chaque fichier figurant dans la table TypeLib qui est déclenchée pour être désinstallé.
ms.assetid: fea5bdc1-ac27-4d02-bcea-5c97366dd394
title: Action UnregisterTypeLibraries
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b399f80d940839c5e94028a9c32e706f4826341a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106535636"
---
# <a name="unregistertypelibraries-action"></a><span data-ttu-id="0dad9-104">Action UnregisterTypeLibraries</span><span class="sxs-lookup"><span data-stu-id="0dad9-104">UnregisterTypeLibraries Action</span></span>

<span data-ttu-id="0dad9-105">L’action UnregisterTypeLibraries annule l’inscription des bibliothèques de types à partir du système.</span><span class="sxs-lookup"><span data-stu-id="0dad9-105">The UnregisterTypeLibraries action unregisters type libraries from the system.</span></span> <span data-ttu-id="0dad9-106">Cette action s’applique à chaque fichier figurant dans la table [TypeLib](typelib-table.md) qui est déclenchée pour être désinstallé.</span><span class="sxs-lookup"><span data-stu-id="0dad9-106">This action is applied to each file listed in the [TypeLib](typelib-table.md) table that is triggered to be uninstalled.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="0dad9-107">Restrictions de séquence</span><span class="sxs-lookup"><span data-stu-id="0dad9-107">Sequence Restrictions</span></span>

<span data-ttu-id="0dad9-108">L’action UnregisterTypeLibraries doit précéder l’action [RemoveFiles](removefiles-action.md) .</span><span class="sxs-lookup"><span data-stu-id="0dad9-108">The UnregisterTypeLibraries action must come before the [RemoveFiles](removefiles-action.md) action.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="0dad9-109">Messages ActionData</span><span class="sxs-lookup"><span data-stu-id="0dad9-109">ActionData Messages</span></span>



| <span data-ttu-id="0dad9-110">Champ</span><span class="sxs-lookup"><span data-stu-id="0dad9-110">Field</span></span> | <span data-ttu-id="0dad9-111">Description des données d’action</span><span class="sxs-lookup"><span data-stu-id="0dad9-111">Description of action data</span></span>                        |
|-------|---------------------------------------------------|
| <span data-ttu-id="0dad9-112">\[1\]</span><span class="sxs-lookup"><span data-stu-id="0dad9-112">\[1\]</span></span> | <span data-ttu-id="0dad9-113">[GUID](guid.md) d’une bibliothèque de types non inscrite.</span><span class="sxs-lookup"><span data-stu-id="0dad9-113">[GUID](guid.md) of an unregistered type library.</span></span> |



 

 

 



