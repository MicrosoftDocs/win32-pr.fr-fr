---
description: les développeurs de packages de Windows Installer peuvent choisir d’utiliser un type d’action personnalisé 53 quand les actions standard sont insuffisantes pour exécuter l’installation.
ms.assetid: d024c73e-c2dc-4187-a8ae-ed96dc7c107e
title: Type d’action personnalisé 53
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 776b78c2dbc8aa233175eeacfa8d16521968dfceeb6b97504e639946c6284b84
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118947890"
---
# <a name="custom-action-type-53"></a>Type d’action personnalisé 53

cette action personnalisée est écrite en JScript, par exemple ECMA 262. Windows le programme d’installation ne prend pas en charge JScript 1,0. Pour plus d’informations, consultez [scripts](scripts.md).

## <a name="source"></a>Source

Le champ source de la [table CustomAction](customaction-table.md) contient un nom de propriété ou une clé de la [table de propriétés](property-table.md) pour une propriété contenant le texte du script.

## <a name="type-value"></a>Valeur de type

Incluez la valeur suivante dans la colonne type de la [table CustomAction](customaction-table.md) pour spécifier le type numérique de base d’une action personnalisée 32 bits.



| Constantes                                                            | Valeur hexadécimale | Decimal |
|----------------------------------------------------------------------|-------------|---------|
| **msidbCustomActionTypeJScript**  +  **msidbCustomActionTypeProperty** | 0x035       | 53      |



 

Windows Le programme d’installation peut utiliser des actions personnalisées 64 bits sur les systèmes d’exploitation 64 bits. Une action personnalisée 64 bits basée sur des scripts doit inclure le bit **msidbCustomActionType64BitScript** dans son type numérique. Pour plus d’informations [, consultez actions personnalisées 64 bits](64-bit-custom-actions.md). Incluez la valeur suivante dans la colonne type de la [table CustomAction](customaction-table.md) pour spécifier le type numérique de base d’une action personnalisée 64 bits.



| Constantes                                                                                                   | Valeur hexadécimale | Decimal |
|-------------------------------------------------------------------------------------------------------------|-------------|---------|
| **msidbCustomActionTypeJScript**  +  **msidbCustomActionTypeProperty**  +  **msidbCustomActionType64BitScript** | 0x0001035   | 4149    |



 

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

## <a name="remarks"></a>Remarques

une action personnalisée écrite en JScript nécessite l’objet de [**Session**](session-object.md) d’installation. Étant donné que l’objet **session** n’existe peut-être pas lors d’une restauration d’installation, une action personnalisée différée écrite dans un script utilise l’une des méthodes décrites dans [obtention d’informations de contexte pour les actions personnalisées d’exécution différée](obtaining-context-information-for-deferred-execution-custom-actions.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Actions personnalisées \_](custom-actions.md)
</dt> </dl>

 

 



