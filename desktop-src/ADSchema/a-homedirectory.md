---
title: Attribut Home-Directory
description: Répertoire de départ du compte.
ms.assetid: 7fd431f2-f2e0-476f-82ed-04f776c234eb
ms.tgt_platform: multiple
keywords:
- Schéma AD d’attribut Home-Directory
- Schéma AD de l’attribut homeDirectory
topic_type:
- apiref
api_name:
- Home-Directory
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b7ef4ef612bfb2e91184d0e442115f712496f8bd788bb441bba7e7caa388031b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119305229"
---
# <a name="home-directory-attribute"></a>Attribut Home-Directory

Répertoire de départ du compte. Si [**le**](a-homedrive.md) lecteur de disque est défini et spécifie une lettre de lecteur, **HomeDirectory** doit être un chemin d’accès UNC. Sinon, **HomeDirectory** est un chemin d’accès local complet incluant la lettre de lecteur (par exemple, *DriveLetter ***: \\**_Directory_* _\\_ * _Folder_). Cette valeur peut être une chaîne NULL.



| Entrée | Valeur |
|-------------------|------------------------------------------------------------------------------------|
| CN                | Home-Directory                                                                     |
| LDAP-Display-Name | homeDirectory                                                                      |
| Taille              | \-                                                                                 |
| Mettre à jour le privilège  | Administrateur de domaine                                                               |
| Fréquence des mises à jour  | Lorsque l’enregistrement de l’utilisateur est créé et chaque fois que le répertoire de départ doit être modifié. |
| Attribute-Id      | 1.2.840.113556.1.4.44                                                              |
| System-ID-GUID    | bf967985-0de6-11d0-a285-00aa003049e2                                               |
| Syntaxe            | [**String(Unicode)**](s-string-unicode.md)                                        |



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
|------------------------|-------------------------------------------------------------------------------------|
| ID de lien                | \-                                                                                  |
| MAPI-Id                | \-                                                                                  |
| System-Only            | Faux                                                                               |
| Est de valeur unique       | Vrai                                                                                |
| Est indexé             | Faux                                                                               |
| Dans le catalogue global      | Faux                                                                               |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                                                        |
| Range-Lower            | \-                                                                                  |
| Range-Upper            | \-                                                                                  |
| Search-Flags           | 0x00000010                                                                          |
| System-Flags           | 0x00000010                                                                          |
| Classes utilisées dans        | [**Utilisateur**](c-user.md)<br/> [**posixAccount**](c-posixaccount.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrée | Valeur |
|------------------------|-------------------------------------------------------------------------------------|
| ID de lien                | \-                                                                                  |
| MAPI-Id                | \-                                                                                  |
| System-Only            | Faux                                                                               |
| Est de valeur unique       | Vrai                                                                                |
| Est indexé             | Faux                                                                               |
| Dans le catalogue global      | Faux                                                                               |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                                                        |
| Range-Lower            | \-                                                                                  |
| Range-Upper            | \-                                                                                  |
| Search-Flags           | 0x00000010                                                                          |
| System-Flags           | 0x00000010                                                                          |
| Classes utilisées dans        | [**Utilisateur**](c-user.md)<br/> [**posixAccount**](c-posixaccount.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrée | Valeur |
|------------------------|-------------------------------------------------------------------------------------|
| ID de lien                | \-                                                                                  |
| MAPI-Id                | \-                                                                                  |
| System-Only            | Faux                                                                               |
| Est de valeur unique       | Vrai                                                                                |
| Est indexé             | Faux                                                                               |
| Dans le catalogue global      | Faux                                                                               |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                                                        |
| Range-Lower            | \-                                                                                  |
| Range-Upper            | \-                                                                                  |
| Search-Flags           | 0x00000010                                                                          |
| System-Flags           | 0x00000010                                                                          |
| Classes utilisées dans        | [**Utilisateur**](c-user.md)<br/> [**posixAccount**](c-posixaccount.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrée | Valeur |
|------------------------|-------------------------------------------------------------------------------------|
| ID de lien                | \-                                                                                  |
| MAPI-Id                | \-                                                                                  |
| System-Only            | Faux                                                                               |
| Est de valeur unique       | Vrai                                                                                |
| Est indexé             | Faux                                                                               |
| Dans le catalogue global      | Faux                                                                               |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                                                        |
| Range-Lower            | \-                                                                                  |
| Range-Upper            | \-                                                                                  |
| Search-Flags           | 0x00000010                                                                          |
| System-Flags           | 0x00000010                                                                          |
| Classes utilisées dans        | [**Utilisateur**](c-user.md)<br/> [**posixAccount**](c-posixaccount.md)<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**homeDrive**](a-homedrive.md)
</dt> </dl>

 

 





