---
title: ms-DS-attribut-Text-Encrypted-Text-Password-allowed
description: Indique si Active Directory stockera le mot de passe dans le format de chiffrement réversible.
ms.assetid: 67067cf6-60e3-4626-bf8c-a0a1264a899e
ms.tgt_platform: multiple
keywords:
- Schéma Active Directory de l’attribut ms-DS-Encrypted-Text-Password-allowed-Password
- Schéma AD de l’attribut ms-DS-UserEncryptedTextPasswordAllowed
topic_type:
- apiref
api_name:
- ms-DS-User-Encrypted-Text-Password-Allowed
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2d99ae61566ceec94336fd58951214dfc3255d2e
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104479757"
---
# <a name="ms-ds-user-encrypted-text-password-allowed-attribute"></a>ms-DS-attribut-Text-Encrypted-Text-Password-allowed

Indique si Active Directory stockera le mot de passe dans le format de chiffrement réversible. True si le mot de passe est stocké dans le format de chiffrement réversible ; Sinon, false.

> [!Note]  
> Cet attribut n’est pas utilisé par [services AD LDS (Active Directory Lightweight Directory Services)](/previous-versions/windows/desktop/adam/active-directory-lightweight-directory-services) et est uniquement inclus pour l’exhaustivité/la parité avec UserAccountControl. AD LDS ne stocke pas les mots de passe avec un chiffrement réversible, quelle que soit la valeur de cet attribut sur un objet donné ou si la stratégie de sécurité de l’ordinateur se rapporte à un chiffrement réversible sur l’ordinateur lui-même.

 



| Entrée | Valeur |
|-------------------|--------------------------------------------|
| CN                | ms-DS-User-Encrypted-Text-Password-allowed |
| LDAP-Display-Name | ms-DS-UserEncryptedTextPasswordAllowed     |
| Taille              | \-                                         |
| Mettre à jour le privilège  | \-                                         |
| Fréquence des mises à jour  | \-                                         |
| Attribute-Id      | 1.2.840.113556.1.4.1856                    |
| System-ID-GUID    | 5a87c7f2-93c5-454c-a8c5-8cb09613292e       |
| Syntaxe            | [**Boolean**](s-boolean.md)               |



## <a name="implementations"></a>Implémentations

-   [**ADAM**](#adam)

## <a name="adam"></a>ADAM



| Entrée | Valeur |
|------------------------|-------------------------------------------------------------------|
| ID de lien                | \-                                                                |
| MAPI-Id                | \-                                                                |
| System-Only            | Faux                                                             |
| Est de valeur unique       | Vrai                                                              |
| Est indexé             | Faux                                                             |
| Dans le catalogue global      | Faux                                                             |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                                      |
| Range-Lower            | \-                                                                |
| Range-Upper            | \-                                                                |
| Search-Flags           | 0x00000000                                                        |
| System-Flags           | 0x00000010                                                        |
| Classes utilisées dans        | [**ms-DS-Bindable-objet**](c-msds-bindableobject.md)<br/> |



## <a name="remarks"></a>Notes

Dans ADAM, cet attribut remplace l’indicateur de [**\_ mot de \_ \_ \_ passe de \_ texte chiffré de publicités UF**](/windows/desktop/api/iads/ne-iads-ads_user_flag_enum) de l’attribut [**UserAccountControl**](a-useraccountcontrol.md) .

 

