---
description: Le tableau suivant répertorie les mappages entre les types de données Variant et les types de données OLE DB.
ms.assetid: 213458bf-b847-4ced-8a92-686b4eee6d07
title: Mappages de type de données
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9beae5a9ce1fbaafadfae54979d63c97310f57db
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112435"
---
# <a name="data-type-mappings"></a>Mappages de type de données

Le tableau suivant répertorie les mappages entre les types de données Variant et les types de données OLE DB.




| Type de données variant | Type de données OLE DB |
|-------------------|------------------|
| VT \_ bool          | DBTYPE \_ bool     |
| VT \_ BSTR          | DBTYPE, \_ BSTR     |
| VT \_ ByRef         | DBTYPE avec \_ ByRef    |
| VT \_ ca            | DBTYPE \_ CY       |
| \_Date VT          | \_Date DbType     |
| \_valeur décimale VT       | DBTYPE, \_ décimale  |
| VT \_ vide         | DBTYPE \_ vide    |
| de VT \_ fileTime      | DBTYPE \_ fileTime |
| \_GUID VT          | \_GUID DbType     |
| VT \_ I1            | DBTYPE \_ I1       |
| VT \_ I2            | DBTYPE \_ I2       |
| VT \_            | DBTYPE \_ I4       |
| Le \_ i8 VT            | Le \_ i8 DbType       |
| VT \_ null          | DBTYPE \_ null     |
| VT \_ R4            | DBTYPE \_ R4       |
| VT \_ R8            | \_UI8 DbType      |
| \_vecteur VT        | DBTYPE, \_ vecteur   |
| \_WSTR VT          | \_WSTR DbType     |



 

Le tableau suivant répertorie les mappages entre les types de données XML et les types de données OLE DB.



| Type de données variant | Type de données OLE DB |
|-------------------|------------------|
| Granule. NUMÉRIQUE        | \_octets DbType    |
| Granule. SÉQUENCE           | Le \_ i8 DbType       |
| BOOLEAN           | DBTYPE \_ bool     |
| CHAR              | DBTYPE \_ Str      |
| DATE              | \_Date DbType     |
| DATETIME          | \_Date DbType     |
| Date et heure. TZ       | \_Date DbType     |
| CORRECTION de. 14,4        | DBTYPE \_ R4       |
| FLOAT             | DBTYPE \_ R8       |
| I1                | DBTYPE \_ I1       |
| I2                | DBTYPE \_ I2       |
| I4                | DBTYPE \_ I4       |
| I8                | Le \_ i8 DbType       |
| INT               | Le \_ i8 DbType       |
| LONG              | DBTYPE \_ I4       |
| NUMBER            | DBTYPE \_ R8       |
| R4                | DBTYPE \_ R4       |
| R8                | DBTYPE \_ R8       |
| STRING            | \_WSTR DbType     |
| TEMPS              | DBTYPE \_ fileTime |
| Simultanément. TZ           | DBTYPE \_ fileTime |
| UI1               | \_UI2 DbType      |
| UI2               | \_UI2 DbType      |
| UI4               | DBTYPE \_ UI4      |
| UI8               | \_UI8 DbType      |
| URI               | \_WSTR DbType     |
| UUID              | \_GUID DbType     |



 

Vous pouvez convertir des données de type chaîne en d’autres types de données. Pour plus d’informations, consultez [cast du type de données d’une colonne](-search-sql-castingdatacolumntype.md).

 

 



