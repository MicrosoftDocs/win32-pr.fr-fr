---
title: Attribut des objets connus
description: Cet attribut contient une liste de conteneurs d’objets connus par GUID et par nom unique.
ms.assetid: e3c2d243-6734-4c2f-9ead-bc4ec071d1f1
ms.tgt_platform: multiple
keywords:
- Schéma Active Directory des attributs d’objets bien connus
- Schéma AD de l’attribut wellKnownObjects
topic_type:
- apiref
api_name:
- Well-Known-Objects
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 16e21df3db14a29de137af4792f0e9ca6df27b90
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104480197"
---
# <a name="well-known-objects-attribute"></a>Attribut des objets connus

Cet attribut contient une liste de conteneurs d’objets connus par GUID et par nom unique. Les objets connus sont des conteneurs système. Ces informations sont utilisées pour récupérer un objet après qu’il a été déplacé en utilisant uniquement le GUID et le nom de domaine. Chaque fois que l’objet est déplacé, le système met automatiquement à jour la partie nom unique des valeurs des objets connus qui sont référencés par l’objet. Le fichier ntdsapi. h contient les définitions suivantes, qui peuvent être utilisées pour récupérer un objet (les GUID associés à ces objets sont contenus dans ntdsapi. h) :

-   \_conteneur d’utilisateurs GUID \_ \_ W
-   \_conteneur de calculs \_ GUID \_ W
-   \_conteneur de systèmes GUID \_ \_ W
-   \_conteneur de \_ contrôleurs de domaine GUID \_ \_ W
-   conteneur d’infrastructure de GUID \_ \_ \_ W
-   \_conteneur d' \_ objets supprimés GUID \_ \_ W
-   GUID \_ LOSTANDFOUND \_ conteneur \_ W
-   \_conteneur FOREIGNSECURITYPRINCIPALS \_ conteneur \_ W
-   \_conteneur de données du programme GUID \_ \_ \_ W
-   GUID \_ de \_ conteneur de données de programme Microsoft \_ \_ \_ W
-   GUID \_ NTDS \_ quotas \_ conteneur \_ W



| Entrée | Valeur |
|-------------------|-------------------------------------------------|
| CN                | Objets bien connus                              |
| LDAP-Display-Name | wellKnownObjects                                |
| Taille              | \-                                              |
| Mettre à jour le privilège  | Cette valeur est définie par le système.                |
| Fréquence des mises à jour  | Chaque fois que l’un des conteneurs système est déplacé. |
| Attribute-Id      | 1.2.840.113556.1.4.618                          |
| System-ID-GUID    | 05308983-7688-11d1-aded-00c04fd8d5cd            |
| Syntaxe            | [**Object(DN-Binary)**](s-object-dn-binary.md) |



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
|------------------------|---------------------------------|
| ID de lien                | \-                              |
| MAPI-Id                | \-                              |
| System-Only            | Vrai                            |
| Est de valeur unique       | Faux                           |
| Est indexé             | Faux                           |
| Dans le catalogue global      | Vrai                            |
| Descripteur de sécurité NT | O :BAG : BAD : S :                    |
| Range-Lower            | \-                              |
| Range-Upper            | \-                              |
| Search-Flags           | 0x00000000                      |
| System-Flags           | 0x00000012                      |
| Classes utilisées dans        | [**Retour au début**](c-top.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Entrée | Valeur |
|------------------------|---------------------------------|
| ID de lien                | \-                              |
| MAPI-Id                | \-                              |
| System-Only            | Vrai                            |
| Est de valeur unique       | Faux                           |
| Est indexé             | Faux                           |
| Dans le catalogue global      | Vrai                            |
| Descripteur de sécurité NT | O :BAG : BAD : S :                    |
| Range-Lower            | 16                              |
| Range-Upper            | 16                              |
| Search-Flags           | 0x00000000                      |
| System-Flags           | 0x00000012                      |
| Classes utilisées dans        | [**Retour au début**](c-top.md)<br/> |



## <a name="adam"></a>ADAM



| Entrée | Valeur |
|------------------------|---------------------------------|
| ID de lien                | \-                              |
| MAPI-Id                | \-                              |
| System-Only            | Vrai                            |
| Est de valeur unique       | Faux                           |
| Est indexé             | Faux                           |
| Dans le catalogue global      | Vrai                            |
| Descripteur de sécurité NT | O :BAG : BAD : S :                    |
| Range-Lower            | 16                              |
| Range-Upper            | 16                              |
| Search-Flags           | 0x00000000                      |
| System-Flags           | 0x00000012                      |
| Classes utilisées dans        | [**Retour au début**](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrée | Valeur |
|------------------------|---------------------------------|
| ID de lien                | \-                              |
| MAPI-Id                | \-                              |
| System-Only            | Vrai                            |
| Est de valeur unique       | Faux                           |
| Est indexé             | Faux                           |
| Dans le catalogue global      | Vrai                            |
| Descripteur de sécurité NT | O :BAG : BAD : S :                    |
| Range-Lower            | 16                              |
| Range-Upper            | 16                              |
| Search-Flags           | 0x00000000                      |
| System-Flags           | 0x00000012                      |
| Classes utilisées dans        | [**Retour au début**](c-top.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrée | Valeur |
|------------------------|---------------------------------|
| ID de lien                | \-                              |
| MAPI-Id                | \-                              |
| System-Only            | Vrai                            |
| Est de valeur unique       | Faux                           |
| Est indexé             | Faux                           |
| Dans le catalogue global      | Vrai                            |
| Descripteur de sécurité NT | O :BAG : BAD : S :                    |
| Range-Lower            | 16                              |
| Range-Upper            | 16                              |
| Search-Flags           | 0x00000000                      |
| System-Flags           | 0x00000012                      |
| Classes utilisées dans        | [**Retour au début**](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrée | Valeur |
|------------------------|---------------------------------|
| ID de lien                | \-                              |
| MAPI-Id                | \-                              |
| System-Only            | Vrai                            |
| Est de valeur unique       | Faux                           |
| Est indexé             | Faux                           |
| Dans le catalogue global      | Vrai                            |
| Descripteur de sécurité NT | O :BAG : BAD : S :                    |
| Range-Lower            | 16                              |
| Range-Upper            | 16                              |
| Search-Flags           | 0x00000000                      |
| System-Flags           | 0x00000012                      |
| Classes utilisées dans        | [**Retour au début**](c-top.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrée | Valeur |
|------------------------|---------------------------------|
| ID de lien                | \-                              |
| MAPI-Id                | \-                              |
| System-Only            | Vrai                            |
| Est de valeur unique       | Faux                           |
| Est indexé             | Faux                           |
| Dans le catalogue global      | Vrai                            |
| Descripteur de sécurité NT | O :BAG : BAD : S :                    |
| Range-Lower            | 16                              |
| Range-Upper            | 16                              |
| Search-Flags           | 0x00000000                      |
| System-Flags           | 0x00000012                      |
| Classes utilisées dans        | [**Retour au début**](c-top.md)<br/> |



 

 





