---
title: MS-SQL-attribut de type
description: Type de réplication utilisé par ce serveur SQL Server.
ms.assetid: 8e7fa9ab-9a25-4ee3-9134-68af698a5fb8
ms.tgt_platform: multiple
keywords:
- Schéma AD d’attribut de type MS-SQL
- Schéma AD d’attribut de type mS-SQL
topic_type:
- apiref
api_name:
- MS-SQL-Type
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 057b85b0c522a891cc31cde699fd062897c54818
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "103845545"
---
# <a name="ms-sql-type-attribute"></a>MS-SQL-attribut de type

Type de réplication utilisé par ce serveur SQL Server. Les valeurs suivantes sont les valeurs possibles pour cet attribut.



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
-   [**Windows Server 2008**](#windows-server-2008)
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



 

 





