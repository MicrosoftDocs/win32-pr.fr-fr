---
title: Attribut Postal-Code
description: Code postal ou postal pour la remise du courrier.
ms.assetid: bc8c4f52-df95-4676-beee-e6b86ba668a9
ms.tgt_platform: multiple
keywords:
- Schéma AD d’attribut Postal-Code
- Schéma Active Directory de l’attribut postalCode
topic_type:
- apiref
api_name:
- Postal-Code
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e8bb8340e2a87ef399bf5bdac8d3c0f9f867db570c5b4db06b8c457da1b40747
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119022411"
---
# <a name="postal-code-attribute"></a>Attribut Postal-Code

Code postal ou postal pour la remise du courrier.



| Entrée | Valeur |
|-------------------|-----------------------------------------------------------------------------|
| CN                | Postal-Code                                                                 |
| LDAP-Display-Name | postalCode                                                                  |
| Taille              | \-                                                                          |
| Mettre à jour le privilège  | Administrateur de domaine ou propriétaire du compte.                                      |
| Fréquence des mises à jour  | Lorsque l’enregistrement de l’utilisateur est créé et chaque fois que l’adresse doit être modifiée. |
| Attribute-Id      | 2.5.4.17                                                                    |
| System-ID-GUID    | bf9679fd-0de6-11d0-a285-00aa003049e2                                        |
| Syntaxe            | [**String(Unicode)**](s-string-unicode.md)                                 |



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
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID de lien                | \-                                                                                                                                                                                                                                                                                                              |
| MAPI-Id                | 0x3A2A                                                                                                                                                                                                                                                                                                          |
| System-Only            | Faux                                                                                                                                                                                                                                                                                                           |
| Est de valeur unique       | Vrai                                                                                                                                                                                                                                                                                                            |
| Est indexé             | Faux                                                                                                                                                                                                                                                                                                           |
| Dans le catalogue global      | Faux                                                                                                                                                                                                                                                                                                           |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                                                                                                                                                                                                                                                                                    |
| Range-Lower            | 1                                                                                                                                                                                                                                                                                                               |
| Range-Upper            | 40                                                                                                                                                                                                                                                                                                              |
| Search-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                      |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                      |
| Classes utilisées dans        | [**Organisation**](c-organization.md)<br/> [**Organizational-Person**](c-organizationalperson.md)<br/> [**Rôle organisationnel**](c-organizationalrole.md)<br/> [**Unité d’organisation**](c-organizationalunit.md)<br/> [**Personne privée**](c-residentialperson.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Entrée | Valeur |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID de lien                | \-                                                                                                                                                                                                                                                                                                                                                                      |
| MAPI-Id                | 0x3A2A                                                                                                                                                                                                                                                                                                                                                                  |
| System-Only            | Faux                                                                                                                                                                                                                                                                                                                                                                   |
| Est de valeur unique       | Vrai                                                                                                                                                                                                                                                                                                                                                                    |
| Est indexé             | Faux                                                                                                                                                                                                                                                                                                                                                                   |
| Dans le catalogue global      | Faux                                                                                                                                                                                                                                                                                                                                                                   |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                                                                                                                                                                                                                                                                                                                                            |
| Range-Lower            | 1                                                                                                                                                                                                                                                                                                                                                                       |
| Range-Upper            | 40                                                                                                                                                                                                                                                                                                                                                                      |
| Search-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                              |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                              |
| Classes utilisées dans        | [**Organisation**](c-organization.md)<br/> [**Organizational-Person**](c-organizationalperson.md)<br/> [**Rôle organisationnel**](c-organizationalrole.md)<br/> [**Unité d’organisation**](c-organizationalunit.md)<br/> [**Personne privée**](c-residentialperson.md)<br/> [**rFC822LocalPart**](c-rfc822localpart.md)<br/> |



## <a name="adam"></a>ADAM



| Entrée | Valeur |
|------------------------|------------------------------------------------------------------------------------------------------------------|
| ID de lien                | \-                                                                                                               |
| MAPI-Id                | 0x3A2A                                                                                                           |
| System-Only            | Faux                                                                                                            |
| Est de valeur unique       | Vrai                                                                                                             |
| Est indexé             | Faux                                                                                                            |
| Dans le catalogue global      | Faux                                                                                                            |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                                                                                     |
| Range-Lower            | 1                                                                                                                |
| Range-Upper            | 40                                                                                                               |
| Search-Flags           | 0x00000010                                                                                                       |
| System-Flags           | 0x00000010                                                                                                       |
| Classes utilisées dans        | [**Organisation**](c-organization.md)<br/> [**Unité d’organisation**](c-organizationalunit.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrée | Valeur |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID de lien                | \-                                                                                                                                                                                                                                                                                                                                                                      |
| MAPI-Id                | 0x3A2A                                                                                                                                                                                                                                                                                                                                                                  |
| System-Only            | Faux                                                                                                                                                                                                                                                                                                                                                                   |
| Est de valeur unique       | Vrai                                                                                                                                                                                                                                                                                                                                                                    |
| Est indexé             | Faux                                                                                                                                                                                                                                                                                                                                                                   |
| Dans le catalogue global      | Faux                                                                                                                                                                                                                                                                                                                                                                   |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                                                                                                                                                                                                                                                                                                                                            |
| Range-Lower            | 1                                                                                                                                                                                                                                                                                                                                                                       |
| Range-Upper            | 40                                                                                                                                                                                                                                                                                                                                                                      |
| Search-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                              |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                              |
| Classes utilisées dans        | [**Organisation**](c-organization.md)<br/> [**Organizational-Person**](c-organizationalperson.md)<br/> [**Rôle organisationnel**](c-organizationalrole.md)<br/> [**Unité d’organisation**](c-organizationalunit.md)<br/> [**Personne privée**](c-residentialperson.md)<br/> [**rFC822LocalPart**](c-rfc822localpart.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrée | Valeur |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID de lien                | \-                                                                                                                                                                                                                                                                                                                                                                      |
| MAPI-Id                | 0x3A2A                                                                                                                                                                                                                                                                                                                                                                  |
| System-Only            | Faux                                                                                                                                                                                                                                                                                                                                                                   |
| Est de valeur unique       | Vrai                                                                                                                                                                                                                                                                                                                                                                    |
| Est indexé             | Faux                                                                                                                                                                                                                                                                                                                                                                   |
| Dans le catalogue global      | Faux                                                                                                                                                                                                                                                                                                                                                                   |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                                                                                                                                                                                                                                                                                                                                            |
| Range-Lower            | 1                                                                                                                                                                                                                                                                                                                                                                       |
| Range-Upper            | 40                                                                                                                                                                                                                                                                                                                                                                      |
| Search-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                              |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                              |
| Classes utilisées dans        | [**Organisation**](c-organization.md)<br/> [**Organizational-Person**](c-organizationalperson.md)<br/> [**Rôle organisationnel**](c-organizationalrole.md)<br/> [**Unité d’organisation**](c-organizationalunit.md)<br/> [**Personne privée**](c-residentialperson.md)<br/> [**rFC822LocalPart**](c-rfc822localpart.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrée | Valeur |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID de lien                | \-                                                                                                                                                                                                                                                                                                                                                                      |
| MAPI-Id                | 0x3A2A                                                                                                                                                                                                                                                                                                                                                                  |
| System-Only            | Faux                                                                                                                                                                                                                                                                                                                                                                   |
| Est de valeur unique       | Vrai                                                                                                                                                                                                                                                                                                                                                                    |
| Est indexé             | Faux                                                                                                                                                                                                                                                                                                                                                                   |
| Dans le catalogue global      | Faux                                                                                                                                                                                                                                                                                                                                                                   |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                                                                                                                                                                                                                                                                                                                                            |
| Range-Lower            | 1                                                                                                                                                                                                                                                                                                                                                                       |
| Range-Upper            | 40                                                                                                                                                                                                                                                                                                                                                                      |
| Search-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                              |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                              |
| Classes utilisées dans        | [**Organisation**](c-organization.md)<br/> [**Organizational-Person**](c-organizationalperson.md)<br/> [**Rôle organisationnel**](c-organizationalrole.md)<br/> [**Unité d’organisation**](c-organizationalunit.md)<br/> [**Personne privée**](c-residentialperson.md)<br/> [**rFC822LocalPart**](c-rfc822localpart.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrée | Valeur |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID de lien                | \-                                                                                                                                                                                                                                                                                                                                                                      |
| MAPI-Id                | 0x3A2A                                                                                                                                                                                                                                                                                                                                                                  |
| System-Only            | Faux                                                                                                                                                                                                                                                                                                                                                                   |
| Est de valeur unique       | Vrai                                                                                                                                                                                                                                                                                                                                                                    |
| Est indexé             | Faux                                                                                                                                                                                                                                                                                                                                                                   |
| Dans le catalogue global      | Faux                                                                                                                                                                                                                                                                                                                                                                   |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                                                                                                                                                                                                                                                                                                                                            |
| Range-Lower            | 1                                                                                                                                                                                                                                                                                                                                                                       |
| Range-Upper            | 40                                                                                                                                                                                                                                                                                                                                                                      |
| Search-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                              |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                              |
| Classes utilisées dans        | [**Organisation**](c-organization.md)<br/> [**Organizational-Person**](c-organizationalperson.md)<br/> [**Rôle organisationnel**](c-organizationalrole.md)<br/> [**Unité d’organisation**](c-organizationalunit.md)<br/> [**Personne privée**](c-residentialperson.md)<br/> [**rFC822LocalPart**](c-rfc822localpart.md)<br/> |



 

 





