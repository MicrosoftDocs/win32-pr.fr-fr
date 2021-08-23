---
title: attribut de Type MS-SQL
description: type de réplication utilisé par ce serveur de SQL.
ms.assetid: 8e7fa9ab-9a25-4ee3-9134-68af698a5fb8
ms.tgt_platform: multiple
keywords:
- schéma AD d’attribut de Type MS-SQL
- schéma AD d’attribut de Type mS-SQL
topic_type:
- apiref
api_name:
- MS-SQL-Type
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 15850884b8071fc103abf2c8d3f12ad68d4f5ed946ef2b491b4907b87b1cb524
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119583289"
---
# <a name="ms-sql-type-attribute"></a>attribut de Type MS-SQL

type de réplication utilisé par ce serveur de SQL. Les valeurs suivantes sont les valeurs possibles pour cet attribut.



| Valeur        | Description                           |
|--------------|---------------------------------------|
| 0<br/> | Réplication transactionnelle.<br/> |
| 1<br/> | Réplication d'instantané.<br/>      |
| 2<br/> | Réplication de fusion.<br/>         |



 



| Entrée | Valeur |
|-------------------|---------------------------------------------|
| CN                | Type MS-SQL                                 |
| LDAP-Display-Name | Type mS-SQL                                 |
| Taille              | \-                                          |
| Mettre à jour le privilège  | Administrateur de domaine                        |
| Fréquence des mises à jour  | Lorsque la réplication est configurée.                 |
| Attribute-Id      | 1.2.840.113556.1.4.1391                     |
| System-ID-GUID    | ca48eba8-ccee-11d2-9993-0000f87a57d4        |
| Syntaxe            | [**String(Unicode)**](s-string-unicode.md) |



## <a name="implementations"></a>Implémentations

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server



| Entrée | Valeur |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| ID de lien                | \-                                                                                                                                  |
| MAPI-Id                | \-                                                                                                                                  |
| System-Only            | Faux                                                                                                                               |
| Est de valeur unique       | Vrai                                                                                                                                |
| Est indexé             | Faux                                                                                                                               |
| Dans le catalogue global      | Faux                                                                                                                               |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                                                                                                        |
| Range-Lower            | \-                                                                                                                                  |
| Range-Upper            | \-                                                                                                                                  |
| Search-Flags           | 0x00000000                                                                                                                          |
| System-Flags           | 0x00000010                                                                                                                          |
| Classes utilisées dans        | [**MS-SQL-SQLPublication**](c-ms-sql-sqlpublication.md)<br/> [**MS-SQL-OLAPDatabase**](c-ms-sql-olapdatabase.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Entrée | Valeur |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| ID de lien                | \-                                                                                                                                  |
| MAPI-Id                | \-                                                                                                                                  |
| System-Only            | Faux                                                                                                                               |
| Est de valeur unique       | Vrai                                                                                                                                |
| Est indexé             | Faux                                                                                                                               |
| Dans le catalogue global      | Faux                                                                                                                               |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                                                                                                        |
| Range-Lower            | \-                                                                                                                                  |
| Range-Upper            | \-                                                                                                                                  |
| Search-Flags           | 0x00000000                                                                                                                          |
| System-Flags           | 0x00000010                                                                                                                          |
| Classes utilisées dans        | [**MS-SQL-SQLPublication**](c-ms-sql-sqlpublication.md)<br/> [**MS-SQL-OLAPDatabase**](c-ms-sql-olapdatabase.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrée | Valeur |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| ID de lien                | \-                                                                                                                                  |
| MAPI-Id                | \-                                                                                                                                  |
| System-Only            | Faux                                                                                                                               |
| Est de valeur unique       | Vrai                                                                                                                                |
| Est indexé             | Faux                                                                                                                               |
| Dans le catalogue global      | Faux                                                                                                                               |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                                                                                                        |
| Range-Lower            | \-                                                                                                                                  |
| Range-Upper            | \-                                                                                                                                  |
| Search-Flags           | 0x00000000                                                                                                                          |
| System-Flags           | 0x00000010                                                                                                                          |
| Classes utilisées dans        | [**MS-SQL-SQLPublication**](c-ms-sql-sqlpublication.md)<br/> [**MS-SQL-OLAPDatabase**](c-ms-sql-olapdatabase.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrée | Valeur |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| ID de lien                | \-                                                                                                                                  |
| MAPI-Id                | \-                                                                                                                                  |
| System-Only            | Faux                                                                                                                               |
| Est de valeur unique       | Vrai                                                                                                                                |
| Est indexé             | Faux                                                                                                                               |
| Dans le catalogue global      | Faux                                                                                                                               |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                                                                                                        |
| Range-Lower            | \-                                                                                                                                  |
| Range-Upper            | \-                                                                                                                                  |
| Search-Flags           | 0x00000000                                                                                                                          |
| System-Flags           | 0x00000010                                                                                                                          |
| Classes utilisées dans        | [**MS-SQL-SQLPublication**](c-ms-sql-sqlpublication.md)<br/> [**MS-SQL-OLAPDatabase**](c-ms-sql-olapdatabase.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrée | Valeur |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| ID de lien                | \-                                                                                                                                  |
| MAPI-Id                | \-                                                                                                                                  |
| System-Only            | Faux                                                                                                                               |
| Est de valeur unique       | Vrai                                                                                                                                |
| Est indexé             | Faux                                                                                                                               |
| Dans le catalogue global      | Faux                                                                                                                               |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                                                                                                        |
| Range-Lower            | \-                                                                                                                                  |
| Range-Upper            | \-                                                                                                                                  |
| Search-Flags           | 0x00000000                                                                                                                          |
| System-Flags           | 0x00000010                                                                                                                          |
| Classes utilisées dans        | [**MS-SQL-SQLPublication**](c-ms-sql-sqlpublication.md)<br/> [**MS-SQL-OLAPDatabase**](c-ms-sql-olapdatabase.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrée | Valeur |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| ID de lien                | \-                                                                                                                                  |
| MAPI-Id                | \-                                                                                                                                  |
| System-Only            | Faux                                                                                                                               |
| Est de valeur unique       | Vrai                                                                                                                                |
| Est indexé             | Faux                                                                                                                               |
| Dans le catalogue global      | Faux                                                                                                                               |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                                                                                                        |
| Range-Lower            | \-                                                                                                                                  |
| Range-Upper            | \-                                                                                                                                  |
| Search-Flags           | 0x00000000                                                                                                                          |
| System-Flags           | 0x00000010                                                                                                                          |
| Classes utilisées dans        | [**MS-SQL-SQLPublication**](c-ms-sql-sqlpublication.md)<br/> [**MS-SQL-OLAPDatabase**](c-ms-sql-olapdatabase.md)<br/> |



 

 





