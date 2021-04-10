---
title: Attribut Object-Sid
description: Valeur binaire qui spécifie l’identificateur de sécurité (SID) de l’utilisateur. Le SID est une valeur unique utilisée pour identifier l’utilisateur en tant que principal de sécurité.
ms.assetid: 78ef0158-f59e-43df-b3fc-fb0f709936f6
ms.tgt_platform: multiple
keywords:
- Schéma AD d’attribut Object-Sid
- Schéma AD de l’attribut objectSid
topic_type:
- apiref
api_name:
- Object-Sid
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b536650177f873cbbc349096e84c3de274b8d376
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104107638"
---
# <a name="object-sid-attribute"></a>Attribut Object-Sid

Valeur binaire qui spécifie l’identificateur de sécurité (SID) de l’utilisateur. Le SID est une valeur unique utilisée pour identifier l’utilisateur en tant que principal de sécurité.



| Entrée | Valeur |
|-------------------|--------------------------------------------------------------|
| CN                | Object-Sid                                                   |
| LDAP-Display-Name | objectSid                                                    |
| Taille              | \-                                                           |
| Mettre à jour le privilège  | Cette valeur est définie par le système.                             |
| Fréquence des mises à jour  | Cette valeur est définie par le système lors de la création du compte. |
| Attribute-Id      | 1.2.840.113556.1.4.146                                       |
| System-ID-GUID    | bf9679e8-0de6-11d0-a285-00aa003049e2                         |
| Syntaxe            | [**Chaîne (SID)**](s-string-sid.md)                          |



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
|------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID de lien                | \-                                                                                                                                                                                                                                                         |
| MAPI-Id                | 0x8027                                                                                                                                                                                                                                                     |
| System-Only            | Faux                                                                                                                                                                                                                                                      |
| Est de valeur unique       | Vrai                                                                                                                                                                                                                                                       |
| Est indexé             | Vrai                                                                                                                                                                                                                                                       |
| Dans le catalogue global      | Vrai                                                                                                                                                                                                                                                       |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                                                                                                                                                                                                                               |
| Range-Lower            | 0                                                                                                                                                                                                                                                          |
| Range-Upper            | 28                                                                                                                                                                                                                                                         |
| Search-Flags           | 0x00000009                                                                                                                                                                                                                                                 |
| System-Flags           | 0x00000012                                                                                                                                                                                                                                                 |
| Classes utilisées dans        | [**Étranger-sécurité-principal**](c-foreignsecurityprincipal.md)<br/> [**MSMQ-migrated-User**](c-msmqmigrateduser.md)<br/> [**Sam-domaine-base**](c-samdomainbase.md)<br/> [**Sécurité-principal**](c-securityprincipal.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Entrée | Valeur |
|------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID de lien                | \-                                                                                                                                                                                                                                                         |
| MAPI-Id                | 0x8027                                                                                                                                                                                                                                                     |
| System-Only            | Vrai                                                                                                                                                                                                                                                       |
| Est de valeur unique       | Vrai                                                                                                                                                                                                                                                       |
| Est indexé             | Vrai                                                                                                                                                                                                                                                       |
| Dans le catalogue global      | Vrai                                                                                                                                                                                                                                                       |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                                                                                                                                                                                                                               |
| Range-Lower            | 0                                                                                                                                                                                                                                                          |
| Range-Upper            | 28                                                                                                                                                                                                                                                         |
| Search-Flags           | 0x00000009                                                                                                                                                                                                                                                 |
| System-Flags           | 0x00000012                                                                                                                                                                                                                                                 |
| Classes utilisées dans        | [**Étranger-sécurité-principal**](c-foreignsecurityprincipal.md)<br/> [**MSMQ-migrated-User**](c-msmqmigrateduser.md)<br/> [**Sam-domaine-base**](c-samdomainbase.md)<br/> [**Sécurité-principal**](c-securityprincipal.md)<br/> |



## <a name="adam"></a>ADAM



| Entrée | Valeur |
|------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID de lien                | \-                                                                                                                                                                                               |
| MAPI-Id                | 0x8027                                                                                                                                                                                           |
| System-Only            | Vrai                                                                                                                                                                                             |
| Est de valeur unique       | Vrai                                                                                                                                                                                             |
| Est indexé             | Vrai                                                                                                                                                                                             |
| Dans le catalogue global      | Vrai                                                                                                                                                                                             |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                                                                                                                                                                     |
| Range-Lower            | 0                                                                                                                                                                                                |
| Range-Upper            | 28                                                                                                                                                                                               |
| Search-Flags           | 0x00000009                                                                                                                                                                                       |
| System-Flags           | 0x00000012                                                                                                                                                                                       |
| Classes utilisées dans        | [**Étranger-sécurité-principal**](c-foreignsecurityprincipal.md)<br/> [**ms-DS-bind-proxy**](c-msds-bindproxy.md)<br/> [**Sécurité-principal**](c-securityprincipal.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrée | Valeur |
|------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID de lien                | \-                                                                                                                                                                                                                                                         |
| MAPI-Id                | 0x8027                                                                                                                                                                                                                                                     |
| System-Only            | Vrai                                                                                                                                                                                                                                                       |
| Est de valeur unique       | Vrai                                                                                                                                                                                                                                                       |
| Est indexé             | Vrai                                                                                                                                                                                                                                                       |
| Dans le catalogue global      | Vrai                                                                                                                                                                                                                                                       |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                                                                                                                                                                                                                               |
| Range-Lower            | 0                                                                                                                                                                                                                                                          |
| Range-Upper            | 28                                                                                                                                                                                                                                                         |
| Search-Flags           | 0x00000009                                                                                                                                                                                                                                                 |
| System-Flags           | 0x00000012                                                                                                                                                                                                                                                 |
| Classes utilisées dans        | [**Étranger-sécurité-principal**](c-foreignsecurityprincipal.md)<br/> [**MSMQ-migrated-User**](c-msmqmigrateduser.md)<br/> [**Sam-domaine-base**](c-samdomainbase.md)<br/> [**Sécurité-principal**](c-securityprincipal.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrée | Valeur |
|------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID de lien                | \-                                                                                                                                                                                                                                                         |
| MAPI-Id                | 0x8027                                                                                                                                                                                                                                                     |
| System-Only            | Vrai                                                                                                                                                                                                                                                       |
| Est de valeur unique       | Vrai                                                                                                                                                                                                                                                       |
| Est indexé             | Vrai                                                                                                                                                                                                                                                       |
| Dans le catalogue global      | Vrai                                                                                                                                                                                                                                                       |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                                                                                                                                                                                                                               |
| Range-Lower            | 0                                                                                                                                                                                                                                                          |
| Range-Upper            | 28                                                                                                                                                                                                                                                         |
| Search-Flags           | 0x00000009                                                                                                                                                                                                                                                 |
| System-Flags           | 0x00000012                                                                                                                                                                                                                                                 |
| Classes utilisées dans        | [**Étranger-sécurité-principal**](c-foreignsecurityprincipal.md)<br/> [**MSMQ-migrated-User**](c-msmqmigrateduser.md)<br/> [**Sam-domaine-base**](c-samdomainbase.md)<br/> [**Sécurité-principal**](c-securityprincipal.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrée | Valeur |
|------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID de lien                | \-                                                                                                                                                                                                                                                         |
| MAPI-Id                | 0x8027                                                                                                                                                                                                                                                     |
| System-Only            | Vrai                                                                                                                                                                                                                                                       |
| Est de valeur unique       | Vrai                                                                                                                                                                                                                                                       |
| Est indexé             | Vrai                                                                                                                                                                                                                                                       |
| Dans le catalogue global      | Vrai                                                                                                                                                                                                                                                       |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                                                                                                                                                                                                                               |
| Range-Lower            | 0                                                                                                                                                                                                                                                          |
| Range-Upper            | 28                                                                                                                                                                                                                                                         |
| Search-Flags           | 0x00000009                                                                                                                                                                                                                                                 |
| System-Flags           | 0x00000012                                                                                                                                                                                                                                                 |
| Classes utilisées dans        | [**Étranger-sécurité-principal**](c-foreignsecurityprincipal.md)<br/> [**MSMQ-migrated-User**](c-msmqmigrateduser.md)<br/> [**Sam-domaine-base**](c-samdomainbase.md)<br/> [**Sécurité-principal**](c-securityprincipal.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrée | Valeur |
|------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID de lien                | \-                                                                                                                                                                                                                                                         |
| MAPI-Id                | 0x8027                                                                                                                                                                                                                                                     |
| System-Only            | Vrai                                                                                                                                                                                                                                                       |
| Est de valeur unique       | Vrai                                                                                                                                                                                                                                                       |
| Est indexé             | Vrai                                                                                                                                                                                                                                                       |
| Dans le catalogue global      | Vrai                                                                                                                                                                                                                                                       |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                                                                                                                                                                                                                               |
| Range-Lower            | 0                                                                                                                                                                                                                                                          |
| Range-Upper            | 28                                                                                                                                                                                                                                                         |
| Search-Flags           | 0x00000009                                                                                                                                                                                                                                                 |
| System-Flags           | 0x00000012                                                                                                                                                                                                                                                 |
| Classes utilisées dans        | [**Étranger-sécurité-principal**](c-foreignsecurityprincipal.md)<br/> [**MSMQ-migrated-User**](c-msmqmigrateduser.md)<br/> [**Sam-domaine-base**](c-samdomainbase.md)<br/> [**Sécurité-principal**](c-securityprincipal.md)<br/> |



 

 





