---
title: Pwd-Last-Set (attribut)
description: Date et heure de la dernière modification du mot de passe de ce compte.
ms.assetid: 06ca5cd5-a285-488a-9db0-c698b82a847d
ms.tgt_platform: multiple
keywords:
- Pwd-schéma Active Directory de l’attribut Last-Set
- Schéma AD de l’attribut pwdLastSet
topic_type:
- apiref
api_name:
- Pwd-Last-Set
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a43c4ca87523e94c69d575495339d5491b1d650d059fbf2b7ab9a046cad98275
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119837509"
---
# <a name="pwd-last-set-attribute"></a>Pwd-Last-Set (attribut)

Date et heure de la dernière modification du mot de passe de ce compte. Cette valeur est stockée sous la forme d’un grand entier qui représente le nombre d’intervalles de nanosecondes de 100 depuis le 1er janvier 1601 (UTC). Si cette valeur est définie sur 0 et que l’attribut [**User-Account-Control**](a-useraccountcontrol.md) ne contient pas l’indicateur de mot de passe uf ne pas faire **\_ \_ expirer \_** , l’utilisateur doit définir le mot de passe à la prochaine ouverture de session.



| Entrée | Valeur |
|-------------------|--------------------------------------|
| CN                | Pwd-dernier jeu                         |
| LDAP-Display-Name | pwdLastSet                           |
| Taille              | 8 octets                              |
| Mettre à jour le privilège  | Cette valeur est définie par le système.     |
| Fréquence des mises à jour  | Chaque fois que le mot de passe est modifié.   |
| Attribute-Id      | 1.2.840.113556.1.4.96                |
| System-ID-GUID    | bf967a0a-0de6-11d0-a285-00aa003049e2 |
| Syntaxe            | [**Défini**](s-interval.md)       |



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
| Est indexé             | Faux                             |
| Dans le catalogue global      | Faux                             |
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
| System-Only            | Faux                             |
| Est de valeur unique       | Vrai                              |
| Est indexé             | Faux                             |
| Dans le catalogue global      | Faux                             |
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
| System-Only            | Faux                                                             |
| Est de valeur unique       | Vrai                                                              |
| Est indexé             | Faux                                                             |
| Dans le catalogue global      | Faux                                                             |
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
| System-Only            | Faux                             |
| Est de valeur unique       | Vrai                              |
| Est indexé             | Faux                             |
| Dans le catalogue global      | Faux                             |
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
| System-Only            | Faux                             |
| Est de valeur unique       | Vrai                              |
| Est indexé             | Faux                             |
| Dans le catalogue global      | Faux                             |
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
| System-Only            | Faux                             |
| Est de valeur unique       | Vrai                              |
| Est indexé             | Faux                             |
| Dans le catalogue global      | Faux                             |
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
| System-Only            | Faux                             |
| Est de valeur unique       | Vrai                              |
| Est indexé             | Faux                             |
| Dans le catalogue global      | Faux                             |
| Descripteur de sécurité NT | O :BAG : BAD : S :                      |
| Range-Lower            | \-                                |
| Range-Upper            | \-                                |
| Search-Flags           | 0x00000000                        |
| System-Flags           | 0x00000010                        |
| Classes utilisées dans        | [**Utilisateur**](c-user.md)<br/> |



## <a name="remarks"></a>Remarques

La partie haute de ce grand entier correspond au membre **dwHighDateTime** de la structure [**fileTime**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime) et la partie inférieure correspond au membre **dwLowDateTime** de la structure **fileTime** .

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Contrôle de compte d’utilisateur**](a-useraccountcontrol.md)
</dt> </dl>

 

