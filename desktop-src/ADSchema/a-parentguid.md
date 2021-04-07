---
title: Attribut parent-GUID
description: Il s’agit d’un attribut construit, inventé pour prendre en charge le contrôle DirSync. Cet attribut contient l’objectGuid du parent d’un objet lors de la réplication de la création, du changement de nom ou du déplacement d’un objet.
ms.assetid: caf2491b-c0bf-4ea1-80ec-d44cf9307551
ms.tgt_platform: multiple
keywords:
- Schéma AD de l’attribut parent-GUID
- Schéma AD de l’attribut parentGUID
topic_type:
- apiref
api_name:
- Parent-GUID
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 38b01faf958f4add9c7788d630321d7c225f5026
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "103845353"
---
# <a name="parent-guid-attribute"></a>Attribut parent-GUID

Il s’agit d’un attribut construit, inventé pour prendre en charge le contrôle DirSync. Cet attribut contient l’objectGuid du parent d’un objet lors de la réplication de la création, du changement de nom ou du déplacement d’un objet.



| Entrée | Valeur |
|-------------------|-------------------------------------------------------|
| CN                | GUID parent                                           |
| LDAP-Display-Name | parentGUID                                            |
| Taille              | 16 octets                                              |
| Mettre à jour le privilège  | Cette valeur est définie par le système.                      |
| Fréquence des mises à jour  | Pendant la réplication                                    |
| Attribute-Id      | 1.2.840.113556.1.4.1224                               |
| System-ID-GUID    | 2df90d74-009f-11d2-aa4c-00c04fd7d83a                  |
| Syntaxe            | [**Object(Replica-Link)**](s-object-replica-link.md) |



## <a name="implementations"></a>Implémentations

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**ADAM**](#adam)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server



| Entrée | Valeur |
|------------------------|--------------|
| ID de lien                | \-           |
| MAPI-Id                | \-           |
| System-Only            | Vrai         |
| Est de valeur unique       | Vrai         |
| Est indexé             | Faux        |
| Dans le catalogue global      | Faux        |
| Descripteur de sécurité NT | O :BAG : BAD : S : |
| Range-Lower            | \-           |
| Range-Upper            | \-           |
| Search-Flags           | 0x00000000   |
| System-Flags           | 0x08000014   |
| Classes utilisées dans        | \-           |



## <a name="windows-server-2003"></a>Windows Server 2003



| Entrée | Valeur |
|------------------------|--------------|
| ID de lien                | \-           |
| MAPI-Id                | \-           |
| System-Only            | Vrai         |
| Est de valeur unique       | Vrai         |
| Est indexé             | Faux        |
| Dans le catalogue global      | Faux        |
| Descripteur de sécurité NT | O :BAG : BAD : S : |
| Range-Lower            | \-           |
| Range-Upper            | \-           |
| Search-Flags           | 0x00000000   |
| System-Flags           | 0x08000014   |
| Classes utilisées dans        | \-           |



## <a name="adam"></a>ADAM



| Entrée | Valeur |
|------------------------|--------------|
| ID de lien                | \-           |
| MAPI-Id                | \-           |
| System-Only            | Vrai         |
| Est de valeur unique       | Vrai         |
| Est indexé             | Faux        |
| Dans le catalogue global      | Faux        |
| Descripteur de sécurité NT | O :BAG : BAD : S : |
| Range-Lower            | \-           |
| Range-Upper            | \-           |
| Search-Flags           | 0x00000000   |
| System-Flags           | 0x08000014   |
| Classes utilisées dans        | \-           |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrée | Valeur |
|------------------------|--------------|
| ID de lien                | \-           |
| MAPI-Id                | \-           |
| System-Only            | Vrai         |
| Est de valeur unique       | Vrai         |
| Est indexé             | Faux        |
| Dans le catalogue global      | Faux        |
| Descripteur de sécurité NT | O :BAG : BAD : S : |
| Range-Lower            | \-           |
| Range-Upper            | \-           |
| Search-Flags           | 0x00000000   |
| System-Flags           | 0x08000014   |
| Classes utilisées dans        | \-           |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrée | Valeur |
|------------------------|--------------|
| ID de lien                | \-           |
| MAPI-Id                | \-           |
| System-Only            | Vrai         |
| Est de valeur unique       | Vrai         |
| Est indexé             | Faux        |
| Dans le catalogue global      | Faux        |
| Descripteur de sécurité NT | O :BAG : BAD : S : |
| Range-Lower            | \-           |
| Range-Upper            | \-           |
| Search-Flags           | 0x00000000   |
| System-Flags           | 0x08000014   |
| Classes utilisées dans        | \-           |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrée | Valeur |
|------------------------|--------------|
| ID de lien                | \-           |
| MAPI-Id                | \-           |
| System-Only            | Vrai         |
| Est de valeur unique       | Vrai         |
| Est indexé             | Faux        |
| Dans le catalogue global      | Faux        |
| Descripteur de sécurité NT | O :BAG : BAD : S : |
| Range-Lower            | \-           |
| Range-Upper            | \-           |
| Search-Flags           | 0x00000000   |
| System-Flags           | 0x08000014   |
| Classes utilisées dans        | \-           |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrée | Valeur |
|------------------------|--------------|
| ID de lien                | \-           |
| MAPI-Id                | \-           |
| System-Only            | Vrai         |
| Est de valeur unique       | Vrai         |
| Est indexé             | Faux        |
| Dans le catalogue global      | Faux        |
| Descripteur de sécurité NT | O :BAG : BAD : S : |
| Range-Lower            | \-           |
| Range-Upper            | \-           |
| Search-Flags           | 0x00000000   |
| System-Flags           | 0x08000014   |
| Classes utilisées dans        | \-           |



 

 




