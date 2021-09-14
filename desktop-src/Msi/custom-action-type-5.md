---
description: les développeurs de packages de Windows Installer peuvent choisir d’utiliser un type d’action personnalisé 5 quand les actions standard sont insuffisantes pour exécuter l’installation.
ms.assetid: 32b10271-44b1-4c5d-9c8b-eed1b4cd31e2
title: Type d’action personnalisé 5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85460c9a41dca060ca2634c013999c2c340ddfa1
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127091790"
---
# <a name="custom-action-type-5"></a>Type d’action personnalisé 5

cette action personnalisée est écrite en JScript, par exemple ECMA 262. Windows le programme d’installation ne prend pas en charge JScript 1,0. Pour plus d’informations, consultez [scripts](scripts.md).

## <a name="source"></a>Source

Le script est généré à partir d’un flux binaire temporaire. Le champ source de la [table CustomAction](customaction-table.md) contient une clé pour la [table binaire](binary-table.md). La colonne de données de la table binaire contient les données de flux. Un flux distinct est alloué pour chaque ligne.

De nouvelles données binaires peuvent être insérées à partir d’un fichier à l’aide de [**MsiRecordSetStream**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordsetstreama) , puis de [**MsiViewModify**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewmodify) pour insérer l’enregistrement dans la table. Lorsque l’action personnalisée est appelée, les données de flux sont copiées dans un fichier temporaire, qui est ensuite traité selon le type d’action personnalisée.

## <a name="type-value"></a>Valeur de type

Incluez la valeur suivante dans la colonne type de la [table CustomAction](customaction-table.md) pour spécifier le type numérique de base de l’action personnalisée 32 bits.



| Constantes                                                              | Valeur hexadécimale | Decimal |
|------------------------------------------------------------------------|-------------|---------|
| **msidbCustomActionTypeJScript**  +  **msidbCustomActionTypeBinaryData** | 0x05        | 5       |



 

Windows Le programme d’installation peut utiliser des actions personnalisées 64 bits sur les systèmes d’exploitation 64 bits. Une action personnalisée 64 bits basée sur des scripts doit inclure le bit **msidbCustomActionType64BitScript** dans son type numérique. Pour plus d’informations [, consultez actions personnalisées 64 bits](64-bit-custom-actions.md). Incluez la valeur suivante dans la colonne type de la [table CustomAction](customaction-table.md) pour spécifier le type numérique de base d’une action personnalisée 64 bits.



| Constantes                                                                                                     | Valeur hexadécimale | Decimal |
|---------------------------------------------------------------------------------------------------------------|-------------|---------|
| **msidbCustomActionTypeJScript**  +  **msidbCustomActionTypeBinaryData**  +  **msidbCustomActionType64BitScript** | 0x0001005   | 4101    |



 

## <a name="target"></a>Cible

Le champ cible de la [table CustomAction](customaction-table.md) contient une fonction de script facultative. Le traitement envoie tout d’abord le script pour l’analyse, puis appelle la fonction de script facultative.

## <a name="return-processing-options"></a>Options de traitement des retours

Incluez les bits d’indicateur facultatifs dans la colonne type de la [table CustomAction](customaction-table.md) pour spécifier les options de traitement des retours. Pour obtenir une description des options et des valeurs, consultez [options de traitement des retours d’actions personnalisées](custom-action-return-processing-options.md).

## <a name="execution-scheduling-options"></a>Options de planification de l’exécution

Incluez les bits d’indicateur facultatifs dans la colonne type de la [table CustomAction](customaction-table.md) pour spécifier les options de planification de l’exécution. Ces options contrôlent l’exécution multiple des actions personnalisées. Pour obtenir une description des options, consultez [options de planification de l’exécution des actions personnalisées](custom-action-execution-scheduling-options.md).

## <a name="in-script-execution-options"></a>In-Script les options d’exécution

Incluez des bits d’indicateur facultatifs dans la colonne type de la [table CustomAction](customaction-table.md) pour spécifier une option d’exécution in-script. Ces options copient le code d’action dans le script d’exécution, de restauration ou de validation. Pour obtenir une description des options, consultez [action personnalisée In-Script options d’exécution](custom-action-in-script-execution-options.md).

## <a name="return-values"></a>Valeurs de retour

les fonctions facultatives écrites dans le script doivent retourner l’une des valeurs décrites dans [valeurs de retour des Actions personnalisées JScript et VBScript](return-values-of-jscript-and-vbscript-custom-actions.md).

## <a name="remarks"></a>Notes

une action personnalisée écrite en JScript ou VBScript nécessite l’installation de l' [**objet Session**](session-object.md). Le programme d’installation joint l’objet de **session** au script avec la *session* de nom. Étant donné que l’objet **session** n’existe peut-être pas lors d’une restauration de l’installation, une action personnalisée différée écrite dans le script doit utiliser l’une des méthodes ou propriétés de l’objet **session** décrit dans la section [obtention d’informations de contexte pour les actions personnalisées d’exécution différée](obtaining-context-information-for-deferred-execution-custom-actions.md) afin d’extraire son contexte.

Lorsqu’une table de base de données est exportée, chaque flux est écrit sous la forme d’un fichier distinct dans le sous-dossier nommé d’après la table, à l’aide de la clé primaire en tant que nom de fichier (colonne de nom pour la table binaire), avec l’extension par défaut « . IBD ». Le nom doit utiliser le format de nom de fichier 8,3 Si le système de fichiers ou le système de gestion de version ne prend pas en charge les noms de fichiers longs. Le fichier d’archive persistant remplace les données de flux par le nom de fichier utilisé, afin que les données puissent être localisées lors de l’importation de la table.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Actions personnalisées \_](custom-actions.md)
</dt> </dl>

 

 



