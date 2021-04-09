---
title: Attribut Extra-Columns
description: Il s’agit d’un attribut à valeurs multiples dont les valeurs se composent d’un tuple de 5 (nom d’attribut), (titre de colonne), (visibilité par défaut (0, 1)), (largeur de colonne (\ 8211 ; 1 pour la largeur automatique)), 0 (réservé pour une utilisation future doit être égal à zéro).
ms.assetid: aafe4657-0295-4af2-a7d0-8c7561516e17
ms.tgt_platform: multiple
keywords:
- Schéma AD d’attribut Extra-Columns
- Schéma AD de l’attribut extraColumns
topic_type:
- apiref
api_name:
- Extra-Columns
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de0bc74532296c5e0f23da9635bb26df299ae60b
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "103744380"
---
# <a name="extra-columns-attribute"></a>Attribut Extra-Columns

Il s’agit d’un attribut à valeurs multiples dont les valeurs se composent d’un tuple de 5 : (nom de l’attribut), (titre de colonne), (visibilité par défaut (0, 1)), (largeur de colonne (1 pour la largeur automatique), 0 (réservé à un usage futur). Cette valeur est utilisée par la console utilisateurs et ordinateurs Active Directory.



| Entrée | Valeur |
|-------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| CN                | Extra-Columns                                                                                                                                                        |
| LDAP-Display-Name | extraColumns                                                                                                                                                         |
| Taille              | Chaque valeur correspond à la taille de la chaîne des 5 tuples ci-dessus. Par défaut, il y aura 22 valeurs sur l’objet d’affichage par défaut dans le conteneur DisplaySpecifier. |
| Mettre à jour le privilège  | Administrateur de domaine                                                                                                                                                 |
| Fréquence des mises à jour  | Ce sera uniquement mis à jour si un service comme Exchange est installé.                                                                                                   |
| Attribute-Id      | 1.2.840.113556.1.4.1687                                                                                                                                              |
| System-ID-GUID    | d24e2846-1dd9-4bcf-99d7-a6227cc86da7                                                                                                                                 |
| Syntaxe            | [**String(Unicode)**](s-string-unicode.md)                                                                                                                          |



## <a name="implementations"></a>Implémentations

-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-server-2003"></a>Windows Server 2003



| Entrée | Valeur |
|------------------------|------------------------------------------------------------|
| ID de lien                | \-                                                         |
| MAPI-Id                | \-                                                         |
| System-Only            | Faux                                                      |
| Est de valeur unique       | Faux                                                      |
| Est indexé             | Faux                                                      |
| Dans le catalogue global      | Faux                                                      |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                               |
| Range-Lower            | \-                                                         |
| Range-Upper            | \-                                                         |
| Search-Flags           | 0x00000000                                                 |
| System-Flags           | 0x00000010                                                 |
| Classes utilisées dans        | [**Display-specifier**](c-displayspecifier.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrée | Valeur |
|------------------------|------------------------------------------------------------|
| ID de lien                | \-                                                         |
| MAPI-Id                | \-                                                         |
| System-Only            | Faux                                                      |
| Est de valeur unique       | Faux                                                      |
| Est indexé             | Faux                                                      |
| Dans le catalogue global      | Faux                                                      |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                               |
| Range-Lower            | \-                                                         |
| Range-Upper            | \-                                                         |
| Search-Flags           | 0x00000000                                                 |
| System-Flags           | 0x00000010                                                 |
| Classes utilisées dans        | [**Display-specifier**](c-displayspecifier.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrée | Valeur |
|------------------------|------------------------------------------------------------|
| ID de lien                | \-                                                         |
| MAPI-Id                | \-                                                         |
| System-Only            | Faux                                                      |
| Est de valeur unique       | Faux                                                      |
| Est indexé             | Faux                                                      |
| Dans le catalogue global      | Faux                                                      |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                               |
| Range-Lower            | \-                                                         |
| Range-Upper            | \-                                                         |
| Search-Flags           | 0x00000000                                                 |
| System-Flags           | 0x00000010                                                 |
| Classes utilisées dans        | [**Display-specifier**](c-displayspecifier.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrée | Valeur |
|------------------------|------------------------------------------------------------|
| ID de lien                | \-                                                         |
| MAPI-Id                | \-                                                         |
| System-Only            | Faux                                                      |
| Est de valeur unique       | Faux                                                      |
| Est indexé             | Faux                                                      |
| Dans le catalogue global      | Faux                                                      |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                               |
| Range-Lower            | \-                                                         |
| Range-Upper            | \-                                                         |
| Search-Flags           | 0x00000000                                                 |
| System-Flags           | 0x00000010                                                 |
| Classes utilisées dans        | [**Display-specifier**](c-displayspecifier.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrée | Valeur |
|------------------------|------------------------------------------------------------|
| ID de lien                | \-                                                         |
| MAPI-Id                | \-                                                         |
| System-Only            | Faux                                                      |
| Est de valeur unique       | Faux                                                      |
| Est indexé             | Faux                                                      |
| Dans le catalogue global      | Faux                                                      |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                               |
| Range-Lower            | \-                                                         |
| Range-Upper            | \-                                                         |
| Search-Flags           | 0x00000000                                                 |
| System-Flags           | 0x00000010                                                 |
| Classes utilisées dans        | [**Display-specifier**](c-displayspecifier.md)<br/> |



 

 





