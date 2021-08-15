---
description: La \_ table tables est une table système en lecture seule qui répertorie toutes les tables de la base de données. Interrogez cette table pour savoir si une table existe.
ms.assetid: d064855b-8c10-476e-9570-cc3ab48ae998
title: Table _Tables
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 10c251693d89bb23634b222518e98dba270856e672362bcdc9acddd3c0b86c56
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119013317"
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

## <a name="remarks"></a>Remarques

étant donné que la \_ table tables est une table système qui ne peut pas être modifiée par le biais de requêtes SQL, vous ne pouvez pas obtenir les clés primaires avec la fonction [**MsiDatabaseGetPrimaryKeys**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasegetprimarykeysa) ou la [**propriété PrimaryKeys**](database-primarykeys.md).

 

 



