---
title: Attribut Street-Address
description: Adresse postale.
ms.assetid: 09a94b72-14cb-4d4d-b885-4015f65db139
ms.tgt_platform: multiple
keywords:
- Schéma AD d’attribut Street-Address
- Schéma AD de l’attribut Street
topic_type:
- apiref
api_name:
- Street-Address
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a44cf03e89ee4f969d12e435f1fd3f31f535e9050bd667f220b5c6852a1bd092
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119645619"
---
# <a name="street-address-attribute"></a>Attribut Street-Address

Adresse postale.



| Entrée | Valeur |
|-------------------|----------------------------------------------------------------------------------|
| CN                | Street-Address                                                                   |
| LDAP-Display-Name | street                                                                           |
| Taille              | \-                                                                               |
| Mettre à jour le privilège  | Tout le monde peut mettre à jour cet objet en fonction de la sécurité de l’objet en cours de création. |
| Fréquence des mises à jour  | \-                                                                               |
| Attribute-Id      | 2.5.4.9                                                                          |
| System-ID-GUID    | bf967a3a-0de6-11d0-a285-00aa003049e2                                             |
| Syntaxe            | [**String(Unicode)**](s-string-unicode.md)                                      |



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
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID de lien                | \-                                                                                                                                                                                                                                                                                                                                                        |
| MAPI-Id                | 0x813A                                                                                                                                                                                                                                                                                                                                                    |
| System-Only            | Faux                                                                                                                                                                                                                                                                                                                                                     |
| Est de valeur unique       | Vrai                                                                                                                                                                                                                                                                                                                                                      |
| Est indexé             | Faux                                                                                                                                                                                                                                                                                                                                                     |
| Dans le catalogue global      | Vrai                                                                                                                                                                                                                                                                                                                                                      |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                                                                                                                                                                                                                                                                                                                              |
| Range-Lower            | 1                                                                                                                                                                                                                                                                                                                                                         |
| Range-Upper            | 1 024                                                                                                                                                                                                                                                                                                                                                      |
| Search-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                |
| System-Flags           | 0x00000012                                                                                                                                                                                                                                                                                                                                                |
| Classes utilisées dans        | [**Localité**](c-locality.md)<br/> [**Organisation**](c-organization.md)<br/> [**Organizational-Person**](c-organizationalperson.md)<br/> [**Rôle organisationnel**](c-organizationalrole.md)<br/> [**Unité d’organisation**](c-organizationalunit.md)<br/> [**Personne privée**](c-residentialperson.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Entrée | Valeur |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID de lien                | \-                                                                                                                                                                                                                                                                                                                                                                                                                |
| MAPI-Id                | 0x813A                                                                                                                                                                                                                                                                                                                                                                                                            |
| System-Only            | Faux                                                                                                                                                                                                                                                                                                                                                                                                             |
| Est de valeur unique       | Vrai                                                                                                                                                                                                                                                                                                                                                                                                              |
| Est indexé             | Faux                                                                                                                                                                                                                                                                                                                                                                                                             |
| Dans le catalogue global      | Vrai                                                                                                                                                                                                                                                                                                                                                                                                              |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                                                                                                                                                                                                                                                                                                                                                                                      |
| Range-Lower            | 1                                                                                                                                                                                                                                                                                                                                                                                                                 |
| Range-Upper            | 1 024                                                                                                                                                                                                                                                                                                                                                                                                              |
| Search-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                                                                        |
| System-Flags           | 0x00000012                                                                                                                                                                                                                                                                                                                                                                                                        |
| Classes utilisées dans        | [**Localité**](c-locality.md)<br/> [**Organisation**](c-organization.md)<br/> [**Organizational-Person**](c-organizationalperson.md)<br/> [**Rôle organisationnel**](c-organizationalrole.md)<br/> [**Unité d’organisation**](c-organizationalunit.md)<br/> [**Personne privée**](c-residentialperson.md)<br/> [**rFC822LocalPart**](c-rfc822localpart.md)<br/> |



## <a name="adam"></a>ADAM



| Entrée | Valeur |
|------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID de lien                | \-                                                                                                                                                         |
| MAPI-Id                | 0x813A                                                                                                                                                     |
| System-Only            | Faux                                                                                                                                                      |
| Est de valeur unique       | Vrai                                                                                                                                                       |
| Est indexé             | Faux                                                                                                                                                      |
| Dans le catalogue global      | Vrai                                                                                                                                                       |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                                                                                                                               |
| Range-Lower            | 1                                                                                                                                                          |
| Range-Upper            | 1 024                                                                                                                                                       |
| Search-Flags           | 0x00000010                                                                                                                                                 |
| System-Flags           | 0x00000012                                                                                                                                                 |
| Classes utilisées dans        | [**Localité**](c-locality.md)<br/> [**Organisation**](c-organization.md)<br/> [**Unité d’organisation**](c-organizationalunit.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrée | Valeur |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID de lien                | \-                                                                                                                                                                                                                                                                                                                                                                                                                |
| MAPI-Id                | 0x813A                                                                                                                                                                                                                                                                                                                                                                                                            |
| System-Only            | Faux                                                                                                                                                                                                                                                                                                                                                                                                             |
| Est de valeur unique       | Vrai                                                                                                                                                                                                                                                                                                                                                                                                              |
| Est indexé             | Faux                                                                                                                                                                                                                                                                                                                                                                                                             |
| Dans le catalogue global      | Vrai                                                                                                                                                                                                                                                                                                                                                                                                              |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                                                                                                                                                                                                                                                                                                                                                                                      |
| Range-Lower            | 1                                                                                                                                                                                                                                                                                                                                                                                                                 |
| Range-Upper            | 1 024                                                                                                                                                                                                                                                                                                                                                                                                              |
| Search-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                                                                        |
| System-Flags           | 0x00000012                                                                                                                                                                                                                                                                                                                                                                                                        |
| Classes utilisées dans        | [**Localité**](c-locality.md)<br/> [**Organisation**](c-organization.md)<br/> [**Organizational-Person**](c-organizationalperson.md)<br/> [**Rôle organisationnel**](c-organizationalrole.md)<br/> [**Unité d’organisation**](c-organizationalunit.md)<br/> [**Personne privée**](c-residentialperson.md)<br/> [**rFC822LocalPart**](c-rfc822localpart.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrée | Valeur |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID de lien                | \-                                                                                                                                                                                                                                                                                                                                                                                                                |
| MAPI-Id                | 0x813A                                                                                                                                                                                                                                                                                                                                                                                                            |
| System-Only            | Faux                                                                                                                                                                                                                                                                                                                                                                                                             |
| Est de valeur unique       | Vrai                                                                                                                                                                                                                                                                                                                                                                                                              |
| Est indexé             | Faux                                                                                                                                                                                                                                                                                                                                                                                                             |
| Dans le catalogue global      | Vrai                                                                                                                                                                                                                                                                                                                                                                                                              |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                                                                                                                                                                                                                                                                                                                                                                                      |
| Range-Lower            | 1                                                                                                                                                                                                                                                                                                                                                                                                                 |
| Range-Upper            | 1 024                                                                                                                                                                                                                                                                                                                                                                                                              |
| Search-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                                                                        |
| System-Flags           | 0x00000012                                                                                                                                                                                                                                                                                                                                                                                                        |
| Classes utilisées dans        | [**Localité**](c-locality.md)<br/> [**Organisation**](c-organization.md)<br/> [**Organizational-Person**](c-organizationalperson.md)<br/> [**Rôle organisationnel**](c-organizationalrole.md)<br/> [**Unité d’organisation**](c-organizationalunit.md)<br/> [**Personne privée**](c-residentialperson.md)<br/> [**rFC822LocalPart**](c-rfc822localpart.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrée | Valeur |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID de lien                | \-                                                                                                                                                                                                                                                                                                                                                                                                                |
| MAPI-Id                | 0x813A                                                                                                                                                                                                                                                                                                                                                                                                            |
| System-Only            | Faux                                                                                                                                                                                                                                                                                                                                                                                                             |
| Est de valeur unique       | Vrai                                                                                                                                                                                                                                                                                                                                                                                                              |
| Est indexé             | Faux                                                                                                                                                                                                                                                                                                                                                                                                             |
| Dans le catalogue global      | Vrai                                                                                                                                                                                                                                                                                                                                                                                                              |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                                                                                                                                                                                                                                                                                                                                                                                      |
| Range-Lower            | 1                                                                                                                                                                                                                                                                                                                                                                                                                 |
| Range-Upper            | 1 024                                                                                                                                                                                                                                                                                                                                                                                                              |
| Search-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                                                                        |
| System-Flags           | 0x00000012                                                                                                                                                                                                                                                                                                                                                                                                        |
| Classes utilisées dans        | [**Localité**](c-locality.md)<br/> [**Organisation**](c-organization.md)<br/> [**Organizational-Person**](c-organizationalperson.md)<br/> [**Rôle organisationnel**](c-organizationalrole.md)<br/> [**Unité d’organisation**](c-organizationalunit.md)<br/> [**Personne privée**](c-residentialperson.md)<br/> [**rFC822LocalPart**](c-rfc822localpart.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrée | Valeur |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID de lien                | \-                                                                                                                                                                                                                                                                                                                                                                                                                |
| MAPI-Id                | 0x813A                                                                                                                                                                                                                                                                                                                                                                                                            |
| System-Only            | Faux                                                                                                                                                                                                                                                                                                                                                                                                             |
| Est de valeur unique       | Vrai                                                                                                                                                                                                                                                                                                                                                                                                              |
| Est indexé             | Faux                                                                                                                                                                                                                                                                                                                                                                                                             |
| Dans le catalogue global      | Vrai                                                                                                                                                                                                                                                                                                                                                                                                              |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                                                                                                                                                                                                                                                                                                                                                                                      |
| Range-Lower            | 1                                                                                                                                                                                                                                                                                                                                                                                                                 |
| Range-Upper            | 1 024                                                                                                                                                                                                                                                                                                                                                                                                              |
| Search-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                                                                        |
| System-Flags           | 0x00000012                                                                                                                                                                                                                                                                                                                                                                                                        |
| Classes utilisées dans        | [**Localité**](c-locality.md)<br/> [**Organisation**](c-organization.md)<br/> [**Organizational-Person**](c-organizationalperson.md)<br/> [**Rôle organisationnel**](c-organizationalrole.md)<br/> [**Unité d’organisation**](c-organizationalunit.md)<br/> [**Personne privée**](c-residentialperson.md)<br/> [**rFC822LocalPart**](c-rfc822localpart.md)<br/> |



 

 





