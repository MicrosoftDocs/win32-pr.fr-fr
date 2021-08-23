---
title: ms-DS-attribut-Encryption-types pris en charge
description: Algorithmes de chiffrement pris en charge par les comptes d’utilisateur, d’ordinateur ou de confiance. Notez que le KDC utilise ces informations lors de la génération d’un ticket de service pour ce compte.
ms.assetid: 6f9055a9-531e-4f4b-8703-aca5531a3bcb
ms.tgt_platform: multiple
keywords:
- Schéma AD des attributs de types de chiffrement pris en charge par ms-DS
- Schéma Active Directory de l’attribut msDS-SupportedEncryptionTypes
topic_type:
- apiref
api_name:
- ms-DS-Supported-Encryption-Types
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c1d092061dfebcea8e9a0e4f4a060010e16102108d1e2e74f05e6df2db706141
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119544339"
---
# <a name="ms-ds-supported-encryption-types-attribute"></a>ms-DS-attribut-Encryption-types pris en charge

Algorithmes de chiffrement pris en charge par les comptes d’utilisateur, d’ordinateur ou de confiance.

> [!Note]  
> Le KDC utilise ces informations lors de la génération d’un ticket de service pour ce compte. Les services et les ordinateurs peuvent automatiquement mettre à jour cet attribut sur leurs comptes respectifs dans Active Directory et ont donc besoin d’un accès en écriture à cet attribut.

 



| Entrée | Valeur |
|-------------------|--------------------------------------|
| CN                | ms-DS-types de chiffrement pris en charge     |
| LDAP-Display-Name | msDS-SupportedEncryptionTypes        |
| Taille              | \-                                   |
| Mettre à jour le privilège  | \-                                   |
| Fréquence des mises à jour  | \-                                   |
| Attribute-Id      | 1.2.840.113556.1.4.1963              |
| System-ID-GUID    | 20119867-1d04-4ab7-9371-cfc3d5df0afd |
| Syntaxe            | [**Énumération**](s-enumeration.md) |



## <a name="implementations"></a>Implémentations

-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-server-2008"></a>Windows Server 2008



| Entrée | Valeur |
|------------------------|----------------------------------------------------------------------------------------|
| ID de lien                | \-                                                                                     |
| MAPI-Id                | \-                                                                                     |
| System-Only            | Faux                                                                                  |
| Est de valeur unique       | Vrai                                                                                   |
| Est indexé             | Faux                                                                                  |
| Dans le catalogue global      | Faux                                                                                  |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                                                           |
| Range-Lower            | \-                                                                                     |
| Range-Upper            | \-                                                                                     |
| Search-Flags           | 0x00000000                                                                             |
| System-Flags           | 0x00000010                                                                             |
| Classes utilisées dans        | [**Domaine approuvé**](c-trusteddomain.md)<br/> [**Utilisateur**](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrée | Valeur |
|------------------------|----------------------------------------------------------------------------------------|
| ID de lien                | \-                                                                                     |
| MAPI-Id                | \-                                                                                     |
| System-Only            | Faux                                                                                  |
| Est de valeur unique       | Vrai                                                                                   |
| Est indexé             | Faux                                                                                  |
| Dans le catalogue global      | Faux                                                                                  |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                                                           |
| Range-Lower            | \-                                                                                     |
| Range-Upper            | \-                                                                                     |
| Search-Flags           | 0x00000000                                                                             |
| System-Flags           | 0x00000010                                                                             |
| Classes utilisées dans        | [**Domaine approuvé**](c-trusteddomain.md)<br/> [**Utilisateur**](c-user.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrée | Valeur |
|------------------------|----------------------------------------------------------------------------------------|
| ID de lien                | \-                                                                                     |
| MAPI-Id                | \-                                                                                     |
| System-Only            | Faux                                                                                  |
| Est de valeur unique       | Vrai                                                                                   |
| Est indexé             | Faux                                                                                  |
| Dans le catalogue global      | Faux                                                                                  |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                                                           |
| Range-Lower            | \-                                                                                     |
| Range-Upper            | \-                                                                                     |
| Search-Flags           | 0x00000000                                                                             |
| System-Flags           | 0x00000010                                                                             |
| Classes utilisées dans        | [**Domaine approuvé**](c-trusteddomain.md)<br/> [**Utilisateur**](c-user.md)<br/> |



 

 





