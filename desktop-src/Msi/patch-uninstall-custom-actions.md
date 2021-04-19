---
description: Vous pouvez utiliser l’option de désinstallation de correctif de l’action personnalisée pour spécifier que le programme d’installation doit exécuter l’action personnalisée uniquement lorsqu’un correctif est désinstallé.
ms.assetid: c741aa40-ba4c-459e-936a-19c002620c30
title: Actions personnalisées de désinstallation des correctifs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b90cfffbdb37f1f2fab046b794010a790e9a5212
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106515434"
---
# <a name="patch-uninstall-custom-actions"></a><span data-ttu-id="336a4-103">Actions personnalisées de désinstallation des correctifs</span><span class="sxs-lookup"><span data-stu-id="336a4-103">Patch Uninstall Custom Actions</span></span>

<span data-ttu-id="336a4-104">Vous pouvez utiliser l' [option de désinstallation de correctif de l’action personnalisée](custom-action-patch-uninstall-option.md) pour spécifier que le programme d’installation doit exécuter l’action personnalisée uniquement lorsqu’un correctif est désinstallé.</span><span class="sxs-lookup"><span data-stu-id="336a4-104">You can use the [Custom Action Patch Uninstall option](custom-action-patch-uninstall-option.md) to specify that the installer run the custom action only when a patch is uninstalled.</span></span>

<span data-ttu-id="336a4-105">**Windows Installer 4,5 et versions ultérieures :** Vous pouvez utiliser l' [option de désinstallation de correctif de l’action personnalisée](custom-action-patch-uninstall-option.md) pour spécifier que le programme d’installation n’exécute l’action personnalisée que lorsqu’un correctif est désinstallé.</span><span class="sxs-lookup"><span data-stu-id="336a4-105">**Windows Installer 4.5 and later:** You can use the [Custom Action Patch Uninstall Option](custom-action-patch-uninstall-option.md) to specify that the installer only run the custom action when a patch is uninstalled.</span></span>

<span data-ttu-id="336a4-106">\*\*[Windows Installer 4,0 et versions antérieures](not-supported-in-windows-installer-4-0.md): \* \*</span><span class="sxs-lookup"><span data-stu-id="336a4-106">\*\*[Windows Installer 4.0 and earlier](not-supported-in-windows-installer-4-0.md):  \*\*</span></span>

<span data-ttu-id="336a4-107">L' [option de désinstallation corrective de l’action personnalisée](custom-action-patch-uninstall-option.md) n’est pas disponible.</span><span class="sxs-lookup"><span data-stu-id="336a4-107">The [Custom Action Patch Uninstall option](custom-action-patch-uninstall-option.md) is not available.</span></span> <span data-ttu-id="336a4-108">Il n’existe aucune méthode permettant de marquer une [action personnalisée](custom-actions.md) dans un package correctif à exécuter lorsque le correctif est désinstallé, car le programme d’installation n’applique pas les packages de correctifs en cours de désinstallation.</span><span class="sxs-lookup"><span data-stu-id="336a4-108">There is no method for marking a [custom action](custom-actions.md) within a patch package to be run when the patch is uninstalled because the installer does not apply the patch packages being uninstalled.</span></span>

<span data-ttu-id="336a4-109">Pour qu’une [action personnalisée](custom-actions.md) s’exécute lors de la désinstallation d’un correctif particulier, l’action personnalisée doit être présente dans l’application d’origine ou être dans un correctif pour le produit qui est toujours appliqué.</span><span class="sxs-lookup"><span data-stu-id="336a4-109">To have a [custom action](custom-actions.md) run when a particular patch is uninstalled, the custom action must either be present in the original application or be in a patch for the product that is always applied.</span></span>

<span data-ttu-id="336a4-110">Les développeurs peuvent utiliser la propriété [**MsiPatchRemovalList**](msipatchremovallist.md) pour créer un package Windows Installer ou un correctif qui effectue des [actions personnalisées](custom-actions.md) sur la suppression d’un correctif.</span><span class="sxs-lookup"><span data-stu-id="336a4-110">Developers can use the [**MsiPatchRemovalList**](msipatchremovallist.md) property to author a Windows Installer package or patch that performs [custom actions](custom-actions.md) on the removal of a patch.</span></span> <span data-ttu-id="336a4-111">L’action personnalisée peut être créée dans le package d’installation d’origine, un correctif qui a déjà été appliqué au package ou un correctif logiciel qui ne peut pas être [installé](uninstallable-patches.md).</span><span class="sxs-lookup"><span data-stu-id="336a4-111">The custom action can be authored into the original installation package, a patch that has already been applied to the package, or a patch that is not an [uninstallable patch](uninstallable-patches.md).</span></span> <span data-ttu-id="336a4-112">L’action personnalisée peut être conditionnée sur la propriété **MsiPatchRemovalList** dans les tables de séquence.</span><span class="sxs-lookup"><span data-stu-id="336a4-112">The custom action can be conditionalized on the **MsiPatchRemovalList** property in the sequence tables.</span></span> <span data-ttu-id="336a4-113">Pour plus d’informations sur l’inconditionnel des actions, consultez [utilisation des propriétés dans les instructions conditionnelles](using-properties-in-conditional-statements.md) .</span><span class="sxs-lookup"><span data-stu-id="336a4-113">See [Using Properties in Conditional Statements](using-properties-in-conditional-statements.md) for more information about conditionalizing actions.</span></span>

<span data-ttu-id="336a4-114">L’action personnalisée peut obtenir les GUID des correctifs qui sont supprimés de la valeur de la propriété [**MsiPatchRemovalList**](msipatchremovallist.md) .</span><span class="sxs-lookup"><span data-stu-id="336a4-114">The custom action can obtain the GUIDs of patches being removed from the value of the [**MsiPatchRemovalList**](msipatchremovallist.md) property.</span></span> <span data-ttu-id="336a4-115">L’action personnalisée peut déterminer si l’état d’installation du correctif est appliqué, obsolète ou remplacé en appelant la propriété [**MsiGetPatchInfoEx**](/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa) ou [**PatchProperty**](patch-patchproperty.md) de l' [objet patch](patch-object.md).</span><span class="sxs-lookup"><span data-stu-id="336a4-115">The custom action can determine whether the installation state of the patch is applied, obsolete, or superseded by calling the [**MsiGetPatchInfoEx**](/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa) or the [**PatchProperty**](patch-patchproperty.md) property of the [Patch object](patch-object.md).</span></span>

<span data-ttu-id="336a4-116">Si l’action personnalisée nécessite des métadonnées spéciales du correctif, le correctif doit contenir une action personnalisée qui écrit les métadonnées dans un registre ou un emplacement de fichier lorsque le correctif est appliqué.</span><span class="sxs-lookup"><span data-stu-id="336a4-116">If the custom action requires special metadata from the patch, the patch should contain a custom action that writes the metadata to a registry or file location when the patch is applied.</span></span> <span data-ttu-id="336a4-117">L’action personnalisée dans l’application d’origine ou un correctif qui est toujours appliqué peut obtenir les informations nécessaires pour supprimer les modifications du correctif.</span><span class="sxs-lookup"><span data-stu-id="336a4-117">The custom action in the original application or a patch that is always applied can obtain the information needed to remove the patch's changes.</span></span>

<span data-ttu-id="336a4-118">Les correctifs qui effectuent des modifications qui sont difficiles à annuler ne doivent pas être marqués comme des [correctifs non installables](uninstallable-patches.md).</span><span class="sxs-lookup"><span data-stu-id="336a4-118">Patches making changes that are difficult to undo correctly should not be marked as [uninstallable patches](uninstallable-patches.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="336a4-119">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="336a4-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="336a4-120">Séquencement des correctifs</span><span class="sxs-lookup"><span data-stu-id="336a4-120">Patch Sequencing</span></span>](sequencing-patches.md)
</dt> <dt>

[<span data-ttu-id="336a4-121">Suppression des correctifs</span><span class="sxs-lookup"><span data-stu-id="336a4-121">Removing Patches</span></span>](removing-patches.md)
</dt> <dt>

[<span data-ttu-id="336a4-122">Correctifs désinstallés</span><span class="sxs-lookup"><span data-stu-id="336a4-122">Uninstallable Patches</span></span>](uninstallable-patches.md)
</dt> <dt>

[<span data-ttu-id="336a4-123">Désinstallation des correctifs</span><span class="sxs-lookup"><span data-stu-id="336a4-123">Uninstalling Patches</span></span>](uninstalling-patches.md)
</dt> <dt>

[<span data-ttu-id="336a4-124">**MSIPATCHREMOVE**</span><span class="sxs-lookup"><span data-stu-id="336a4-124">**MSIPATCHREMOVE**</span></span>](msipatchremove.md)
</dt> <dt>

[<span data-ttu-id="336a4-125">**MsiEnumapplicationsEx**</span><span class="sxs-lookup"><span data-stu-id="336a4-125">**MsiEnumapplicationsEx**</span></span>](/windows/desktop/api/Msi/nf-msi-msienumproductsexa)
</dt> <dt>

[<span data-ttu-id="336a4-126">**MsiGetPatchInfoEx**</span><span class="sxs-lookup"><span data-stu-id="336a4-126">**MsiGetPatchInfoEx**</span></span>](/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa)
</dt> <dt>

[<span data-ttu-id="336a4-127">**MsiRemovePatches**</span><span class="sxs-lookup"><span data-stu-id="336a4-127">**MsiRemovePatches**</span></span>](/windows/desktop/api/Msi/nf-msi-msiremovepatchesa)
</dt> </dl>

 

 



