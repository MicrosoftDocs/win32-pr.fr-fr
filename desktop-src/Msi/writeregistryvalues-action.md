---
description: L’action WriteRegistryValues définit les informations de registre d’une application.
ms.assetid: ab121de3-f07d-401a-b52a-246a555c142c
title: Action WriteRegistryValues
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be13cc5cf5a817e44caa34b9084115b7dda8cee3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106530585"
---
# <a name="writeregistryvalues-action"></a>Action WriteRegistryValues

L’action WriteRegistryValues définit les informations de registre d’une application. Les informations du Registre sont contrôlées par la [table des composants](component-table.md). Une valeur de Registre est écrite dans le Registre si le composant correspondant a été configuré pour être installé localement ou en tant qu’exécution à partir de la source. Pour plus d’informations, consultez la [table Registry](registry-table.md).

## <a name="sequence-restrictions"></a>Restrictions de séquence

L' [action InstallValidate](installvalidate-action.md) doit précéder l’action WriteRegistryValues. S’il existe une [action RemoveRegistryValues](removeregistryvalues-action.md), elle doit être antérieure à l’action WriteRegistryValues.

Une action personnalisée peut être utilisée pour ajouter des lignes à la [table du Registre](registry-table.md) pendant une transaction d’installation, de désinstallation ou de réparation. Ces lignes ne sont pas conservées dans la table de Registre et les informations ne sont disponibles que pendant la transaction en cours. L’action personnalisée doit donc être exécutée à chaque installation, désinstallation ou transaction de réparation qui requiert les informations contenues dans ces lignes supplémentaires. L’action personnalisée doit précéder les actions [RemoveRegistryValues](removeregistryvalues-action.md) et WriteRegistryValues dans la séquence d’action.

## <a name="actiondata-messages"></a>Messages ActionData



| Champ | Description des données d’action                               |
|-------|----------------------------------------------------------|
| \[1\] | Chemin d’accès à la clé de registre de la valeur écrite dans le registre.       |
| \[2\] | Chaîne de texte mise en forme nom de la valeur écrite dans le registre. |
| \[3\] | Chaîne de texte mise en forme de la valeur écrite dans le registre.      |



 

 

 



