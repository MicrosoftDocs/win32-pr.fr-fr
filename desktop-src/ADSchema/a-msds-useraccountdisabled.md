---
title: attribut ms-DS-User-Account-Disabled
description: Indique si un compte est activé ou désactivé.
ms.assetid: 5d6ced7b-ca0f-4afa-b394-e61e80454f3d
ms.tgt_platform: multiple
keywords:
- Schéma Active Directory ms-DS-User-Account-Disabled Attribute
- Schéma Active Directory de l’attribut msDS-UserAccountDisabled
topic_type:
- apiref
api_name:
- ms-DS-User-Account-Disabled
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 30a01c0b83599a8d6309f6639b94f5d0321180df
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104480341"
---
# <a name="ms-ds-user-account-disabled-attribute"></a>attribut ms-DS-User-Account-Disabled

Indique si un compte est activé ou désactivé. True si le compte est désactivé ; Sinon, false.



| Entrée | Valeur |
|-------------------|--------------------------------------|
| CN                | ms-DS-User-Account-désactivé          |
| LDAP-Display-Name | msDS-UserAccountDisabled             |
| Taille              | \-                                   |
| Mettre à jour le privilège  | \-                                   |
| Fréquence des mises à jour  | \-                                   |
| Attribute-Id      | 1.2.840.113556.1.4.1853              |
| System-ID-GUID    | 7c708658-7372-4211-b22b-13a45ffd1d61 |
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

Dans ADAM, cet attribut remplace l' [**indicateur \_ \_ ACCOUNTDISABLE de publicités UF**](/windows/desktop/api/iads/ne-iads-ads_user_flag_enum) de l’attribut [**UserAccountControl**](a-useraccountcontrol.md) .

 

