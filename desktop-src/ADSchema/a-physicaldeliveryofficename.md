---
title: attribut physique-delivery-Office-Name
description: Contient l’emplacement du bureau dans le lieu de travail de l’utilisateur.
ms.assetid: a6be61bf-9a9a-4b97-bdf8-894c173efadd
ms.tgt_platform: multiple
keywords:
- schéma active directory de l’attribut de Office de remise physique
- Schéma AD de l’attribut physicalDeliveryOfficeName
topic_type:
- apiref
api_name:
- Physical-Delivery-Office-Name
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a574c7214f18d9cef46a64885ca2855fdaf3227a9dece159458d5f1cb07d8b7c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119647769"
---
# <a name="physical-delivery-office-name-attribute"></a>attribut physique-delivery-Office-Name

Contient l’emplacement du bureau dans le lieu de travail de l’utilisateur.



| Entrée | Valeur |
|-------------------|-------------------------------------------------------------------------------------|
| CN                | Physical-delivery-Office-Name                                                       |
| LDAP-Display-Name | physicalDeliveryOfficeName                                                          |
| Taille              | \-                                                                                  |
| Mettre à jour le privilège  | Administrateur de domaine ou propriétaire du compte.                                              |
| Fréquence des mises à jour  | Lorsque l’enregistrement de l’utilisateur est créé et chaque fois que l’emplacement du Bureau doit être modifié. |
| Attribute-Id      | 2.5.4.19                                                                            |
| System-ID-GUID    | bf9679f7-0de6-11d0-a285-00aa003049e2                                                |
| Syntaxe            | [**String(Unicode)**](s-string-unicode.md)                                         |



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
| MAPI-Id                | 0x3A19                                                                                                                                                                                                                                                                                                          |
| System-Only            | Faux                                                                                                                                                                                                                                                                                                           |
| Est de valeur unique       | Vrai                                                                                                                                                                                                                                                                                                            |
| Est indexé             | Vrai                                                                                                                                                                                                                                                                                                            |
| Dans le catalogue global      | Faux                                                                                                                                                                                                                                                                                                           |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                                                                                                                                                                                                                                                                                    |
| Range-Lower            | 1                                                                                                                                                                                                                                                                                                               |
| Range-Upper            | 128                                                                                                                                                                                                                                                                                                             |
| Search-Flags           | 0x00000005                                                                                                                                                                                                                                                                                                      |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                      |
| Classes utilisées dans        | [**Organisation**](c-organization.md)<br/> [**Organizational-Person**](c-organizationalperson.md)<br/> [**Rôle organisationnel**](c-organizationalrole.md)<br/> [**Unité d’organisation**](c-organizationalunit.md)<br/> [**Personne privée**](c-residentialperson.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Entrée | Valeur |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID de lien                | \-                                                                                                                                                                                                                                                                                                                                                                      |
| MAPI-Id                | 0x3A19                                                                                                                                                                                                                                                                                                                                                                  |
| System-Only            | Faux                                                                                                                                                                                                                                                                                                                                                                   |
| Est de valeur unique       | Vrai                                                                                                                                                                                                                                                                                                                                                                    |
| Est indexé             | Vrai                                                                                                                                                                                                                                                                                                                                                                    |
| Dans le catalogue global      | Faux                                                                                                                                                                                                                                                                                                                                                                   |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                                                                                                                                                                                                                                                                                                                                            |
| Range-Lower            | 1                                                                                                                                                                                                                                                                                                                                                                       |
| Range-Upper            | 128                                                                                                                                                                                                                                                                                                                                                                     |
| Search-Flags           | 0x00000005                                                                                                                                                                                                                                                                                                                                                              |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                              |
| Classes utilisées dans        | [**Organisation**](c-organization.md)<br/> [**Organizational-Person**](c-organizationalperson.md)<br/> [**Rôle organisationnel**](c-organizationalrole.md)<br/> [**Unité d’organisation**](c-organizationalunit.md)<br/> [**Personne privée**](c-residentialperson.md)<br/> [**rFC822LocalPart**](c-rfc822localpart.md)<br/> |



## <a name="adam"></a>ADAM



| Entrée | Valeur |
|------------------------|------------------------------------------------------------------------------------------------------------------|
| ID de lien                | \-                                                                                                               |
| MAPI-Id                | 0x3A19                                                                                                           |
| System-Only            | Faux                                                                                                            |
| Est de valeur unique       | Vrai                                                                                                             |
| Est indexé             | Vrai                                                                                                             |
| Dans le catalogue global      | Faux                                                                                                            |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                                                                                     |
| Range-Lower            | 1                                                                                                                |
| Range-Upper            | 128                                                                                                              |
| Search-Flags           | 0x00000005                                                                                                       |
| System-Flags           | 0x00000010                                                                                                       |
| Classes utilisées dans        | [**Organisation**](c-organization.md)<br/> [**Unité d’organisation**](c-organizationalunit.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrée | Valeur |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID de lien                | \-                                                                                                                                                                                                                                                                                                                                                                      |
| MAPI-Id                | 0x3A19                                                                                                                                                                                                                                                                                                                                                                  |
| System-Only            | Faux                                                                                                                                                                                                                                                                                                                                                                   |
| Est de valeur unique       | Vrai                                                                                                                                                                                                                                                                                                                                                                    |
| Est indexé             | Vrai                                                                                                                                                                                                                                                                                                                                                                    |
| Dans le catalogue global      | Faux                                                                                                                                                                                                                                                                                                                                                                   |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                                                                                                                                                                                                                                                                                                                                            |
| Range-Lower            | 1                                                                                                                                                                                                                                                                                                                                                                       |
| Range-Upper            | 128                                                                                                                                                                                                                                                                                                                                                                     |
| Search-Flags           | 0x00000005                                                                                                                                                                                                                                                                                                                                                              |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                              |
| Classes utilisées dans        | [**Organisation**](c-organization.md)<br/> [**Organizational-Person**](c-organizationalperson.md)<br/> [**Rôle organisationnel**](c-organizationalrole.md)<br/> [**Unité d’organisation**](c-organizationalunit.md)<br/> [**Personne privée**](c-residentialperson.md)<br/> [**rFC822LocalPart**](c-rfc822localpart.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrée | Valeur |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID de lien                | \-                                                                                                                                                                                                                                                                                                                                                                      |
| MAPI-Id                | 0x3A19                                                                                                                                                                                                                                                                                                                                                                  |
| System-Only            | Faux                                                                                                                                                                                                                                                                                                                                                                   |
| Est de valeur unique       | Vrai                                                                                                                                                                                                                                                                                                                                                                    |
| Est indexé             | Vrai                                                                                                                                                                                                                                                                                                                                                                    |
| Dans le catalogue global      | Faux                                                                                                                                                                                                                                                                                                                                                                   |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                                                                                                                                                                                                                                                                                                                                            |
| Range-Lower            | 1                                                                                                                                                                                                                                                                                                                                                                       |
| Range-Upper            | 128                                                                                                                                                                                                                                                                                                                                                                     |
| Search-Flags           | 0x00000005                                                                                                                                                                                                                                                                                                                                                              |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                              |
| Classes utilisées dans        | [**Organisation**](c-organization.md)<br/> [**Organizational-Person**](c-organizationalperson.md)<br/> [**Rôle organisationnel**](c-organizationalrole.md)<br/> [**Unité d’organisation**](c-organizationalunit.md)<br/> [**Personne privée**](c-residentialperson.md)<br/> [**rFC822LocalPart**](c-rfc822localpart.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrée | Valeur |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID de lien                | \-                                                                                                                                                                                                                                                                                                                                                                      |
| MAPI-Id                | 0x3A19                                                                                                                                                                                                                                                                                                                                                                  |
| System-Only            | Faux                                                                                                                                                                                                                                                                                                                                                                   |
| Est de valeur unique       | Vrai                                                                                                                                                                                                                                                                                                                                                                    |
| Est indexé             | Vrai                                                                                                                                                                                                                                                                                                                                                                    |
| Dans le catalogue global      | Faux                                                                                                                                                                                                                                                                                                                                                                   |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                                                                                                                                                                                                                                                                                                                                            |
| Range-Lower            | 1                                                                                                                                                                                                                                                                                                                                                                       |
| Range-Upper            | 128                                                                                                                                                                                                                                                                                                                                                                     |
| Search-Flags           | 0x00000005                                                                                                                                                                                                                                                                                                                                                              |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                              |
| Classes utilisées dans        | [**Organisation**](c-organization.md)<br/> [**Organizational-Person**](c-organizationalperson.md)<br/> [**Rôle organisationnel**](c-organizationalrole.md)<br/> [**Unité d’organisation**](c-organizationalunit.md)<br/> [**Personne privée**](c-residentialperson.md)<br/> [**rFC822LocalPart**](c-rfc822localpart.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrée | Valeur |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID de lien                | \-                                                                                                                                                                                                                                                                                                                                                                      |
| MAPI-Id                | 0x3A19                                                                                                                                                                                                                                                                                                                                                                  |
| System-Only            | Faux                                                                                                                                                                                                                                                                                                                                                                   |
| Est de valeur unique       | Vrai                                                                                                                                                                                                                                                                                                                                                                    |
| Est indexé             | Vrai                                                                                                                                                                                                                                                                                                                                                                    |
| Dans le catalogue global      | Faux                                                                                                                                                                                                                                                                                                                                                                   |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                                                                                                                                                                                                                                                                                                                                            |
| Range-Lower            | 1                                                                                                                                                                                                                                                                                                                                                                       |
| Range-Upper            | 128                                                                                                                                                                                                                                                                                                                                                                     |
| Search-Flags           | 0x00000005                                                                                                                                                                                                                                                                                                                                                              |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                              |
| Classes utilisées dans        | [**Organisation**](c-organization.md)<br/> [**Organizational-Person**](c-organizationalperson.md)<br/> [**Rôle organisationnel**](c-organizationalrole.md)<br/> [**Unité d’organisation**](c-organizationalunit.md)<br/> [**Personne privée**](c-residentialperson.md)<br/> [**rFC822LocalPart**](c-rfc822localpart.md)<br/> |



 

 





