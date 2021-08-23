---
description: La table ODBCAttribute contient des informations sur les attributs des pilotes et des traducteurs de Open Database Connectivity (ODBC).
ms.assetid: 82fd83d4-22dd-4641-807b-d2b263918e4c
title: Table ODBCAttribute
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e31e67cde1625812d1c5b8af7dc3bd24347891d3a769e24deeb02db7cc44396
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118943177"
---
# <a name="odbcattribute-table"></a>Table ODBCAttribute

La table ODBCAttribute contient des informations sur les attributs des pilotes et des traducteurs de Open Database Connectivity (ODBC).

La table ODBCAttribute contient les colonnes suivantes.



| Colonne    | Type                         | Clé | Nullable |
|-----------|------------------------------|-----|----------|
| Pilote\_  | [Identificateur](identifier.md) | O   | N        |
| Attribut | [Text](text.md)             | O   | N        |
| Valeur     | [Correct](formatted.md)   | N   | O        |



 

## <a name="columns"></a>Colonnes

<dl> <dt>

<span id="Driver_"></span><span id="driver_"></span><span id="DRIVER_"></span>Pilote\_
</dt> <dd>

Nom de jeton interne pour un pilote. Clé primaire pour la table. Clé étrangère dans la [table ODBCDriver](odbcdriver-table.md).

</dd> <dt>

<span id="Attribute"></span><span id="attribute"></span><span id="ATTRIBUTE"></span>Attribut
</dt> <dd>

Nom de l’attribut de pilote. Clé primaire pour la table.

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

 

 



