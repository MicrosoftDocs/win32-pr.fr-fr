---
description: L’action RegisterProgIdInfo gère l’inscription des informations ProgId OLE avec le système.
ms.assetid: f6fd4d0d-d2dc-4953-9402-314c7932746b
title: Action RegisterProgIdInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4c7d53ca4c4125c6ebfc4d089c1c5a0934f9a58
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106534248"
---
# <a name="registerprogidinfo-action"></a>Action RegisterProgIdInfo

L’action RegisterProgIdInfo gère l’inscription des informations ProgId OLE avec le système.

## <a name="sequence-restrictions"></a>Restrictions de séquence

L’action RegisterProgIdInfo doit être postérieure à l’action [InstallFiles](installfiles-action.md) , à l’action [UnregisterProgIdInfo](unregisterprogidinfo-action.md) , à l’action [RegisterClassInfo](registerclassinfo-action.md) et à l’action [RegisterExtensionInfo](registerextensioninfo-action.md) .

Le séquencement des actions dans le groupe suivant est limité. Si un sous-ensemble de ces actions se produit ensemble dans une table de séquences, elles doivent avoir le même ordre de séquence relatif comme indiqué :

-   [UnregisterClassInfo](unregisterclassinfo-action.md)
-   [UnregisterExtensionInfo](unregisterextensioninfo-action.md)
-   [UnregisterProgIdInfo](unregisterprogidinfo-action.md)
-   [UnregisterMIMEInfo](unregistermimeinfo-action.md)
-   [RegisterClassInfo](registerclassinfo-action.md)
-   [RegisterExtensionInfo](registerextensioninfo-action.md)
-   RegisterProgIdInfo
-   [RegisterMIMEInfo](registermimeinfo-action.md)

Par exemple, RegisterProgIdInfo doit venir après [RegisterExtensionInfo](registerextensioninfo-action.md) dans la table Sequence.

## <a name="actiondata-messages"></a>Messages ActionData



| Champ | Description des données d’action                |
|-------|-------------------------------------------|
| \[1\] | Identificateur du programme enregistré. |



 

## <a name="remarks"></a>Notes

L’action RegisterProgIdInfo enregistre toutes les informations ProgId pour les serveurs qui sont spécifiés dans la [table ProgID](progid-table.md) et pour lesquels le serveur de classe ou d’extension correspondant a été sélectionné pour être installé.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Table de classe](class-table.md)
</dt> <dt>

[Table d’extension](extension-table.md)
</dt> </dl>

 

 



