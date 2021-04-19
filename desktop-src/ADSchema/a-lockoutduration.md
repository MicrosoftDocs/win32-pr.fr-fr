---
title: Attribut Lockout-Duration
description: Durée de verrouillage d’un compte en raison du dépassement de la Lockout-Threshold.
ms.assetid: 6a26ef80-86ed-433f-9032-cdd1aaf00388
ms.tgt_platform: multiple
keywords:
- Schéma AD d’attribut Lockout-Duration
- Schéma AD de l’attribut lockoutDuration
topic_type:
- apiref
api_name:
- Lockout-Duration
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 526fedef47bea20148a591259dbc7ec1702b5a15
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "106509956"
---
# <a name="lockout-duration-attribute"></a>Attribut Lockout-Duration

Durée de verrouillage d’un compte en raison du dépassement du [**seuil de verrouillage**](a-lockoutthreshold.md) . Cette valeur est stockée sous la forme d’un entier long qui représente la valeur négative du nombre d’intervalles de 100 nanosecondes à partir du moment où le [**seuil de verrouillage**](a-lockoutthreshold.md) est dépassé avant le déverrouillage du compte.



| Entrée | Valeur |
|-------------------|--------------------------------------|
| CN                | Lockout-Duration                     |
| LDAP-Display-Name | lockoutDuration                      |
| Taille              | \-                                   |
| Mettre à jour le privilège  | Administrateur de domaine                 |
| Fréquence des mises à jour  | \-                                   |
| Attribute-Id      | 1.2.840.113556.1.4.60                |
| System-ID-GUID    | bf9679a5-0de6-11d0-a285-00aa003049e2 |
| Syntaxe            | [**Défini**](s-interval.md)       |



## <a name="implementations"></a>Implémentations

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server



| Entrée | Valeur |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID de lien                | \-                                                                                                                                                    |
| MAPI-Id                | \-                                                                                                                                                    |
| System-Only            | Faux                                                                                                                                                 |
| Est de valeur unique       | Vrai                                                                                                                                                  |
| Est indexé             | Faux                                                                                                                                                 |
| Dans le catalogue global      | Faux                                                                                                                                                 |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                                                                                                                          |
| Range-Lower            | \-                                                                                                                                                    |
| Range-Upper            | \-                                                                                                                                                    |
| Search-Flags           | 0x00000000                                                                                                                                            |
| System-Flags           | 0x00000010                                                                                                                                            |
| Classes utilisées dans        | [**Stratégie de domaine**](c-domainpolicy.md)<br/> [**Sam-domaine**](c-samdomain.md)<br/> [**Sam-domaine-base**](c-samdomainbase.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Entrée | Valeur |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID de lien                | \-                                                                                                                                                    |
| MAPI-Id                | \-                                                                                                                                                    |
| System-Only            | Faux                                                                                                                                                 |
| Est de valeur unique       | Vrai                                                                                                                                                  |
| Est indexé             | Faux                                                                                                                                                 |
| Dans le catalogue global      | Faux                                                                                                                                                 |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                                                                                                                          |
| Range-Lower            | \-                                                                                                                                                    |
| Range-Upper            | \-                                                                                                                                                    |
| Search-Flags           | 0x00000000                                                                                                                                            |
| System-Flags           | 0x00000010                                                                                                                                            |
| Classes utilisées dans        | [**Stratégie de domaine**](c-domainpolicy.md)<br/> [**Sam-domaine**](c-samdomain.md)<br/> [**Sam-domaine-base**](c-samdomainbase.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrée | Valeur |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID de lien                | \-                                                                                                                                                    |
| MAPI-Id                | \-                                                                                                                                                    |
| System-Only            | Faux                                                                                                                                                 |
| Est de valeur unique       | Vrai                                                                                                                                                  |
| Est indexé             | Faux                                                                                                                                                 |
| Dans le catalogue global      | Faux                                                                                                                                                 |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                                                                                                                          |
| Range-Lower            | \-                                                                                                                                                    |
| Range-Upper            | \-                                                                                                                                                    |
| Search-Flags           | 0x00000000                                                                                                                                            |
| System-Flags           | 0x00000010                                                                                                                                            |
| Classes utilisées dans        | [**Stratégie de domaine**](c-domainpolicy.md)<br/> [**Sam-domaine**](c-samdomain.md)<br/> [**Sam-domaine-base**](c-samdomainbase.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrée | Valeur |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID de lien                | \-                                                                                                                                                    |
| MAPI-Id                | \-                                                                                                                                                    |
| System-Only            | Faux                                                                                                                                                 |
| Est de valeur unique       | Vrai                                                                                                                                                  |
| Est indexé             | Faux                                                                                                                                                 |
| Dans le catalogue global      | Faux                                                                                                                                                 |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                                                                                                                          |
| Range-Lower            | \-                                                                                                                                                    |
| Range-Upper            | \-                                                                                                                                                    |
| Search-Flags           | 0x00000000                                                                                                                                            |
| System-Flags           | 0x00000010                                                                                                                                            |
| Classes utilisées dans        | [**Stratégie de domaine**](c-domainpolicy.md)<br/> [**Sam-domaine**](c-samdomain.md)<br/> [**Sam-domaine-base**](c-samdomainbase.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrée | Valeur |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID de lien                | \-                                                                                                                                                    |
| MAPI-Id                | \-                                                                                                                                                    |
| System-Only            | Faux                                                                                                                                                 |
| Est de valeur unique       | Vrai                                                                                                                                                  |
| Est indexé             | Faux                                                                                                                                                 |
| Dans le catalogue global      | Faux                                                                                                                                                 |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                                                                                                                          |
| Range-Lower            | \-                                                                                                                                                    |
| Range-Upper            | \-                                                                                                                                                    |
| Search-Flags           | 0x00000000                                                                                                                                            |
| System-Flags           | 0x00000010                                                                                                                                            |
| Classes utilisées dans        | [**Stratégie de domaine**](c-domainpolicy.md)<br/> [**Sam-domaine**](c-samdomain.md)<br/> [**Sam-domaine-base**](c-samdomainbase.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrée | Valeur |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID de lien                | \-                                                                                                                                                    |
| MAPI-Id                | \-                                                                                                                                                    |
| System-Only            | Faux                                                                                                                                                 |
| Est de valeur unique       | Vrai                                                                                                                                                  |
| Est indexé             | Faux                                                                                                                                                 |
| Dans le catalogue global      | Faux                                                                                                                                                 |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                                                                                                                          |
| Range-Lower            | \-                                                                                                                                                    |
| Range-Upper            | \-                                                                                                                                                    |
| Search-Flags           | 0x00000000                                                                                                                                            |
| System-Flags           | 0x00000010                                                                                                                                            |
| Classes utilisées dans        | [**Stratégie de domaine**](c-domainpolicy.md)<br/> [**Sam-domaine**](c-samdomain.md)<br/> [**Sam-domaine-base**](c-samdomainbase.md)<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Seuil de verrouillage**](a-lockoutthreshold.md)
</dt> </dl>

 

 





