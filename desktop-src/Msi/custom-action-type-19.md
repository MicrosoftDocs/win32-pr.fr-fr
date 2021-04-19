---
description: Les développeurs de packages de Windows Installer peuvent choisir d’utiliser une action personnalisée de type 19 quand les actions standard sont insuffisantes pour exécuter l’installation.
ms.assetid: c6df5462-e20e-4486-8480-8c747193c5d9
title: Type d’action personnalisée 19
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 695f86db0848bd65884ce5e233b4d9a249275c1d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106531432"
---
# <a name="custom-action-type-19"></a>Type d’action personnalisée 19

Cette action personnalisée affiche un message d’erreur spécifié, retourne un échec, puis termine l’installation. Le message d’erreur affiché peut être fourni sous la forme d’une chaîne ou d’un index dans la [table d’erreurs](error-table.md).

## <a name="source"></a>Source

Laissez la colonne source de la [table CustomAction](customaction-table.md) vide.

## <a name="type-value"></a>Valeur de type

Incluez la valeur suivante dans la colonne type de la table CustomAction pour spécifier le type numérique de base.



| Constantes                                                               | Valeur hexadécimale | Decimal |
|-------------------------------------------------------------------------|-------------|---------|
| **msidbCustomActionTypeTextData**  +  **msidbCustomActionTypeSourceFile** | 0x013       | 19      |



 

## <a name="target"></a>Cible

La colonne cible de la [table CustomAction](customaction-table.md) contient une chaîne de texte mise en forme à l’aide de la fonctionnalité spécifiée dans [**MsiFormatRecord**](/windows/desktop/api/Msiquery/nf-msiquery-msiformatrecorda) (sans les spécificateurs de champ numérique). Les paramètres à remplacer sont placés entre crochets, \[ ... \] et peuvent être des propriétés, des variables d’environnement (% prefix), des chemins d’accès de fichier (préfixe \# ) ou des chemins d’accès de répertoire de composant ($ prefix). Si, après la mise en forme de la chaîne, la valeur est un entier, cet entier est utilisé comme index dans la [table d’erreurs](error-table.md) pour récupérer le message à afficher. Si, après la mise en forme, la chaîne contient des caractères non numériques, la chaîne est affichée en tant que message.

## <a name="return-processing-options"></a>Options de traitement des retours

L’action personnalisée n’utilise pas d’options.

## <a name="execution-scheduling-options"></a>Options de planification de l’exécution

L’action personnalisée n’utilise pas d’options.

## <a name="in-script-execution-options"></a>In-Script les options d’exécution

L’action personnalisée n’utilise pas d’options.

## <a name="return-values"></a>Valeurs de retour

Consultez [valeurs de retour de l’action personnalisée](custom-action-return-values.md).

## <a name="remarks"></a>Notes

Par exemple, les actions personnalisées CAError1, CAError2, CAError3 et CAError4 retournent ces messages.

[Table CustomAction](customaction-table.md)



| Action   | Type | Source | Cible                              |
|----------|------|--------|-------------------------------------|
| CAError1 | 19   |        | \[Prop1\]                           |
| CAError2 | 19   |        | Échec de l’installation en raison de Error2. |
| CAError3 | 19   |        | 25000                               |
| CAError4 | 19   |        | \[Prop2\]                           |



 

[Table de propriétés](property-table.md)



| Propriété | Valeur                                 |
|----------|---------------------------------------|
| Prop1    | « Échec de l’installation en raison de Error1 ». |
| Prop2    | « 25100 »                               |



 

[Table des erreurs](error-table.md)



| Code  | Message                             |
|-------|-------------------------------------|
| 25000 | Échec de l’installation en raison de Error3. |
| 25100 | Échec de l’installation en raison de Error4. |



 

Ces actions personnalisées retournent les messages d’erreur suivants :



| Action personnalisée | Chaîne de message retournée             |
|---------------|-------------------------------------|
| CAError1      | Échec de l’installation en raison de Error1. |
| CAError2      | Échec de l’installation en raison de Error2. |
| CAError3      | Échec de l’installation en raison de Error3. |
| CAError4      | Échec de l’installation en raison de Error4. |



 

Notez que, étant donné que l’ordre d’évaluation des conditions de lancement ne peut pas être garanti en créant la [table LaunchCondition](launchcondition-table.md), vous devez utiliser une action personnalisée type 19 actions personnalisées dans votre installation pour évaluer des conditions dans un ordre spécifique.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Actions personnalisées \_](custom-actions.md)
</dt> </dl>

 

 



