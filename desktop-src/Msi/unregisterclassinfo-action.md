---
description: L’action UnregisterClassInfo gère la suppression des informations de classe COM du Registre système. Elle utilise la table AppId.
ms.assetid: 579a69ee-92cd-4d4c-a007-998ec042f9fc
title: Action UnregisterClassInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0c2116d67231e915adc1c4ad792dfd577c7fa50d4982c526f0c3f1b14b8abe9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119810249"
---
# <a name="unregisterclassinfo-action"></a>Action UnregisterClassInfo

L’action UnregisterClassInfo gère la suppression des informations de classe COM du Registre système. Elle utilise la [table AppID](appid-table.md).

## <a name="sequence-restrictions"></a>Restrictions de séquence

L’action UnregisterClassInfo doit venir après l’action [InstallInitialize](installinitialize-action.md) et avant l’action [RegisterClassInfo](registerclassinfo-action.md) .

[RemoveRegistryValues](removeregistryvalues-action.md) doit précéder UnregisterClassInfo dans la séquence.

Le séquencement des actions dans le groupe suivant est limité. Si un sous-ensemble de ces actions se produit ensemble dans une table de séquences, elles doivent se produire dans la même séquence relative, comme indiqué dans le tableau suivant :

-   UnregisterClassInfo
-   [UnregisterExtensionInfo](unregisterextensioninfo-action.md)
-   [UnregisterProgIdInfo](unregisterprogidinfo-action.md)
-   [UnregisterMIMEInfo](unregistermimeinfo-action.md)
-   [RegisterClassInfo](registerclassinfo-action.md)
-   [RegisterExtensionInfo](registerextensioninfo-action.md)
-   [RegisterProgIdInfo](registerprogidinfo-action.md)
-   [RegisterMIMEInfo](registermimeinfo-action.md)

Par exemple, [RegisterExtensionInfo](registerextensioninfo-action.md) doit précéder UnregisterClassInfo dans la table Sequence.

## <a name="actiondata-messages"></a>Messages ActionData



| Champ | Description des données d’action      |
|-------|---------------------------------|
| \[1\] | GUID de la classe COM non inscrite. |



 

## <a name="remarks"></a>Remarques

Le programme d’installation définit la propriété [**OLEAdvtSupport**](oleadvtsupport.md) sur true lorsque le système de l’utilisateur actuel a été mis à niveau pour fonctionner avec Install-on-demand via com. Si le système ne prend pas en charge l’installation à la demande via COM, UnregisterClassInfo supprime toutes les classes COM listées dans la [table de classe](class-table.md) associée aux fonctionnalités ou fonctionnalités installées comme publiées à partir du Registre système. Dans le cas contraire, cette action supprime uniquement les classes COM associées aux fonctionnalités sélectionnées pour être désinstallées dans le registre système.

 

 



