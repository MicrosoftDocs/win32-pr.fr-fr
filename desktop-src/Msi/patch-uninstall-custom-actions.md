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
# <a name="patch-uninstall-custom-actions"></a>Actions personnalisées de désinstallation des correctifs

Vous pouvez utiliser l' [option de désinstallation de correctif de l’action personnalisée](custom-action-patch-uninstall-option.md) pour spécifier que le programme d’installation doit exécuter l’action personnalisée uniquement lorsqu’un correctif est désinstallé.

**Windows Installer 4,5 et versions ultérieures :** Vous pouvez utiliser l' [option de désinstallation de correctif de l’action personnalisée](custom-action-patch-uninstall-option.md) pour spécifier que le programme d’installation n’exécute l’action personnalisée que lorsqu’un correctif est désinstallé.

**[Windows Installer 4,0 et versions antérieures](not-supported-in-windows-installer-4-0.md): * *

L' [option de désinstallation corrective de l’action personnalisée](custom-action-patch-uninstall-option.md) n’est pas disponible. Il n’existe aucune méthode permettant de marquer une [action personnalisée](custom-actions.md) dans un package correctif à exécuter lorsque le correctif est désinstallé, car le programme d’installation n’applique pas les packages de correctifs en cours de désinstallation.

Pour qu’une [action personnalisée](custom-actions.md) s’exécute lors de la désinstallation d’un correctif particulier, l’action personnalisée doit être présente dans l’application d’origine ou être dans un correctif pour le produit qui est toujours appliqué.

Les développeurs peuvent utiliser la propriété [**MsiPatchRemovalList**](msipatchremovallist.md) pour créer un package Windows Installer ou un correctif qui effectue des [actions personnalisées](custom-actions.md) sur la suppression d’un correctif. L’action personnalisée peut être créée dans le package d’installation d’origine, un correctif qui a déjà été appliqué au package ou un correctif logiciel qui ne peut pas être [installé](uninstallable-patches.md). L’action personnalisée peut être conditionnée sur la propriété **MsiPatchRemovalList** dans les tables de séquence. Pour plus d’informations sur l’inconditionnel des actions, consultez [utilisation des propriétés dans les instructions conditionnelles](using-properties-in-conditional-statements.md) .

L’action personnalisée peut obtenir les GUID des correctifs qui sont supprimés de la valeur de la propriété [**MsiPatchRemovalList**](msipatchremovallist.md) . L’action personnalisée peut déterminer si l’état d’installation du correctif est appliqué, obsolète ou remplacé en appelant la propriété [**MsiGetPatchInfoEx**](/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa) ou [**PatchProperty**](patch-patchproperty.md) de l' [objet patch](patch-object.md).

Si l’action personnalisée nécessite des métadonnées spéciales du correctif, le correctif doit contenir une action personnalisée qui écrit les métadonnées dans un registre ou un emplacement de fichier lorsque le correctif est appliqué. L’action personnalisée dans l’application d’origine ou un correctif qui est toujours appliqué peut obtenir les informations nécessaires pour supprimer les modifications du correctif.

Les correctifs qui effectuent des modifications qui sont difficiles à annuler ne doivent pas être marqués comme des [correctifs non installables](uninstallable-patches.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Séquencement des correctifs](sequencing-patches.md)
</dt> <dt>

[Suppression des correctifs](removing-patches.md)
</dt> <dt>

[Correctifs désinstallés](uninstallable-patches.md)
</dt> <dt>

[Désinstallation des correctifs](uninstalling-patches.md)
</dt> <dt>

[**MSIPATCHREMOVE**](msipatchremove.md)
</dt> <dt>

[**MsiEnumapplicationsEx**](/windows/desktop/api/Msi/nf-msi-msienumproductsexa)
</dt> <dt>

[**MsiGetPatchInfoEx**](/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa)
</dt> <dt>

[**MsiRemovePatches**](/windows/desktop/api/Msi/nf-msi-msiremovepatchesa)
</dt> </dl>

 

 



