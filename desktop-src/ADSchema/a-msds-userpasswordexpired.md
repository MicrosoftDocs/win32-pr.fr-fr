---
title: attribut ms-DS-User-Password-expirés
description: Indique si le mot de passe du compte auquel cet attribut fait référence a expiré.
ms.assetid: cab4a2e8-b440-45d2-8da8-9f020ffee08c
ms.tgt_platform: multiple
keywords:
- Schéma AD de l’attribut ms-DS-User-Password-expirer
- Schéma Active Directory de l’attribut msDS-UserPasswordExpired
topic_type:
- apiref
api_name:
- ms-DS-User-Password-Expired
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a187f9d0b2be2feeca076d7c7eef82a34ca5827a9d07c76b2d711a5196f84ba8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118425355"
---
# <a name="ms-ds-user-password-expired-attribute"></a>attribut ms-DS-User-Password-expirés

Indique si le mot de passe du compte auquel cet attribut fait référence a expiré. True si le mot de passe a expiré ; Sinon, false.



| Entrée | Valeur |
|-------------------|--------------------------------------|
| CN                | ms-DS-utilisateur-mot de passe-expiré          |
| LDAP-Display-Name | msDS-UserPasswordExpired             |
| Taille              | \-                                   |
| Mettre à jour le privilège  | \-                                   |
| Fréquence des mises à jour  | \-                                   |
| Attribute-Id      | 1.2.840.113556.1.4.1858              |
| System-ID-GUID    | 565c7ab5-e13e-47f6-abb5-de741806f125 |
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
| System-Flags           | 0x00000014                                                        |
| Classes utilisées dans        | [**ms-DS-Bindable-objet**](c-msds-bindableobject.md)<br/> |



## <a name="remarks"></a>Remarques

Dans ADAM, cet attribut remplace l’indicateur de [**mot de passe de publicités \_ \_ \_ UF**](/windows/desktop/api/iads/ne-iads-ads_user_flag_enum) de l’attribut [**UserAccountControl**](a-useraccountcontrol.md) .

 

