---
description: L’action RemoveRegistryValues peut uniquement supprimer des valeurs du Registre système qui ont été créées dans la table du registre ou la table RemoveRegistry.
ms.assetid: aa05eb75-15f2-4e2a-a8e2-a770ad078b41
title: Action RemoveRegistryValues
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a5fe284043f76cbffe3fe6a6887f46d6ab16ba65e9103efce6e4e62baac31d31
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119339659"
---
# <a name="removeregistryvalues-action"></a>Action RemoveRegistryValues

L’action RemoveRegistryValues peut uniquement supprimer des valeurs du Registre système qui ont été créées dans la [table du Registre](registry-table.md) ou la [table RemoveRegistry](removeregistry-table.md). Cette action supprime une valeur de Registre qui a été créée dans la table du Registre si le composant associé a été installé localement ou comme étant exécuté à partir de la source et est maintenant configuré pour être désinstallé. Cette action supprime une valeur de Registre qui a été créée dans la table RemoveRegistry si le composant associé est configuré pour être installé localement ou comme étant exécuté à partir de la source.

## <a name="sequence-restrictions"></a>Restrictions de séquence

L’action [InstallValidate](installvalidate-action.md) doit être appelée avant d’appeler RemoveRegistryValues. Si une action [WriteRegistryValues](writeregistryvalues-action.md) est utilisée, elle doit être postérieure à RemoveRegistryValues. RemoveRegistryValues doit précéder [UnregisterMIMEInfo](unregistermimeinfo-action.md) ou [UnregisterProgIDInfo](unregisterprogidinfo-action.md).

Une action personnalisée peut être utilisée pour ajouter des lignes à la [table du Registre](registry-table.md) pendant une transaction d’installation, de désinstallation ou de réparation. Ces lignes ne sont pas conservées dans la table de Registre et les informations ne sont disponibles que pendant la transaction en cours. L’action personnalisée doit donc être exécutée à chaque installation, désinstallation ou transaction de réparation qui requiert les informations contenues dans ces lignes supplémentaires. L’action personnalisée doit précéder les actions RemoveRegistryValues et [WriteRegistryValues](writeregistryvalues-action.md) dans la séquence d’action.

## <a name="actiondata-messages"></a>Messages ActionData



| Champ | Description des données d’action                          |
|-------|-----------------------------------------------------|
| \[1\] | Chemin d’accès du Registre à la clé de la valeur de Registre supprimée.     |
| \[2\] | Chaîne mise en forme du nom de la valeur de Registre supprimée. |



 

## <a name="remarks"></a>Remarques

Pour supprimer une valeur de Registre, enregistrez la valeur dans la colonne valeur de la table Registre. Si l’action WriteRegistryValues a attaché des \_ \_ chaînes reg multisz à la valeur de la [table Registry](registry-table.md), l’action RemoveRegistryValues supprime uniquement les chaînes de la valeur de registre.

 

 



