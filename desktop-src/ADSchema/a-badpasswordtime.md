---
title: Attribut d’heure de mot de passe incorrect
description: Date et heure de la dernière tentative d’ouverture de session sur ce compte avec un mot de passe non valide.
ms.assetid: 8e8c5b73-b42d-4a62-89af-c0ff2fe106d8
ms.tgt_platform: multiple
keywords:
- Schéma AD d’attribut de mot de passe incorrect
- Schéma AD de l’attribut badPasswordTime
topic_type:
- apiref
api_name:
- Bad-Password-Time
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2130e9bf09b70ee96c934027dc8369b8fdb73139396bc1aa1f9f7edffb4d7b7d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119022767"
---
# <a name="bad-password-time-attribute"></a>Attribut d’heure de mot de passe incorrect

Date et heure de la dernière tentative d’ouverture de session sur ce compte avec un mot de passe non valide. Cette valeur est stockée sous la forme d’un grand entier qui représente le nombre d’intervalles de 100 nanosecondes depuis le 1er janvier 1601 (UTC). La valeur zéro signifie que la dernière fois qu’un mot de passe incorrect a été utilisé est inconnu.



| Entrée | Valeur |
|-------------------|-------------------------------------------|
| CN                | Mot de passe incorrect                         |
| LDAP-Display-Name | badPasswordTime                           |
| Taille              | 8 octets                                   |
| Mettre à jour le privilège  | Cette valeur est définie par le système.          |
| Fréquence des mises à jour  | Chaque fois que l’utilisateur entre un mot de passe incorrect. |
| Attribute-Id      | 1.2.840.113556.1.4.49                     |
| System-ID-GUID    | bf96792d-0de6-11d0-a285-00aa003049e2      |
| Syntaxe            | [**Défini**](s-interval.md)            |



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



## <a name="adam"></a>ADAM



| Entrée | Valeur |
|------------------------|-------------------------------------------------------------------|
| ID de lien                | \-                                                                |
| MAPI-Id                | \-                                                                |
| System-Only            | Vrai                                                              |
| Est de valeur unique       | Vrai                                                              |
| Est indexé             | Faux                                                             |
| Dans le catalogue global      | Faux                                                             |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                                      |
| Range-Lower            | \-                                                                |
| Range-Upper            | \-                                                                |
| Search-Flags           | 0x00000000                                                        |
| System-Flags           | 0x00000011                                                        |
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



## <a name="remarks"></a>Remarques

La partie haute de ce grand entier correspond au membre **dwHighDateTime** de la structure [**fileTime**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime) et la partie inférieure correspond au membre **dwLowDateTime** de la structure **fileTime** .

Cet attribut n’est pas répliqué et est conservé séparément sur chaque contrôleur de domaine du domaine. Pour obtenir une valeur précise pour le dernier mot de passe incorrect de l’utilisateur dans le domaine, chaque contrôleur de domaine dans le domaine doit être interrogé. La valeur la plus élevée obtenue représente l’heure réelle du mot de passe incorrect.

 

