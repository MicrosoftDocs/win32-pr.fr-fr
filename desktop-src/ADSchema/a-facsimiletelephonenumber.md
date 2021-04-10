---
title: Attribut télécopie-numéro de téléphone
description: Contient le numéro de téléphone de l’ordinateur de télécopie professionnel de l’utilisateur.
ms.assetid: 3862b049-19f5-4067-941d-d1a3a049bc56
ms.tgt_platform: multiple
keywords:
- Télécopie-schéma AD-attribut de numéro de téléphone
- Schéma AD de l’attribut facsimileTelephoneNumber
topic_type:
- apiref
api_name:
- Facsimile-Telephone-Number
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2686a355aedc12a37a12a218ab623e8b02e055d2
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "103844669"
---
# <a name="facsimile-telephone-number-attribute"></a>Attribut télécopie-numéro de téléphone

Contient le numéro de téléphone de l’ordinateur de télécopie professionnel de l’utilisateur.



| Entrée | Valeur |
|-------------------|---------------------------------------------|
| CN                | Télécopie-numéro de téléphone                  |
| LDAP-Display-Name | facsimileTelephoneNumber                    |
| Taille              | \-                                          |
| Mettre à jour le privilège  | Administrateur de domaine ou propriétaire du compte.      |
| Fréquence des mises à jour  | Chaque fois que le numéro de télécopie doit être modifié.    |
| Attribute-Id      | 2.5.4.23                                    |
| System-ID-GUID    | bf967974-0de6-11d0-a285-00aa003049e2        |
| Syntaxe            | [**String(Unicode)**](s-string-unicode.md) |



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
| MAPI-Id                | 0x3A23                                                                                                                                                                                                                                                                                                          |
| System-Only            | Faux                                                                                                                                                                                                                                                                                                           |
| Est de valeur unique       | Vrai                                                                                                                                                                                                                                                                                                            |
| Est indexé             | Faux                                                                                                                                                                                                                                                                                                           |
| Dans le catalogue global      | Faux                                                                                                                                                                                                                                                                                                           |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                                                                                                                                                                                                                                                                                    |
| Range-Lower            | 1                                                                                                                                                                                                                                                                                                               |
| Range-Upper            | 64                                                                                                                                                                                                                                                                                                              |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                                                                                                      |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                      |
| Classes utilisées dans        | [**Organisation**](c-organization.md)<br/> [**Organizational-Person**](c-organizationalperson.md)<br/> [**Rôle organisationnel**](c-organizationalrole.md)<br/> [**Unité d’organisation**](c-organizationalunit.md)<br/> [**Personne privée**](c-residentialperson.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Entrée | Valeur |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID de lien                | \-                                                                                                                                                                                                                                                                                                                                                                      |
| MAPI-Id                | 0x3A23                                                                                                                                                                                                                                                                                                                                                                  |
| System-Only            | Faux                                                                                                                                                                                                                                                                                                                                                                   |
| Est de valeur unique       | Vrai                                                                                                                                                                                                                                                                                                                                                                    |
| Est indexé             | Faux                                                                                                                                                                                                                                                                                                                                                                   |
| Dans le catalogue global      | Faux                                                                                                                                                                                                                                                                                                                                                                   |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                                                                                                                                                                                                                                                                                                                                            |
| Range-Lower            | 1                                                                                                                                                                                                                                                                                                                                                                       |
| Range-Upper            | 64                                                                                                                                                                                                                                                                                                                                                                      |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                                                                                                                                                              |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                              |
| Classes utilisées dans        | [**Organisation**](c-organization.md)<br/> [**Organizational-Person**](c-organizationalperson.md)<br/> [**Rôle organisationnel**](c-organizationalrole.md)<br/> [**Unité d’organisation**](c-organizationalunit.md)<br/> [**Personne privée**](c-residentialperson.md)<br/> [**rFC822LocalPart**](c-rfc822localpart.md)<br/> |



## <a name="adam"></a>ADAM



| Entrée | Valeur |
|------------------------|------------------------------------------------------------------------------------------------------------------|
| ID de lien                | \-                                                                                                               |
| MAPI-Id                | 0x3A23                                                                                                           |
| System-Only            | Faux                                                                                                            |
| Est de valeur unique       | Vrai                                                                                                             |
| Est indexé             | Faux                                                                                                            |
| Dans le catalogue global      | Faux                                                                                                            |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                                                                                     |
| Range-Lower            | 1                                                                                                                |
| Range-Upper            | 64                                                                                                               |
| Search-Flags           | 0x00000000                                                                                                       |
| System-Flags           | 0x00000010                                                                                                       |
| Classes utilisées dans        | [**Organisation**](c-organization.md)<br/> [**Unité d’organisation**](c-organizationalunit.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrée | Valeur |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID de lien                | \-                                                                                                                                                                                                                                                                                                                                                                      |
| MAPI-Id                | 0x3A23                                                                                                                                                                                                                                                                                                                                                                  |
| System-Only            | Faux                                                                                                                                                                                                                                                                                                                                                                   |
| Est de valeur unique       | Vrai                                                                                                                                                                                                                                                                                                                                                                    |
| Est indexé             | Faux                                                                                                                                                                                                                                                                                                                                                                   |
| Dans le catalogue global      | Faux                                                                                                                                                                                                                                                                                                                                                                   |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                                                                                                                                                                                                                                                                                                                                            |
| Range-Lower            | 1                                                                                                                                                                                                                                                                                                                                                                       |
| Range-Upper            | 64                                                                                                                                                                                                                                                                                                                                                                      |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                                                                                                                                                              |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                              |
| Classes utilisées dans        | [**Organisation**](c-organization.md)<br/> [**Organizational-Person**](c-organizationalperson.md)<br/> [**Rôle organisationnel**](c-organizationalrole.md)<br/> [**Unité d’organisation**](c-organizationalunit.md)<br/> [**Personne privée**](c-residentialperson.md)<br/> [**rFC822LocalPart**](c-rfc822localpart.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrée | Valeur |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID de lien                | \-                                                                                                                                                                                                                                                                                                                                                                      |
| MAPI-Id                | 0x3A23                                                                                                                                                                                                                                                                                                                                                                  |
| System-Only            | Faux                                                                                                                                                                                                                                                                                                                                                                   |
| Est de valeur unique       | Vrai                                                                                                                                                                                                                                                                                                                                                                    |
| Est indexé             | Faux                                                                                                                                                                                                                                                                                                                                                                   |
| Dans le catalogue global      | Faux                                                                                                                                                                                                                                                                                                                                                                   |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                                                                                                                                                                                                                                                                                                                                            |
| Range-Lower            | 1                                                                                                                                                                                                                                                                                                                                                                       |
| Range-Upper            | 64                                                                                                                                                                                                                                                                                                                                                                      |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                                                                                                                                                              |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                              |
| Classes utilisées dans        | [**Organisation**](c-organization.md)<br/> [**Organizational-Person**](c-organizationalperson.md)<br/> [**Rôle organisationnel**](c-organizationalrole.md)<br/> [**Unité d’organisation**](c-organizationalunit.md)<br/> [**Personne privée**](c-residentialperson.md)<br/> [**rFC822LocalPart**](c-rfc822localpart.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrée | Valeur |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID de lien                | \-                                                                                                                                                                                                                                                                                                                                                                      |
| MAPI-Id                | 0x3A23                                                                                                                                                                                                                                                                                                                                                                  |
| System-Only            | Faux                                                                                                                                                                                                                                                                                                                                                                   |
| Est de valeur unique       | Vrai                                                                                                                                                                                                                                                                                                                                                                    |
| Est indexé             | Faux                                                                                                                                                                                                                                                                                                                                                                   |
| Dans le catalogue global      | Faux                                                                                                                                                                                                                                                                                                                                                                   |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                                                                                                                                                                                                                                                                                                                                            |
| Range-Lower            | 1                                                                                                                                                                                                                                                                                                                                                                       |
| Range-Upper            | 64                                                                                                                                                                                                                                                                                                                                                                      |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                                                                                                                                                              |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                              |
| Classes utilisées dans        | [**Organisation**](c-organization.md)<br/> [**Organizational-Person**](c-organizationalperson.md)<br/> [**Rôle organisationnel**](c-organizationalrole.md)<br/> [**Unité d’organisation**](c-organizationalunit.md)<br/> [**Personne privée**](c-residentialperson.md)<br/> [**rFC822LocalPart**](c-rfc822localpart.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrée | Valeur |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID de lien                | \-                                                                                                                                                                                                                                                                                                                                                                      |
| MAPI-Id                | 0x3A23                                                                                                                                                                                                                                                                                                                                                                  |
| System-Only            | Faux                                                                                                                                                                                                                                                                                                                                                                   |
| Est de valeur unique       | Vrai                                                                                                                                                                                                                                                                                                                                                                    |
| Est indexé             | Faux                                                                                                                                                                                                                                                                                                                                                                   |
| Dans le catalogue global      | Faux                                                                                                                                                                                                                                                                                                                                                                   |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                                                                                                                                                                                                                                                                                                                                            |
| Range-Lower            | 1                                                                                                                                                                                                                                                                                                                                                                       |
| Range-Upper            | 64                                                                                                                                                                                                                                                                                                                                                                      |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                                                                                                                                                              |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                              |
| Classes utilisées dans        | [**Organisation**](c-organization.md)<br/> [**Organizational-Person**](c-organizationalperson.md)<br/> [**Rôle organisationnel**](c-organizationalrole.md)<br/> [**Unité d’organisation**](c-organizationalunit.md)<br/> [**Personne privée**](c-residentialperson.md)<br/> [**rFC822LocalPart**](c-rfc822localpart.md)<br/> |



 

 





