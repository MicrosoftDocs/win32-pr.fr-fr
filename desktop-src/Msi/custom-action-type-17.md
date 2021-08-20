---
description: les développeurs de packages de Windows Installer peuvent choisir d’utiliser un type d’action personnalisé 17 quand les actions standard sont insuffisantes pour exécuter l’installation.
ms.assetid: 99efd6d5-e0a3-4e66-ae55-252d19090d31
title: Type d’action personnalisée 17
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6c54d19f99c552b731d88ab62926212539381f40e202a044c31a41fd906a7c1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118947987"
---
# <a name="custom-action-type-17"></a>Type d’action personnalisée 17

Cette action personnalisée appelle une bibliothèque de liens dynamiques (DLL) écrite en C ou C++.

## <a name="source"></a>Source

La DLL est installée avec l’application pendant la session active. Le champ source de la [table CustomAction](customaction-table.md) contient une clé de la [table de fichiers](file-table.md). L’emplacement du code d’action personnalisé est déterminé par la résolution du chemin d’accès cible de ce fichier ; par conséquent, cette action personnalisée doit être appelée une fois que ce fichier a été installé et avant d’être supprimé.

## <a name="type-value"></a>Valeur de type

Incluez la valeur suivante dans la colonne type de la [table CustomAction](customaction-table.md) pour spécifier le type numérique de base.



| Constantes                                                          | Valeur hexadécimale | Decimal |
|--------------------------------------------------------------------|-------------|---------|
| **msidbCustomActionTypeDll**  +  **msidbCustomActionTypeSourceFile** | 0x011       | 17      |



 

## <a name="target"></a>Cible

La DLL est appelée à l’aide du point d’entrée nommé dans le champ cible de la [table CustomAction](customaction-table.md), en passant un argument unique qui est le descripteur à la session d’installation actuelle. Le nom du point d’entrée spécifié dans la table doit correspondre à celui exporté à partir de la DLL. Notez que si la fonction d’entrée n’est pas spécifiée par un. Fichier DEF ou d’une spécification/EXPORT : linker, le nom peut avoir un trait de soulignement de début et un @4 suffixe «». La fonction appelée doit spécifier la \_ \_ Convention d’appel StdCall.

## <a name="return-processing-options"></a>Options de traitement des retours

Incluez les bits d’indicateur facultatifs dans la colonne type de la [table CustomAction](customaction-table.md) pour spécifier les options de traitement des retours. Pour obtenir une description des options et des valeurs, consultez [options de traitement des retours d’actions personnalisées](custom-action-return-processing-options.md).

## <a name="execution-scheduling-options"></a>Options de planification de l’exécution

Incluez les bits d’indicateur facultatifs dans la colonne type de la [table CustomAction](customaction-table.md) pour spécifier les options de planification de l’exécution. Ces options contrôlent l’exécution multiple des actions personnalisées. Pour obtenir une description des options, consultez [options de planification de l’exécution des actions personnalisées](custom-action-execution-scheduling-options.md).

## <a name="in-script-execution-options"></a>In-Script les options d’exécution

Incluez des bits d’indicateur facultatifs dans la colonne type de la [table CustomAction](customaction-table.md) pour spécifier une option d’exécution in-script. Ces options copient le code d’action dans le script d’exécution, de restauration ou de validation. Pour obtenir une description des options, consultez [action personnalisée In-Script options d’exécution](custom-action-in-script-execution-options.md).

## <a name="return-values"></a>Valeurs de retour

Consultez [valeurs de retour de l’action personnalisée](custom-action-return-values.md).

## <a name="remarks"></a>Remarques

Une action personnalisée qui appelle une bibliothèque de liens dynamiques (DLL) requiert un handle pour la session d’installation. S’il s’agit également d’une action personnalisée d’exécution différée, la session n’existe peut-être plus pendant l’exécution du script d’installation. Pour plus d’informations sur la façon dont une action personnalisée de ce type peut obtenir des informations de contexte, consultez [obtention d’informations de contexte pour les actions personnalisées d’exécution différée](obtaining-context-information-for-deferred-execution-custom-actions.md).

Les actions personnalisées s’exécutent dans un thread distinct et peuvent avoir un accès limité au système. Les actions personnalisées qui s’exécutent de façon asynchrone bloquent le thread principal à l’arrêt de la séquence actuelle ou de la session d’installation jusqu’à ce qu’elles retournent.

Les actions personnalisées qui font référence à un fichier installé comme source, telles que le type d’action personnalisé 17 (DLL), doivent respecter les restrictions de séquencement suivantes :

-   L’action personnalisée doit être séquencée après l' [action CostFinalize](costfinalize-action.md). Cela permet à l’action personnalisée de résoudre le chemin d’accès nécessaire pour localiser la DLL.
-   Si le fichier source n’est pas déjà installé sur l’ordinateur, les actions personnalisées différées (dans le script) de ce type doivent être séquencées après l' [action InstallFiles](installfiles-action.md).
-   Si le fichier source n’est pas déjà installé sur l’ordinateur, les actions personnalisées non différées de ce type doivent être séquencées après l' [action InstallFinalize](installfinalize-action.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Actions personnalisées \_](custom-actions.md)
</dt> <dt>

[Actions personnalisées d’exécution différée](deferred-execution-custom-actions.md)
</dt> <dt>

[Bibliothèques de liens dynamiques](dynamic-link-libraries.md)
</dt> </dl>

 

 



