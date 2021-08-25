---
title: Attribut Home-Drive
description: Spécifie la lettre de lecteur à laquelle mapper le chemin d’accès UNC spécifié par homeDirectory.
ms.assetid: fa402e14-febf-4ed9-bcc6-a6bfd405068c
ms.tgt_platform: multiple
keywords:
- Schéma AD d’attribut Home-Drive
- Schéma AD de l’attribut homeDrive
topic_type:
- apiref
api_name:
- Home-Drive
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a33e7d31f175f3675da86c56cbd0617fe566c93a95272517eff97f24fac3f53
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119925539"
---
# <a name="home-drive-attribute"></a>Attribut Home-Drive

Spécifie la lettre de lecteur à laquelle mapper le chemin d’accès UNC spécifié par [**HomeDirectory**](a-homedirectory.md). La lettre de lecteur doit être spécifiée sous la forme *LettreLecteur * * * :** où *LettreLecteur* est la lettre du lecteur à mapper. Le *LettreLecteur* doit être une seule lettre majuscule et le signe deux-points ( :) est requis.



| Entrée | Valeur |
|-------------------|-----------------------------------------------------------------------------------|
| CN                | Home-Drive                                                                        |
| LDAP-Display-Name | homeDrive                                                                         |
| Taille              | 2 octets                                                                           |
| Mettre à jour le privilège  | L’administrateur de domaine définit cette valeur.                                         |
| Fréquence des mises à jour  | Lorsque l’enregistrement d’un utilisateur est créé et chaque fois que le lecteur de démarrage doit être modifié. |
| Attribute-Id      | 1.2.840.113556.1.4.45                                                             |
| System-ID-GUID    | bf967986-0de6-11d0-a285-00aa003049e2                                              |
| Syntaxe            | [**String(Unicode)**](s-string-unicode.md)                                       |



## <a name="implementations"></a>Implémentations

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
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
| Est indexé             | Faux                             |
| Dans le catalogue global      | Faux                             |
| Descripteur de sécurité NT | O :BAG : BAD : S :                      |
| Range-Lower            | \-                                |
| Range-Upper            | \-                                |
| Search-Flags           | 0x00000010                        |
| System-Flags           | 0x00000010                        |
| Classes utilisées dans        | [**Utilisateur**](c-user.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Entrée | Valeur |
|------------------------|-----------------------------------|
| ID de lien                | \-                                |
| MAPI-Id                | \-                                |
| System-Only            | Faux                             |
| Est de valeur unique       | Vrai                              |
| Est indexé             | Faux                             |
| Dans le catalogue global      | Faux                             |
| Descripteur de sécurité NT | O :BAG : BAD : S :                      |
| Range-Lower            | \-                                |
| Range-Upper            | \-                                |
| Search-Flags           | 0x00000010                        |
| System-Flags           | 0x00000010                        |
| Classes utilisées dans        | [**Utilisateur**](c-user.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrée | Valeur |
|------------------------|-----------------------------------|
| ID de lien                | \-                                |
| MAPI-Id                | \-                                |
| System-Only            | Faux                             |
| Est de valeur unique       | Vrai                              |
| Est indexé             | Faux                             |
| Dans le catalogue global      | Faux                             |
| Descripteur de sécurité NT | O :BAG : BAD : S :                      |
| Range-Lower            | \-                                |
| Range-Upper            | \-                                |
| Search-Flags           | 0x00000010                        |
| System-Flags           | 0x00000010                        |
| Classes utilisées dans        | [**Utilisateur**](c-user.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrée | Valeur |
|------------------------|-----------------------------------|
| ID de lien                | \-                                |
| MAPI-Id                | \-                                |
| System-Only            | Faux                             |
| Est de valeur unique       | Vrai                              |
| Est indexé             | Faux                             |
| Dans le catalogue global      | Faux                             |
| Descripteur de sécurité NT | O :BAG : BAD : S :                      |
| Range-Lower            | \-                                |
| Range-Upper            | \-                                |
| Search-Flags           | 0x00000010                        |
| System-Flags           | 0x00000010                        |
| Classes utilisées dans        | [**Utilisateur**](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrée | Valeur |
|------------------------|-----------------------------------|
| ID de lien                | \-                                |
| MAPI-Id                | \-                                |
| System-Only            | Faux                             |
| Est de valeur unique       | Vrai                              |
| Est indexé             | Faux                             |
| Dans le catalogue global      | Faux                             |
| Descripteur de sécurité NT | O :BAG : BAD : S :                      |
| Range-Lower            | \-                                |
| Range-Upper            | \-                                |
| Search-Flags           | 0x00000010                        |
| System-Flags           | 0x00000010                        |
| Classes utilisées dans        | [**Utilisateur**](c-user.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrée | Valeur |
|------------------------|-----------------------------------|
| ID de lien                | \-                                |
| MAPI-Id                | \-                                |
| System-Only            | Faux                             |
| Est de valeur unique       | Vrai                              |
| Est indexé             | Faux                             |
| Dans le catalogue global      | Faux                             |
| Descripteur de sécurité NT | O :BAG : BAD : S :                      |
| Range-Lower            | \-                                |
| Range-Upper            | \-                                |
| Search-Flags           | 0x00000010                        |
| System-Flags           | 0x00000010                        |
| Classes utilisées dans        | [**Utilisateur**](c-user.md)<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**homeDirectory**](a-homedirectory.md)
</dt> </dl>

 

 





