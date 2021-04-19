---
description: L’action RemoveRegistryValues peut uniquement supprimer des valeurs du Registre système qui ont été créées dans la table du registre ou la table RemoveRegistry.
ms.assetid: aa05eb75-15f2-4e2a-a8e2-a770ad078b41
title: Action RemoveRegistryValues
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0e6e7473be344faa08ed456e72e3b9c80c4aa8f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106519952"
---
# <a name="removeregistryvalues-action"></a><span data-ttu-id="6ed9f-103">Action RemoveRegistryValues</span><span class="sxs-lookup"><span data-stu-id="6ed9f-103">RemoveRegistryValues Action</span></span>

<span data-ttu-id="6ed9f-104">L’action RemoveRegistryValues peut uniquement supprimer des valeurs du Registre système qui ont été créées dans la [table du Registre](registry-table.md) ou la [table RemoveRegistry](removeregistry-table.md).</span><span class="sxs-lookup"><span data-stu-id="6ed9f-104">The RemoveRegistryValues action can only remove values from the system registry that have been authored into the [Registry table](registry-table.md) or the [RemoveRegistry table](removeregistry-table.md).</span></span> <span data-ttu-id="6ed9f-105">Cette action supprime une valeur de Registre qui a été créée dans la table du Registre si le composant associé a été installé localement ou comme étant exécuté à partir de la source et est maintenant configuré pour être désinstallé.</span><span class="sxs-lookup"><span data-stu-id="6ed9f-105">This action removes a registry value that has been authored into the Registry table if the associated component was installed locally or as run from source and is now set to be uninstalled.</span></span> <span data-ttu-id="6ed9f-106">Cette action supprime une valeur de Registre qui a été créée dans la table RemoveRegistry si le composant associé est configuré pour être installé localement ou comme étant exécuté à partir de la source.</span><span class="sxs-lookup"><span data-stu-id="6ed9f-106">This action removes a registry value that has been authored into the RemoveRegistry table if the associated component is set to be installed locally or as run from source.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="6ed9f-107">Restrictions de séquence</span><span class="sxs-lookup"><span data-stu-id="6ed9f-107">Sequence Restrictions</span></span>

<span data-ttu-id="6ed9f-108">L’action [InstallValidate](installvalidate-action.md) doit être appelée avant d’appeler RemoveRegistryValues.</span><span class="sxs-lookup"><span data-stu-id="6ed9f-108">The [InstallValidate](installvalidate-action.md) action must be called before calling RemoveRegistryValues.</span></span> <span data-ttu-id="6ed9f-109">Si une action [WriteRegistryValues](writeregistryvalues-action.md) est utilisée, elle doit être postérieure à RemoveRegistryValues.</span><span class="sxs-lookup"><span data-stu-id="6ed9f-109">If a [WriteRegistryValues](writeregistryvalues-action.md) action is used, it must come after RemoveRegistryValues.</span></span> <span data-ttu-id="6ed9f-110">RemoveRegistryValues doit précéder [UnregisterMIMEInfo](unregistermimeinfo-action.md) ou [UnregisterProgIDInfo](unregisterprogidinfo-action.md).</span><span class="sxs-lookup"><span data-stu-id="6ed9f-110">RemoveRegistryValues must come before [UnregisterMIMEInfo](unregistermimeinfo-action.md) or [UnregisterProgIDInfo](unregisterprogidinfo-action.md).</span></span>

<span data-ttu-id="6ed9f-111">Une action personnalisée peut être utilisée pour ajouter des lignes à la [table du Registre](registry-table.md) pendant une transaction d’installation, de désinstallation ou de réparation.</span><span class="sxs-lookup"><span data-stu-id="6ed9f-111">A custom action can be used to add rows to the [Registry table](registry-table.md) during an installation, uninstallation, or repair transaction.</span></span> <span data-ttu-id="6ed9f-112">Ces lignes ne sont pas conservées dans la table de Registre et les informations ne sont disponibles que pendant la transaction en cours.</span><span class="sxs-lookup"><span data-stu-id="6ed9f-112">These rows do not persist in the Registry table and the information is only available during the current transaction.</span></span> <span data-ttu-id="6ed9f-113">L’action personnalisée doit donc être exécutée à chaque installation, désinstallation ou transaction de réparation qui requiert les informations contenues dans ces lignes supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="6ed9f-113">The custom action must therefore be run in every installation, uninstallation, or repair transaction that requires the information in these additional rows.</span></span> <span data-ttu-id="6ed9f-114">L’action personnalisée doit précéder les actions RemoveRegistryValues et [WriteRegistryValues](writeregistryvalues-action.md) dans la séquence d’action.</span><span class="sxs-lookup"><span data-stu-id="6ed9f-114">The custom action must come before the RemoveRegistryValues and [WriteRegistryValues](writeregistryvalues-action.md) actions in the action sequence.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="6ed9f-115">Messages ActionData</span><span class="sxs-lookup"><span data-stu-id="6ed9f-115">ActionData Messages</span></span>



| <span data-ttu-id="6ed9f-116">Champ</span><span class="sxs-lookup"><span data-stu-id="6ed9f-116">Field</span></span> | <span data-ttu-id="6ed9f-117">Description des données d’action</span><span class="sxs-lookup"><span data-stu-id="6ed9f-117">Description of action data</span></span>                          |
|-------|-----------------------------------------------------|
| <span data-ttu-id="6ed9f-118">\[1\]</span><span class="sxs-lookup"><span data-stu-id="6ed9f-118">\[1\]</span></span> | <span data-ttu-id="6ed9f-119">Chemin d’accès du Registre à la clé de la valeur de Registre supprimée.</span><span class="sxs-lookup"><span data-stu-id="6ed9f-119">Registry path to key of removed registry value.</span></span>     |
| <span data-ttu-id="6ed9f-120">\[2\]</span><span class="sxs-lookup"><span data-stu-id="6ed9f-120">\[2\]</span></span> | <span data-ttu-id="6ed9f-121">Chaîne mise en forme du nom de la valeur de Registre supprimée.</span><span class="sxs-lookup"><span data-stu-id="6ed9f-121">Formatted string of name of removed registry value.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="6ed9f-122">Notes</span><span class="sxs-lookup"><span data-stu-id="6ed9f-122">Remarks</span></span>

<span data-ttu-id="6ed9f-123">Pour supprimer une valeur de Registre, enregistrez la valeur dans la colonne valeur de la table Registre.</span><span class="sxs-lookup"><span data-stu-id="6ed9f-123">To remove a registry value, record the value in the Value column of the Registry table.</span></span> <span data-ttu-id="6ed9f-124">Si l’action WriteRegistryValues a attaché des \_ \_ chaînes reg multisz à la valeur de la [table Registry](registry-table.md), l’action RemoveRegistryValues supprime uniquement les chaînes de la valeur de registre.</span><span class="sxs-lookup"><span data-stu-id="6ed9f-124">If the WriteRegistryValues action has attached REG\_MULTI\_SZ strings to the value in the [Registry table](registry-table.md), then the RemoveRegistryValues action removes only those strings from the registry value.</span></span>

 

 



