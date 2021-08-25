---
description: les développeurs de packages de Windows Installer peuvent choisir d’utiliser un type d’action personnalisé 37 quand les actions standard sont insuffisantes pour exécuter l’installation.
ms.assetid: 1c1e4f4f-1ccb-444c-940a-a1963d97714d
title: Type d’action personnalisé 37
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b1595279d2c8f66e1b899ad88ad6a9d5c164c2727b5c905ce66700479ed32446
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119996818"
---
# <a name="custom-action-type-37"></a>Type d’action personnalisé 37

cette action personnalisée est écrite en JScript, par exemple ECMA 262. Windows le programme d’installation ne prend pas en charge JScript 1,0. Pour plus d’informations, consultez [scripts](scripts.md).

## <a name="source"></a>Source

Le champ source de la [table CustomAction](customaction-table.md) contient la valeur null. Le code de script de l’action personnalisée est stocké sous la forme d’une chaîne de texte de script littéral dans le champ cible.

## <a name="type-value"></a>Valeur de type

Incluez la valeur suivante dans la colonne type de la [table CustomAction](customaction-table.md) pour spécifier le type numérique de base d’une action personnalisée 32 bits.



| Constantes                                                             | Valeur hexadécimale | Decimal |
|-----------------------------------------------------------------------|-------------|---------|
| **msidbCustomActionTypeJScript**  +  **msidbCustomActionTypeDirectory** | 0x025       | 37      |



 

Windows Le programme d’installation peut utiliser des actions personnalisées 64 bits sur les systèmes d’exploitation 64 bits. Une action personnalisée 64 bits basée sur des scripts doit inclure le bit **msidbCustomActionType64BitScript** dans son type numérique. Pour plus d’informations [, consultez actions personnalisées 64 bits](64-bit-custom-actions.md). Incluez la valeur suivante dans la colonne type de la [table CustomAction](customaction-table.md) pour spécifier le type numérique de base d’une action personnalisée 64 bits.



| Constantes                                                                                                    | Valeur hexadécimale | Decimal |
|--------------------------------------------------------------------------------------------------------------|-------------|---------|
| **msidbCustomActionTypeJScript**  +  **msidbCustomActionTypeDirectory**  +  **msidbCustomActionType64BitScript** | 0x0001025   | 4133    |



 

## <a name="target"></a>Cible

Le champ cible de la [table CustomAction](customaction-table.md) contient le code de script de l’action personnalisée sous la forme d’une chaîne de texte de script littéral.

## <a name="return-processing-options"></a>Options de traitement des retours

Incluez les bits d’indicateur facultatifs dans la colonne type de la [table CustomAction](customaction-table.md) pour spécifier les options de traitement des retours. Pour obtenir une description des options et des valeurs, consultez [options de traitement des retours d’actions personnalisées](custom-action-return-processing-options.md).

## <a name="execution-scheduling-options"></a>Options de planification de l’exécution

Incluez les bits d’indicateur facultatifs dans la colonne type de la [table CustomAction](customaction-table.md) pour spécifier les options de planification de l’exécution. Ces options contrôlent l’exécution multiple des actions personnalisées. Pour obtenir une description des options, consultez [options de planification de l’exécution des actions personnalisées](custom-action-execution-scheduling-options.md).

## <a name="in-script-execution-options"></a>In-Script les options d’exécution

Incluez des bits d’indicateur facultatifs dans la colonne type de la [table CustomAction](customaction-table.md) pour spécifier une option d’exécution in-script. Ces options copient le code d’action dans le script d’exécution, de restauration ou de validation. Pour obtenir une description des options, consultez [action personnalisée In-Script options d’exécution](custom-action-in-script-execution-options.md).

## <a name="return-values"></a>Valeurs de retour

Ce type d’action personnalisé retourne toujours Success.

## <a name="remarks"></a>Remarques

une action personnalisée écrite en JScript ou VBScript requiert l’objet de [**Session**](session-object.md) d’installation. Le programme d’installation joint l' **objet de session** au script avec le nom « session ». Étant donné que l’objet **session** n’existe peut-être pas lors d’une restauration de l’installation, une action personnalisée différée écrite dans le script doit utiliser l’une des méthodes ou propriétés de l’objet **session** décrit dans la section [obtention d’informations de contexte pour les actions personnalisées d’exécution différée](obtaining-context-information-for-deferred-execution-custom-actions.md) afin d’extraire son contexte.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Actions personnalisées \_](custom-actions.md)
</dt> </dl>

 

 



