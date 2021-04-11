---
title: ACS-DSBM-Priority (attribut)
description: Cet attribut contient la priorité de ce gestionnaire de bande passante de réseau (SBM).
ms.assetid: 08dd49d2-a2fa-4707-8302-25566680b91d
ms.tgt_platform: multiple
keywords:
- ACS-DSBM-schéma AD d’attribut de priorité
- Schéma AD de l’attribut aCSDSBMPriority
topic_type:
- apiref
api_name:
- ACS-DSBM-Priority
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6dd32c9e9cca95dbd5f52569de0b61e886033d13
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104108323"
---
# <a name="acs-dsbm-priority-attribute"></a>ACS-DSBM-Priority (attribut)

Cet attribut contient la priorité de ce gestionnaire de bande passante de réseau (SBM). Lorsqu’un nouveau DSBM (Subnet Bandwidth Manager) désigné doit être choisi, cette valeur est envoyée à d’autres SBMs dans le domaine dans le cadre d’un message de demande de \_ prêt. Le SBM avec la priorité la plus élevée est élu comme nouveau DSBM.



| Entrée | Valeur |
|-------------------|--------------------------------------|
| CN                | ACS-DSBM-Priority                    |
| LDAP-Display-Name | aCSDSBMPriority                      |
| Taille              | 4 octets                              |
| Mettre à jour le privilège  | \-                                   |
| Fréquence des mises à jour  | \-                                   |
| Attribute-Id      | 1.2.840.113556.1.4.776               |
| System-ID-GUID    | 1cb3559e-56d0-11d1-a9c6-0000f80367c1 |
| Syntaxe            | [**Enumeration**](s-enumeration.md) |



## <a name="implementations"></a>Implémentations

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server



| Entrée | Valeur |
|------------------------|----------------------------------------------|
| ID de lien                | \-                                           |
| MAPI-Id                | \-                                           |
| System-Only            | Faux                                        |
| Est de valeur unique       | Vrai                                         |
| Est indexé             | Faux                                        |
| Dans le catalogue global      | Faux                                        |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                 |
| Range-Lower            | \-                                           |
| Range-Upper            | \-                                           |
| Search-Flags           | 0x00000000                                   |
| System-Flags           | 0x00000010                                   |
| Classes utilisées dans        | [**ACS-sous-réseau**](c-acssubnet.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Entrée | Valeur |
|------------------------|----------------------------------------------|
| ID de lien                | \-                                           |
| MAPI-Id                | \-                                           |
| System-Only            | Faux                                        |
| Est de valeur unique       | Vrai                                         |
| Est indexé             | Faux                                        |
| Dans le catalogue global      | Faux                                        |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                 |
| Range-Lower            | \-                                           |
| Range-Upper            | \-                                           |
| Search-Flags           | 0x00000000                                   |
| System-Flags           | 0x00000010                                   |
| Classes utilisées dans        | [**ACS-sous-réseau**](c-acssubnet.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrée | Valeur |
|------------------------|----------------------------------------------|
| ID de lien                | \-                                           |
| MAPI-Id                | \-                                           |
| System-Only            | Faux                                        |
| Est de valeur unique       | Vrai                                         |
| Est indexé             | Faux                                        |
| Dans le catalogue global      | Faux                                        |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                 |
| Range-Lower            | \-                                           |
| Range-Upper            | \-                                           |
| Search-Flags           | 0x00000000                                   |
| System-Flags           | 0x00000010                                   |
| Classes utilisées dans        | [**ACS-sous-réseau**](c-acssubnet.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrée | Valeur |
|------------------------|----------------------------------------------|
| ID de lien                | \-                                           |
| MAPI-Id                | \-                                           |
| System-Only            | Faux                                        |
| Est de valeur unique       | Vrai                                         |
| Est indexé             | Faux                                        |
| Dans le catalogue global      | Faux                                        |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                 |
| Range-Lower            | \-                                           |
| Range-Upper            | \-                                           |
| Search-Flags           | 0x00000000                                   |
| System-Flags           | 0x00000010                                   |
| Classes utilisées dans        | [**ACS-sous-réseau**](c-acssubnet.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrée | Valeur |
|------------------------|----------------------------------------------|
| ID de lien                | \-                                           |
| MAPI-Id                | \-                                           |
| System-Only            | Faux                                        |
| Est de valeur unique       | Vrai                                         |
| Est indexé             | Faux                                        |
| Dans le catalogue global      | Faux                                        |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                 |
| Range-Lower            | \-                                           |
| Range-Upper            | \-                                           |
| Search-Flags           | 0x00000000                                   |
| System-Flags           | 0x00000010                                   |
| Classes utilisées dans        | [**ACS-sous-réseau**](c-acssubnet.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrée | Valeur |
|------------------------|----------------------------------------------|
| ID de lien                | \-                                           |
| MAPI-Id                | \-                                           |
| System-Only            | Faux                                        |
| Est de valeur unique       | Vrai                                         |
| Est indexé             | Faux                                        |
| Dans le catalogue global      | Faux                                        |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                 |
| Range-Lower            | \-                                           |
| Range-Upper            | \-                                           |
| Search-Flags           | 0x00000000                                   |
| System-Flags           | 0x00000010                                   |
| Classes utilisées dans        | [**ACS-sous-réseau**](c-acssubnet.md)<br/> |



 

 





