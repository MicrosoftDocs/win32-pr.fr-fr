---
title: NT-attribut mixte de domaine
description: Indique que le domaine est en mode natif ou en mode mixte. Cet attribut se trouve dans l’objet domainDNS (Head) pour le domaine.
ms.assetid: 49872cbc-844f-4d60-89b6-0150b9116740
ms.tgt_platform: multiple
keywords:
- Schéma AD d’attribut de domaine mixte NT
- Schéma AD de l’attribut nTMixedDomain
topic_type:
- apiref
api_name:
- NT-Mixed-Domain
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 39148883e2b5d57157c334854ab7ebdfa61b69ac61d7a0100fc8470b741909c4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119703029"
---
# <a name="nt-mixed-domain-attribute"></a>NT-attribut mixte de domaine

Indique que le domaine est en mode natif ou en mode mixte. Cet attribut se trouve dans l’objet domainDNS (Head) pour le domaine.



| Entrée | Valeur |
|-------------------|---------------------------------------|
| CN                | NT-mixte-domaine                       |
| LDAP-Display-Name | nTMixedDomain                         |
| Taille              | 4 octets. Mode mixte 1, mode natif 0. |
| Mettre à jour le privilège  | \-                                    |
| Fréquence des mises à jour  | \-                                    |
| Attribute-Id      | 1.2.840.113556.1.4.357                |
| System-ID-GUID    | 3e97891f-8c01-11d0-afda-00c04fd930c9  |
| Syntaxe            | [**Énumération**](s-enumeration.md)  |



## <a name="implementations"></a>Implémentations

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server



| Entrée | Valeur |
|------------------------|----------------------------------------------|
| ID de lien                | \-                                           |
| MAPI-Id                | \-                                           |
| System-Only            | Faux                                        |
| Est de valeur unique       | Vrai                                         |
| Est indexé             | Faux                                        |
| Dans le catalogue global      | Faux                                        |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                 |
| Range-Lower            | \-                                           |
| Range-Upper            | \-                                           |
| Search-Flags           | 0x00000000                                   |
| System-Flags           | 0x00000010                                   |
| Classes utilisées dans        | [**Sam-domaine**](c-samdomain.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Entrée | Valeur |
|------------------------|-----------------------------------------------------------------------------------------|
| ID de lien                | \-                                                                                      |
| MAPI-Id                | \-                                                                                      |
| System-Only            | Faux                                                                                   |
| Est de valeur unique       | Vrai                                                                                    |
| Est indexé             | Faux                                                                                   |
| Dans le catalogue global      | Faux                                                                                   |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                                                            |
| Range-Lower            | \-                                                                                      |
| Range-Upper            | \-                                                                                      |
| Search-Flags           | 0x00000000                                                                              |
| System-Flags           | 0x00000010                                                                              |
| Classes utilisées dans        | [**Référence croisée**](c-crossref.md)<br/> [**Sam-domaine**](c-samdomain.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrée | Valeur |
|------------------------|-----------------------------------------------------------------------------------------|
| ID de lien                | \-                                                                                      |
| MAPI-Id                | \-                                                                                      |
| System-Only            | Faux                                                                                   |
| Est de valeur unique       | Vrai                                                                                    |
| Est indexé             | Faux                                                                                   |
| Dans le catalogue global      | Faux                                                                                   |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                                                            |
| Range-Lower            | \-                                                                                      |
| Range-Upper            | \-                                                                                      |
| Search-Flags           | 0x00000000                                                                              |
| System-Flags           | 0x00000010                                                                              |
| Classes utilisées dans        | [**Référence croisée**](c-crossref.md)<br/> [**Sam-domaine**](c-samdomain.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrée | Valeur |
|------------------------|-----------------------------------------------------------------------------------------|
| ID de lien                | \-                                                                                      |
| MAPI-Id                | \-                                                                                      |
| System-Only            | Faux                                                                                   |
| Est de valeur unique       | Vrai                                                                                    |
| Est indexé             | Faux                                                                                   |
| Dans le catalogue global      | Faux                                                                                   |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                                                            |
| Range-Lower            | \-                                                                                      |
| Range-Upper            | \-                                                                                      |
| Search-Flags           | 0x00000000                                                                              |
| System-Flags           | 0x00000010                                                                              |
| Classes utilisées dans        | [**Référence croisée**](c-crossref.md)<br/> [**Sam-domaine**](c-samdomain.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrée | Valeur |
|------------------------|-----------------------------------------------------------------------------------------|
| ID de lien                | \-                                                                                      |
| MAPI-Id                | \-                                                                                      |
| System-Only            | Faux                                                                                   |
| Est de valeur unique       | Vrai                                                                                    |
| Est indexé             | Faux                                                                                   |
| Dans le catalogue global      | Faux                                                                                   |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                                                            |
| Range-Lower            | \-                                                                                      |
| Range-Upper            | \-                                                                                      |
| Search-Flags           | 0x00000000                                                                              |
| System-Flags           | 0x00000010                                                                              |
| Classes utilisées dans        | [**Référence croisée**](c-crossref.md)<br/> [**Sam-domaine**](c-samdomain.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrée | Valeur |
|------------------------|-----------------------------------------------------------------------------------------|
| ID de lien                | \-                                                                                      |
| MAPI-Id                | \-                                                                                      |
| System-Only            | Faux                                                                                   |
| Est de valeur unique       | Vrai                                                                                    |
| Est indexé             | Faux                                                                                   |
| Dans le catalogue global      | Faux                                                                                   |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                                                            |
| Range-Lower            | \-                                                                                      |
| Range-Upper            | \-                                                                                      |
| Search-Flags           | 0x00000000                                                                              |
| System-Flags           | 0x00000010                                                                              |
| Classes utilisées dans        | [**Référence croisée**](c-crossref.md)<br/> [**Sam-domaine**](c-samdomain.md)<br/> |



 

 





