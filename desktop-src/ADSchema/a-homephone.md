---
title: Téléphone-page d’hébergement principal
description: Numéro de téléphone principal de l’utilisateur.
ms.assetid: 624d89fd-942c-448d-bd51-7d93954370b1
ms.tgt_platform: multiple
keywords:
- Téléphone-page d’hébergement principal-schéma active directory
- Schéma AD de l’attribut homePhone
topic_type:
- apiref
api_name:
- Phone-Home-Primary
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 321ba35912db00e8b33f840d73cd68010166c7e38a19e6b6a43e64bc886a8496
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118176708"
---
# <a name="phone-home-primary-attribute"></a>Téléphone-page d’hébergement principal

Numéro de téléphone principal de l’utilisateur.



| Entrée | Valeur |
|-------------------|----------------------------------------------------------------------------------|
| CN                | Téléphone-page d’hébergement principal                                                               |
| LDAP-Display-Name | homePhone                                                                        |
| Taille              | \-                                                                               |
| Mettre à jour le privilège  | Administrateur de domaine ou propriétaire du compte.                                           |
| Fréquence des mises à jour  | Lorsque l’enregistrement de l’utilisateur est créé et chaque fois que le numéro de téléphone doit être modifié. |
| Attribute-Id      | 0.9.2342.19200300.100.1.20                                                       |
| System-ID-GUID    | f0f8ffa1-1191-11d0-a060-00aa006c33ed                                             |
| Syntaxe            | [**String(Unicode)**](s-string-unicode.md)                                      |



## <a name="implementations"></a>Implémentations

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server



| Entrée | Valeur |
|------------------------|--------------------------------------------------------------------|
| ID de lien                | \-                                                                 |
| MAPI-Id                | 0x3A09                                                             |
| System-Only            | Faux                                                              |
| Est de valeur unique       | Vrai                                                               |
| Est indexé             | Faux                                                              |
| Dans le catalogue global      | Vrai                                                               |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                                       |
| Range-Lower            | 1                                                                  |
| Range-Upper            | 64                                                                 |
| Search-Flags           | 0x00000000                                                         |
| System-Flags           | 0x00000010                                                         |
| Classes utilisées dans        | [**Organizational-Person**](c-organizationalperson.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Entrée | Valeur |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID de lien                | \-                                                                                                                                                       |
| MAPI-Id                | 0x3A09                                                                                                                                                   |
| System-Only            | Faux                                                                                                                                                    |
| Est de valeur unique       | Vrai                                                                                                                                                     |
| Est indexé             | Faux                                                                                                                                                    |
| Dans le catalogue global      | Vrai                                                                                                                                                     |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                                                                                                                             |
| Range-Lower            | 1                                                                                                                                                        |
| Range-Upper            | 64                                                                                                                                                       |
| Search-Flags           | 0x00000000                                                                                                                                               |
| System-Flags           | 0x00000010                                                                                                                                               |
| Classes utilisées dans        | [**inetOrgPerson**](c-inetorgperson.md)<br/> [**Organizational-Person**](c-organizationalperson.md)<br/> [**Utilisateur**](c-user.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrée | Valeur |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID de lien                | \-                                                                                                                                                       |
| MAPI-Id                | 0x3A09                                                                                                                                                   |
| System-Only            | Faux                                                                                                                                                    |
| Est de valeur unique       | Vrai                                                                                                                                                     |
| Est indexé             | Faux                                                                                                                                                    |
| Dans le catalogue global      | Vrai                                                                                                                                                     |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                                                                                                                             |
| Range-Lower            | 1                                                                                                                                                        |
| Range-Upper            | 64                                                                                                                                                       |
| Search-Flags           | 0x00000000                                                                                                                                               |
| System-Flags           | 0x00000010                                                                                                                                               |
| Classes utilisées dans        | [**inetOrgPerson**](c-inetorgperson.md)<br/> [**Organizational-Person**](c-organizationalperson.md)<br/> [**Utilisateur**](c-user.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrée | Valeur |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID de lien                | \-                                                                                                                                                       |
| MAPI-Id                | 0x3A09                                                                                                                                                   |
| System-Only            | Faux                                                                                                                                                    |
| Est de valeur unique       | Vrai                                                                                                                                                     |
| Est indexé             | Faux                                                                                                                                                    |
| Dans le catalogue global      | Vrai                                                                                                                                                     |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                                                                                                                             |
| Range-Lower            | 1                                                                                                                                                        |
| Range-Upper            | 64                                                                                                                                                       |
| Search-Flags           | 0x00000000                                                                                                                                               |
| System-Flags           | 0x00000010                                                                                                                                               |
| Classes utilisées dans        | [**inetOrgPerson**](c-inetorgperson.md)<br/> [**Organizational-Person**](c-organizationalperson.md)<br/> [**Utilisateur**](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrée | Valeur |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID de lien                | \-                                                                                                                                                       |
| MAPI-Id                | 0x3A09                                                                                                                                                   |
| System-Only            | Faux                                                                                                                                                    |
| Est de valeur unique       | Vrai                                                                                                                                                     |
| Est indexé             | Faux                                                                                                                                                    |
| Dans le catalogue global      | Vrai                                                                                                                                                     |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                                                                                                                             |
| Range-Lower            | 1                                                                                                                                                        |
| Range-Upper            | 64                                                                                                                                                       |
| Search-Flags           | 0x00000000                                                                                                                                               |
| System-Flags           | 0x00000010                                                                                                                                               |
| Classes utilisées dans        | [**inetOrgPerson**](c-inetorgperson.md)<br/> [**Organizational-Person**](c-organizationalperson.md)<br/> [**Utilisateur**](c-user.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrée | Valeur |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID de lien                | \-                                                                                                                                                       |
| MAPI-Id                | 0x3A09                                                                                                                                                   |
| System-Only            | Faux                                                                                                                                                    |
| Est de valeur unique       | Vrai                                                                                                                                                     |
| Est indexé             | Faux                                                                                                                                                    |
| Dans le catalogue global      | Vrai                                                                                                                                                     |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                                                                                                                             |
| Range-Lower            | 1                                                                                                                                                        |
| Range-Upper            | 64                                                                                                                                                       |
| Search-Flags           | 0x00000000                                                                                                                                               |
| System-Flags           | 0x00000010                                                                                                                                               |
| Classes utilisées dans        | [**inetOrgPerson**](c-inetorgperson.md)<br/> [**Organizational-Person**](c-organizationalperson.md)<br/> [**Utilisateur**](c-user.md)<br/> |



 

 





