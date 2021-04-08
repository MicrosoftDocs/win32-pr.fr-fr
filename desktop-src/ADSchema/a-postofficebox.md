---
title: Attribut de zone postérieure au bureau
description: Numéro de la boîte postale pour cet objet.
ms.assetid: e782271a-2f79-42af-9c62-5723917a6f47
ms.tgt_platform: multiple
keywords:
- Schéma AD de l’attribut de zone postérieure au bureau
- Schéma AD de l’attribut postOfficeBox
topic_type:
- apiref
api_name:
- Post-Office-Box
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a8dc8edd327a8b7577e7a8256a8e2f082aad13c8
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "103949844"
---
# <a name="post-office-box-attribute"></a>Attribut de zone postérieure au bureau

Numéro de la boîte postale pour cet objet.



| Entrée | Valeur |
|-------------------|-----------------------------------------------------------------------------|
| CN                | Boîte postale                                                             |
| LDAP-Display-Name | postOfficeBox                                                               |
| Taille              | \-                                                                          |
| Mettre à jour le privilège  | Administrateur de domaine ou propriétaire du compte.                                      |
| Fréquence des mises à jour  | Lorsque l’enregistrement de l’utilisateur est créé et chaque fois que l’adresse doit être modifiée. |
| Attribute-Id      | 2.5.4.18                                                                    |
| System-ID-GUID    | bf9679fb-0de6-11d0-a285-00aa003049e2                                        |
| Syntaxe            | [**String(Unicode)**](s-string-unicode.md)                                 |



## <a name="implementations"></a>Implémentations

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**ADAM**](#adam)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server



| Entrée | Valeur |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID de lien                | \-                                                                                                                                                                                                                                                                                                              |
| MAPI-Id                | 0x3A2B                                                                                                                                                                                                                                                                                                          |
| System-Only            | Faux                                                                                                                                                                                                                                                                                                           |
| Est de valeur unique       | Faux                                                                                                                                                                                                                                                                                                           |
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
| MAPI-Id                | 0x3A2B                                                                                                                                                                                                                                                                                                                                                                  |
| System-Only            | Faux                                                                                                                                                                                                                                                                                                                                                                   |
| Est de valeur unique       | Faux                                                                                                                                                                                                                                                                                                                                                                   |
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
| MAPI-Id                | 0x3A2B                                                                                                           |
| System-Only            | Faux                                                                                                            |
| Est de valeur unique       | Faux                                                                                                            |
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
| MAPI-Id                | 0x3A2B                                                                                                                                                                                                                                                                                                                                                                  |
| System-Only            | Faux                                                                                                                                                                                                                                                                                                                                                                   |
| Est de valeur unique       | Faux                                                                                                                                                                                                                                                                                                                                                                   |
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
| MAPI-Id                | 0x3A2B                                                                                                                                                                                                                                                                                                                                                                  |
| System-Only            | Faux                                                                                                                                                                                                                                                                                                                                                                   |
| Est de valeur unique       | Faux                                                                                                                                                                                                                                                                                                                                                                   |
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
| MAPI-Id                | 0x3A2B                                                                                                                                                                                                                                                                                                                                                                  |
| System-Only            | Faux                                                                                                                                                                                                                                                                                                                                                                   |
| Est de valeur unique       | Faux                                                                                                                                                                                                                                                                                                                                                                   |
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
| MAPI-Id                | 0x3A2B                                                                                                                                                                                                                                                                                                                                                                  |
| System-Only            | Faux                                                                                                                                                                                                                                                                                                                                                                   |
| Est de valeur unique       | Faux                                                                                                                                                                                                                                                                                                                                                                   |
| Est indexé             | Faux                                                                                                                                                                                                                                                                                                                                                                   |
| Dans le catalogue global      | Faux                                                                                                                                                                                                                                                                                                                                                                   |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                                                                                                                                                                                                                                                                                                                                            |
| Range-Lower            | 1                                                                                                                                                                                                                                                                                                                                                                       |
| Range-Upper            | 40                                                                                                                                                                                                                                                                                                                                                                      |
| Search-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                              |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                              |
| Classes utilisées dans        | [**Organisation**](c-organization.md)<br/> [**Organizational-Person**](c-organizationalperson.md)<br/> [**Rôle organisationnel**](c-organizationalrole.md)<br/> [**Unité d’organisation**](c-organizationalunit.md)<br/> [**Personne privée**](c-residentialperson.md)<br/> [**rFC822LocalPart**](c-rfc822localpart.md)<br/> |



 

 





