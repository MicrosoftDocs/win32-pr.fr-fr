---
description: L’action CreateShortcuts gère la création de raccourcis.
ms.assetid: 2e8a30ec-e8e7-4855-addb-2501bf85ab54
title: Action CreateShortcuts
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e59ae3cdcc9d35091690742322617f3c9d07628
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104035094"
---
# <a name="createshortcuts-action"></a><span data-ttu-id="95f13-103">Action CreateShortcuts</span><span class="sxs-lookup"><span data-stu-id="95f13-103">CreateShortcuts Action</span></span>

<span data-ttu-id="95f13-104">L’action CreateShortcuts gère la création de raccourcis.</span><span class="sxs-lookup"><span data-stu-id="95f13-104">The CreateShortcuts action manages the creation of shortcuts.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="95f13-105">Restrictions de séquence</span><span class="sxs-lookup"><span data-stu-id="95f13-105">Sequence Restrictions</span></span>

<span data-ttu-id="95f13-106">L’action CreateShortcuts doit être postérieure à l’action [InstallFiles](installfiles-action.md) et à l’action [RemoveShortcuts](removeshortcuts-action.md) .</span><span class="sxs-lookup"><span data-stu-id="95f13-106">The CreateShortcuts action must come after the [InstallFiles](installfiles-action.md) action and the [RemoveShortcuts](removeshortcuts-action.md) action.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="95f13-107">Messages ActionData</span><span class="sxs-lookup"><span data-stu-id="95f13-107">ActionData Messages</span></span>



| <span data-ttu-id="95f13-108">Champ</span><span class="sxs-lookup"><span data-stu-id="95f13-108">Field</span></span> | <span data-ttu-id="95f13-109">Description des données d’action</span><span class="sxs-lookup"><span data-stu-id="95f13-109">Description of action data</span></span>      |
|-------|---------------------------------|
| <span data-ttu-id="95f13-110">\[1\]</span><span class="sxs-lookup"><span data-stu-id="95f13-110">\[1\]</span></span> | <span data-ttu-id="95f13-111">Identificateur du raccourci créé.</span><span class="sxs-lookup"><span data-stu-id="95f13-111">Identifier of created shortcut.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="95f13-112">Notes</span><span class="sxs-lookup"><span data-stu-id="95f13-112">Remarks</span></span>

<span data-ttu-id="95f13-113">L’action CreateShortcuts crée des raccourcis vers les fichiers de clé des composants des fonctionnalités qui sont sélectionnés pour l’installation ou la publication.</span><span class="sxs-lookup"><span data-stu-id="95f13-113">The CreateShortcuts action creates shortcuts to the key files of components of features that are selected for installation or advertisement.</span></span>

## <a name="related-topics"></a><span data-ttu-id="95f13-114">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="95f13-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="95f13-115">Tableau de raccourcis</span><span class="sxs-lookup"><span data-stu-id="95f13-115">Shortcut Table</span></span>](shortcut-table.md)
</dt> <dt>

[<span data-ttu-id="95f13-116">Table MsiShortcutProperty</span><span class="sxs-lookup"><span data-stu-id="95f13-116">MsiShortcutProperty Table</span></span>](msishortcutproperty-table.md)
</dt> </dl>

 

 



