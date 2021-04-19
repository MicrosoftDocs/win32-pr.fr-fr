---
description: Utilisez l’indicateur d’option suivant pour spécifier que le programme d’installation doit exécuter l’action personnalisée uniquement lorsqu’un correctif est en cours de désinstallation. Pour définir l’option, ajoutez la valeur de ce tableau à la valeur du champ ExtendedType de la table CustomAction.
ms.assetid: aa4d9e21-5316-42b5-a22e-c7a5becd3cae
title: Option de désinstallation corrective de l’action personnalisée
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 108365876393733f7cc520ae565bb2c5ea7ff3df
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106545142"
---
# <a name="custom-action-patch-uninstall-option"></a><span data-ttu-id="dbbb1-104">Option de désinstallation corrective de l’action personnalisée</span><span class="sxs-lookup"><span data-stu-id="dbbb1-104">Custom Action Patch Uninstall Option</span></span>

<span data-ttu-id="dbbb1-105">Utilisez l’indicateur d’option suivant pour spécifier que le programme d’installation doit exécuter l’action personnalisée uniquement lorsqu’un correctif est en cours de désinstallation.</span><span class="sxs-lookup"><span data-stu-id="dbbb1-105">Use the following option flag to specify that the installer run the custom action only when a patch is being uninstalled.</span></span> <span data-ttu-id="dbbb1-106">Pour définir l’option, ajoutez la valeur de ce tableau à la valeur du champ ExtendedType de la [table CustomAction](customaction-table.md).</span><span class="sxs-lookup"><span data-stu-id="dbbb1-106">To set the option, add the value in this table to the value in the ExtendedType field of the [CustomAction table](customaction-table.md).</span></span>

<span data-ttu-id="dbbb1-107">**[Windows Installer 4,0 et versions antérieures](not-supported-in-windows-installer-4-0.md):** Non pris en charge.</span><span class="sxs-lookup"><span data-stu-id="dbbb1-107">**[Windows Installer 4.0 and earlier](not-supported-in-windows-installer-4-0.md):** Not supported.</span></span> <span data-ttu-id="dbbb1-108">Cette option est disponible à partir de Windows Installer 4,5.</span><span class="sxs-lookup"><span data-stu-id="dbbb1-108">This option is available beginning with Windows Installer 4.5.</span></span>



| <span data-ttu-id="dbbb1-109">Constante</span><span class="sxs-lookup"><span data-stu-id="dbbb1-109">Constant</span></span>                                | <span data-ttu-id="dbbb1-110">Valeur hexadécimale</span><span class="sxs-lookup"><span data-stu-id="dbbb1-110">Hexadecimal</span></span> | <span data-ttu-id="dbbb1-111">Decimal</span><span class="sxs-lookup"><span data-stu-id="dbbb1-111">Decimal</span></span> | <span data-ttu-id="dbbb1-112">Description</span><span class="sxs-lookup"><span data-stu-id="dbbb1-112">Description</span></span>                                                    |
|-----------------------------------------|-------------|---------|----------------------------------------------------------------|
| <span data-ttu-id="dbbb1-113">**msidbCustomActionTypePatchUninstall**</span><span class="sxs-lookup"><span data-stu-id="dbbb1-113">**msidbCustomActionTypePatchUninstall**</span></span> | <span data-ttu-id="dbbb1-114">0x8000</span><span class="sxs-lookup"><span data-stu-id="dbbb1-114">0x8000</span></span>      | <span data-ttu-id="dbbb1-115">32 768</span><span class="sxs-lookup"><span data-stu-id="dbbb1-115">32768</span></span>   | <span data-ttu-id="dbbb1-116">L’action personnalisée s’exécute uniquement lorsqu’un correctif est en cours de désinstallation.</span><span class="sxs-lookup"><span data-stu-id="dbbb1-116">The custom action runs only when a patch is being uninstalled.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="dbbb1-117">Notes</span><span class="sxs-lookup"><span data-stu-id="dbbb1-117">Remarks</span></span>

<span data-ttu-id="dbbb1-118">Cet attribut peut être ajouté à une action personnalisée en le créant dans le package Windows Installer (fichier. msi).</span><span class="sxs-lookup"><span data-stu-id="dbbb1-118">This attribute can be added to a custom action by authoring it in the Windows Installer package (.msi file).</span></span> <span data-ttu-id="dbbb1-119">Une nouvelle action personnalisée avec cet attribut peut être ajoutée par un correctif.</span><span class="sxs-lookup"><span data-stu-id="dbbb1-119">A new custom action with this attribute can be added by a patch.</span></span> <span data-ttu-id="dbbb1-120">Une action personnalisée ayant cet attribut peut être mise à jour par un correctif.</span><span class="sxs-lookup"><span data-stu-id="dbbb1-120">A custom action having this attribute can be updated by a patch.</span></span> <span data-ttu-id="dbbb1-121">Cet attribut ne peut pas être ajouté ou supprimé par un correctif à une action personnalisée existante.</span><span class="sxs-lookup"><span data-stu-id="dbbb1-121">This attribute cannot be added or removed by a patch to an existing custom action.</span></span>

<span data-ttu-id="dbbb1-122">Si un correctif ajoute ou met à jour une action personnalisée avec cet attribut, Windows Installer exécute l’action personnalisée nouvelle ou mise à jour lorsque le correctif est désinstallé.</span><span class="sxs-lookup"><span data-stu-id="dbbb1-122">If a patch adds or updates a custom action with this attribute, Windows Installer runs the new or updated custom action when the patch is uninstalled.</span></span> <span data-ttu-id="dbbb1-123">Windows Installer rend les mises à jour dans le correctif en cours de désinstallation disponibles pour l’action personnalisée de désinstallation des correctifs.</span><span class="sxs-lookup"><span data-stu-id="dbbb1-123">Windows Installer makes the updates within the patch being uninstalled available to the patch uninstall custom action.</span></span> <span data-ttu-id="dbbb1-124">Le correctif doit inclure une [table *<PatchGUID>* MsiTransformView](msitransformview.md) pour fournir ces informations à Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="dbbb1-124">The patch must include a [MsiTransformView *<PatchGUID>*](msitransformview.md) table to provide this information to Windows Installer.</span></span>

<span data-ttu-id="dbbb1-125">Lorsqu’un package qui contient une action personnalisée avec l’attribut **msidbCustomActionTypePatchUninstall** est installé à l’aide d’une version du programme d’installation antérieure à Windows Installer 4,0, le programme d’installation n’appelle pas l’action personnalisée lorsque le correctif est désinstallé.</span><span class="sxs-lookup"><span data-stu-id="dbbb1-125">When a package that contains a custom action with the **msidbCustomActionTypePatchUninstall** attribute is installed using an installer version earlier than Windows Installer 4.0, the installer does not call the custom action when the patch is uninstalled.</span></span> <span data-ttu-id="dbbb1-126">L’installation peut exécuter l’action personnalisée pendant l’installation, la réparation ou la mise à jour du package.</span><span class="sxs-lookup"><span data-stu-id="dbbb1-126">The install can run the custom action during the installation, repair, or update of the package.</span></span>

<span data-ttu-id="dbbb1-127">Les actions personnalisées avec l’attribut **msidbCustomActionTypePatchUninstall** doivent être conditionnées à l’aide de la propriété [**MSIPATCHREMOVE**](msipatchremove.md) pour empêcher l’action personnalisée de s’exécuter lors de l’installation, la réparation ou la mise à jour à l’aide d’un système avec Windows Installer 4,0 ou une version antérieure.</span><span class="sxs-lookup"><span data-stu-id="dbbb1-127">Custom actions with the **msidbCustomActionTypePatchUninstall** attribute should be conditioned using the [**MSIPATCHREMOVE**](msipatchremove.md) property to prevent the custom action from running when installing, repairing, or updating using a system with Windows Installer 4.0 or earlier.</span></span> <span data-ttu-id="dbbb1-128">Lorsque Windows Installer 4,5 et versions ultérieures est installé, tous les correctifs sur le système ayant des actions personnalisées marquées avec l’attribut **msidbCustomActionTypePatchUninstall** exécutent l’action personnalisée pendant la désinstallation des correctifs.</span><span class="sxs-lookup"><span data-stu-id="dbbb1-128">When Windows Installer 4.5 and later is installed, all the patches on the system having custom actions marked with the **msidbCustomActionTypePatchUninstall** attribute run the custom action during patch uninstallation.</span></span> <span data-ttu-id="dbbb1-129">Si Windows Installer 4,5 ou une version ultérieure est supprimé du système, les correctifs perdent la fonctionnalité de désinstallation des correctifs de l’action personnalisée.</span><span class="sxs-lookup"><span data-stu-id="dbbb1-129">If Windows Installer 4.5 or later is removed from the system, patches lose the custom action patch uninstall functionality.</span></span>

<span data-ttu-id="dbbb1-130">Pour plus d’informations sur l’exécution d’une action personnalisée pendant la désinstallation d’un correctif à l’aide d’une version antérieure à Windows Installer 4,5, consultez [patch Uninstall Custom actions](patch-uninstall-custom-actions.md).</span><span class="sxs-lookup"><span data-stu-id="dbbb1-130">For information about running a custom action during the uninstallation of a patch using a version earlier than Windows Installer 4.5, see [Patch Uninstall Custom Actions](patch-uninstall-custom-actions.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="dbbb1-131">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="dbbb1-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dbbb1-132">Options d’exécution d’une action personnalisée In-Script</span><span class="sxs-lookup"><span data-stu-id="dbbb1-132">Custom Action In-Script Execution Options</span></span>](custom-action-in-script-execution-options.md)
</dt> <dt>

[<span data-ttu-id="dbbb1-133">Référence des actions personnalisées</span><span class="sxs-lookup"><span data-stu-id="dbbb1-133">Custom Action Reference</span></span>](custom-action-reference.md)
</dt> <dt>

[<span data-ttu-id="dbbb1-134">À propos des actions personnalisées</span><span class="sxs-lookup"><span data-stu-id="dbbb1-134">About Custom Actions</span></span>](about-custom-actions.md)
</dt> <dt>

[<span data-ttu-id="dbbb1-135">Utilisation d’actions personnalisées</span><span class="sxs-lookup"><span data-stu-id="dbbb1-135">Using Custom Actions</span></span>](using-custom-actions.md)
</dt> <dt>

[<span data-ttu-id="dbbb1-136">MsiTransformView *<PatchGUID>*</span><span class="sxs-lookup"><span data-stu-id="dbbb1-136">MsiTransformView *<PatchGUID>*</span></span>](msitransformview.md)
</dt> </dl>

 

 



