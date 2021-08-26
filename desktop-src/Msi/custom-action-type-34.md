---
description: les développeurs de packages de Windows Installer peuvent choisir d’utiliser un type d’action personnalisé 34 quand les actions standard sont insuffisantes pour exécuter l’installation.
ms.assetid: 4d0e4f01-0530-4202-bc78-b6e52670b8e5
title: Type d’action personnalisé 34
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4173633e7912897a3327d6d4c9c556d33f38bbd7f45cca6d4a1d96ef916b08ec
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120077939"
---
# <a name="custom-action-type-34"></a>Type d’action personnalisé 34

Cette action personnalisée appelle un exécutable lancé avec une ligne de commande. Pour plus d’informations, consultez [fichiers exécutables](executable-files.md).

## <a name="source"></a>Source

L’exécutable est généré à partir d’un fichier. Le champ source de la table [CustomAction](customaction-table.md) contient une clé dans la table de [répertoires](directory-table.md) . L’entrée de table de répertoire référencée est utilisée pour résoudre le chemin d’accès complet à un répertoire de travail. Cela ne doit pas obligatoirement être le chemin d’accès au répertoire contenant le fichier exécutable.

## <a name="type-value"></a>Valeur de type

Incluez la valeur suivante dans la colonne type de la table [CustomAction](customaction-table.md) pour spécifier le type numérique de base.



| Constantes                                                         | Valeur hexadécimale | Decimal |
|-------------------------------------------------------------------|-------------|---------|
| **msidbCustomActionTypeExe**  +  **msidbCustomActionTypeDirectory** | 0x022       | 34      |



 

## <a name="target"></a>Cible

La colonne cible de la table [CustomAction](customaction-table.md) contient le chemin d’accès complet et le nom du fichier exécutable suivi d’arguments facultatifs pour l’exécutable. Le chemin d’accès complet et le nom du fichier exécutable sont requis. Les guillemets doivent être utilisés autour des chemins d’accès ou des noms de fichiers longs. La valeur est traitée comme du texte [mis en forme](formatted.md) et peut contenir des références à des propriétés, des fichiers, des répertoires ou d’autres attributs de texte mis en forme.

## <a name="return-processing-options"></a>Options de traitement des retours

Incluez les bits d’indicateur facultatifs dans la colonne type de la table [CustomAction](customaction-table.md) pour spécifier les options de traitement des retours. Pour obtenir une description des options et des valeurs, consultez [options de traitement des retours d’actions personnalisées](custom-action-return-processing-options.md).

## <a name="execution-scheduling-options"></a>Options de planification de l’exécution

Incluez les bits d’indicateur facultatifs dans la colonne type de la table [CustomAction](customaction-table.md) pour spécifier les options de planification de l’exécution. Ces options contrôlent l’exécution multiple des actions personnalisées. Pour obtenir une description des options, consultez [options de planification de l’exécution des actions personnalisées](custom-action-execution-scheduling-options.md).

## <a name="in-script-execution-options"></a>In-Script les options d’exécution

Incluez des bits d’indicateur facultatifs dans la colonne type de la table [CustomAction](customaction-table.md) pour spécifier une option d’exécution in-script. Ces options copient le code d’action dans le script d’exécution, de restauration ou de validation. Pour obtenir une description des options, consultez [action personnalisée In-Script options d’exécution](custom-action-in-script-execution-options.md).

## <a name="return-values"></a>Valeurs de retour

Les actions personnalisées qui sont des [fichiers exécutables](executable-files.md) doivent retourner la valeur 0 en cas de réussite. Le programme d’installation interprète toute autre valeur de retour comme un échec. Pour ignorer les valeurs de retour, définissez l’indicateur de bit **msidbCustomActionTypeContinue** dans le champ type de la table [CustomAction](customaction-table.md) .

## <a name="remarks"></a>Remarques

Une action personnalisée qui lance un exécutable prend une ligne de commande, qui contient généralement des propriétés qui sont désignées dynamiquement. S’il s’agit également d’une [action personnalisée d’exécution différée](deferred-execution-custom-actions.md), le programme d’installation utilise [**CreateProcessAsUser**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessasusera) ou [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) pour créer le processus lorsque l’action personnalisée est appelée à partir du script d’installation.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Actions personnalisées \_](custom-actions.md)
</dt> </dl>

 

 
