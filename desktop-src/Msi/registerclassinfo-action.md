---
description: L’action RegisterClassInfo gère l’inscription des informations de classe COM auprès du système. Elle utilise la table AppId.
ms.assetid: f8b60a75-9c0e-41c5-b6af-6a05a26b2d71
title: Action RegisterClassInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd916772bc236dfc86df336347514c10d5dfbce7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106527458"
---
# <a name="registerclassinfo-action"></a>Action RegisterClassInfo

L’action RegisterClassInfo gère l’inscription des informations de classe COM auprès du système. Elle utilise la [table AppID](appid-table.md).

## <a name="sequence-restrictions"></a>Restrictions de séquence

L’action RegisterClassInfo doit être postérieure à l’action [InstallFiles](installfiles-action.md) et à l’action [UnregisterClassInfo](unregisterclassinfo-action.md) .

Le séquencement des actions dans le groupe suivant est limité. Si un sous-ensemble de ces actions se produit ensemble dans une table de séquences, elles doivent avoir le même ordre de séquence relatif comme indiqué :

-   [UnregisterClassInfo](unregisterclassinfo-action.md)
-   [UnregisterExtensionInfo](unregisterextensioninfo-action.md)
-   [UnregisterProgIdInfo](unregisterprogidinfo-action.md)
-   [UnregisterMIMEInfo](unregistermimeinfo-action.md)
-   RegisterClassInfo
-   [RegisterExtensionInfo](registerextensioninfo-action.md)
-   [RegisterProgIdInfo](registerprogidinfo-action.md)
-   [RegisterMIMEInfo](registermimeinfo-action.md)

Par exemple, RegisterClassInfo doit venir après [UnregisterMIMEInfo](unregistermimeinfo-action.md) dans la table Sequence.

## <a name="actiondata-messages"></a>Messages ActionData



| Champ | Description des données d’action                          |
|-------|-----------------------------------------------------|
| \[1\] | Identificateur de classe GUID du serveur COM inscrit. |



 

## <a name="remarks"></a>Notes

Si le système prend en charge l’installation à la demande pour les serveurs OLE, RegisterClassInfo inscrit toutes les classes COM dans la [table de classes](class-table.md) associée à une fonctionnalité sélectionnée pour être installée ou publiée. Dans le cas contraire, cette action inscrit uniquement les classes COM associées à une fonctionnalité sélectionnée pour l’installation.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Propriété OLEAdvtSupport**](oleadvtsupport.md)
</dt> </dl>

 

 



