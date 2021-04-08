---
description: L’action RegisterMIMEInfo enregistre les informations de Registre liées à MIME auprès du système.
ms.assetid: 2ba88b5f-bd8a-4572-af82-9c0b91b9b6d9
title: Action RegisterMIMEInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41130d9e595cc2d95557470f79c217f3c3235d75
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103756466"
---
# <a name="registermimeinfo-action"></a>Action RegisterMIMEInfo

L’action RegisterMIMEInfo enregistre les informations de Registre liées à MIME auprès du système.

## <a name="sequence-restrictions"></a>Restrictions de séquence

L’action RegisterMIMEInfo doit être postérieure à l’action [InstallFiles](installfiles-action.md) , à l’action [UnregisterMIMEInfo](unregistermimeinfo-action.md) , à l’action [RegisterClassInfo](registerclassinfo-action.md) et à l’action [RegisterExtensionInfo](registerextensioninfo-action.md) .

Le séquencement des actions dans le groupe suivant est limité. Si un sous-ensemble de ces actions se produit ensemble dans une table de séquences, elles doivent avoir le même ordre de séquence relatif comme indiqué :

-   [UnregisterClassInfo](unregisterclassinfo-action.md)
-   [UnregisterExtensionInfo](unregisterextensioninfo-action.md)
-   [UnregisterProgIdInfo](unregisterprogidinfo-action.md)
-   [UnregisterMIMEInfo](unregistermimeinfo-action.md)
-   [RegisterClassInfo](registerclassinfo-action.md)
-   [RegisterExtensionInfo](registerextensioninfo-action.md)
-   [RegisterProgIdInfo](registerprogidinfo-action.md)
-   RegisterMIMEInfo

Par exemple, RegisterMIMEInfo doit venir après [UnregisterMIMEInfo](unregistermimeinfo-action.md) dans la table Sequence.

## <a name="actiondata-messages"></a>Messages ActionData



| Champ | Description des données d’action                   |
|-------|----------------------------------------------|
| \[1\] | Identificateur du type de contenu MIME inscrit.  |
| \[2\] | Extension associée au type de contenu MIME. |



 

## <a name="remarks"></a>Notes

L’action RegisterMIMEInfo enregistre toutes les informations MIME pour les serveurs à partir de la [table MIME](mime-table.md) pour laquelle le serveur de classe ou d’extension correspondant a été sélectionné pour être installé.

 

 



