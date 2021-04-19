---
description: La table LaunchCondition est utilisée par l’action LaunchConditions. Elle contient une liste de conditions qui doivent toutes être satisfaites pour que l’installation commence.
ms.assetid: 6e550cc7-c479-417e-ab89-882d8fece4e1
title: Table LaunchCondition
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d67834f058575dde297454480040028ef9c5732
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106514188"
---
# <a name="launchcondition-table"></a>Table LaunchCondition

La table LaunchCondition est utilisée par l' [action LaunchConditions](launchconditions-action.md). Elle contient une liste de conditions qui doivent toutes être satisfaites pour que l’installation commence.

La table LaunchCondition contient les colonnes suivantes.



| Colonne      | Type                       | Clé | Nullable |
|-------------|----------------------------|-----|----------|
| Condition   | [Condition](condition.md) | O   | N        |
| Description | [Correct](formatted.md) | N   | N        |



 

## <a name="columns"></a>Colonnes

<dl> <dt>

<span id="Condition"></span><span id="condition"></span><span id="CONDITION"></span>Etat
</dt> <dd>

Expression qui doit avoir la valeur true pour que l’installation commence.

</dd> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Descriptive
</dt> <dd>

Texte localisable à afficher lorsque la condition échoue et que l’installation doit être terminée.

</dd> </dl>

## <a name="remarks"></a>Notes

Vous ne pouvez pas garantir l’ordre dans lequel les conditions de lancement sont évaluées en créant cette table. S’il est nécessaire de contrôler l’ordre dans lequel les conditions sont évaluées, vous devez le faire à l’aide de l’action personnalisée type 19 actions personnalisées dans votre installation.

## <a name="validation"></a>Validation

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE46](ice46.md)  
[ICE79](ice79.md)  
[ICE86](ice86.md)  
</dl>

 

 



