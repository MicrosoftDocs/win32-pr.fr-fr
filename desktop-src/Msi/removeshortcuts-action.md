---
description: L’action RemoveShortcuts gère la suppression d’un raccourci publié dont la fonctionnalité est sélectionnée pour la désinstallation ou un raccourci non publié dont le composant est sélectionné pour la désinstallation. Pour plus d’informations, consultez le tableau des raccourcis.
ms.assetid: 897e8a13-d9c5-4f98-8785-c0f053a11f3d
title: Action RemoveShortcuts
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 151f5fac6733e61b7ba27320a5e79c522abcc3e0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106518537"
---
# <a name="removeshortcuts-action"></a><span data-ttu-id="66741-104">Action RemoveShortcuts</span><span class="sxs-lookup"><span data-stu-id="66741-104">RemoveShortcuts Action</span></span>

<span data-ttu-id="66741-105">L’action RemoveShortcuts gère la suppression d’un raccourci publié dont la fonctionnalité est sélectionnée pour la désinstallation ou un raccourci non publié dont le composant est sélectionné pour la désinstallation.</span><span class="sxs-lookup"><span data-stu-id="66741-105">The RemoveShortcuts action manages the removal of an advertised shortcut whose feature is selected for uninstallation or a nonadvertised shortcut whose component is selected for uninstallation.</span></span> <span data-ttu-id="66741-106">Pour plus d’informations, consultez le [tableau des raccourcis](shortcut-table.md).</span><span class="sxs-lookup"><span data-stu-id="66741-106">For more information, see the [Shortcut Table](shortcut-table.md).</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="66741-107">Restrictions de séquence</span><span class="sxs-lookup"><span data-stu-id="66741-107">Sequence Restrictions</span></span>

<span data-ttu-id="66741-108">L’action RemoveShortcuts doit précéder l’action [CreateShortcuts](createshortcuts-action.md) .</span><span class="sxs-lookup"><span data-stu-id="66741-108">The RemoveShortcuts action must come before the [CreateShortcuts](createshortcuts-action.md) action.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="66741-109">Messages ActionData</span><span class="sxs-lookup"><span data-stu-id="66741-109">ActionData Messages</span></span>



| <span data-ttu-id="66741-110">Champ</span><span class="sxs-lookup"><span data-stu-id="66741-110">Field</span></span> | <span data-ttu-id="66741-111">Description des données d’action</span><span class="sxs-lookup"><span data-stu-id="66741-111">Description of action data</span></span>      |
|-------|---------------------------------|
| <span data-ttu-id="66741-112">\[1\]</span><span class="sxs-lookup"><span data-stu-id="66741-112">\[1\]</span></span> | <span data-ttu-id="66741-113">Identificateur du raccourci supprimé.</span><span class="sxs-lookup"><span data-stu-id="66741-113">Identifier of removed shortcut.</span></span> |



 

 

 



