---
description: les développeurs de packages de Windows Installer peuvent choisir d’utiliser un type d’action personnalisé 18 quand les actions standard sont insuffisantes pour exécuter l’installation.
ms.assetid: 8a7311a6-41c6-431e-982d-60bacf06454e
title: Type d’action personnalisée 18
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b3befbb614e9ee78961cf5b8ef969bdb3d6e7b6c0cb713a267cab3d09b4588d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118379275"
---
# <a name="custom-action-type-18"></a>Type d’action personnalisée 18

Cette action personnalisée appelle un exécutable lancé avec une ligne de commande.

## <a name="source"></a>Source

L’exécutable est généré à partir d’un fichier installé avec l’application. Le champ source de la [table CustomAction](customaction-table.md) contient une clé de la [table de fichiers](file-table.md). L’emplacement du code d’action personnalisé est déterminé par la résolution du chemin d’accès cible de ce fichier ; par conséquent, cette action personnalisée doit être appelée une fois que le fichier a été installé et avant d’être supprimé.

## <a name="type-value"></a>Valeur de type

Incluez la valeur suivante dans la colonne type de la [table CustomAction](customaction-table.md) pour spécifier le type numérique de base.



| Constantes                                                          | Valeur hexadécimale | Decimal |
|--------------------------------------------------------------------|-------------|---------|
| **msidbCustomActionTypeExe**  +  **msidbCustomActionTypeSourceFile** | 0x012       | 18      |



 

## <a name="target"></a>Cible

La colonne cible de la [table CustomAction](customaction-table.md) contient la chaîne de ligne de commande pour l’exécutable identifié dans la colonne source.

## <a name="return-processing-options"></a>Options de traitement des retours

Incluez les bits d’indicateur facultatifs dans la colonne type de la [table CustomAction](customaction-table.md) pour spécifier les options de traitement des retours. Pour obtenir une description des options et des valeurs, consultez [options de traitement des retours d’actions personnalisées](custom-action-return-processing-options.md).

## <a name="execution-scheduling-options"></a>Options de planification de l’exécution

Incluez les bits d’indicateur facultatifs dans la colonne type de la [table CustomAction](customaction-table.md) pour spécifier les options de planification de l’exécution. Ces options contrôlent l’exécution multiple des actions personnalisées. Pour obtenir une description des options, consultez [options de planification de l’exécution des actions personnalisées](custom-action-execution-scheduling-options.md).

## <a name="in-script-execution-options"></a>In-Script les options d’exécution

Incluez des bits d’indicateur facultatifs dans la colonne type de la [table CustomAction](customaction-table.md) pour spécifier une option d’exécution in-script. Ces options copient le code d’action dans le script d’exécution, de restauration ou de validation. Pour obtenir une description des options, consultez [action personnalisée In-Script options d’exécution](custom-action-in-script-execution-options.md).

## <a name="return-values"></a>Valeurs de retour

Les actions personnalisées qui sont des [fichiers exécutables](executable-files.md) doivent retourner la valeur 0 en cas de réussite. Le programme d’installation interprète toute autre valeur de retour comme un échec. Pour ignorer les valeurs de retour, définissez l’indicateur de bit **msidbCustomActionTypeContinue** dans le champ type de la table CustomAction.

## <a name="remarks"></a>Remarques

Une action personnalisée qui lance un exécutable prend une ligne de commande, qui contient généralement des propriétés qui sont désignées dynamiquement. S’il s’agit également d’une [action personnalisée d’exécution différée](deferred-execution-custom-actions.md), le programme d’installation utilise [**CreateProcessAsUser**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessasusera) ou [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) pour créer le processus lorsque l’action personnalisée est appelée à partir du script d’installation.

Les actions personnalisées qui font référence à un fichier installé comme source, telles que le type d’action personnalisé 18 (EXE), doivent respecter les restrictions de séquencement suivantes :

-   L’action personnalisée doit être séquencée après l' [action CostFinalize](costfinalize-action.md). Cela permet à l’action personnalisée de résoudre le chemin d’accès nécessaire pour localiser le fichier exécutable.
-   Si le fichier source n’est pas déjà installé sur l’ordinateur, les actions personnalisées différées (dans le script) de ce type doivent être séquencées après l' [action InstallFiles](installfiles-action.md).
-   Si le fichier source n’est pas déjà installé sur l’ordinateur, les actions personnalisées non différées de ce type doivent être séquencées après l' [action InstallFinalize](installfinalize-action.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Actions personnalisées \_](custom-actions.md)
</dt> <dt>

[Fichiers exécutables](executable-files.md)
</dt> </dl>

 

 
