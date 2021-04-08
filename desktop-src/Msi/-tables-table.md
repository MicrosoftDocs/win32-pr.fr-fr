---
description: La \_ table tables est une table système en lecture seule qui répertorie toutes les tables de la base de données. Interrogez cette table pour savoir si une table existe.
ms.assetid: d064855b-8c10-476e-9570-cc3ab48ae998
title: Table _Tables
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d2dc3ebafd969a07676f64f674f76c3e16ebe059
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864545"
---
# <a name="_tables-table"></a>\_Table tables

La \_ table tables est une table système en lecture seule qui répertorie toutes les tables de la base de données. Interrogez cette table pour savoir si une table existe.

La \_ table tables contient la colonne suivante.



| Colonne | Type             | Clé | Nullable |
|--------|------------------|-----|----------|
| Nom   | [Text](text.md) | O   | N        |



 

## <a name="column"></a>Colonne

<dl> <dt>

<span id="Name"></span><span id="name"></span><span id="NAME"></span>Nomme
</dt> <dd>

Nom de l’une des tables.

</dd> </dl>

## <a name="remarks"></a>Notes

Étant donné que la \_ table tables est une table système qui ne peut pas être modifiée par le biais de requêtes SQL, vous ne pouvez pas obtenir les clés primaires avec la fonction [**MsiDatabaseGetPrimaryKeys**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasegetprimarykeysa) ou la [**propriété PrimaryKeys**](database-primarykeys.md).

 

 



