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
ms.openlocfilehash: 7af661ca1317f7506e5bcdbf611010b0fe4c058d5f1e3f1e5f31b917737a6e64
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118425429"
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



## <a name="remarks"></a>Remarques

Dans ADAM, cet attribut remplace l’indicateur passwd des publicités qui n' [**\_ \_ \_ expirent \_**](/windows/desktop/api/iads/ne-iads-ads_user_flag_enum) pas de l’attribut [**UserAccountControl**](a-useraccountcontrol.md) .

 

