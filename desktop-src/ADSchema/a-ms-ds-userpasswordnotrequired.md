---
title: ms-DS-User-Password-not-required (attribut)
description: Indique si un mot de passe est requis pour le compte auquel cet attribut fait référence.
ms.assetid: 86779c6f-d05c-409a-afe4-99ebf7c0593e
ms.tgt_platform: multiple
keywords:
- Schéma AD de l’attribut ms-DS-User-Password-not-required
- Schéma AD de l’attribut ms-DS-UserPasswordNotRequired
topic_type:
- apiref
api_name:
- ms-DS-User-Password-Not-Required
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c8ebb439af9a960d2dc0721940d9f4d2ab852b6
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104108211"
---
# <a name="ms-ds-user-password-not-required-attribute"></a>ms-DS-User-Password-not-required (attribut)

Indique si un mot de passe est requis pour le compte auquel cet attribut fait référence. True si un mot de passe n’est pas requis ; Sinon, false.



| Entrée | Valeur |
|-------------------|--------------------------------------|
| CN                | ms-DS-utilisateur-mot de passe-non-requis     |
| LDAP-Display-Name | ms-DS-UserPasswordNotRequired        |
| Taille              | \-                                   |
| Mettre à jour le privilège  | \-                                   |
| Fréquence des mises à jour  | \-                                   |
| Attribute-Id      | 1.2.840.113556.1.4.1854              |
| System-ID-GUID    | 8f066172-a25e-4f53-8dcd-0a67d5fb883d |
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

Dans ADAM, cet attribut remplace l' [**indicateur \_ ADS \_ \_ NOTREQD passwd**](/windows/desktop/api/iads/ne-iads-ads_user_flag_enum) de l’attribut [**UserAccountControl**](a-useraccountcontrol.md) .

 

