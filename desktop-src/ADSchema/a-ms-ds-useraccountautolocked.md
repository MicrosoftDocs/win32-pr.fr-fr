---
title: ms-DS-User-Account-attribut verrouillé automatiquement
description: Indique si le compte auquel cet attribut fait référence a été verrouillé.
ms.assetid: f9d9c98a-3c4f-4687-8133-4476aeec10e8
ms.tgt_platform: multiple
keywords:
- Schéma Active Directory ms-DS-User-Account-auto-Locked
- Schéma AD de l’attribut ms-DS-UserAccountAutoLocked
topic_type:
- apiref
api_name:
- ms-DS-User-Account-Auto-Locked
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6623a1b348af14fecc8dab41a44439bf2d745bf9
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104033348"
---
# <a name="ms-ds-user-account-auto-locked-attribute"></a>ms-DS-User-Account-attribut verrouillé automatiquement

Indique si le compte auquel cet attribut fait référence a été verrouillé. True si le compte est verrouillé ; Sinon, false.



| Entrée | Valeur |
|-------------------|--------------------------------------|
| CN                | ms-DS-User-Account-auto-verrouillé       |
| LDAP-Display-Name | ms-DS-UserAccountAutoLocked          |
| Taille              | \-                                   |
| Mettre à jour le privilège  | \-                                   |
| Fréquence des mises à jour  | \-                                   |
| Attribute-Id      | 1.2.840.113556.1.4.1857              |
| System-ID-GUID    | f2dd7bab-1f3b-47cf-89fa-143b56ad0a3d |
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



## <a name="remarks"></a>Notes

Dans ADAM, cet attribut remplace l’indicateur de [**\_ \_ verrouillage des publicités UF**](/windows/desktop/api/iads/ne-iads-ads_user_flag_enum) de l’attribut [**UserAccountControl**](a-useraccountcontrol.md) .

 

