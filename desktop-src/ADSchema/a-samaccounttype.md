---
title: Attribut SAM-Account-type
description: Cet attribut contient des informations sur chaque objet de type de compte.
ms.assetid: 00479b89-1d96-4ace-bbd8-053ca9e548b0
ms.tgt_platform: multiple
keywords:
- Schéma AD de l’attribut SAM-Account-type
- Schéma AD de l’attribut sAMAccountType
topic_type:
- apiref
api_name:
- SAM-Account-Type
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f51de46dac0faabcc248159f7dcabafcd6060725
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "103943104"
---
# <a name="sam-account-type-attribute"></a>Attribut SAM-Account-type

Cet attribut contient des informations sur chaque objet de type de compte. Vous pouvez énumérer une liste de types de comptes, ou vous pouvez utiliser l’API afficher les informations pour créer une liste. Étant donné que les ordinateurs, les comptes d’utilisateurs normaux et les comptes de confiance peuvent également être énumérés en tant qu’objets utilisateur, les valeurs de ces comptes doivent être une plage contiguë.

Les valeurs possibles pour cet attribut sont les suivantes :

-   \_Objet de domaine sam \_ 0x0
-   \_Objet de groupe sam \_ 0x10000000
-   SAM \_ objet de groupe non de \_ sécurité \_ \_ 0x10000001
-   \_Objet alias Sam \_ 0x20000000
-   SAM \_ non- \_ sécurité d’objet d' \_ alias \_ 0x20000001
-   SAM \_ User, \_ objet 0x30000000
-   SAM \_ \_ compte d’utilisateur normal \_ 0x30000000
-   \_Compte d’ordinateur sam \_ 0x30000001
-   \_Compte de confiance sam \_ 0x30000002
-   SAM \_ app \_ Basic \_ Group 0x40000000
-   SAM \_ \_ 0x40000001 groupe de requêtes d’application \_
-   \_Type de compte Sam \_ \_ Max 0x7FFFFFFF



| Entrée | Valeur |
|-------------------|-----------------------------------------------------------------|
| CN                | Type de compte SAM                                                |
| LDAP-Display-Name | sAMAccountType                                                  |
| Taille              | \-                                                              |
| Mettre à jour le privilège  | Cette valeur est définie par le système.                                |
| Fréquence des mises à jour  | Cela est défini par le système d’exploitation lors de la création de l’objet. |
| Attribute-Id      | 1.2.840.113556.1.4.302                                          |
| System-ID-GUID    | 6e7b626c-64f2-11d0-afd2-00c04fd930c9                            |
| Syntaxe            | [**Enumeration**](s-enumeration.md)                            |



## <a name="implementations"></a>Implémentations

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server



| Entrée | Valeur |
|------------------------|--------------------------------------------------------------|
| ID de lien                | \-                                                           |
| MAPI-Id                | \-                                                           |
| System-Only            | Faux                                                        |
| Est de valeur unique       | Vrai                                                         |
| Est indexé             | Vrai                                                         |
| Dans le catalogue global      | Vrai                                                         |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                                 |
| Range-Lower            | \-                                                           |
| Range-Upper            | \-                                                           |
| Search-Flags           | 0x00000001                                                   |
| System-Flags           | 0x00000012                                                   |
| Classes utilisées dans        | [**Sécurité-principal**](c-securityprincipal.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Entrée | Valeur |
|------------------------|--------------------------------------------------------------|
| ID de lien                | \-                                                           |
| MAPI-Id                | \-                                                           |
| System-Only            | Faux                                                        |
| Est de valeur unique       | Vrai                                                         |
| Est indexé             | Vrai                                                         |
| Dans le catalogue global      | Vrai                                                         |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                                 |
| Range-Lower            | \-                                                           |
| Range-Upper            | \-                                                           |
| Search-Flags           | 0x00000001                                                   |
| System-Flags           | 0x00000012                                                   |
| Classes utilisées dans        | [**Sécurité-principal**](c-securityprincipal.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrée | Valeur |
|------------------------|--------------------------------------------------------------|
| ID de lien                | \-                                                           |
| MAPI-Id                | \-                                                           |
| System-Only            | Faux                                                        |
| Est de valeur unique       | Vrai                                                         |
| Est indexé             | Vrai                                                         |
| Dans le catalogue global      | Vrai                                                         |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                                 |
| Range-Lower            | \-                                                           |
| Range-Upper            | \-                                                           |
| Search-Flags           | 0x00000001                                                   |
| System-Flags           | 0x00000012                                                   |
| Classes utilisées dans        | [**Sécurité-principal**](c-securityprincipal.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrée | Valeur |
|------------------------|--------------------------------------------------------------|
| ID de lien                | \-                                                           |
| MAPI-Id                | \-                                                           |
| System-Only            | Faux                                                        |
| Est de valeur unique       | Vrai                                                         |
| Est indexé             | Vrai                                                         |
| Dans le catalogue global      | Vrai                                                         |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                                 |
| Range-Lower            | \-                                                           |
| Range-Upper            | \-                                                           |
| Search-Flags           | 0x00000001                                                   |
| System-Flags           | 0x00000012                                                   |
| Classes utilisées dans        | [**Sécurité-principal**](c-securityprincipal.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrée | Valeur |
|------------------------|--------------------------------------------------------------|
| ID de lien                | \-                                                           |
| MAPI-Id                | \-                                                           |
| System-Only            | Faux                                                        |
| Est de valeur unique       | Vrai                                                         |
| Est indexé             | Vrai                                                         |
| Dans le catalogue global      | Vrai                                                         |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                                 |
| Range-Lower            | \-                                                           |
| Range-Upper            | \-                                                           |
| Search-Flags           | 0x00000001                                                   |
| System-Flags           | 0x00000012                                                   |
| Classes utilisées dans        | [**Sécurité-principal**](c-securityprincipal.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrée | Valeur |
|------------------------|--------------------------------------------------------------|
| ID de lien                | \-                                                           |
| MAPI-Id                | \-                                                           |
| System-Only            | Faux                                                        |
| Est de valeur unique       | Vrai                                                         |
| Est indexé             | Vrai                                                         |
| Dans le catalogue global      | Vrai                                                         |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                                 |
| Range-Lower            | \-                                                           |
| Range-Upper            | \-                                                           |
| Search-Flags           | 0x00000001                                                   |
| System-Flags           | 0x00000012                                                   |
| Classes utilisées dans        | [**Sécurité-principal**](c-securityprincipal.md)<br/> |



 

 





