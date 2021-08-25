---
title: Attribut SD-Rights-effective
description: Cet attribut construit retourne une valeur DWORD unique qui peut avoir jusqu’à trois bits Set OWNER \_ Security \_ INFORMATIONDACL \_ Security \_ INFORMATIONSACL \_ Security \_ Information Security. Si un bit est défini, l’utilisateur dispose d’un accès en écriture à la partie correspondante du descripteur de sécurité. Owner correspond à la fois au propriétaire et au groupe.
ms.assetid: 66d1aefb-49be-42fc-b144-3fb95c59dd0f
ms.tgt_platform: multiple
keywords:
- Schéma AD d’attribut de haute qualité SD
- Schéma AD de l’attribut sDRightsEffective
topic_type:
- apiref
api_name:
- SD-Rights-Effective
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d65591c935955133ca004c066249e9c6ec4a2effa102ad8b0e2650e6e5155749
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119923219"
---
# <a name="sd-rights-effective-attribute"></a>Attribut SD-Rights-effective

Cet attribut construit retourne une valeur **DWORD** unique qui peut avoir jusqu’à trois bits définis :

-   \_informations de sécurité du propriétaire \_
-   \_informations de sécurité DACL \_
-   \_informations de sécurité SACL \_

Si un bit est défini, l’utilisateur dispose d’un accès en écriture à la partie correspondante du descripteur de sécurité. Owner correspond à la fois au propriétaire et au groupe.



| Entrée | Valeur |
|-------------------|--------------------------------------|
| CN                | SD-droits-effectifs                  |
| LDAP-Display-Name | sDRightsEffective                    |
| Taille              | \-                                   |
| Mettre à jour le privilège  | \-                                   |
| Fréquence des mises à jour  | \-                                   |
| Attribute-Id      | 1.2.840.113556.1.4.1304              |
| System-ID-GUID    | c3dbafa6-33df-11d2-98b2-0000f87a57d4 |
| Syntaxe            | [**Énumération**](s-enumeration.md) |



## <a name="implementations"></a>Implémentations

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**ADAM**](#adam)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server



| Entrée | Valeur |
|------------------------|---------------------------------|
| ID de lien                | \-                              |
| MAPI-Id                | \-                              |
| System-Only            | Faux                           |
| Est de valeur unique       | Vrai                            |
| Est indexé             | Faux                           |
| Dans le catalogue global      | Faux                           |
| Descripteur de sécurité NT | O :BAG : BAD : S :                    |
| Range-Lower            | \-                              |
| Range-Upper            | \-                              |
| Search-Flags           | 0x00000000                      |
| System-Flags           | 0x08000014                      |
| Classes utilisées dans        | [**Retour au début**](c-top.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Entrée | Valeur |
|------------------------|---------------------------------|
| ID de lien                | \-                              |
| MAPI-Id                | \-                              |
| System-Only            | Faux                           |
| Est de valeur unique       | Vrai                            |
| Est indexé             | Faux                           |
| Dans le catalogue global      | Faux                           |
| Descripteur de sécurité NT | O :BAG : BAD : S :                    |
| Range-Lower            | \-                              |
| Range-Upper            | \-                              |
| Search-Flags           | 0x00000000                      |
| System-Flags           | 0x08000014                      |
| Classes utilisées dans        | [**Retour au début**](c-top.md)<br/> |



## <a name="adam"></a>ADAM



| Entrée | Valeur |
|------------------------|---------------------------------|
| ID de lien                | \-                              |
| MAPI-Id                | \-                              |
| System-Only            | Faux                           |
| Est de valeur unique       | Vrai                            |
| Est indexé             | Faux                           |
| Dans le catalogue global      | Faux                           |
| Descripteur de sécurité NT | O :BAG : BAD : S :                    |
| Range-Lower            | \-                              |
| Range-Upper            | \-                              |
| Search-Flags           | 0x00000000                      |
| System-Flags           | 0x08000014                      |
| Classes utilisées dans        | [**Retour au début**](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrée | Valeur |
|------------------------|---------------------------------|
| ID de lien                | \-                              |
| MAPI-Id                | \-                              |
| System-Only            | Faux                           |
| Est de valeur unique       | Vrai                            |
| Est indexé             | Faux                           |
| Dans le catalogue global      | Faux                           |
| Descripteur de sécurité NT | O :BAG : BAD : S :                    |
| Range-Lower            | \-                              |
| Range-Upper            | \-                              |
| Search-Flags           | 0x00000000                      |
| System-Flags           | 0x08000014                      |
| Classes utilisées dans        | [**Retour au début**](c-top.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrée | Valeur |
|------------------------|---------------------------------|
| ID de lien                | \-                              |
| MAPI-Id                | \-                              |
| System-Only            | Faux                           |
| Est de valeur unique       | Vrai                            |
| Est indexé             | Faux                           |
| Dans le catalogue global      | Faux                           |
| Descripteur de sécurité NT | O :BAG : BAD : S :                    |
| Range-Lower            | \-                              |
| Range-Upper            | \-                              |
| Search-Flags           | 0x00000000                      |
| System-Flags           | 0x08000014                      |
| Classes utilisées dans        | [**Retour au début**](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrée | Valeur |
|------------------------|---------------------------------|
| ID de lien                | \-                              |
| MAPI-Id                | \-                              |
| System-Only            | Faux                           |
| Est de valeur unique       | Vrai                            |
| Est indexé             | Faux                           |
| Dans le catalogue global      | Faux                           |
| Descripteur de sécurité NT | O :BAG : BAD : S :                    |
| Range-Lower            | \-                              |
| Range-Upper            | \-                              |
| Search-Flags           | 0x00000000                      |
| System-Flags           | 0x08000014                      |
| Classes utilisées dans        | [**Retour au début**](c-top.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrée | Valeur |
|------------------------|---------------------------------|
| ID de lien                | \-                              |
| MAPI-Id                | \-                              |
| System-Only            | Faux                           |
| Est de valeur unique       | Vrai                            |
| Est indexé             | Faux                           |
| Dans le catalogue global      | Faux                           |
| Descripteur de sécurité NT | O :BAG : BAD : S :                    |
| Range-Lower            | \-                              |
| Range-Upper            | \-                              |
| Search-Flags           | 0x00000000                      |
| System-Flags           | 0x08000014                      |
| Classes utilisées dans        | [**Retour au début**](c-top.md)<br/> |



 

 





