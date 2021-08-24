---
description: L’action UnregisterMIMEInfo annule l’enregistrement des informations de Registre liées à MIME à partir du système. L’action annule l’enregistrement des informations MIME pour les serveurs de la table MIME pour lesquels la fonctionnalité correspondante est actuellement sélectionnée pour être désinstallée.
ms.assetid: 9a5c12da-e78f-4c99-9b82-d41624593c61
title: Action UnregisterMIMEInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e03ea1c50aa543615edc0ed875bd83b3338cdb261d09e01232e0fe76f7aa51ee
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119810139"
---
# <a name="unregistermimeinfo-action"></a>Action UnregisterMIMEInfo

L’action UnregisterMIMEInfo annule l’enregistrement des informations de Registre liées à MIME à partir du système. L’action annule l’enregistrement des informations MIME pour les serveurs de la [table MIME](mime-table.md) pour lesquels la fonctionnalité correspondante est actuellement sélectionnée pour être désinstallée.

## <a name="sequence-restrictions"></a>Restrictions de séquence

L’action UnregisterMIMEInfo doit venir après l’action [InstallInitialize](installinitialize-action.md) , [UnregisterClassInfo](unregisterclassinfo-action.md) action, [UnregisterExtensionInfo](unregisterextensioninfo-action.md) action et avant l’action [RegisterMIMEInfo](registermimeinfo-action.md) .

[RemoveRegistryValues](removeregistryvalues-action.md) doit précéder UnregisterMIMEInfo dans la séquence.

Le séquencement des actions dans le groupe suivant est limité. Si un sous-ensemble de ces actions se produit ensemble dans une table de séquences, elles doivent avoir le même ordre de séquence relatif comme indiqué :

-   [UnregisterClassInfo](unregisterclassinfo-action.md)
-   [UnregisterExtensionInfo](unregisterextensioninfo-action.md)
-   [UnregisterProgIdInfo](unregisterprogidinfo-action.md)
-   UnregisterMIMEInfo
-   [RegisterClassInfo](registerclassinfo-action.md)
-   [RegisterExtensionInfo](registerextensioninfo-action.md)
-   [RegisterProgIdInfo](registerprogidinfo-action.md)
-   [RegisterMIMEInfo](registermimeinfo-action.md)

Par exemple, UnregisterMIMEInfo doit précéder [RegisterExtensionInfo](registerextensioninfo-action.md) dans la table Sequence.

## <a name="actiondata-messages"></a>Messages ActionData



| Champ | Description des données d’action                    |
|-------|-----------------------------------------------|
| \[1\] | Identificateur du type de contenu MIME non inscrit. |
| \[2\] | Extension associée au type de contenu MIME.  |



 

 

 



