---
title: Attribut Manager
description: Contient le nom unique de l’utilisateur qui est le responsable de l’utilisateur. L’objet utilisateur du gestionnaire contient une propriété directReports qui contient des références à tous les objets utilisateur dont les propriétés Manager ont pour valeur ce nom unique.
ms.assetid: 40743784-a99c-4ec0-9140-9f865c073244
ms.tgt_platform: multiple
keywords:
- Schéma Active Directory des attributs du gestionnaire
- Schéma Active Directory des attributs du gestionnaire
topic_type:
- apiref
api_name:
- Manager
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f42c659a436f9798861f5c37df19f8d10db91127
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104385411"
---
# <a name="manager-attribute"></a>Attribut Manager

Contient le nom unique de l’utilisateur qui est le responsable de l’utilisateur. L’objet utilisateur du gestionnaire contient une propriété directReports qui contient des références à tous les objets utilisateur dont les propriétés Manager ont pour valeur ce nom unique.



| Entrée | Valeur |
|-------------------|-----------------------------------------------------------------------------|
| CN                | Manager                                                                     |
| LDAP-Display-Name | manager                                                                     |
| Taille              | \-                                                                          |
| Mettre à jour le privilège  | Administrateur de domaine ou propriétaire du compte.                                      |
| Fréquence des mises à jour  | Lorsque l’enregistrement de l’utilisateur est créé et chaque fois que le gestionnaire doit être modifié. |
| Attribute-Id      | 0.9.2342.19200300.100.1.10                                                  |
| System-ID-GUID    | bf9679b5-0de6-11d0-a285-00aa003049e2                                        |
| Syntaxe            | [**Object(DS-DN)**](s-object-ds-dn.md)                                     |



## <a name="implementations"></a>Implémentations

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server



| Entrée | Valeur |
|------------------------|--------------------------------------------------------------------|
| ID de lien                | 42                                                                 |
| MAPI-Id                | 0x8005                                                             |
| System-Only            | Faux                                                              |
| Est de valeur unique       | Vrai                                                               |
| Est indexé             | Faux                                                              |
| Dans le catalogue global      | Vrai                                                               |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                                       |
| Range-Lower            | \-                                                                 |
| Range-Upper            | \-                                                                 |
| Search-Flags           | 0x00000010                                                         |
| System-Flags           | 0x00000010                                                         |
| Classes utilisées dans        | [**Organizational-Person**](c-organizationalperson.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Entrée | Valeur |
|------------------------|------------------------------------------------------------------------------------------------------------------------|
| ID de lien                | 42                                                                                                                     |
| MAPI-Id                | 0x8005                                                                                                                 |
| System-Only            | Faux                                                                                                                  |
| Est de valeur unique       | Vrai                                                                                                                   |
| Est indexé             | Faux                                                                                                                  |
| Dans le catalogue global      | Vrai                                                                                                                   |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                                                                                           |
| Range-Lower            | \-                                                                                                                     |
| Range-Upper            | \-                                                                                                                     |
| Search-Flags           | 0x00000010                                                                                                             |
| System-Flags           | 0x00000010                                                                                                             |
| Classes utilisées dans        | [**inetOrgPerson**](c-inetorgperson.md)<br/> [**Organizational-Person**](c-organizationalperson.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrée | Valeur |
|------------------------|------------------------------------------------------------------------------------------------------------------------|
| ID de lien                | 42                                                                                                                     |
| MAPI-Id                | 0x8005                                                                                                                 |
| System-Only            | Faux                                                                                                                  |
| Est de valeur unique       | Vrai                                                                                                                   |
| Est indexé             | Faux                                                                                                                  |
| Dans le catalogue global      | Vrai                                                                                                                   |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                                                                                           |
| Range-Lower            | \-                                                                                                                     |
| Range-Upper            | \-                                                                                                                     |
| Search-Flags           | 0x00000010                                                                                                             |
| System-Flags           | 0x00000010                                                                                                             |
| Classes utilisées dans        | [**inetOrgPerson**](c-inetorgperson.md)<br/> [**Organizational-Person**](c-organizationalperson.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrée | Valeur |
|------------------------|------------------------------------------------------------------------------------------------------------------------|
| ID de lien                | 42                                                                                                                     |
| MAPI-Id                | 0x8005                                                                                                                 |
| System-Only            | Faux                                                                                                                  |
| Est de valeur unique       | Vrai                                                                                                                   |
| Est indexé             | Faux                                                                                                                  |
| Dans le catalogue global      | Vrai                                                                                                                   |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                                                                                           |
| Range-Lower            | \-                                                                                                                     |
| Range-Upper            | \-                                                                                                                     |
| Search-Flags           | 0x00000010                                                                                                             |
| System-Flags           | 0x00000010                                                                                                             |
| Classes utilisées dans        | [**inetOrgPerson**](c-inetorgperson.md)<br/> [**Organizational-Person**](c-organizationalperson.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrée | Valeur |
|------------------------|------------------------------------------------------------------------------------------------------------------------|
| ID de lien                | 42                                                                                                                     |
| MAPI-Id                | 0x8005                                                                                                                 |
| System-Only            | Faux                                                                                                                  |
| Est de valeur unique       | Vrai                                                                                                                   |
| Est indexé             | Faux                                                                                                                  |
| Dans le catalogue global      | Vrai                                                                                                                   |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                                                                                           |
| Range-Lower            | \-                                                                                                                     |
| Range-Upper            | \-                                                                                                                     |
| Search-Flags           | 0x00000010                                                                                                             |
| System-Flags           | 0x00000010                                                                                                             |
| Classes utilisées dans        | [**inetOrgPerson**](c-inetorgperson.md)<br/> [**Organizational-Person**](c-organizationalperson.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrée | Valeur |
|------------------------|------------------------------------------------------------------------------------------------------------------------|
| ID de lien                | 42                                                                                                                     |
| MAPI-Id                | 0x8005                                                                                                                 |
| System-Only            | Faux                                                                                                                  |
| Est de valeur unique       | Vrai                                                                                                                   |
| Est indexé             | Faux                                                                                                                  |
| Dans le catalogue global      | Vrai                                                                                                                   |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                                                                                           |
| Range-Lower            | \-                                                                                                                     |
| Range-Upper            | \-                                                                                                                     |
| Search-Flags           | 0x00000010                                                                                                             |
| System-Flags           | 0x00000010                                                                                                             |
| Classes utilisées dans        | [**inetOrgPerson**](c-inetorgperson.md)<br/> [**Organizational-Person**](c-organizationalperson.md)<br/> |



 

 





