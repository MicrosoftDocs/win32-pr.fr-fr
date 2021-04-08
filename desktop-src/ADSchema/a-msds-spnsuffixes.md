---
title: attribut ms-DS-SPN-suffixes
description: Cet attribut décrit les suffixes des noms d’hôtes DNS utilisés par les serveurs de la forêt. Ces suffixes DNS seront partagés avec d’autres forêts qui ont une approbation inter-forêts avec cette forêt.
ms.assetid: 56153832-1228-419f-99d4-eb1ce3edc867
ms.tgt_platform: multiple
keywords:
- Schéma AD des attributs ms-DS-SPN-suffixes
- Schéma Active Directory de l’attribut msDS-SPNSuffixes
topic_type:
- apiref
api_name:
- ms-DS-SPN-Suffixes
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c91f7ce8c92e8a81437d90bb0d80383b9ad334ee
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "103943168"
---
# <a name="ms-ds-spn-suffixes-attribute"></a>attribut ms-DS-SPN-suffixes

Cet attribut décrit les suffixes des noms d’hôtes DNS utilisés par les serveurs de la forêt. Ces suffixes DNS seront partagés avec d’autres forêts qui ont une approbation inter-forêts avec cette forêt.



| Entrée | Valeur |
|-------------------|----------------------------------------------|
| CN                | ms-DS-SPN-suffixes                           |
| LDAP-Display-Name | msDS-SPNSuffixes                             |
| Taille              | 255 octets                                    |
| Mettre à jour le privilège  | Administrateur de domaine                         |
| Fréquence des mises à jour  | Lorsque les serveurs de la forêt obtiennent un nouveau suffixe. |
| Attribute-Id      | 1.2.840.113556.1.4.1715                      |
| System-ID-GUID    | 789ee1eb-8c8e-4e4c-8cec-79b31b7617b5         |
| Syntaxe            | [**String(Unicode)**](s-string-unicode.md)  |



## <a name="implementations"></a>Implémentations

-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-server-2003"></a>Windows Server 2003



| Entrée | Valeur |
|------------------------|---------------------------------------------------------------|
| ID de lien                | \-                                                            |
| MAPI-Id                | \-                                                            |
| System-Only            | Faux                                                         |
| Est de valeur unique       | Faux                                                         |
| Est indexé             | Faux                                                         |
| Dans le catalogue global      | Faux                                                         |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                                  |
| Range-Lower            | \-                                                            |
| Range-Upper            | \-                                                            |
| Search-Flags           | 0x00000000                                                    |
| System-Flags           | 0x00000010                                                    |
| Classes utilisées dans        | [**Cross-Ref-Container**](c-crossrefcontainer.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrée | Valeur |
|------------------------|---------------------------------------------------------------|
| ID de lien                | \-                                                            |
| MAPI-Id                | \-                                                            |
| System-Only            | Faux                                                         |
| Est de valeur unique       | Faux                                                         |
| Est indexé             | Faux                                                         |
| Dans le catalogue global      | Faux                                                         |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                                  |
| Range-Lower            | \-                                                            |
| Range-Upper            | \-                                                            |
| Search-Flags           | 0x00000000                                                    |
| System-Flags           | 0x00000010                                                    |
| Classes utilisées dans        | [**Cross-Ref-Container**](c-crossrefcontainer.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrée | Valeur |
|------------------------|---------------------------------------------------------------|
| ID de lien                | \-                                                            |
| MAPI-Id                | \-                                                            |
| System-Only            | Faux                                                         |
| Est de valeur unique       | Faux                                                         |
| Est indexé             | Faux                                                         |
| Dans le catalogue global      | Faux                                                         |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                                  |
| Range-Lower            | \-                                                            |
| Range-Upper            | \-                                                            |
| Search-Flags           | 0x00000000                                                    |
| System-Flags           | 0x00000010                                                    |
| Classes utilisées dans        | [**Cross-Ref-Container**](c-crossrefcontainer.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrée | Valeur |
|------------------------|---------------------------------------------------------------|
| ID de lien                | \-                                                            |
| MAPI-Id                | \-                                                            |
| System-Only            | Faux                                                         |
| Est de valeur unique       | Faux                                                         |
| Est indexé             | Faux                                                         |
| Dans le catalogue global      | Faux                                                         |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                                  |
| Range-Lower            | \-                                                            |
| Range-Upper            | \-                                                            |
| Search-Flags           | 0x00000000                                                    |
| System-Flags           | 0x00000010                                                    |
| Classes utilisées dans        | [**Cross-Ref-Container**](c-crossrefcontainer.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrée | Valeur |
|------------------------|---------------------------------------------------------------|
| ID de lien                | \-                                                            |
| MAPI-Id                | \-                                                            |
| System-Only            | Faux                                                         |
| Est de valeur unique       | Faux                                                         |
| Est indexé             | Faux                                                         |
| Dans le catalogue global      | Faux                                                         |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                                  |
| Range-Lower            | \-                                                            |
| Range-Upper            | \-                                                            |
| Search-Flags           | 0x00000000                                                    |
| System-Flags           | 0x00000010                                                    |
| Classes utilisées dans        | [**Cross-Ref-Container**](c-crossrefcontainer.md)<br/> |



 

 





