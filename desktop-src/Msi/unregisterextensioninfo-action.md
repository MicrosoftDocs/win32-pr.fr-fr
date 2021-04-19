---
description: L’action UnregisterExtensionInfo gère la suppression des informations relatives à l’extension à partir du Registre système.
ms.assetid: 62bb9d17-c221-4bd2-bd7f-9930e28bb946
title: Action UnregisterExtensionInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85d069a686c5f0e517a0cc9556634895216dd8cb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106539333"
---
# <a name="unregisterextensioninfo-action"></a>Action UnregisterExtensionInfo

L’action UnregisterExtensionInfo gère la suppression des informations relatives à l’extension à partir du Registre système.

## <a name="sequence-restrictions"></a>Restrictions de séquence

L’action UnregisterExtensionInfo doit venir après l’action [InstallInitialize](installinitialize-action.md) et avant l’action [RegisterExtensionInfo](registerextensioninfo-action.md) .

[RemoveRegistryValues](removeregistryvalues-action.md) doit précéder UnregisterExtensionInfo dans la séquence.

Le séquencement des actions dans le groupe suivant est limité. Si un sous-ensemble de ces actions se produit ensemble dans une table de séquences, elles doivent avoir le même ordre de séquence relatif comme indiqué :

-   [UnregisterClassInfo](unregisterclassinfo-action.md)
-   UnregisterExtensionInfo
-   [UnregisterProgIdInfo](unregisterprogidinfo-action.md)
-   [UnregisterMIMEInfo](unregistermimeinfo-action.md)
-   [RegisterClassInfo](registerclassinfo-action.md)
-   [RegisterExtensionInfo](registerextensioninfo-action.md)
-   [RegisterProgIdInfo](registerprogidinfo-action.md)
-   [RegisterMIMEInfo](registermimeinfo-action.md)

Par exemple, UnregisterExtensionInfo doit précéder [UnregisterProgIdInfo](unregisterprogidinfo-action.md) dans la table Sequence.

## <a name="actiondata-messages"></a>Messages ActionData



| Champ | Description des données d’action |
|-------|----------------------------|
| \[1\] | Extension supprimée.         |



 

## <a name="remarks"></a>Notes

Si le système ne prend pas en charge l’installation à la demande des serveurs d’extension, UnregisterExtensionInfo supprime tous les serveurs d’extension de la [table d’extension](extension-table.md) associée à une fonctionnalité désinstallée ou à une fonctionnalité installée comme publiée à partir du Registre. Dans le cas contraire, cette action supprime les serveurs d’extension associés à une fonctionnalité qui est sélectionnée pour être supprimée du Registre.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Propriété ShellAdvtSupport**](shelladvtsupport.md)
</dt> </dl>

 

 



