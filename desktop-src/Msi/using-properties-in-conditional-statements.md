---
description: La valeur logique d’une propriété qui a été définie est true.
ms.assetid: aee818aa-912d-4e59-b061-61cd35993593
title: Utilisation des propriétés dans les instructions conditionnelles
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73596c465c4bcc0864caf8512e97c92d68f05fc4
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127222921"
---
# <a name="using-properties-in-conditional-statements"></a>Utilisation des propriétés dans les instructions conditionnelles

La valeur logique d’une propriété qui a été définie est true. Pour déterminer si une propriété est définie sans réellement obtenir sa valeur, testez l’expression logique « MyProperty » ou « non-MyProperty ». Lorsque la propriété MyProperty est définie, la première évaluation prend la valeur true et la dernière la valeur false.

Une ou plusieurs propriétés peuvent être combinées avec des opérateurs pour former des expressions logiques utilisées dans des instructions conditionnelles. Pour plus d’informations sur les opérateurs qui peuvent être utilisés dans les instructions conditionnelles, consultez [syntaxe d’instruction conditionnelle](conditional-statement-syntax.md).

Une instruction conditionnelle utilisant des propriétés peut être entrée dans la colonne condition de la [table condition](condition-table.md) pour modifier l’état de sélection d’une entrée dans la [table des fonctionnalités](feature-table.md).

Les instructions conditionnelles avec une ou plusieurs propriétés sont couramment utilisées dans la colonne condition des tables de base de données.

Les tables suivantes ont chacune une colonne pour les expressions conditionnelles :

-   [Table de conditions](condition-table.md)
-   [Table ControlEvent,](controlevent-table.md)
-   [Table LaunchCondition](launchcondition-table.md)
-   [Table InstallUISequence](installuisequence-table.md)
-   [Table InstallExecuteSequence](installexecutesequence-table.md)
-   [Table ControlCondition](controlcondition-table.md)
-   [Table AdminExecuteSequence](adminexecutesequence-table.md)
-   [Table AdvtExecuteSequence](advtexecutesequence-table.md)
-   [Table AdminUISequence](adminuisequence-table.md)

Notez que les six tables de séquences d’action comportent des champs pour une condition. Si l’expression conditionnelle de ce champ a la valeur false, le programme d’installation ignore cette action.

Si vous définissez une [propriété privée](private-properties.md) dans la séquence d’interface utilisateur en créant une action personnalisée dans l’une des tables de séquence de l’interface utilisateur, cette propriété n’est pas définie dans la séquence d’exécution. Pour définir la propriété dans la séquence d’exécution, vous devez également placer une action personnalisée dans une table de séquence d’exécution. Vous pouvez également faire de la propriété une [propriété publique](public-properties.md) et l’inclure dans la propriété [**SecureCustomProperties**](securecustomproperties.md) .

Pour plus d’informations, consultez [utilisation d’une table de séquences](using-a-sequence-table.md) ou [utilisation de propriétés](using-properties.md).

 

 



