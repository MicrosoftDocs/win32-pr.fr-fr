---
description: La \_ table de validation est une table système qui contient les noms de colonne et les valeurs de colonne pour toutes les tables de la base de données.
ms.assetid: 52b1c537-efb6-4bb8-9e7f-b4848be52a71
title: Table _Validation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 666f00ccccda11706dce6a8d7e04e0efea91b7cd
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127093005"
---
# <a name="_validation-table"></a>\_Tableau de validation

La \_ table de validation est une table système qui contient les noms de colonne et les valeurs de colonne pour toutes les tables de la base de données. Il est utilisé pendant le processus de validation de la base de données pour s’assurer que toutes les colonnes sont comptabilisées et ont les valeurs correctes. Cette table n’est pas fournie avec la base de données du programme d’installation.

La \_ table de validation contient les colonnes suivantes.



| Colonne      | Type                               | Clé | Nullable |
|-------------|------------------------------------|-----|----------|
| Table de charge de travail       | [Identificateur](identifier.md)       | O   | N        |
| Colonne      | [Identificateur](identifier.md)       | O   | N        |
| Nullable    | [Text](text.md)                   | N   | N        |
| MinValue    | [DoubleInteger](doubleinteger.md) | N   | O        |
| MaxValue    | [DoubleInteger](doubleinteger.md) | N   | O        |
| Keytable    | [Identificateur](identifier.md)       | N   | O        |
| KeyColumn   | [Integer](integer.md)             | N   | O        |
| Category    | [Text](text.md)                   | N   | O        |
| Définissez         | [Text](text.md)                   | N   | O        |
| Description | [Text](text.md)                   | N   | O        |



 

## <a name="columns"></a>Colonnes

<dl> <dt>

<span id="Table"></span><span id="table"></span><span id="TABLE"></span>Tableau
</dt> <dd>

Utilisé pour identifier une table particulière. Cette clé et la clé de colonne forment la clé primaire de la \_ table de validation.

</dd> <dt>

<span id="Column"></span><span id="column"></span><span id="COLUMN"></span>Chronique
</dt> <dd>

Utilisé pour identifier une colonne particulière de la table. Cette clé et la clé de table forment la clé primaire de la \_ table de validation.

</dd> <dt>

<span id="Nullable"></span><span id="nullable"></span><span id="NULLABLE"></span>Nullable
</dt> <dd>

Indique si la colonne peut contenir une valeur null.

Cette colonne peut avoir l’une des valeurs suivantes.



| String | Signification                                   |
|--------|-------------------------------------------|
| O      | Oui, la colonne peut avoir une valeur null.    |
| N      | Non, la colonne ne peut pas avoir de valeur null. |



 

</dd> <dt>

<span id="MinValue"></span><span id="minvalue"></span><span id="MINVALUE"></span>MinValue
</dt> <dd>

Ce champ s’applique aux colonnes ayant une valeur numérique. Le champ contient la valeur minimale autorisée. Il peut s’agir de la valeur minimale pour un entier ou de la valeur minimale pour une chaîne de date ou de version.

</dd> <dt>

<span id="MaxValue"></span><span id="maxvalue"></span><span id="MAXVALUE"></span>MaxValue
</dt> <dd>

Ce champ s’applique aux colonnes ayant une valeur numérique. Le champ est la valeur maximale autorisée. Il peut s’agir de la valeur maximale d’un entier ou de la valeur maximale d’une chaîne de date ou de version.

</dd> <dt>

<span id="KeyTable"></span><span id="keytable"></span><span id="KEYTABLE"></span>Keytable
</dt> <dd>

Ce champ s’applique aux colonnes qui sont des clés externes. Le champ identifié dans la colonne doit être lié au numéro de colonne spécifié par KeyColumn dans la table nommée dans keytable. Il peut s’agir d’une liste de tables séparées par des points-virgules.

</dd> <dt>

<span id="KeyColumn"></span><span id="keycolumn"></span><span id="KEYCOLUMN"></span>KeyColumn
</dt> <dd>

Ce champ s’applique aux colonnes de table qui sont des clés externes. Le champ identifié dans la colonne doit être lié au numéro de colonne spécifié par KeyColumn dans la table nommée dans keytable. La plage autorisée du champ KeyColumn est 1-32.

</dd> <dt>

<span id="Category"></span><span id="category"></span><span id="CATEGORY"></span>Catégorie
</dt> <dd>

Il s’agit du type de données contenues dans le champ de base de données spécifié par les colonnes de table et de colonne de la \_ table de validation. S’il s’agit d’un type ayant une valeur numérique, par exemple [entier](integer.md), [DoubleInteger](doubleinteger.md) ou [heure/date](time-date.md), entrez null dans ce champ et spécifiez la plage de valeurs à l’aide des colonnes MinValue et MaxValue. Utilisez la colonne catégorie pour spécifier les types de données non numériques décrits dans [types de données de colonne](column-data-types.md).

</dd> <dt>

<span id="Set"></span><span id="set"></span><span id="SET"></span>Définie
</dt> <dd>

Il s’agit d’une liste de valeurs autorisées pour ce champ, séparées par des points-virgules. Ce champ est généralement utilisé pour les énumérations.

</dd> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Descriptive
</dt> <dd>

Description des données stockées dans la colonne.

</dd> </dl>

## <a name="validation"></a>Validation

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE32](ice32.md)  
</dl>

## <a name="remarks"></a>Notes

Le champ de catégorie de ce tableau s’applique uniquement aux données de chaîne. Si le champ de colonne fait référence à une colonne avec des données binaires, le type de données binaire doit être spécifié dans le champ catégorie. Les types de colonne de données Integer ignorent le champ Category pendant la validation.

 

 



