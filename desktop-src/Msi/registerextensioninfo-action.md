---
description: L’action RegisterExtensionInfo gère l’inscription des informations relatives à l’extension avec le système.
ms.assetid: 3c243ca3-9fa7-41ec-968e-7954d7d45432
title: Action RegisterExtensionInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0310344b6579ef65faac41238bb607ce98411b52
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106517065"
---
# <a name="registerextensioninfo-action"></a>Action RegisterExtensionInfo

L’action RegisterExtensionInfo gère l’inscription des informations relatives à l’extension avec le système.

## <a name="sequence-restrictions"></a>Restrictions de séquence

L’action RegisterExtensionInfo doit être postérieure à l’action [InstallFiles](installfiles-action.md) et à l’action [UnregisterExtensionInfo](unregisterextensioninfo-action.md) .

Le séquencement des actions dans le groupe suivant est limité. Si un sous-ensemble de ces actions se produit ensemble dans une table de séquences, elles doivent avoir le même ordre de séquence relatif comme indiqué :

-   [UnregisterClassInfo](unregisterclassinfo-action.md)
-   [UnregisterExtensionInfo](unregisterextensioninfo-action.md)
-   [UnregisterProgIdInfo](unregisterprogidinfo-action.md)
-   [UnregisterMIMEInfo](unregistermimeinfo-action.md)
-   [RegisterClassInfo](registerclassinfo-action.md)
-   RegisterExtensionInfo
-   [RegisterProgIdInfo](registerprogidinfo-action.md)
-   [RegisterMIMEInfo](registermimeinfo-action.md)

Par exemple, RegisterExtensionInfo doit venir après [UnregisterMIMEInfo](unregistermimeinfo-action.md) dans la table Sequence.

## <a name="actiondata-messages"></a>Messages ActionData



| Champ | Description des données d’action |
|-------|----------------------------|
| \[1\] | Extension inscrite.      |



 

## <a name="remarks"></a>Notes

Si le système prend en charge l’installation à la demande pour les serveurs d’extension, RegisterExtensionInfo inscrit tous les serveurs d’extension dans la [table d’extension](extension-table.md) associée aux fonctionnalités définies pour l’installation ou la publication. Dans le cas contraire, cette action inscrit uniquement les serveurs d’extension associés aux fonctionnalités définies sur installation.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Propriété ShellAdvtSupport**](shelladvtsupport.md)
</dt> </dl>

 

 



