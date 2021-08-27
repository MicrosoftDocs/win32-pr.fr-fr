---
description: La table ODBCSourceAttribute contient des informations sur les attributs des sources de données.
ms.assetid: 8ee50fd7-507e-484f-9a16-de5449470562
title: Table ODBCSourceAttribute
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c6d84ca19dfd059df4ff8f79d9409ef23288800f09e84d45e1b55d81bc8641e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120082709"
---
# <a name="odbcsourceattribute-table"></a>Table ODBCSourceAttribute

La table ODBCSourceAttribute contient des informations sur les attributs des sources de données.

La table ODBCSourceAttribute contient les colonnes suivantes.



| Colonne       | Type                         | Clé | Nullable |
|--------------|------------------------------|-----|----------|
| Mustek\_ | [Identificateur](identifier.md) | O   | N        |
| Attribut    | [Text](text.md)             | O   | N        |
| Valeur        | [Correct](formatted.md)   | N   | O        |



 

## <a name="columns"></a>Colonnes

<dl> <dt>

<span id="DataSource_"></span><span id="datasource_"></span><span id="DATASOURCE_"></span>Mustek\_
</dt> <dd>

Nom de jeton interne de la source de données. Clé primaire pour la table.

</dd> <dt>

<span id="Attribute"></span><span id="attribute"></span><span id="ATTRIBUTE"></span>Attribut
</dt> <dd>

Nom de l’attribut de source de données. Clé primaire pour la table.

</dd> <dt>

<span id="Value"></span><span id="value"></span><span id="VALUE"></span>Ajoutée
</dt> <dd>

Valeur de chaîne localisable pour l’attribut.

</dd> </dl>

## <a name="remarks"></a>Remarques

Les actions [InstallODBC](installodbc-action.md) et [RemoveODBC](removeodbc-action.md) dans les [*tables de séquence*](s-gly.md) traitent les informations contenues dans ce tableau. Pour plus d’informations sur l’utilisation des *tables de séquences*, consultez [utilisation d’une table de séquences](using-a-sequence-table.md).

## <a name="validation"></a>Validation

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE32](ice32.md)  
[ICE46](ice46.md)  
</dl>

 

 



