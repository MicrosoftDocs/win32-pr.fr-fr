---
title: Attribut de nom d’utilisateur principal
description: Cet attribut contient l’UPN qui est un nom de connexion de style Internet pour un utilisateur basé sur la norme Internet RFC 822.
ms.assetid: 588e76fa-45b6-4853-821a-9e5730255b9f
ms.tgt_platform: multiple
keywords:
- Schéma Active Directory de l’attribut User-Principal-Name
- Schéma AD de l’attribut userPrincipalName
topic_type:
- apiref
api_name:
- User-Principal-Name
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5ba8ac5196de660c4cff4b90801470581cc660491902ec5b48f0ced8337c498b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119835284"
---
# <a name="user-principal-name-attribute"></a>Attribut de nom d’utilisateur principal

Cet attribut contient l’UPN qui est un nom de connexion de style Internet pour un utilisateur basé sur la norme Internet [RFC 822](https://www.ietf.org/rfc/rfc0822.txt). L’UPN est plus petit que le nom unique et il est plus facile à mémoriser. Par Convention, cette valeur doit correspondre au nom de messagerie de l’utilisateur. La valeur définie pour cet attribut est égale à la longueur de l’ID de l’utilisateur et du nom de domaine. Pour plus d’informations sur cet attribut, consultez [User Naming Attributes](/windows/desktop/AD/naming-properties).



| Entrée | Valeur |
|-------------------|---------------------------------------------|
| CN                | User-Principal-Name                         |
| LDAP-Display-Name | userPrincipalName                           |
| Taille              | \-                                          |
| Mettre à jour le privilège  | Administrateur de domaine ou propriétaire du compte.      |
| Fréquence des mises à jour  | En théorie, cela ne doit jamais changer.         |
| Attribute-Id      | 1.2.840.113556.1.4.656                      |
| System-ID-GUID    | 28630ebb-41d5-11d1-a9c1-0000f80367c1        |
| Syntaxe            | [**String(Unicode)**](s-string-unicode.md) |



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
|------------------------|-----------------------------------|
| ID de lien                | \-                                |
| MAPI-Id                | \-                                |
| System-Only            | Faux                             |
| Est de valeur unique       | Vrai                              |
| Est indexé             | Vrai                              |
| Dans le catalogue global      | Vrai                              |
| Descripteur de sécurité NT | O :BAG : BAD : S :                      |
| Range-Lower            | \-                                |
| Range-Upper            | \-                                |
| Search-Flags           | 0x00000001                        |
| System-Flags           | 0x00000012                        |
| Classes utilisées dans        | [**Utilisateur**](c-user.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Entrée | Valeur |
|------------------------|-----------------------------------|
| ID de lien                | \-                                |
| MAPI-Id                | \-                                |
| System-Only            | Faux                             |
| Est de valeur unique       | Vrai                              |
| Est indexé             | Vrai                              |
| Dans le catalogue global      | Vrai                              |
| Descripteur de sécurité NT | O :BAG : BAD : S :                      |
| Range-Lower            | \-                                |
| Range-Upper            | \-                                |
| Search-Flags           | 0x00000001                        |
| System-Flags           | 0x00000012                        |
| Classes utilisées dans        | [**Utilisateur**](c-user.md)<br/> |



## <a name="adam"></a>ADAM



| Entrée | Valeur |
|------------------------|--------------|
| ID de lien                | \-           |
| MAPI-Id                | \-           |
| System-Only            | Faux        |
| Est de valeur unique       | Vrai         |
| Est indexé             | Vrai         |
| Dans le catalogue global      | Vrai         |
| Descripteur de sécurité NT | O :BAG : BAD : S : |
| Range-Lower            | \-           |
| Range-Upper            | \-           |
| Search-Flags           | 0x00000001   |
| System-Flags           | 0x00000012   |
| Classes utilisées dans        | \-           |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrée | Valeur |
|------------------------|-----------------------------------|
| ID de lien                | \-                                |
| MAPI-Id                | \-                                |
| System-Only            | Faux                             |
| Est de valeur unique       | Vrai                              |
| Est indexé             | Vrai                              |
| Dans le catalogue global      | Vrai                              |
| Descripteur de sécurité NT | O :BAG : BAD : S :                      |
| Range-Lower            | \-                                |
| Range-Upper            | \-                                |
| Search-Flags           | 0x00000001                        |
| System-Flags           | 0x00000012                        |
| Classes utilisées dans        | [**Utilisateur**](c-user.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrée | Valeur |
|------------------------|-----------------------------------|
| ID de lien                | \-                                |
| MAPI-Id                | \-                                |
| System-Only            | Faux                             |
| Est de valeur unique       | Vrai                              |
| Est indexé             | Vrai                              |
| Dans le catalogue global      | Vrai                              |
| Descripteur de sécurité NT | O :BAG : BAD : S :                      |
| Range-Lower            | \-                                |
| Range-Upper            | \-                                |
| Search-Flags           | 0x00000001                        |
| System-Flags           | 0x00000012                        |
| Classes utilisées dans        | [**Utilisateur**](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrée | Valeur |
|------------------------|-----------------------------------|
| ID de lien                | \-                                |
| MAPI-Id                | \-                                |
| System-Only            | Faux                             |
| Est de valeur unique       | Vrai                              |
| Est indexé             | Vrai                              |
| Dans le catalogue global      | Vrai                              |
| Descripteur de sécurité NT | O :BAG : BAD : S :                      |
| Range-Lower            | \-                                |
| Range-Upper            | \-                                |
| Search-Flags           | 0x00000001                        |
| System-Flags           | 0x00000012                        |
| Classes utilisées dans        | [**Utilisateur**](c-user.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrée | Valeur |
|------------------------|-----------------------------------|
| ID de lien                | \-                                |
| MAPI-Id                | \-                                |
| System-Only            | Faux                             |
| Est de valeur unique       | Vrai                              |
| Est indexé             | Vrai                              |
| Dans le catalogue global      | Vrai                              |
| Descripteur de sécurité NT | O :BAG : BAD : S :                      |
| Range-Lower            | \-                                |
| Range-Upper            | \-                                |
| Search-Flags           | 0x00000001                        |
| System-Flags           | 0x00000012                        |
| Classes utilisées dans        | [**Utilisateur**](c-user.md)<br/> |



## <a name="remarks"></a>Remarques

Dans ADAM, cet attribut ne doit pas être au format standard Internet RFC 822. Il peut s’agir d’un nom simple.

 

