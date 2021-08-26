---
description: les développeurs de packages de Windows Installer peuvent choisir d’utiliser une action personnalisée type 1 lorsque les actions standard sont insuffisantes pour exécuter l’installation.
ms.assetid: 277b875f-37f1-4f4d-98ae-7a18131de4f0
title: Type d’action personnalisé 1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3437fcd8a9a0da84ecb03f2527d30b6644210b2feb2ccc6c5f6558c3667a0d9b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120044899"
---
# <a name="custom-action-type-1"></a>Type d’action personnalisé 1

Cette action personnalisée appelle une bibliothèque de liens dynamiques (DLL) écrite en C ou C++.

## <a name="source"></a>Source

La DLL est générée à partir d’un flux binaire temporaire. Le champ source de la [table CustomAction](customaction-table.md) contient une clé pour la [table binaire](binary-table.md).

La colonne de données de la table binaire contient les données de flux. Un flux distinct est alloué pour chaque ligne. De nouvelles données binaires peuvent être insérées à partir d’un fichier à l’aide de [**MsiRecordSetStream**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordsetstreama) , puis de [**MsiViewModify**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewmodify) pour insérer l’enregistrement dans la table. Lorsque l’action personnalisée est appelée, les données de flux sont copiées dans un fichier temporaire, qui est ensuite traité en fonction du type d’action personnalisée.

## <a name="type-value"></a>Valeur de type

Incluez les bits d’indicateur suivants dans la colonne type de la [table CustomAction](customaction-table.md) pour spécifier le type numérique de base.



| Constantes                                                          | Valeur hexadécimale | Decimal |
|--------------------------------------------------------------------|-------------|---------|
| **msidbCustomActionTypeDll**  +  **msidbCustomActionTypeBinaryData** | 0x001       | 1       |



 

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

Lorsqu’une table de base de données est exportée, chaque flux est écrit sous la forme d’un fichier distinct dans le sous-dossier nommé d’après la table, à l’aide de la clé primaire en tant que nom de fichier (colonne de nom pour la table binaire), avec l’extension par défaut « . IBD ». Le nom doit utiliser le format 8,3 Si le système de fichiers ou le système de gestion de version ne prend pas en charge les noms de fichiers longs. Le fichier d’archive persistant remplace les données de flux par le nom de fichier utilisé, afin que les données puissent être localisées lors de l’importation de la table.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Actions personnalisées \_](custom-actions.md)
</dt> <dt>

[Bibliothèques de liens dynamiques](dynamic-link-libraries.md)
</dt> <dt>

[Obtention d’informations de contexte pour les actions personnalisées d’exécution différée](obtaining-context-information-for-deferred-execution-custom-actions.md)
</dt> </dl>

 

 



