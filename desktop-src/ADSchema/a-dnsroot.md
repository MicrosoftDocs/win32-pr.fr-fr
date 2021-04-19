---
title: Attribut Dns-Root
description: Nom de domaine DNS le plus élevé affecté à une partition de domaine/répertoire.
ms.assetid: 0b33daad-b5c5-4126-86fa-abd3e0006c5f
ms.tgt_platform: multiple
keywords:
- Schéma AD d’attribut Dns-Root
- Schéma AD de l’attribut dnsRoot
topic_type:
- apiref
api_name:
- Dns-Root
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2a2c2fd2c39e8f0015d7641eccd27279b3478ec4
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "106514877"
---
# <a name="dns-root-attribute"></a>Attribut Dns-Root

Nom de domaine DNS le plus élevé affecté à une partition de domaine/répertoire. Cette valeur est définie sur un objet crossRef et est utilisée, entre autres, pour la génération de références. Lors de la recherche dans l’ensemble de l’arborescence de domaine, la recherche doit être lancée au niveau de l’objet Dns-Root. Cet attribut peut être à valeurs multiples, auquel cas plusieurs références sont générées.



| Entrée | Valeur |
|-------------------|---------------------------------------------|
| CN                | Dns-Root                                    |
| LDAP-Display-Name | dnsRoot                                     |
| Taille              | \-                                          |
| Mettre à jour le privilège  | Cette valeur est définie par le système.            |
| Fréquence des mises à jour  | \-                                          |
| Attribute-Id      | 1.2.840.113556.1.4.28                       |
| System-ID-GUID    | bf967959-0de6-11d0-a285-00aa003049e2        |
| Syntaxe            | [**String(Unicode)**](s-string-unicode.md) |



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
|------------------------|--------------------------------------------|
| ID de lien                | \-                                         |
| MAPI-Id                | \-                                         |
| System-Only            | Faux                                      |
| Est de valeur unique       | Faux                                      |
| Est indexé             | Vrai                                       |
| Dans le catalogue global      | Faux                                      |
| Descripteur de sécurité NT | O :BAG : BAD : S :                               |
| Range-Lower            | 1                                          |
| Range-Upper            | 255                                        |
| Search-Flags           | 0x00000001                                 |
| System-Flags           | 0x00000010                                 |
| Classes utilisées dans        | [**Référence croisée**](c-crossref.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Entrée | Valeur |
|------------------------|--------------------------------------------|
| ID de lien                | \-                                         |
| MAPI-Id                | \-                                         |
| System-Only            | Faux                                      |
| Est de valeur unique       | Faux                                      |
| Est indexé             | Vrai                                       |
| Dans le catalogue global      | Faux                                      |
| Descripteur de sécurité NT | O :BAG : BAD : S :                               |
| Range-Lower            | 1                                          |
| Range-Upper            | 255                                        |
| Search-Flags           | 0x00000001                                 |
| System-Flags           | 0x00000010                                 |
| Classes utilisées dans        | [**Référence croisée**](c-crossref.md)<br/> |



## <a name="adam"></a>ADAM



| Entrée | Valeur |
|------------------------|--------------------------------------------|
| ID de lien                | \-                                         |
| MAPI-Id                | \-                                         |
| System-Only            | Faux                                      |
| Est de valeur unique       | Faux                                      |
| Est indexé             | Vrai                                       |
| Dans le catalogue global      | Faux                                      |
| Descripteur de sécurité NT | O :BAG : BAD : S :                               |
| Range-Lower            | 1                                          |
| Range-Upper            | 255                                        |
| Search-Flags           | 0x00000001                                 |
| System-Flags           | 0x00000010                                 |
| Classes utilisées dans        | [**Référence croisée**](c-crossref.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrée | Valeur |
|------------------------|--------------------------------------------|
| ID de lien                | \-                                         |
| MAPI-Id                | \-                                         |
| System-Only            | Faux                                      |
| Est de valeur unique       | Faux                                      |
| Est indexé             | Vrai                                       |
| Dans le catalogue global      | Faux                                      |
| Descripteur de sécurité NT | O :BAG : BAD : S :                               |
| Range-Lower            | 1                                          |
| Range-Upper            | 255                                        |
| Search-Flags           | 0x00000001                                 |
| System-Flags           | 0x00000010                                 |
| Classes utilisées dans        | [**Référence croisée**](c-crossref.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrée | Valeur |
|------------------------|--------------------------------------------|
| ID de lien                | \-                                         |
| MAPI-Id                | \-                                         |
| System-Only            | Faux                                      |
| Est de valeur unique       | Faux                                      |
| Est indexé             | Vrai                                       |
| Dans le catalogue global      | Faux                                      |
| Descripteur de sécurité NT | O :BAG : BAD : S :                               |
| Range-Lower            | 1                                          |
| Range-Upper            | 255                                        |
| Search-Flags           | 0x00000001                                 |
| System-Flags           | 0x00000010                                 |
| Classes utilisées dans        | [**Référence croisée**](c-crossref.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrée | Valeur |
|------------------------|--------------------------------------------|
| ID de lien                | \-                                         |
| MAPI-Id                | \-                                         |
| System-Only            | Faux                                      |
| Est de valeur unique       | Faux                                      |
| Est indexé             | Vrai                                       |
| Dans le catalogue global      | Faux                                      |
| Descripteur de sécurité NT | O :BAG : BAD : S :                               |
| Range-Lower            | 1                                          |
| Range-Upper            | 255                                        |
| Search-Flags           | 0x00000001                                 |
| System-Flags           | 0x00000010                                 |
| Classes utilisées dans        | [**Référence croisée**](c-crossref.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrée | Valeur |
|------------------------|--------------------------------------------|
| ID de lien                | \-                                         |
| MAPI-Id                | \-                                         |
| System-Only            | Faux                                      |
| Est de valeur unique       | Faux                                      |
| Est indexé             | Vrai                                       |
| Dans le catalogue global      | Faux                                      |
| Descripteur de sécurité NT | O :BAG : BAD : S :                               |
| Range-Lower            | 1                                          |
| Range-Upper            | 255                                        |
| Search-Flags           | 0x00000001                                 |
| System-Flags           | 0x00000010                                 |
| Classes utilisées dans        | [**Référence croisée**](c-crossref.md)<br/> |



 

 





