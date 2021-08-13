---
description: Le tableau suivant identifie les types de base des actions personnalisées et indique les valeurs qui figurent dans les champs type, source et cible de la table CustomAction pour chaque type.
ms.assetid: 8713451e-c0e7-4bec-bfb6-dfe4125d5a44
title: Types d’actions personnalisées
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf0be8a9465c9a3567a867bab911d7539e8700219515c86bb5a8fc2b7d5eff68
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118624304"
---
# <a name="custom-action-types"></a>Types d’actions personnalisées

Le tableau suivant identifie les types de base des actions personnalisées et indique les valeurs qui figurent dans les champs type, source et cible de la table [CustomAction](customaction-table.md) pour chaque type. Les actions personnalisées de base peuvent être modifiées en incluant des bits d’indicateur facultatifs dans la colonne Type. Pour obtenir une description des options et des valeurs, consultez les rubriques suivantes :

-   [Options de traitement des retours d’actions personnalisées](custom-action-return-processing-options.md)
-   [Options de planification de l’exécution des actions personnalisées](custom-action-execution-scheduling-options.md)
-   [Options d’exécution d’une action personnalisée In-Script](custom-action-in-script-execution-options.md)
-   [Option de désinstallation corrective de l’action personnalisée](custom-action-patch-uninstall-option.md)

Utilisez les liens vers le type d’action personnalisé de base pour une description et les options disponibles pour chaque type.



| Type d’action personnalisée de base                                                                                                                           | Type | Source                                                                                                                              | Cible                                                                                                                                     |
|----------------------------------------------------------------------------------------------------------------------------------------------------|------|-------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| [Type d’action personnalisé 1](custom-action-type-1.md) Fichier DLL stocké dans un flux de table binaire.<br/>                                               | 1    | Clé de table [binaire](binary-table.md) .                                                                                            | Point d’entrée de la DLL.                                                                                                                           |
| [Type d’action personnalisé 2](custom-action-type-2.md) Fichier EXE stocké dans un flux de table binaire.<br/>                                               | 2    | Clé de table [binaire](binary-table.md) .                                                                                            | Chaîne de ligne de commande.                                                                                                                       |
| le [Type d’Action personnalisé 5](custom-action-type-5.md)JScript fichier stocké dans un flux de table binaire.<br/>                                           | 5    | Clé de table [binaire](binary-table.md) .                                                                                            | fonction JScript facultative qui peut être appelée.                                                                                           |
| [Type d’action personnalisé 6](custom-action-type-6.md) Fichier VBScript stocké dans un flux de table binaire.<br/>                                          | 6    | Clé de table [binaire](binary-table.md) .                                                                                            | Fonction VBScript facultative qui peut être appelée.                                                                                          |
| [Type d’action personnalisée 17](custom-action-type-17.md) Fichier DLL installé avec un produit.<br/>                                            | 17   | Clé de la table de [fichiers](file-table.md) .                                                                                                | Point d’entrée de la DLL.                                                                                                                           |
| [Type d’action personnalisée 18](custom-action-type-18.md) Fichier exécutable installé avec un produit.<br/>                                            | 18   | Clé de la table de [fichiers](file-table.md) .                                                                                                | Chaîne de ligne de commande.                                                                                                                       |
| [Type d’action personnalisée 19](custom-action-type-19.md) Affiche un message d’erreur spécifié et retourne un échec, en terminant l’installation.<br/> | 19   | Vide                                                                                                                               | Chaîne de texte [mise en forme](formatted.md) . Message littéral ou index dans la table d' [Erreurs](error-table.md) .                           |
| [Type d’Action personnalisée 21](custom-action-type-21.md)JScript fichier installé avec un produit.<br/>                                        | 21   | Clé de la table de [fichiers](file-table.md) .                                                                                                | fonction JScript facultative qui peut être appelée.                                                                                           |
| [Type d’action personnalisée 22](custom-action-type-22.md) Fichier VBScript installé avec un produit.<br/>                                       | 22   | Clé de la table de [fichiers](file-table.md) .                                                                                                | Fonction VBScript facultative qui peut être appelée.                                                                                          |
| [Type d’action personnalisé 34](custom-action-type-34.md) Fichier EXE dont le chemin fait référence à un répertoire.<br/>                                       | 34   | Clé de la table de [répertoires](directory-table.md) . Il s’agit du répertoire de travail pour l’exécution.                                         | La colonne cible est [mise en forme](formatted.md) et contient le chemin d’accès complet et le nom du fichier exécutable suivi des arguments facultatifs. |
| [Type d’action personnalisé 35](custom-action-type-35.md) Jeu de répertoires avec texte mis en forme.<br/>                                                    | 35   | Clé de la table de [répertoires](directory-table.md) . Le répertoire désigné est défini par la chaîne mise en forme dans le champ cible.   | Chaîne de texte mise en forme.                                                                                                                   |
| le [Type d’Action personnalisé 37](custom-action-type-37.md)JScript texte stocké dans cette table de séquences.<br/>                                           | 37   | Null                                                                                                                                | chaîne de JScript code.                                                                                                                  |
| [Type d’action personnalisé 38](custom-action-type-38.md) Texte VBScript stocké dans cette table de séquences.<br/>                                          | 38   | Null                                                                                                                                | Chaîne de code VBScript.                                                                                                                 |
| [Type d’action personnalisé 50](custom-action-type-50.md) Fichier EXE ayant un chemin d’accès spécifié par une valeur de propriété.<br/>                                 | 50   | Nom de la propriété ou clé de la table de [Propriétés](property-table.md) .                                                                       | Chaîne de ligne de commande.                                                                                                                       |
| [Type d’action personnalisé 51](custom-action-type-51.md) Propriété définie avec le texte mis en forme.<br/>                                                     | 51   | Nom de propriété ou clé de la table de [Propriétés](property-table.md) . Cette propriété est définie par la chaîne mise en forme dans le champ cible. | Chaîne de texte mise en forme.                                                                                                                   |
| le [Type d’Action personnalisé 53](custom-action-type-53.md)JScript texte spécifié par une valeur de propriété.<br/>                                           | 53   | Nom de la propriété ou clé de la table de [Propriétés](property-table.md) .                                                                       | fonction JScript facultative qui peut être appelée.                                                                                           |
| [Type d’action personnalisé 54](custom-action-type-54.md) Texte VBScript spécifié par une valeur de propriété.<br/>                                          | 54   | Nom de la propriété ou clé de la table de [Propriétés](property-table.md) .                                                                       | Fonction VBScript facultative qui peut être appelée.                                                                                          |



 

En outre, les types d’actions personnalisés suivants sont utilisés avec les installations simultanées :

-   [Type d’action personnalisé 7](custom-action-type-7.md)
-   [Type d’action personnalisé 23](custom-action-type-23.md)
-   [Type d’action personnalisé 39](custom-action-type-39.md)

 

 




