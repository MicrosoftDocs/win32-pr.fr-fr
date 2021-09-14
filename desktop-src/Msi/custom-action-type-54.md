---
description: les développeurs de packages de Windows Installer peuvent choisir d’utiliser un type d’action personnalisé 54 quand les actions standard sont insuffisantes pour exécuter l’installation.
ms.assetid: ab348a8e-f5df-4e03-a1b7-1ab1a7fbcb3b
title: Type d’action personnalisé 54
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 623e8d4ffe955c73ef95a5948aa6e043702a35f0
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127091773"
---
# <a name="custom-action-type-54"></a>Type d’action personnalisé 54

Cette action personnalisée est écrite en VBScript. Voir aussi [scripts](scripts.md).

## <a name="source"></a>Source

Le champ source de la [table CustomAction](customaction-table.md) contient un nom de propriété ou une clé de la [table de propriétés](property-table.md) pour une propriété contenant le texte du script.

## <a name="type-value"></a>Valeur de type

Incluez la valeur suivante dans la colonne type de la [table CustomAction](customaction-table.md) pour spécifier le type numérique de base d’une action personnalisée 32 bits.



| Constantes                                                             | Valeur hexadécimale | Decimal |
|-----------------------------------------------------------------------|-------------|---------|
| **msidbCustomActionTypeVBScript**  +  **msidbCustomActionTypeProperty** | 0x036       | 54      |



 

Windows Le programme d’installation peut utiliser des actions personnalisées 64 bits sur les systèmes d’exploitation 64 bits. Une action personnalisée 64 bits basée sur des scripts doit inclure le bit **msidbCustomActionType64BitScript** dans son type numérique. Pour plus d’informations [, consultez actions personnalisées 64 bits](64-bit-custom-actions.md). Incluez la valeur suivante dans la colonne type de la [table CustomAction](customaction-table.md) pour spécifier le type numérique de base d’une action personnalisée 64 bits.



| Constantes                                                                                                    | Valeur hexadécimale | Decimal |
|--------------------------------------------------------------------------------------------------------------|-------------|---------|
| **msidbCustomActionTypeVBScript**  +  **msidbCustomActionTypeProperty**  +  **msidbCustomActionType64BitScript** | 0x0001036   | 4150    |



 

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

une action personnalisée écrite en JScript ou VBScript requiert l’objet de [**Session**](session-object.md) d’installation. Le programme d’installation joint l' **objet de session** au script avec la *session* de nom. Étant donné que l’objet **session** n’existe peut-être pas lors d’une restauration de l’installation, une action personnalisée différée écrite dans le script doit utiliser l’une des méthodes ou propriétés de l’objet **session** décrit dans la section [obtention d’informations de contexte pour les actions personnalisées d’exécution différée](obtaining-context-information-for-deferred-execution-custom-actions.md) afin d’extraire son contexte.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Actions personnalisées \_](custom-actions.md)
</dt> </dl>

 

 



