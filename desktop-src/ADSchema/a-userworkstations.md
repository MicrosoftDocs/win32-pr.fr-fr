---
title: Attribut User-Workstations
description: Contient les noms NetBIOS ou DNS des ordinateurs exécutant Windows NT Workstation ou Windows 2000 professionnel à partir desquels l’utilisateur peut ouvrir une session.
ms.assetid: 92af070b-dadd-404d-8305-d85974639958
ms.tgt_platform: multiple
keywords:
- Schéma AD d’attribut User-Workstations
- Schéma AD de l’attribut userWorkstations
topic_type:
- apiref
api_name:
- User-Workstations
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3cad59905dbf24c8baa13969d9a2ce5452767163
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "103844890"
---
# <a name="user-workstations-attribute"></a>Attribut User-Workstations

Contient les noms NetBIOS ou DNS des ordinateurs exécutant Windows NT Workstation ou Windows 2000 professionnel à partir desquels l’utilisateur peut ouvrir une session. Chaque nom NetBIOS est séparé par une virgule. Les noms multiples doivent être séparés par des virgules.

>[!Note]
>Cet attribut utilisateur ne doit plus être utilisé. Pour gérer les comptes qui peuvent ouvrir une session sur les stations de travail, nous vous recommandons d’utiliser les fonctionnalités « permettre l’ouverture d’une session locale » et « interdire l’ouverture d’une session locale » ou « autoriser l’ouverture d’une session via le Services Bureau à distance » et « interdire l’ouverture d’une session via Services Bureau à distance ».

| Entrée | Valeur |
|-------------------|--------------------------------------------------------------------------------------------|
| CN                | User-Workstations                                                                          |
| LDAP-Display-Name | userWorkstations                                                                           |
| Taille              | \-                                                                                         |
| Mettre à jour le privilège  | Administrateur de domaine ou propriétaire du compte.                                                     |
| Fréquence des mises à jour  | Lorsque l’enregistrement de l’utilisateur est créé et chaque fois que le privilège de connexion de l’utilisateur doit être modifié. |
| Attribute-Id      | 1.2.840.113556.1.4.86                                                                      |
| System-ID-GUID    | bf9679d7-0de6-11d0-a285-00aa003049e2                                                       |
| Syntaxe            | [**String(Unicode)**](s-string-unicode.md)                                                |



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
| Range-Lower            | 0                                 |
| Range-Upper            | 1 024                              |
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
| Range-Lower            | 0                                 |
| Range-Upper            | 1 024                              |
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
| Range-Lower            | 0                                 |
| Range-Upper            | 1 024                              |
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
| Range-Lower            | 0                                 |
| Range-Upper            | 1 024                              |
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
| Range-Lower            | 0                                 |
| Range-Upper            | 1 024                              |
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
| Range-Lower            | 0                                 |
| Range-Upper            | 1 024                              |
| Search-Flags           | 0x00000010                        |
| System-Flags           | 0x00000010                        |
| Classes utilisées dans        | [**Utilisateur**](c-user.md)<br/> |



 

 





