---
title: Attribut Last-Logon
description: La dernière fois que l’utilisateur a ouvert une session.
ms.assetid: 271f4f38-90f9-4add-a3ed-413c224e1fae
ms.tgt_platform: multiple
keywords:
- Schéma AD d’attribut Last-Logon
- Schéma AD de l’attribut lastLogon
topic_type:
- apiref
api_name:
- Last-Logon
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ae01ffabf2d4862c030607b997a4d9057b934f8f
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "103845234"
---
# <a name="last-logon-attribute"></a>Attribut Last-Logon

La dernière fois que l’utilisateur a ouvert une session. Cette valeur est stockée sous la forme d’un grand entier qui représente le nombre d’intervalles de 100 nanosecondes depuis le 1er janvier 1601 (UTC). La valeur zéro signifie que l’heure de la dernière connexion est inconnue.



| Entrée | Valeur |
|-------------------|--------------------------------------|
| CN                | Last-Logon                           |
| LDAP-Display-Name | lastLogon                            |
| Taille              | 8 octets                              |
| Mettre à jour le privilège  | Cette valeur est définie par le système.     |
| Fréquence des mises à jour  | Chaque fois que l’utilisateur ouvre une session.          |
| Attribute-Id      | 1.2.840.113556.1.4.52                |
| System-ID-GUID    | bf967997-0de6-11d0-a285-00aa003049e2 |
| Syntaxe            | [**Défini**](s-interval.md)       |



## <a name="implementations"></a>Implémentations

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
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
| Search-Flags           | 0x00000000                        |
| System-Flags           | 0x00000011                        |
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
| Search-Flags           | 0x00000000                        |
| System-Flags           | 0x00000011                        |
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
| Search-Flags           | 0x00000000                        |
| System-Flags           | 0x00000011                        |
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
| Search-Flags           | 0x00000000                        |
| System-Flags           | 0x00000011                        |
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
| Search-Flags           | 0x00000000                        |
| System-Flags           | 0x00000011                        |
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
| Search-Flags           | 0x00000000                        |
| System-Flags           | 0x00000011                        |
| Classes utilisées dans        | [**Utilisateur**](c-user.md)<br/> |



## <a name="remarks"></a>Notes

La partie haute de ce grand entier correspond au membre **dwHighDateTime** de la structure [**fileTime**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime) et la partie inférieure correspond au membre **dwLowDateTime** de la structure **fileTime** .

Cet attribut n’est pas répliqué et est conservé séparément sur chaque contrôleur de domaine du domaine. Pour obtenir une valeur précise pour la dernière ouverture de session de l’utilisateur dans le domaine, l’attribut **Last-Logon** de l’utilisateur doit être récupéré à partir de chaque contrôleur de domaine du domaine. La valeur la plus élevée Récupérée est l’heure de la dernière ouverture de session pour cet utilisateur.

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime)
</dt> </dl>

 

