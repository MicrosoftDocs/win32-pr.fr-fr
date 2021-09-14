---
description: les développeurs de packages de Windows Installer peuvent choisir d’utiliser un type d’action personnalisé 51 quand les actions standard sont insuffisantes pour exécuter l’installation.
ms.assetid: cdad16ad-426c-4e04-8003-b32c67be7329
title: Type d’action personnalisé 51
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef3224add3a425131ee3308bc4f610b086cd99a2
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127091781"
---
# <a name="custom-action-type-51"></a>Type d’action personnalisé 51

Cette action personnalisée définit une propriété à partir d’une chaîne de texte mise en forme.

Pour affecter une propriété utilisée dans une condition sur un composant ou une fonctionnalité, l’action personnalisée doit précéder l' [action CostFinalize](costfinalize-action.md) dans la séquence d’action.

## <a name="source"></a>Source

Le champ source de la [table CustomAction](customaction-table.md) peut contenir soit le nom d’une propriété, soit une clé de la [table de propriétés](property-table.md). Cette propriété est définie par la chaîne mise en forme dans le champ cible à l’aide de [**MsiSetProperty**](/windows/desktop/api/Msiquery/nf-msiquery-msisetpropertya).

## <a name="type-value"></a>Valeur de type

Incluez la valeur suivante dans la colonne type de la [table CustomAction](customaction-table.md) pour spécifier le type numérique de base.



| Constantes                                                             | Valeur hexadécimale | Decimal |
|-----------------------------------------------------------------------|-------------|---------|
| **msidbCustomActionTypeTextData**  +  **msidbCustomActionTypeProperty** | 0x033       | 51      |



 

## <a name="target"></a>Cible

La colonne cible de la [table CustomAction](customaction-table.md) contient une chaîne de texte mise en forme à l’aide de la fonctionnalité spécifiée dans [**MsiFormatRecord**](/windows/desktop/api/Msiquery/nf-msiquery-msiformatrecorda) (sans les spécificateurs de champ numérique). Les paramètres à remplacer sont placés entre crochets, \[ ... \] et peuvent être des propriétés, des variables d’environnement (% prefix), des chemins d’accès de fichier (préfixe \# ) ou des chemins d’accès de répertoire de composant ($ prefix).

## <a name="return-processing-options"></a>Options de traitement des retours

L’action personnalisée n’utilise pas ces options.

## <a name="execution-scheduling-options"></a>Options de planification de l’exécution

Incluez les bits d’indicateur facultatifs dans la colonne type de la [table CustomAction](customaction-table.md) pour spécifier les options de planification de l’exécution. Ces options contrôlent l’exécution multiple des actions personnalisées. Pour obtenir une description des options, consultez [options de planification de l’exécution des actions personnalisées](custom-action-execution-scheduling-options.md).

## <a name="in-script-execution-options"></a>In-Script les options d’exécution

L’action personnalisée n’utilise pas ces options.

## <a name="return-values"></a>Valeurs de retour

Consultez [valeurs de retour de l’action personnalisée](custom-action-return-values.md).

## <a name="remarks"></a>Notes

Si vous définissez une [propriété privée](private-properties.md) dans la séquence d’interface utilisateur en créant une action personnalisée dans l’une des tables de séquence de l’interface utilisateur, cette propriété n’est pas définie dans la séquence d’exécution. Pour définir la propriété dans la séquence d’exécution, vous devez également placer une action personnalisée dans une table de séquence d’exécution. Vous pouvez également faire de la propriété une [propriété publique](public-properties.md) et l’inclure dans la [**propriété SecureCustomProperties**](securecustomproperties.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Actions personnalisées \_](custom-actions.md)
</dt> <dt>

[Actions personnalisées du texte mis en forme](formatted-text-custom-actions.md)
</dt> </dl>

 

 



