---
description: L’action UnregisterProgIdInfo gère l’annulation de l’inscription des informations ProgId OLE avec le système.
ms.assetid: c9837845-4ffc-4496-8330-11b46d27ec7a
title: Action UnregisterProgIdInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6666e5648cba220dbb9bbc6e2d50c3959c1d73c98f97dcfd8c45cb3de8d94c82
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119786959"
---
# <a name="unregisterprogidinfo-action"></a>Action UnregisterProgIdInfo

L’action UnregisterProgIdInfo gère l’annulation de l’inscription des informations ProgId OLE avec le système.

## <a name="sequence-restrictions"></a>Restrictions de séquence

L’action UnregisterProgIdInfo doit venir après l’action [InstallInitialize](installinitialize-action.md) , [UnregisterClassInfo](unregisterclassinfo-action.md) action, [UnregisterExtensioninfo](unregisterextensioninfo-action.md) action et avant l’action [RegisterProgIdInfo](registerprogidinfo-action.md) .

[RemoveRegistryValues](removeregistryvalues-action.md) doit précéder UnregisterProgIdInfo dans la séquence.

Le séquencement des actions dans le groupe suivant est limité. Si un sous-ensemble de ces actions se produit ensemble dans une table de séquences, elles doivent avoir le même ordre de séquence relatif comme indiqué :

-   [UnregisterClassInfo](unregisterclassinfo-action.md)
-   [UnregisterExtensioninfo](unregisterextensioninfo-action.md)
-   UnregisterProgIdInfo
-   [UnregisterMIMEInfo](unregistermimeinfo-action.md)
-   [RegisterClassInfo](registerclassinfo-action.md)
-   [RegisterExtensionInfo](registerextensioninfo-action.md)
-   [RegisterProgIdInfo](registerprogidinfo-action.md)
-   [RegisterMIMEInfo](registermimeinfo-action.md)

Par exemple, UnregisterProgIdInfo doit précéder [UnregisterMIMEInfo](unregistermimeinfo-action.md) dans la table Sequence.

## <a name="actiondata-messages"></a>Messages ActionData



| Champ | Description des données d’action                |
|-------|-------------------------------------------|
| \[1\] | Identificateur du programme enregistré. |



 

## <a name="remarks"></a>Remarques

L’action UnregisterProgIdInfo supprime les informations ProgId du Registre ([table ProgID](progid-table.md)) pour les fonctionnalités qui sont connectées aux informations d’extension ([table d’extension](extension-table.md)) ou les informations de classe (table de[classes](class-table.md)) et qui sont actuellement sélectionnées pour être désinstallées.

 

 



