---
title: Attribut Country-Code
description: Spécifie le code de pays/région pour la langue choisie par l’utilisateur. cette valeur n’est pas utilisée par Windows 2000.
ms.assetid: 7011cb76-aa86-4203-bcc4-0136bb11c403
ms.tgt_platform: multiple
keywords:
- Schéma AD d’attribut Country-Code
- Schéma AD de l’attribut countryCode
topic_type:
- apiref
api_name:
- Country-Code
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7843a2724043e504538ad6388e92dfc205463e76e082c266b5ee1f4f095207ac
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118961778"
---
# <a name="country-code-attribute"></a>Attribut Country-Code

Spécifie le code de pays/région pour la langue choisie par l’utilisateur. cette valeur n’est pas utilisée par Windows 2000.



| Entrée | Valeur |
|-------------------|-----------------------------------------|
| CN                | Country-Code                            |
| LDAP-Display-Name | countryCode                             |
| Taille              | 2 octets                                 |
| Mettre à jour le privilège  | Propriétaire du compte ou administrateur de domaine   |
| Fréquence des mises à jour  | Lorsque le pays ou la région de l’utilisateur change. |
| Attribute-Id      | 1.2.840.113556.1.4.25                   |
| System-ID-GUID    | 5fd42471-1262-11d0-a060-00aa006c33ed    |
| Syntaxe            | [**Énumération**](s-enumeration.md)    |



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
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| ID de lien                | \-                                                                                                                                |
| MAPI-Id                | \-                                                                                                                                |
| System-Only            | Faux                                                                                                                             |
| Est de valeur unique       | Vrai                                                                                                                              |
| Est indexé             | Faux                                                                                                                             |
| Dans le catalogue global      | Faux                                                                                                                             |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                                                                                                      |
| Range-Lower            | \-                                                                                                                                |
| Range-Upper            | \-                                                                                                                                |
| Search-Flags           | 0x00000010                                                                                                                        |
| System-Flags           | 0x00000010                                                                                                                        |
| Classes utilisées dans        | [**Organizational-Person**](c-organizationalperson.md)<br/> [**Unité d’organisation**](c-organizationalunit.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Entrée | Valeur |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| ID de lien                | \-                                                                                                                                |
| MAPI-Id                | \-                                                                                                                                |
| System-Only            | Faux                                                                                                                             |
| Est de valeur unique       | Vrai                                                                                                                              |
| Est indexé             | Faux                                                                                                                             |
| Dans le catalogue global      | Faux                                                                                                                             |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                                                                                                      |
| Range-Lower            | 0                                                                                                                                 |
| Range-Upper            | 65535                                                                                                                             |
| Search-Flags           | 0x00000010                                                                                                                        |
| System-Flags           | 0x00000010                                                                                                                        |
| Classes utilisées dans        | [**Organizational-Person**](c-organizationalperson.md)<br/> [**Unité d’organisation**](c-organizationalunit.md)<br/> |



## <a name="adam"></a>ADAM



| Entrée | Valeur |
|------------------------|----------------------------------------------------------------|
| ID de lien                | \-                                                             |
| MAPI-Id                | \-                                                             |
| System-Only            | Faux                                                          |
| Est de valeur unique       | Vrai                                                           |
| Est indexé             | Faux                                                          |
| Dans le catalogue global      | Faux                                                          |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                                   |
| Range-Lower            | 0                                                              |
| Range-Upper            | 65535                                                          |
| Search-Flags           | 0x00000010                                                     |
| System-Flags           | 0x00000010                                                     |
| Classes utilisées dans        | [**Unité d’organisation**](c-organizationalunit.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrée | Valeur |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| ID de lien                | \-                                                                                                                                |
| MAPI-Id                | \-                                                                                                                                |
| System-Only            | Faux                                                                                                                             |
| Est de valeur unique       | Vrai                                                                                                                              |
| Est indexé             | Faux                                                                                                                             |
| Dans le catalogue global      | Faux                                                                                                                             |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                                                                                                      |
| Range-Lower            | 0                                                                                                                                 |
| Range-Upper            | 65535                                                                                                                             |
| Search-Flags           | 0x00000010                                                                                                                        |
| System-Flags           | 0x00000010                                                                                                                        |
| Classes utilisées dans        | [**Organizational-Person**](c-organizationalperson.md)<br/> [**Unité d’organisation**](c-organizationalunit.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrée | Valeur |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| ID de lien                | \-                                                                                                                                |
| MAPI-Id                | \-                                                                                                                                |
| System-Only            | Faux                                                                                                                             |
| Est de valeur unique       | Vrai                                                                                                                              |
| Est indexé             | Faux                                                                                                                             |
| Dans le catalogue global      | Faux                                                                                                                             |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                                                                                                      |
| Range-Lower            | 0                                                                                                                                 |
| Range-Upper            | 65535                                                                                                                             |
| Search-Flags           | 0x00000010                                                                                                                        |
| System-Flags           | 0x00000010                                                                                                                        |
| Classes utilisées dans        | [**Organizational-Person**](c-organizationalperson.md)<br/> [**Unité d’organisation**](c-organizationalunit.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrée | Valeur |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| ID de lien                | \-                                                                                                                                |
| MAPI-Id                | \-                                                                                                                                |
| System-Only            | Faux                                                                                                                             |
| Est de valeur unique       | Vrai                                                                                                                              |
| Est indexé             | Faux                                                                                                                             |
| Dans le catalogue global      | Faux                                                                                                                             |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                                                                                                      |
| Range-Lower            | 0                                                                                                                                 |
| Range-Upper            | 65535                                                                                                                             |
| Search-Flags           | 0x00000010                                                                                                                        |
| System-Flags           | 0x00000010                                                                                                                        |
| Classes utilisées dans        | [**Organizational-Person**](c-organizationalperson.md)<br/> [**Unité d’organisation**](c-organizationalunit.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrée | Valeur |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| ID de lien                | \-                                                                                                                                |
| MAPI-Id                | \-                                                                                                                                |
| System-Only            | Faux                                                                                                                             |
| Est de valeur unique       | Vrai                                                                                                                              |
| Est indexé             | Faux                                                                                                                             |
| Dans le catalogue global      | Faux                                                                                                                             |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                                                                                                      |
| Range-Lower            | 0                                                                                                                                 |
| Range-Upper            | 65535                                                                                                                             |
| Search-Flags           | 0x00000010                                                                                                                        |
| System-Flags           | 0x00000010                                                                                                                        |
| Classes utilisées dans        | [**Organizational-Person**](c-organizationalperson.md)<br/> [**Unité d’organisation**](c-organizationalunit.md)<br/> |



 

 





