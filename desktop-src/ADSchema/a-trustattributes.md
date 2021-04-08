---
title: Attribut Trust-Attributes
description: Cet attribut stocke les attributs d’approbation pour un domaine approuvé.
ms.assetid: c85b98a6-4d09-4eb2-821b-58ef558b3460
ms.tgt_platform: multiple
keywords:
- Schéma AD d’attribut Trust-Attributes
- Schéma AD de l’attribut trustAttributes
topic_type:
- apiref
api_name:
- Trust-Attributes
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d81dc06f73fbda5dab7ce8d2a07bfc90323d2b29
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "103744884"
---
# <a name="trust-attributes-attribute"></a>Attribut Trust-Attributes

Cet attribut stocke les attributs d’approbation pour un domaine approuvé. Les valeurs d’attribut possibles sont les suivantes :

-   \_Attribut de \_ confiance \_ : désactivation de la transitivité non transitive.
-   \_ \_ \_ L’approbation parente de l’arborescence d’attributs d’approbation est définie sur le parent de l’arborescence d’organisation.
-   \_ \_ Approbation racine de l’arborescence des attributs de confiance \_ définie sur une autre racine d’arborescence dans la forêt.
-   Le \_ \_ \_ lien de confiance de niveau supérieur d’attribut uniquement valide uniquement pour le client de niveau supérieur.



| Entrée | Valeur |
|-------------------|--------------------------------------|
| CN                | Trust-Attributes                     |
| LDAP-Display-Name | trustAttributes                      |
| Taille              | \-                                   |
| Mettre à jour le privilège  | \-                                   |
| Fréquence des mises à jour  | \-                                   |
| Attribute-Id      | 1.2.840.113556.1.4.470               |
| System-ID-GUID    | 80a67e5a-9f22-11d0-afdd-00c04fd930c9 |
| Syntaxe            | [**Enumeration**](s-enumeration.md) |



## <a name="implementations"></a>Implémentations

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server



| Entrée | Valeur |
|------------------------|------------------------------------------------------|
| ID de lien                | \-                                                   |
| MAPI-Id                | \-                                                   |
| System-Only            | Faux                                                |
| Est de valeur unique       | Vrai                                                 |
| Est indexé             | Faux                                                |
| Dans le catalogue global      | Faux                                                |
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
| System-Only            | Faux                                                |
| Est de valeur unique       | Vrai                                                 |
| Est indexé             | Faux                                                |
| Dans le catalogue global      | Vrai                                                 |
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
| System-Only            | Faux                                                |
| Est de valeur unique       | Vrai                                                 |
| Est indexé             | Faux                                                |
| Dans le catalogue global      | Vrai                                                 |
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
| System-Only            | Faux                                                |
| Est de valeur unique       | Vrai                                                 |
| Est indexé             | Faux                                                |
| Dans le catalogue global      | Vrai                                                 |
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
| System-Only            | Faux                                                |
| Est de valeur unique       | Vrai                                                 |
| Est indexé             | Faux                                                |
| Dans le catalogue global      | Vrai                                                 |
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
| System-Only            | Faux                                                |
| Est de valeur unique       | Vrai                                                 |
| Est indexé             | Faux                                                |
| Dans le catalogue global      | Vrai                                                 |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                         |
| Range-Lower            | \-                                                   |
| Range-Upper            | \-                                                   |
| Search-Flags           | 0x00000000                                           |
| System-Flags           | 0x00000010                                           |
| Classes utilisées dans        | [**Domaine approuvé**](c-trusteddomain.md)<br/> |



 

 





