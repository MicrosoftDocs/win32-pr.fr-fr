---
title: Attribut Address-Type
description: Chaîne de caractères qui décrit le format de l’adresse de l’utilisateur. Les types d’adresses sont mappés aux formats d’adresse. Autrement dit, en examinant le type d’adresse d’un destinataire, les applications clientes peuvent déterminer comment mettre en forme une adresse appropriée pour le destinataire.
ms.assetid: ff39b1f5-1844-43e9-a4a5-2b5f7c396f34
ms.tgt_platform: multiple
keywords:
- Schéma AD d’attribut Address-Type
- Schéma Active Directory des attributs addressType
topic_type:
- apiref
api_name:
- Address-Type
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6ece3b396d619272c616ff1a959d01efb64ccd46
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "106514297"
---
# <a name="address-type-attribute"></a>Attribut Address-Type

Chaîne de caractères qui décrit le format de l’adresse de l’utilisateur. Les types d’adresses sont mappés aux formats d’adresse. Autrement dit, en examinant le type d’adresse d’un destinataire, les applications clientes peuvent déterminer comment mettre en forme une adresse appropriée pour le destinataire.



| Entrée | Valeur |
|-------------------|---------------------------------------------------------------------------------------------------------------------------|
| CN                | Address-Type                                                                                                              |
| LDAP-Display-Name | addressType                                                                                                               |
| Taille              | Types d’adresses : 3COM, ATT, CCMAIL, COMPUSERVE, EX, FAX, MSFAX, MCI, MHS, MS, MSA, MSN, PROFs, SMTP, SNADS, télex, x400, X500 |
| Mettre à jour le privilège  | Cette valeur est définie par le système.                                                                                          |
| Fréquence des mises à jour  | Défini lors de la création de l’objet.                                                                                           |
| Attribute-Id      | 1.2.840.113556.1.2.350                                                                                                    |
| System-ID-GUID    | 5fd42464-1262-11d0-a060-00aa006c33ed                                                                                      |
| Syntaxe            | [**String(Teletex)**](s-string-teletex.md)                                                                               |



## <a name="implementations"></a>Implémentations

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server



| Entrée | Valeur |
|------------------------|----------------------------------------------------------|
| ID de lien                | \-                                                       |
| MAPI-Id                | 0x8048                                                   |
| System-Only            | Faux                                                    |
| Est de valeur unique       | Vrai                                                     |
| Est indexé             | Faux                                                    |
| Dans le catalogue global      | Faux                                                    |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                             |
| Range-Lower            | 1                                                        |
| Range-Upper            | 32                                                       |
| Search-Flags           | 0x00000000                                               |
| System-Flags           | 0x00000010                                               |
| Classes utilisées dans        | [**Modèle d’adresse**](c-addresstemplate.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Entrée | Valeur |
|------------------------|----------------------------------------------------------|
| ID de lien                | \-                                                       |
| MAPI-Id                | 0x8048                                                   |
| System-Only            | Faux                                                    |
| Est de valeur unique       | Vrai                                                     |
| Est indexé             | Faux                                                    |
| Dans le catalogue global      | Faux                                                    |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                             |
| Range-Lower            | 1                                                        |
| Range-Upper            | 32                                                       |
| Search-Flags           | 0x00000000                                               |
| System-Flags           | 0x00000010                                               |
| Classes utilisées dans        | [**Modèle d’adresse**](c-addresstemplate.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrée | Valeur |
|------------------------|----------------------------------------------------------|
| ID de lien                | \-                                                       |
| MAPI-Id                | 0x8048                                                   |
| System-Only            | Faux                                                    |
| Est de valeur unique       | Vrai                                                     |
| Est indexé             | Faux                                                    |
| Dans le catalogue global      | Faux                                                    |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                             |
| Range-Lower            | 1                                                        |
| Range-Upper            | 32                                                       |
| Search-Flags           | 0x00000000                                               |
| System-Flags           | 0x00000010                                               |
| Classes utilisées dans        | [**Modèle d’adresse**](c-addresstemplate.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrée | Valeur |
|------------------------|----------------------------------------------------------|
| ID de lien                | \-                                                       |
| MAPI-Id                | 0x8048                                                   |
| System-Only            | Faux                                                    |
| Est de valeur unique       | Vrai                                                     |
| Est indexé             | Faux                                                    |
| Dans le catalogue global      | Faux                                                    |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                             |
| Range-Lower            | 1                                                        |
| Range-Upper            | 32                                                       |
| Search-Flags           | 0x00000000                                               |
| System-Flags           | 0x00000010                                               |
| Classes utilisées dans        | [**Modèle d’adresse**](c-addresstemplate.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrée | Valeur |
|------------------------|----------------------------------------------------------|
| ID de lien                | \-                                                       |
| MAPI-Id                | 0x8048                                                   |
| System-Only            | Faux                                                    |
| Est de valeur unique       | Vrai                                                     |
| Est indexé             | Faux                                                    |
| Dans le catalogue global      | Faux                                                    |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                             |
| Range-Lower            | 1                                                        |
| Range-Upper            | 32                                                       |
| Search-Flags           | 0x00000000                                               |
| System-Flags           | 0x00000010                                               |
| Classes utilisées dans        | [**Modèle d’adresse**](c-addresstemplate.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrée | Valeur |
|------------------------|----------------------------------------------------------|
| ID de lien                | \-                                                       |
| MAPI-Id                | 0x8048                                                   |
| System-Only            | Faux                                                    |
| Est de valeur unique       | Vrai                                                     |
| Est indexé             | Faux                                                    |
| Dans le catalogue global      | Faux                                                    |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                             |
| Range-Lower            | 1                                                        |
| Range-Upper            | 32                                                       |
| Search-Flags           | 0x00000000                                               |
| System-Flags           | 0x00000010                                               |
| Classes utilisées dans        | [**Modèle d’adresse**](c-addresstemplate.md)<br/> |



 

 





