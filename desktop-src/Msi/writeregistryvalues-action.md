---
description: L’action WriteRegistryValues définit les informations de registre d’une application.
ms.assetid: ab121de3-f07d-401a-b52a-246a555c142c
title: Action WriteRegistryValues
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be13cc5cf5a817e44caa34b9084115b7dda8cee3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106530585"
---
# <a name="writeregistryvalues-action"></a><span data-ttu-id="d0bdb-103">Action WriteRegistryValues</span><span class="sxs-lookup"><span data-stu-id="d0bdb-103">WriteRegistryValues Action</span></span>

<span data-ttu-id="d0bdb-104">L’action WriteRegistryValues définit les informations de registre d’une application.</span><span class="sxs-lookup"><span data-stu-id="d0bdb-104">The WriteRegistryValues action sets up an application's registry information.</span></span> <span data-ttu-id="d0bdb-105">Les informations du Registre sont contrôlées par la [table des composants](component-table.md).</span><span class="sxs-lookup"><span data-stu-id="d0bdb-105">The registry information is gated by the [Component table](component-table.md).</span></span> <span data-ttu-id="d0bdb-106">Une valeur de Registre est écrite dans le Registre si le composant correspondant a été configuré pour être installé localement ou en tant qu’exécution à partir de la source.</span><span class="sxs-lookup"><span data-stu-id="d0bdb-106">A registry value is written to the registry if the corresponding component has been set to be installed either locally or as run from source.</span></span> <span data-ttu-id="d0bdb-107">Pour plus d’informations, consultez la [table Registry](registry-table.md).</span><span class="sxs-lookup"><span data-stu-id="d0bdb-107">For more information, see [Registry table](registry-table.md).</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="d0bdb-108">Restrictions de séquence</span><span class="sxs-lookup"><span data-stu-id="d0bdb-108">Sequence Restrictions</span></span>

<span data-ttu-id="d0bdb-109">L' [action InstallValidate](installvalidate-action.md) doit précéder l’action WriteRegistryValues.</span><span class="sxs-lookup"><span data-stu-id="d0bdb-109">The [InstallValidate action](installvalidate-action.md) must come before the WriteRegistryValues action.</span></span> <span data-ttu-id="d0bdb-110">S’il existe une [action RemoveRegistryValues](removeregistryvalues-action.md), elle doit être antérieure à l’action WriteRegistryValues.</span><span class="sxs-lookup"><span data-stu-id="d0bdb-110">If there is a [RemoveRegistryValues action](removeregistryvalues-action.md), then it must come before the WriteRegistryValues action.</span></span>

<span data-ttu-id="d0bdb-111">Une action personnalisée peut être utilisée pour ajouter des lignes à la [table du Registre](registry-table.md) pendant une transaction d’installation, de désinstallation ou de réparation.</span><span class="sxs-lookup"><span data-stu-id="d0bdb-111">A custom action can be used to add rows to the [Registry table](registry-table.md) during an installation, uninstallation, or repair transaction.</span></span> <span data-ttu-id="d0bdb-112">Ces lignes ne sont pas conservées dans la table de Registre et les informations ne sont disponibles que pendant la transaction en cours.</span><span class="sxs-lookup"><span data-stu-id="d0bdb-112">These rows do not persist in the Registry table and the information is only available during the current transaction.</span></span> <span data-ttu-id="d0bdb-113">L’action personnalisée doit donc être exécutée à chaque installation, désinstallation ou transaction de réparation qui requiert les informations contenues dans ces lignes supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="d0bdb-113">The custom action must therefore be run in every installation, uninstallation, or repair transaction that requires the information in these additional rows.</span></span> <span data-ttu-id="d0bdb-114">L’action personnalisée doit précéder les actions [RemoveRegistryValues](removeregistryvalues-action.md) et WriteRegistryValues dans la séquence d’action.</span><span class="sxs-lookup"><span data-stu-id="d0bdb-114">The custom action must come before the [RemoveRegistryValues](removeregistryvalues-action.md) and WriteRegistryValues actions in the action sequence.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="d0bdb-115">Messages ActionData</span><span class="sxs-lookup"><span data-stu-id="d0bdb-115">ActionData Messages</span></span>



| <span data-ttu-id="d0bdb-116">Champ</span><span class="sxs-lookup"><span data-stu-id="d0bdb-116">Field</span></span> | <span data-ttu-id="d0bdb-117">Description des données d’action</span><span class="sxs-lookup"><span data-stu-id="d0bdb-117">Description of action data</span></span>                               |
|-------|----------------------------------------------------------|
| <span data-ttu-id="d0bdb-118">\[1\]</span><span class="sxs-lookup"><span data-stu-id="d0bdb-118">\[1\]</span></span> | <span data-ttu-id="d0bdb-119">Chemin d’accès à la clé de registre de la valeur écrite dans le registre.</span><span class="sxs-lookup"><span data-stu-id="d0bdb-119">Path to registry key of value written to registry.</span></span>       |
| <span data-ttu-id="d0bdb-120">\[2\]</span><span class="sxs-lookup"><span data-stu-id="d0bdb-120">\[2\]</span></span> | <span data-ttu-id="d0bdb-121">Chaîne de texte mise en forme nom de la valeur écrite dans le registre.</span><span class="sxs-lookup"><span data-stu-id="d0bdb-121">Formatted text string name of value written to registry.</span></span> |
| <span data-ttu-id="d0bdb-122">\[3\]</span><span class="sxs-lookup"><span data-stu-id="d0bdb-122">\[3\]</span></span> | <span data-ttu-id="d0bdb-123">Chaîne de texte mise en forme de la valeur écrite dans le registre.</span><span class="sxs-lookup"><span data-stu-id="d0bdb-123">Formatted text string of value written to registry.</span></span>      |



 

 

 



