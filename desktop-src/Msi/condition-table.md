---
description: La table de conditions peut être utilisée pour modifier l’état de sélection d’une entrée dans la table de fonctionnalités en fonction d’une expression conditionnelle.
ms.assetid: 8e2d7c8d-5734-49aa-ad29-16d4d32cccb4
title: Table de conditions
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 09d9ccb265d69f99a58e155657a0e9d058ba61a920088184ec2b67c3e4506a0b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119926959"
---
# <a name="condition-table"></a>Table de conditions

La table de conditions peut être utilisée pour modifier l’état de sélection d’une entrée dans la [table de fonctionnalités](feature-table.md) en fonction d’une expression conditionnelle.

La table de condition contient les colonnes suivantes.



| Colonne    | Type                         | Clé | Nullable |
|-----------|------------------------------|-----|----------|
| Fonctionnalité\_ | [Identificateur](identifier.md) | O   | N        |
| Niveau     | [Integer](integer.md)       | O   | N        |
| Condition | [Condition](condition.md)   | N   | O        |



 

## <a name="columns"></a>Colonnes

<dl> <dt>

<span id="Feature_"></span><span id="feature_"></span><span id="FEATURE_"></span>Fonctionnalité\_
</dt> <dd>

Clé externe dans la colonne une du tableau des fonctionnalités.

</dd> <dt>

<span id="Level"></span><span id="level"></span><span id="LEVEL"></span>Niveau
</dt> <dd>

Un niveau d’installation conditionnelle pour la fonctionnalité dans la \_ colonne Feature de ce tableau. Le programme d’installation définit le niveau d’installation de cette fonctionnalité au niveau spécifié dans cette colonne si l’expression dans la colonne condition prend la valeur TRUE.

</dd> <dt>

<span id="Condition"></span><span id="condition"></span><span id="CONDITION"></span>Etat
</dt> <dd>

Si cette expression conditionnelle prend la valeur TRUE, la colonne Level de la table Feature est définie sur le niveau d’installation conditionnelle.

L’expression dans la colonne condition ne doit pas contenir de référence à l’état installé d’une fonctionnalité ou d’un composant. Cela est dû au fait que les expressions de la colonne condition sont évaluées avant que le programme d’installation n’évalue les États installés des fonctionnalités et des composants. Toute expression de la table de condition qui tente de vérifier l’état installé d’une fonctionnalité ou d’un composant prend toujours la valeur false.

Pour plus d’informations sur la syntaxe des instructions conditionnelles, consultez [syntaxe d’instruction conditionnelle](conditional-statement-syntax.md).

</dd> </dl>

## <a name="remarks"></a>Remarques

Une fonctionnalité peut être désactivée définitivement en affectant à la colonne niveau la valeur 0.

Le niveau peut être défini en fonction d’une instruction conditionnelle, telle qu’un test pour la plateforme, le système d’exploitation ou un paramètre de propriété particulier.

Les conditions doivent être choisies avec soin afin qu’une fonctionnalité ne soit pas activée lors de l’installation, puis désactivée lors de la désinstallation. Cette fonctionnalité est orpheline et le produit ne peut pas être désinstallé.

Cette table est référencée lorsque l' [action CostFinalize](costfinalize-action.md) est exécutée.

Si la propriété [**présélectionnée**](preselected.md) a la valeur 1, le programme d’installation n’évalue pas la table de conditions. La table de condition affecte uniquement l’installation des fonctionnalités lorsqu’aucune des propriétés suivantes n’a été définie :

<dl>

[**ADDLOCAL**](addlocal.md)  
[**Installez**](remove.md)  
[**ADDSOURCE**](addsource.md)  
[**ADDDEFAULT**](adddefault.md)  
[**INSTALLÉ**](reinstall.md)  
[**PUBLIÉS**](advertise.md)  
[**COMPADDLOCAL**](compaddlocal.md)  
[**COMPADDSOURCE**](compaddsource.md)  
[**COMPADDDEFAULT**](compadddefault.md)  
[**FILEADDLOCAL**](fileaddlocal.md)  
[**FILEADDSOURCE**](fileaddsource.md)  
[**FILEADDDEFAULT**](fileadddefault.md)  
</dl>

## <a name="validation"></a>Validation

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE32](ice32.md)  
[ICE46](ice46.md)  
[ICE79](ice79.md)  
[ICE86](ice86.md)  
</dl>

 

 



