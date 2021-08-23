---
title: Attribut Schema-Info
description: Valeur binaire interne utilisée pour détecter les modifications de schéma entre les contrôleurs de schéma et forcer un cycle de réplication NC de schéma avant la réplication d’un autre contexte de nommage. Utilisé pour résoudre les liens lorsque le FSMO de schéma est pris et qu’une modification est apportée sur plusieurs contrôleurs de périphérique.
ms.assetid: 416cef3f-211b-439d-b177-267806c6a5d2
ms.tgt_platform: multiple
keywords:
- Schéma AD d’attribut Schema-Info
- Schéma AD de l’attribut schemaInfo
topic_type:
- apiref
api_name:
- Schema-Info
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cfa0d55dd29f207b84b0951ee448ba988d128fabfd126f38b2a4692d7cd3e0fa
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119646528"
---
# <a name="schema-info-attribute"></a>Attribut Schema-Info

Valeur binaire interne utilisée pour détecter les modifications de schéma entre les contrôleurs de schéma et forcer un cycle de réplication NC de schéma avant la réplication d’un autre contexte de nommage. Utilisé pour résoudre les liens lorsque le FSMO de schéma est pris et qu’une modification est apportée sur plusieurs contrôleurs de périphérique.



| Entrée | Valeur |
|-------------------|-------------------------------------------------------|
| CN                | Schema-Info                                           |
| LDAP-Display-Name | schemaInfo                                            |
| Taille              | \-                                                    |
| Mettre à jour le privilège  | Cette valeur est définie par le système.                      |
| Fréquence des mises à jour  | \-                                                    |
| Attribute-Id      | 1.2.840.113556.1.4.1358                               |
| System-ID-GUID    | f9fb64ae-93b4-11d2-9945-0000f87a57d4                  |
| Syntaxe            | [**Object(Replica-Link)**](s-object-replica-link.md) |



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
| System-Only            | Vrai                            |
| Est de valeur unique       | Faux                           |
| Est indexé             | Faux                           |
| Dans le catalogue global      | Faux                           |
| Descripteur de sécurité NT | O :BAG : BAD : S :                    |
| Range-Lower            | \-                              |
| Range-Upper            | \-                              |
| Search-Flags           | 0x00000000                      |
| System-Flags           | 0x00000010                      |
| Classes utilisées dans        | [**DMD**](c-dmd.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Entrée | Valeur |
|------------------------|---------------------------------|
| ID de lien                | \-                              |
| MAPI-Id                | \-                              |
| System-Only            | Vrai                            |
| Est de valeur unique       | Faux                           |
| Est indexé             | Faux                           |
| Dans le catalogue global      | Faux                           |
| Descripteur de sécurité NT | O :BAG : BAD : S :                    |
| Range-Lower            | \-                              |
| Range-Upper            | \-                              |
| Search-Flags           | 0x00000000                      |
| System-Flags           | 0x00000010                      |
| Classes utilisées dans        | [**DMD**](c-dmd.md)<br/> |



## <a name="adam"></a>ADAM



| Entrée | Valeur |
|------------------------|---------------------------------|
| ID de lien                | \-                              |
| MAPI-Id                | \-                              |
| System-Only            | Vrai                            |
| Est de valeur unique       | Faux                           |
| Est indexé             | Faux                           |
| Dans le catalogue global      | Faux                           |
| Descripteur de sécurité NT | O :BAG : BAD : S :                    |
| Range-Lower            | \-                              |
| Range-Upper            | \-                              |
| Search-Flags           | 0x00000000                      |
| System-Flags           | 0x00000010                      |
| Classes utilisées dans        | [**DMD**](c-dmd.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrée | Valeur |
|------------------------|---------------------------------|
| ID de lien                | \-                              |
| MAPI-Id                | \-                              |
| System-Only            | Vrai                            |
| Est de valeur unique       | Faux                           |
| Est indexé             | Faux                           |
| Dans le catalogue global      | Faux                           |
| Descripteur de sécurité NT | O :BAG : BAD : S :                    |
| Range-Lower            | \-                              |
| Range-Upper            | \-                              |
| Search-Flags           | 0x00000000                      |
| System-Flags           | 0x00000010                      |
| Classes utilisées dans        | [**DMD**](c-dmd.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrée | Valeur |
|------------------------|---------------------------------|
| ID de lien                | \-                              |
| MAPI-Id                | \-                              |
| System-Only            | Vrai                            |
| Est de valeur unique       | Faux                           |
| Est indexé             | Faux                           |
| Dans le catalogue global      | Faux                           |
| Descripteur de sécurité NT | O :BAG : BAD : S :                    |
| Range-Lower            | \-                              |
| Range-Upper            | \-                              |
| Search-Flags           | 0x00000000                      |
| System-Flags           | 0x00000010                      |
| Classes utilisées dans        | [**DMD**](c-dmd.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrée | Valeur |
|------------------------|---------------------------------|
| ID de lien                | \-                              |
| MAPI-Id                | \-                              |
| System-Only            | Vrai                            |
| Est de valeur unique       | Faux                           |
| Est indexé             | Faux                           |
| Dans le catalogue global      | Faux                           |
| Descripteur de sécurité NT | O :BAG : BAD : S :                    |
| Range-Lower            | \-                              |
| Range-Upper            | \-                              |
| Search-Flags           | 0x00000000                      |
| System-Flags           | 0x00000010                      |
| Classes utilisées dans        | [**DMD**](c-dmd.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrée | Valeur |
|------------------------|---------------------------------|
| ID de lien                | \-                              |
| MAPI-Id                | \-                              |
| System-Only            | Vrai                            |
| Est de valeur unique       | Faux                           |
| Est indexé             | Faux                           |
| Dans le catalogue global      | Faux                           |
| Descripteur de sécurité NT | O :BAG : BAD : S :                    |
| Range-Lower            | \-                              |
| Range-Upper            | \-                              |
| Search-Flags           | 0x00000000                      |
| System-Flags           | 0x00000010                      |
| Classes utilisées dans        | [**DMD**](c-dmd.md)<br/> |



 

 





