---
title: attribut ms-DS-User-subout-expire-Password
description: Indique si le mot de passe du compte auquel cet attribut fait référence expire.
ms.assetid: bafbcb4a-ee45-4f88-8fb2-93840efd1289
ms.tgt_platform: multiple
keywords:
- Schéma Active Directory ms-DS-User-subout-expire-Password Attribute
- Schéma Active Directory de l’attribut msDS-UserDontExpirePassword
topic_type:
- apiref
api_name:
- ms-DS-User-Dont-Expire-Password
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 75d5c0fa709f549a523d628433ee2b3aa626278e
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104107767"
---
# <a name="ms-ds-user-dont-expire-password-attribute"></a>attribut ms-DS-User-subout-expire-Password

Indique si le mot de passe du compte auquel cet attribut fait référence expire. True si le mot de passe n’expire pas ; Sinon, false.



| Entrée | Valeur |
|-------------------|--------------------------------------|
| CN                | ms-DS-User-no-expire-Password      |
| LDAP-Display-Name | msDS-UserDontExpirePassword          |
| Taille              | \-                                   |
| Mettre à jour le privilège  | \-                                   |
| Fréquence des mises à jour  | \-                                   |
| Attribute-Id      | 1.2.840.113556.1.4.1855              |
| System-ID-GUID    | 8788193a-2925-43d9-a221-bb7fff397675 |
| Syntaxe            | [**Boolean**](s-boolean.md)         |



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

Dans ADAM, cet attribut remplace l’indicateur passwd des publicités qui n' [**\_ \_ \_ expirent \_**](/windows/desktop/api/iads/ne-iads-ads_user_flag_enum) pas de l’attribut [**UserAccountControl**](a-useraccountcontrol.md) .

 

