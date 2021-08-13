---
title: Attribut Trust-Type
description: Le type d’approbation, par exemple, Windows NT ou MIT.
ms.assetid: ad3640cd-d634-4ec1-8be8-1fb8272e4b23
ms.tgt_platform: multiple
keywords:
- Schéma AD d’attribut Trust-Type
- Schéma AD de l’attribut trustType
topic_type:
- apiref
api_name:
- Trust-Type
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 94e3591117bb9ae89c0845aae41450812918d3dc3c88e6e31c3f4189f46ef8c9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118681604"
---
# <a name="trust-type-attribute"></a>Attribut Trust-Type

Le type d’approbation, par exemple, Windows NT ou MIT.



| Entrée | Valeur |
|-------------------|--------------------------------------|
| CN                | Trust-Type                           |
| LDAP-Display-Name | trustType                            |
| Taille              | 4 octets                              |
| Mettre à jour le privilège  | Cette valeur est définie par le système.     |
| Fréquence des mises à jour  | Lors de la création d’une approbation.         |
| Attribute-Id      | 1.2.840.113556.1.4.136               |
| System-ID-GUID    | bf967a60-0de6-11d0-a285-00aa003049e2 |
| Syntaxe            | [**Énumération**](s-enumeration.md) |



## <a name="implementations"></a>Implémentations

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server



| Entrée | Valeur |
|------------------------|------------------------------------------------------|
| ID de lien                | \-                                                   |
| MAPI-Id                | \-                                                   |
| System-Only            | False                                                |
| Est de valeur unique       | True                                                 |
| Est indexé             | False                                                |
| Dans le catalogue global      | False                                                |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                         |
| Range-Lower            | \-                                                   |
| Range-Upper            | \-                                                   |
| Search-Flags           | 0x00000000                                           |
| System-Flags           | 0x00000010                                           |
| Classes utilisées dans        | [**Domaine approuvé**](c-trusteddomain.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Entrée | Valeur |
|------------------------|------------------------------------------------------|
| ID de lien                | \-                                                   |
| MAPI-Id                | \-                                                   |
| System-Only            | False                                                |
| Est de valeur unique       | True                                                 |
| Est indexé             | False                                                |
| Dans le catalogue global      | True                                                 |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                         |
| Range-Lower            | \-                                                   |
| Range-Upper            | \-                                                   |
| Search-Flags           | 0x00000000                                           |
| System-Flags           | 0x00000010                                           |
| Classes utilisées dans        | [**Domaine approuvé**](c-trusteddomain.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrée | Valeur |
|------------------------|------------------------------------------------------|
| ID de lien                | \-                                                   |
| MAPI-Id                | \-                                                   |
| System-Only            | False                                                |
| Est de valeur unique       | True                                                 |
| Est indexé             | False                                                |
| Dans le catalogue global      | True                                                 |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                         |
| Range-Lower            | \-                                                   |
| Range-Upper            | \-                                                   |
| Search-Flags           | 0x00000000                                           |
| System-Flags           | 0x00000010                                           |
| Classes utilisées dans        | [**Domaine approuvé**](c-trusteddomain.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrée | Valeur |
|------------------------|------------------------------------------------------|
| ID de lien                | \-                                                   |
| MAPI-Id                | \-                                                   |
| System-Only            | False                                                |
| Est de valeur unique       | True                                                 |
| Est indexé             | False                                                |
| Dans le catalogue global      | True                                                 |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                         |
| Range-Lower            | \-                                                   |
| Range-Upper            | \-                                                   |
| Search-Flags           | 0x00000000                                           |
| System-Flags           | 0x00000010                                           |
| Classes utilisées dans        | [**Domaine approuvé**](c-trusteddomain.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrée | Valeur |
|------------------------|------------------------------------------------------|
| ID de lien                | \-                                                   |
| MAPI-Id                | \-                                                   |
| System-Only            | False                                                |
| Est de valeur unique       | True                                                 |
| Est indexé             | False                                                |
| Dans le catalogue global      | True                                                 |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                         |
| Range-Lower            | \-                                                   |
| Range-Upper            | \-                                                   |
| Search-Flags           | 0x00000000                                           |
| System-Flags           | 0x00000010                                           |
| Classes utilisées dans        | [**Domaine approuvé**](c-trusteddomain.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrée | Valeur |
|------------------------|------------------------------------------------------|
| ID de lien                | \-                                                   |
| MAPI-Id                | \-                                                   |
| System-Only            | False                                                |
| Est de valeur unique       | True                                                 |
| Est indexé             | False                                                |
| Dans le catalogue global      | True                                                 |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                         |
| Range-Lower            | \-                                                   |
| Range-Upper            | \-                                                   |
| Search-Flags           | 0x00000000                                           |
| System-Flags           | 0x00000010                                           |
| Classes utilisées dans        | [**Domaine approuvé**](c-trusteddomain.md)<br/> |



 

 





