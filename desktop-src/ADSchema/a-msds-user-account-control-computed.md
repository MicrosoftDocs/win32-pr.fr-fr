---
title: attribut calculé ms-DS-User-Account-Control
description: msDS-User-Account-Control-controled s’apparente à userAccountControl, mais la valeur de l’attribut peut contenir des bits supplémentaires qui ne sont pas persistants.
ms.assetid: 4c635c04-8d2e-41b4-809c-58ce64271a02
ms.tgt_platform: multiple
keywords:
- Schéma AD de l’attribut calculé ms-DS-User-Account-Control
- Schéma Active Directory msDS-User-Account-Control-attribut calculé
topic_type:
- apiref
api_name:
- ms-DS-User-Account-Control-Computed
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8747bddccdfa65222072592b7f418fd35529d987f9903d71cddf5e01556fec53
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119763259"
---
# <a name="ms-ds-user-account-control-computed-attribute"></a>attribut calculé ms-DS-User-Account-Control

**MSDS-User-Account-Control-controled** s’apparente à [**UserAccountControl**](a-useraccountcontrol.md), mais la valeur de l’attribut peut contenir des bits supplémentaires qui ne sont pas persistants. Les bits calculés sont les suivants :



| Valeur                | Name (défini dans IADs. h)                     |
|----------------------|----------------------------------------------|
| 0x0010<br/>    | **\_verrouillage uf**<br/>                   |
| 0x800000<br/>  | **\_mot de passe UF \_ expiré**<br/>         |
| 0x4000000<br/> | **\_compte de \_ secrets PARTIELs UF \_**<br/> |
| 0x8000000<br/> | **UF \_ utiliser \_ des \_ clés AES**<br/>            |



 

La liste complète des bits utilisés par le contrôle de [**compte**](a-useraccountcontrol.md) d’utilisateur et, par conséquent, le contrôle de compte d' **utilisateur MSDS** peut également être trouvée dans la page de référence de **contrôle de compte d’utilisateur** (mappée via l’FlagSet [ADSI](/windows/desktop/ADSI/active-directory-service-interfaces-adsi) ) ou sur les pages de référence de gestion de réseau pour la structure [**\_ informations utilisateur \_ 1008**](/windows/desktop/api/lmaccess/ns-lmaccess-user_info_1008) .



| Entrée | Valeur |
|-------------------|--------------------------------------|
| CN                | ms-DS-utilisateur-compte-contrôle-calculé  |
| LDAP-Display-Name | msDS-User-Account-Control-calculé   |
| Taille              | \-                                   |
| Mettre à jour le privilège  | \-                                   |
| Fréquence des mises à jour  | \-                                   |
| Attribute-Id      | 1.2.840.113556.1.4.1460              |
| System-ID-GUID    | 2cc4b836-b63f-4940-8d23-ea7acf06af56 |
| Syntaxe            | [**Énumération**](s-enumeration.md) |



## <a name="implementations"></a>Implémentations

-   [**Windows Server 2003**](#windows-server-2003)
-   [**ADAM**](#adam)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-server-2003"></a>Windows Server 2003



| Entrée | Valeur |
|------------------------|-----------------------------------|
| ID de lien                | \-                                |
| MAPI-Id                | \-                                |
| System-Only            | Faux                             |
| Est de valeur unique       | Vrai                              |
| Est indexé             | Faux                             |
| Dans le catalogue global      | Faux                             |
| Descripteur de sécurité NT | O :BAG : BAD : S :                      |
| Range-Lower            | \-                                |
| Range-Upper            | \-                                |
| Search-Flags           | 0x00000000                        |
| System-Flags           | 0x00000014                        |
| Classes utilisées dans        | [**Utilisateur**](c-user.md)<br/> |



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



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrée | Valeur |
|------------------------|-----------------------------------|
| ID de lien                | \-                                |
| MAPI-Id                | \-                                |
| System-Only            | Faux                             |
| Est de valeur unique       | Vrai                              |
| Est indexé             | Faux                             |
| Dans le catalogue global      | Faux                             |
| Descripteur de sécurité NT | O :BAG : BAD : S :                      |
| Range-Lower            | \-                                |
| Range-Upper            | \-                                |
| Search-Flags           | 0x00000000                        |
| System-Flags           | 0x00000014                        |
| Classes utilisées dans        | [**Utilisateur**](c-user.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrée | Valeur |
|------------------------|-----------------------------------|
| ID de lien                | \-                                |
| MAPI-Id                | \-                                |
| System-Only            | Faux                             |
| Est de valeur unique       | Vrai                              |
| Est indexé             | Faux                             |
| Dans le catalogue global      | Faux                             |
| Descripteur de sécurité NT | O :BAG : BAD : S :                      |
| Range-Lower            | \-                                |
| Range-Upper            | \-                                |
| Search-Flags           | 0x00000000                        |
| System-Flags           | 0x00000014                        |
| Classes utilisées dans        | [**Utilisateur**](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrée | Valeur |
|------------------------|-----------------------------------|
| ID de lien                | \-                                |
| MAPI-Id                | \-                                |
| System-Only            | Faux                             |
| Est de valeur unique       | Vrai                              |
| Est indexé             | Faux                             |
| Dans le catalogue global      | Faux                             |
| Descripteur de sécurité NT | O :BAG : BAD : S :                      |
| Range-Lower            | \-                                |
| Range-Upper            | \-                                |
| Search-Flags           | 0x00000000                        |
| System-Flags           | 0x00000014                        |
| Classes utilisées dans        | [**Utilisateur**](c-user.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrée | Valeur |
|------------------------|-----------------------------------|
| ID de lien                | \-                                |
| MAPI-Id                | \-                                |
| System-Only            | Faux                             |
| Est de valeur unique       | Vrai                              |
| Est indexé             | Faux                             |
| Dans le catalogue global      | Faux                             |
| Descripteur de sécurité NT | O :BAG : BAD : S :                      |
| Range-Lower            | \-                                |
| Range-Upper            | \-                                |
| Search-Flags           | 0x00000000                        |
| System-Flags           | 0x00000014                        |
| Classes utilisées dans        | [**Utilisateur**](c-user.md)<br/> |



 

