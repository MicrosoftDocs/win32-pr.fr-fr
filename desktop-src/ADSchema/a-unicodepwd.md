---
title: Attribut Unicode-Pwd
description: Mot de passe de l’utilisateur dans Windows format à sens unique NT (OWF). Windows 2000 utilise le Windows NT OWF. Cette propriété est utilisée uniquement par le système d’exploitation. Notez que vous ne pouvez pas dériver le mot de passe en clair à partir de la forme OWF du mot de passe.
ms.assetid: 07b29a0c-aff2-4abd-8ca8-95f1ce5b566b
ms.tgt_platform: multiple
keywords:
- Schéma AD d’attribut Unicode-Pwd
- attribut unicodePwd schéma AD
topic_type:
- apiref
api_name:
- Unicode-Pwd
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0e21929cf41b58688f768ada0b608ca3ef0892a4a54043c30f5cac2d5a72258b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118681086"
---
# <a name="unicode-pwd-attribute"></a>Attribut Unicode-Pwd

Mot de passe de l’utilisateur dans Windows format à sens unique NT (OWF). Windows 2000 utilise le Windows NT OWF. Cette propriété est utilisée uniquement par le système d’exploitation. Notez que vous ne pouvez pas dériver le mot de passe en clair à partir de la forme OWF du mot de passe.



| Entrée | Valeur |
|-------------------|------------------------------------------------------------------------------|
| CN                | Unicode-Pwd                                                                  |
| LDAP-Display-Name | unicodePwd                                                                   |
| Taille              | \-                                                                           |
| Mettre à jour le privilège  | Administrateur de domaine ou propriétaire du compte.                                       |
| Fréquence des mises à jour  | Lorsque l’enregistrement de l’utilisateur est créé et chaque fois que le mot de passe doit être modifié. |
| Attribute-Id      | 1.2.840.113556.1.4.90                                                        |
| System-ID-GUID    | bf9679e1-0de6-11d0-a285-00aa003049e2                                         |
| Syntaxe            | [**Object(Replica-Link)**](s-object-replica-link.md)                        |



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
| System-Only            | False                             |
| Est de valeur unique       | True                              |
| Est indexé             | False                             |
| Dans le catalogue global      | False                             |
| Descripteur de sécurité NT | O :BAG : BAD : S :                      |
| Range-Lower            | \-                                |
| Range-Upper            | \-                                |
| Search-Flags           | 0x00000000                        |
| System-Flags           | 0x00000010                        |
| Classes utilisées dans        | [**Utilisateur**](c-user.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Entrée | Valeur |
|------------------------|-----------------------------------|
| ID de lien                | \-                                |
| MAPI-Id                | \-                                |
| System-Only            | False                             |
| Est de valeur unique       | True                              |
| Est indexé             | False                             |
| Dans le catalogue global      | False                             |
| Descripteur de sécurité NT | O :BAG : BAD : S :                      |
| Range-Lower            | \-                                |
| Range-Upper            | \-                                |
| Search-Flags           | 0x00000000                        |
| System-Flags           | 0x00000010                        |
| Classes utilisées dans        | [**Utilisateur**](c-user.md)<br/> |



## <a name="adam"></a>ADAM



| Entrée | Valeur |
|------------------------|-------------------------------------------------------------------|
| ID de lien                | \-                                                                |
| MAPI-Id                | \-                                                                |
| System-Only            | False                                                             |
| Est de valeur unique       | True                                                              |
| Est indexé             | False                                                             |
| Dans le catalogue global      | False                                                             |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                                      |
| Range-Lower            | \-                                                                |
| Range-Upper            | \-                                                                |
| Search-Flags           | 0x00000000                                                        |
| System-Flags           | 0x00000010                                                        |
| Classes utilisées dans        | [**ms-DS-Bindable-objet**](c-msds-bindableobject.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrée | Valeur |
|------------------------|-----------------------------------|
| ID de lien                | \-                                |
| MAPI-Id                | \-                                |
| System-Only            | False                             |
| Est de valeur unique       | True                              |
| Est indexé             | False                             |
| Dans le catalogue global      | False                             |
| Descripteur de sécurité NT | O :BAG : BAD : S :                      |
| Range-Lower            | \-                                |
| Range-Upper            | \-                                |
| Search-Flags           | 0x00000000                        |
| System-Flags           | 0x00000010                        |
| Classes utilisées dans        | [**Utilisateur**](c-user.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrée | Valeur |
|------------------------|-----------------------------------|
| ID de lien                | \-                                |
| MAPI-Id                | \-                                |
| System-Only            | False                             |
| Est de valeur unique       | True                              |
| Est indexé             | False                             |
| Dans le catalogue global      | False                             |
| Descripteur de sécurité NT | O :BAG : BAD : S :                      |
| Range-Lower            | \-                                |
| Range-Upper            | \-                                |
| Search-Flags           | 0x00000000                        |
| System-Flags           | 0x00000010                        |
| Classes utilisées dans        | [**Utilisateur**](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrée | Valeur |
|------------------------|-----------------------------------|
| ID de lien                | \-                                |
| MAPI-Id                | \-                                |
| System-Only            | False                             |
| Est de valeur unique       | True                              |
| Est indexé             | False                             |
| Dans le catalogue global      | False                             |
| Descripteur de sécurité NT | O :BAG : BAD : S :                      |
| Range-Lower            | \-                                |
| Range-Upper            | \-                                |
| Search-Flags           | 0x00000000                        |
| System-Flags           | 0x00000010                        |
| Classes utilisées dans        | [**Utilisateur**](c-user.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrée | Valeur |
|------------------------|-----------------------------------|
| ID de lien                | \-                                |
| MAPI-Id                | \-                                |
| System-Only            | False                             |
| Est de valeur unique       | True                              |
| Est indexé             | False                             |
| Dans le catalogue global      | False                             |
| Descripteur de sécurité NT | O :BAG : BAD : S :                      |
| Range-Lower            | \-                                |
| Range-Upper            | \-                                |
| Search-Flags           | 0x00000000                        |
| System-Flags           | 0x00000010                        |
| Classes utilisées dans        | [**Utilisateur**](c-user.md)<br/> |



 

 





