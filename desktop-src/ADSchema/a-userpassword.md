---
title: Attribut User-Password
description: Mot de passe de l’utilisateur au format UTF-8. Il s’agit d’un attribut en écriture seule.
ms.assetid: fcbd5e46-93fc-461e-aa6e-26d08114e73a
ms.tgt_platform: multiple
keywords:
- Schéma AD d’attribut User-Password
- Schéma AD de l’attribut userPassword
topic_type:
- apiref
api_name:
- User-Password
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9d15fae037e2b2e8fdb7889b6ba18e0269244174a80f7a373edc2b1457faced1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119922919"
---
# <a name="user-password-attribute"></a>Attribut User-Password

Mot de passe de l’utilisateur au format UTF-8. Il s’agit d’un attribut en écriture seule.



| Entrée | Valeur |
|-------------------|-------------------------------------------------------|
| CN                | User-Password                                         |
| LDAP-Display-Name | userPassword                                          |
| Taille              | \-                                                    |
| Mettre à jour le privilège  | Administrateur de domaine ou propriétaire du compte.                |
| Fréquence des mises à jour  | \-                                                    |
| Attribute-Id      | 2.5.4.35                                              |
| System-ID-GUID    | bf967a6e-0de6-11d0-a285-00aa003049e2                  |
| Syntaxe            | [**Object(Replica-Link)**](s-object-replica-link.md) |



## <a name="implementations"></a>Implémentations

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**ADAM**](#adam)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server



| Entrée | Valeur |
|------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID de lien                | \-                                                                                                                                                     |
| MAPI-Id                | 0x8153                                                                                                                                                 |
| System-Only            | Faux                                                                                                                                                  |
| Est de valeur unique       | Faux                                                                                                                                                  |
| Est indexé             | Faux                                                                                                                                                  |
| Dans le catalogue global      | Faux                                                                                                                                                  |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                                                                                                                           |
| Range-Lower            | 1                                                                                                                                                      |
| Range-Upper            | 128                                                                                                                                                    |
| Search-Flags           | 0x00000000                                                                                                                                             |
| System-Flags           | 0x00000010                                                                                                                                             |
| Classes utilisées dans        | [**Organisation**](c-organization.md)<br/> [**Unité d’organisation**](c-organizationalunit.md)<br/> [**Personne**](c-person.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Entrée | Valeur |
|------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID de lien                | \-                                                                                                                                                                                                                       |
| MAPI-Id                | 0x8153                                                                                                                                                                                                                   |
| System-Only            | Faux                                                                                                                                                                                                                    |
| Est de valeur unique       | Faux                                                                                                                                                                                                                    |
| Est indexé             | Faux                                                                                                                                                                                                                    |
| Dans le catalogue global      | Faux                                                                                                                                                                                                                    |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                                                                                                                                                                                             |
| Range-Lower            | 1                                                                                                                                                                                                                        |
| Range-Upper            | 128                                                                                                                                                                                                                      |
| Search-Flags           | 0x00000000                                                                                                                                                                                                               |
| System-Flags           | 0x00000010                                                                                                                                                                                                               |
| Classes utilisées dans        | [**Organisation**](c-organization.md)<br/> [**Unité d’organisation**](c-organizationalunit.md)<br/> [**Personne**](c-person.md)<br/> [**simpleSecurityObject**](c-simplesecurityobject.md)<br/> |



## <a name="adam"></a>ADAM



| Entrée | Valeur |
|------------------------|------------------------------------------------------------------------------------------------------------------|
| ID de lien                | \-                                                                                                               |
| MAPI-Id                | 0x8153                                                                                                           |
| System-Only            | Faux                                                                                                            |
| Est de valeur unique       | Faux                                                                                                            |
| Est indexé             | Faux                                                                                                            |
| Dans le catalogue global      | Faux                                                                                                            |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                                                                                     |
| Range-Lower            | 1                                                                                                                |
| Range-Upper            | 128                                                                                                              |
| Search-Flags           | 0x00000000                                                                                                       |
| System-Flags           | 0x00000010                                                                                                       |
| Classes utilisées dans        | [**Organisation**](c-organization.md)<br/> [**Unité d’organisation**](c-organizationalunit.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrée | Valeur |
|------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID de lien                | \-                                                                                                                                                                                                                                                                                                                                                                           |
| MAPI-Id                | 0x8153                                                                                                                                                                                                                                                                                                                                                                       |
| System-Only            | Faux                                                                                                                                                                                                                                                                                                                                                                        |
| Est de valeur unique       | Faux                                                                                                                                                                                                                                                                                                                                                                        |
| Est indexé             | Faux                                                                                                                                                                                                                                                                                                                                                                        |
| Dans le catalogue global      | Faux                                                                                                                                                                                                                                                                                                                                                                        |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                                                                                                                                                                                                                                                                                                                                                 |
| Range-Lower            | 1                                                                                                                                                                                                                                                                                                                                                                            |
| Range-Upper            | 128                                                                                                                                                                                                                                                                                                                                                                          |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                                                                                                                                                                   |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                                   |
| Classes utilisées dans        | [**Organisation**](c-organization.md)<br/> [**Unité d’organisation**](c-organizationalunit.md)<br/> [**Personne**](c-person.md)<br/> [**simpleSecurityObject**](c-simplesecurityobject.md)<br/> [**posixAccount**](c-posixaccount.md)<br/> [**shadowAccount**](c-shadowaccount.md)<br/> [**posixGroup**](c-posixgroup.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrée | Valeur |
|------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID de lien                | \-                                                                                                                                                                                                                                                                                                                                                                           |
| MAPI-Id                | 0x8153                                                                                                                                                                                                                                                                                                                                                                       |
| System-Only            | Faux                                                                                                                                                                                                                                                                                                                                                                        |
| Est de valeur unique       | Faux                                                                                                                                                                                                                                                                                                                                                                        |
| Est indexé             | Faux                                                                                                                                                                                                                                                                                                                                                                        |
| Dans le catalogue global      | Faux                                                                                                                                                                                                                                                                                                                                                                        |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                                                                                                                                                                                                                                                                                                                                                 |
| Range-Lower            | 1                                                                                                                                                                                                                                                                                                                                                                            |
| Range-Upper            | 128                                                                                                                                                                                                                                                                                                                                                                          |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                                                                                                                                                                   |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                                   |
| Classes utilisées dans        | [**Organisation**](c-organization.md)<br/> [**Unité d’organisation**](c-organizationalunit.md)<br/> [**Personne**](c-person.md)<br/> [**simpleSecurityObject**](c-simplesecurityobject.md)<br/> [**posixAccount**](c-posixaccount.md)<br/> [**shadowAccount**](c-shadowaccount.md)<br/> [**posixGroup**](c-posixgroup.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrée | Valeur |
|------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID de lien                | \-                                                                                                                                                                                                                                                                                                                                                                           |
| MAPI-Id                | 0x8153                                                                                                                                                                                                                                                                                                                                                                       |
| System-Only            | Faux                                                                                                                                                                                                                                                                                                                                                                        |
| Est de valeur unique       | Faux                                                                                                                                                                                                                                                                                                                                                                        |
| Est indexé             | Faux                                                                                                                                                                                                                                                                                                                                                                        |
| Dans le catalogue global      | Faux                                                                                                                                                                                                                                                                                                                                                                        |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                                                                                                                                                                                                                                                                                                                                                 |
| Range-Lower            | 1                                                                                                                                                                                                                                                                                                                                                                            |
| Range-Upper            | 128                                                                                                                                                                                                                                                                                                                                                                          |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                                                                                                                                                                   |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                                   |
| Classes utilisées dans        | [**Organisation**](c-organization.md)<br/> [**Unité d’organisation**](c-organizationalunit.md)<br/> [**Personne**](c-person.md)<br/> [**simpleSecurityObject**](c-simplesecurityobject.md)<br/> [**posixAccount**](c-posixaccount.md)<br/> [**shadowAccount**](c-shadowaccount.md)<br/> [**posixGroup**](c-posixgroup.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrée | Valeur |
|------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID de lien                | \-                                                                                                                                                                                                                                                                                                                                                                           |
| MAPI-Id                | 0x8153                                                                                                                                                                                                                                                                                                                                                                       |
| System-Only            | Faux                                                                                                                                                                                                                                                                                                                                                                        |
| Est de valeur unique       | Faux                                                                                                                                                                                                                                                                                                                                                                        |
| Est indexé             | Faux                                                                                                                                                                                                                                                                                                                                                                        |
| Dans le catalogue global      | Faux                                                                                                                                                                                                                                                                                                                                                                        |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                                                                                                                                                                                                                                                                                                                                                 |
| Range-Lower            | 1                                                                                                                                                                                                                                                                                                                                                                            |
| Range-Upper            | 128                                                                                                                                                                                                                                                                                                                                                                          |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                                                                                                                                                                   |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                                   |
| Classes utilisées dans        | [**Organisation**](c-organization.md)<br/> [**Unité d’organisation**](c-organizationalunit.md)<br/> [**Personne**](c-person.md)<br/> [**simpleSecurityObject**](c-simplesecurityobject.md)<br/> [**posixAccount**](c-posixaccount.md)<br/> [**shadowAccount**](c-shadowaccount.md)<br/> [**posixGroup**](c-posixgroup.md)<br/> |



 

 





