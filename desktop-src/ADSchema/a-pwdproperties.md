---
title: Attribut Pwd-Properties
description: Propriétés de mot de passe. Partie de la stratégie de domaine. Un champ de valeur pour indiquer la complexité et les restrictions de stockage.
ms.assetid: 9d73595f-508f-4562-a928-4833df977ab3
ms.tgt_platform: multiple
keywords:
- Schéma AD d’attribut Pwd-Properties
- Schéma AD de l’attribut pwdProperties
topic_type:
- apiref
api_name:
- Pwd-Properties
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7d8338e1bb8279aa5b80e5edaa536c6a246e4912
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "103943106"
---
# <a name="pwd-properties-attribute"></a>Attribut Pwd-Properties

Propriétés de mot de passe. Partie de la stratégie de domaine. Un champ de valeur pour indiquer la complexité et les restrictions de stockage.



| Entrée | Valeur |
|-------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| CN                | Pwd-Properties                                                                                                                                                                                                           |
| LDAP-Display-Name | pwdProperties                                                                                                                                                                                                            |
| Taille              | Entier. \_Mot de passe de domaine \_ complexe 1, \_ mot de passe de domaine \_ aucune \_ \_ modification anonyme 2, \_ mot de passe de domaine \_ sans \_ \_ modification nette 4, \_ administrateurs de verrouillage de domaine \_ 8, \_ Banque de mots de passe de domaine \_ \_ en clair 16, \_ \_ 32 modification du mot de passe du refus de domaine \_ |
| Mettre à jour le privilège  | Administrateur de domaine                                                                                                                                                                                                     |
| Fréquence des mises à jour  | Lorsque la stratégie d’un utilisateur change.                                                                                                                                                                                      |
| Attribute-Id      | 1.2.840.113556.1.4.93                                                                                                                                                                                                    |
| System-ID-GUID    | bf967a0b-0de6-11d0-a285-00aa003049e2                                                                                                                                                                                     |
| Syntaxe            | [**Enumeration**](s-enumeration.md)                                                                                                                                                                                     |



## <a name="implementations"></a>Implémentations

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server



| Entrée | Valeur |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID de lien                | \-                                                                                                                                                    |
| MAPI-Id                | \-                                                                                                                                                    |
| System-Only            | Faux                                                                                                                                                 |
| Est de valeur unique       | Vrai                                                                                                                                                  |
| Est indexé             | Faux                                                                                                                                                 |
| Dans le catalogue global      | Faux                                                                                                                                                 |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                                                                                                                          |
| Range-Lower            | \-                                                                                                                                                    |
| Range-Upper            | \-                                                                                                                                                    |
| Search-Flags           | 0x00000000                                                                                                                                            |
| System-Flags           | 0x00000010                                                                                                                                            |
| Classes utilisées dans        | [**Stratégie de domaine**](c-domainpolicy.md)<br/> [**Sam-domaine**](c-samdomain.md)<br/> [**Sam-domaine-base**](c-samdomainbase.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Entrée | Valeur |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID de lien                | \-                                                                                                                                                    |
| MAPI-Id                | \-                                                                                                                                                    |
| System-Only            | Faux                                                                                                                                                 |
| Est de valeur unique       | Vrai                                                                                                                                                  |
| Est indexé             | Faux                                                                                                                                                 |
| Dans le catalogue global      | Faux                                                                                                                                                 |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                                                                                                                          |
| Range-Lower            | \-                                                                                                                                                    |
| Range-Upper            | \-                                                                                                                                                    |
| Search-Flags           | 0x00000000                                                                                                                                            |
| System-Flags           | 0x00000010                                                                                                                                            |
| Classes utilisées dans        | [**Stratégie de domaine**](c-domainpolicy.md)<br/> [**Sam-domaine**](c-samdomain.md)<br/> [**Sam-domaine-base**](c-samdomainbase.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrée | Valeur |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID de lien                | \-                                                                                                                                                    |
| MAPI-Id                | \-                                                                                                                                                    |
| System-Only            | Faux                                                                                                                                                 |
| Est de valeur unique       | Vrai                                                                                                                                                  |
| Est indexé             | Faux                                                                                                                                                 |
| Dans le catalogue global      | Faux                                                                                                                                                 |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                                                                                                                          |
| Range-Lower            | \-                                                                                                                                                    |
| Range-Upper            | \-                                                                                                                                                    |
| Search-Flags           | 0x00000000                                                                                                                                            |
| System-Flags           | 0x00000010                                                                                                                                            |
| Classes utilisées dans        | [**Stratégie de domaine**](c-domainpolicy.md)<br/> [**Sam-domaine**](c-samdomain.md)<br/> [**Sam-domaine-base**](c-samdomainbase.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrée | Valeur |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID de lien                | \-                                                                                                                                                    |
| MAPI-Id                | \-                                                                                                                                                    |
| System-Only            | Faux                                                                                                                                                 |
| Est de valeur unique       | Vrai                                                                                                                                                  |
| Est indexé             | Faux                                                                                                                                                 |
| Dans le catalogue global      | Faux                                                                                                                                                 |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                                                                                                                          |
| Range-Lower            | \-                                                                                                                                                    |
| Range-Upper            | \-                                                                                                                                                    |
| Search-Flags           | 0x00000000                                                                                                                                            |
| System-Flags           | 0x00000010                                                                                                                                            |
| Classes utilisées dans        | [**Stratégie de domaine**](c-domainpolicy.md)<br/> [**Sam-domaine**](c-samdomain.md)<br/> [**Sam-domaine-base**](c-samdomainbase.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrée | Valeur |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID de lien                | \-                                                                                                                                                    |
| MAPI-Id                | \-                                                                                                                                                    |
| System-Only            | Faux                                                                                                                                                 |
| Est de valeur unique       | Vrai                                                                                                                                                  |
| Est indexé             | Faux                                                                                                                                                 |
| Dans le catalogue global      | Faux                                                                                                                                                 |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                                                                                                                          |
| Range-Lower            | \-                                                                                                                                                    |
| Range-Upper            | \-                                                                                                                                                    |
| Search-Flags           | 0x00000000                                                                                                                                            |
| System-Flags           | 0x00000010                                                                                                                                            |
| Classes utilisées dans        | [**Stratégie de domaine**](c-domainpolicy.md)<br/> [**Sam-domaine**](c-samdomain.md)<br/> [**Sam-domaine-base**](c-samdomainbase.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrée | Valeur |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID de lien                | \-                                                                                                                                                    |
| MAPI-Id                | \-                                                                                                                                                    |
| System-Only            | Faux                                                                                                                                                 |
| Est de valeur unique       | Vrai                                                                                                                                                  |
| Est indexé             | Faux                                                                                                                                                 |
| Dans le catalogue global      | Faux                                                                                                                                                 |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                                                                                                                          |
| Range-Lower            | \-                                                                                                                                                    |
| Range-Upper            | \-                                                                                                                                                    |
| Search-Flags           | 0x00000000                                                                                                                                            |
| System-Flags           | 0x00000010                                                                                                                                            |
| Classes utilisées dans        | [**Stratégie de domaine**](c-domainpolicy.md)<br/> [**Sam-domaine**](c-samdomain.md)<br/> [**Sam-domaine-base**](c-samdomainbase.md)<br/> |



 

 





