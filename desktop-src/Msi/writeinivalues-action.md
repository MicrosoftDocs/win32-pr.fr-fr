---
description: L’action WriteIniValues écrit les informations du fichier. ini que l’application a besoin d’écrire dans ses fichiers. ini.
ms.assetid: ec54db54-293c-4db3-81af-6e8669f27310
title: Action WriteIniValues
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd96e86c361c7fe83b6ad33959149e82fb9d7969
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866049"
---
# <a name="writeinivalues-action"></a><span data-ttu-id="8adb3-103">Action WriteIniValues</span><span class="sxs-lookup"><span data-stu-id="8adb3-103">WriteIniValues Action</span></span>

<span data-ttu-id="8adb3-104">L’action WriteIniValues écrit les informations du fichier. ini que l’application a besoin d’écrire dans ses fichiers. ini.</span><span class="sxs-lookup"><span data-stu-id="8adb3-104">The WriteIniValues action writes the .ini file information that the application needs written to its .ini files.</span></span> <span data-ttu-id="8adb3-105">L’écriture de ces informations est contrôlée par la [table des composants](component-table.md).</span><span class="sxs-lookup"><span data-stu-id="8adb3-105">The writing of this information is gated by the [Component table](component-table.md).</span></span> <span data-ttu-id="8adb3-106">Une valeur. ini est écrite si le composant correspondant a été configuré pour être installé localement ou exécuté à partir de la source.</span><span class="sxs-lookup"><span data-stu-id="8adb3-106">An .ini value is written if the corresponding component has been set to be installed either locally or run from source.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="8adb3-107">Restrictions de séquence</span><span class="sxs-lookup"><span data-stu-id="8adb3-107">Sequence Restrictions</span></span>

<span data-ttu-id="8adb3-108">L’action InstallValidate doit précéder l’action WriteIniValues.</span><span class="sxs-lookup"><span data-stu-id="8adb3-108">The InstallValidate action must come before the WriteIniValues action.</span></span> <span data-ttu-id="8adb3-109">S’il existe une [action RemoveIniValues](removeinivalues-action.md) dans la séquence, elle doit être antérieure à l’action WriteIniValues.</span><span class="sxs-lookup"><span data-stu-id="8adb3-109">If there is a [RemoveIniValues action](removeinivalues-action.md) in the sequence, then it must come before the WriteIniValues action.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="8adb3-110">Messages ActionData</span><span class="sxs-lookup"><span data-stu-id="8adb3-110">ActionData Messages</span></span>



| <span data-ttu-id="8adb3-111">Champ</span><span class="sxs-lookup"><span data-stu-id="8adb3-111">Field</span></span> | <span data-ttu-id="8adb3-112">Description des données d’action</span><span class="sxs-lookup"><span data-stu-id="8adb3-112">Description of action data</span></span>              |
|-------|-----------------------------------------|
| <span data-ttu-id="8adb3-113">\[1\]</span><span class="sxs-lookup"><span data-stu-id="8adb3-113">\[1\]</span></span> | <span data-ttu-id="8adb3-114">Identificateur du fichier. ini.</span><span class="sxs-lookup"><span data-stu-id="8adb3-114">Identifier of .ini file.</span></span>                |
| <span data-ttu-id="8adb3-115">\[2\]</span><span class="sxs-lookup"><span data-stu-id="8adb3-115">\[2\]</span></span> | <span data-ttu-id="8adb3-116">clé du fichier. ini dans la section suivante.</span><span class="sxs-lookup"><span data-stu-id="8adb3-116">.ini file key in the following section.</span></span> |
| <span data-ttu-id="8adb3-117">\[3\]</span><span class="sxs-lookup"><span data-stu-id="8adb3-117">\[3\]</span></span> | <span data-ttu-id="8adb3-118">Élément supprimé du fichier. ini.</span><span class="sxs-lookup"><span data-stu-id="8adb3-118">Item removed from .ini file.</span></span>            |
| <span data-ttu-id="8adb3-119">\[4\]</span><span class="sxs-lookup"><span data-stu-id="8adb3-119">\[4\]</span></span> | <span data-ttu-id="8adb3-120">Valeur supprimée du fichier. ini.</span><span class="sxs-lookup"><span data-stu-id="8adb3-120">Value removed from .ini file.</span></span>           |



 

## <a name="related-topics"></a><span data-ttu-id="8adb3-121">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="8adb3-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8adb3-122">Table IniFile</span><span class="sxs-lookup"><span data-stu-id="8adb3-122">IniFile table</span></span>](inifile-table.md)
</dt> </dl>

 

 



