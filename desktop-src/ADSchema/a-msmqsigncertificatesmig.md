---
title: MSMQ-Sign-Certificates-attribut MIG
description: En mode mixte MSMQ, l’attribut contient la valeur précédente de mSMQSignCertificates. MSMQ prend en charge la migration à partir du service d’annuaire MSMQ 1,0 vers le DS Windows 2000, et le mode mixte spécifie un État dans lequel certains serveurs d’annuaire n’ont pas été mis à niveau vers Windows 2000.
ms.assetid: 0dbc5d97-39e6-4863-a386-541ea2abaadc
ms.tgt_platform: multiple
keywords:
- MSMQ-Sign-Certificates-schéma AD d’attribut MIG
- Schéma AD de l’attribut mSMQSignCertificatesMig
topic_type:
- apiref
api_name:
- MSMQ-Sign-Certificates-Mig
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 91a1916cf98d15da1bd84603a2305543e899d868
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "106515289"
---
# <a name="msmq-sign-certificates-mig-attribute"></a>MSMQ-Sign-Certificates-attribut MIG

En mode mixte MSMQ, l’attribut contient la valeur précédente de mSMQSignCertificates. MSMQ prend en charge la migration à partir du service d’annuaire MSMQ 1,0 vers le DS Windows 2000, et le mode mixte spécifie un État dans lequel certains serveurs d’annuaire n’ont pas été mis à niveau vers Windows 2000.



| Entrée | Valeur |
|-------------------|-------------------------------------------------------|
| CN                | MSMQ-Sign-Certificates-MIG                            |
| LDAP-Display-Name | mSMQSignCertificatesMig                               |
| Taille              | \-                                                    |
| Mettre à jour le privilège  | \-                                                    |
| Fréquence des mises à jour  | \-                                                    |
| Attribute-Id      | 1.2.840.113556.1.4.967                                |
| System-ID-GUID    | 3881b8ea-da3b-11d1-90a5-00c04fd91ab1                  |
| Syntaxe            | [**Object(Replica-Link)**](s-object-replica-link.md) |



## <a name="implementations"></a>Implémentations

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server



| Entrée | Valeur |
|------------------------|-----------------------------------------------------------------------------------------------|
| ID de lien                | \-                                                                                            |
| MAPI-Id                | \-                                                                                            |
| System-Only            | Faux                                                                                         |
| Est de valeur unique       | Vrai                                                                                          |
| Est indexé             | Faux                                                                                         |
| Dans le catalogue global      | Vrai                                                                                          |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                                                                  |
| Range-Lower            | \-                                                                                            |
| Range-Upper            | \-                                                                                            |
| Search-Flags           | 0x00000000                                                                                    |
| System-Flags           | 0x00000010                                                                                    |
| Classes utilisées dans        | [**MSMQ-migrated-User**](c-msmqmigrateduser.md)<br/> [**Utilisateur**](c-user.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Entrée | Valeur |
|------------------------|-----------------------------------------------------------------------------------------------|
| ID de lien                | \-                                                                                            |
| MAPI-Id                | \-                                                                                            |
| System-Only            | Faux                                                                                         |
| Est de valeur unique       | Vrai                                                                                          |
| Est indexé             | Faux                                                                                         |
| Dans le catalogue global      | Vrai                                                                                          |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                                                                  |
| Range-Lower            | \-                                                                                            |
| Range-Upper            | \-                                                                                            |
| Search-Flags           | 0x00000000                                                                                    |
| System-Flags           | 0x00000010                                                                                    |
| Classes utilisées dans        | [**MSMQ-migrated-User**](c-msmqmigrateduser.md)<br/> [**Utilisateur**](c-user.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrée | Valeur |
|------------------------|-----------------------------------------------------------------------------------------------|
| ID de lien                | \-                                                                                            |
| MAPI-Id                | \-                                                                                            |
| System-Only            | Faux                                                                                         |
| Est de valeur unique       | Vrai                                                                                          |
| Est indexé             | Faux                                                                                         |
| Dans le catalogue global      | Vrai                                                                                          |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                                                                  |
| Range-Lower            | \-                                                                                            |
| Range-Upper            | \-                                                                                            |
| Search-Flags           | 0x00000000                                                                                    |
| System-Flags           | 0x00000010                                                                                    |
| Classes utilisées dans        | [**MSMQ-migrated-User**](c-msmqmigrateduser.md)<br/> [**Utilisateur**](c-user.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrée | Valeur |
|------------------------|-----------------------------------------------------------------------------------------------|
| ID de lien                | \-                                                                                            |
| MAPI-Id                | \-                                                                                            |
| System-Only            | Faux                                                                                         |
| Est de valeur unique       | Vrai                                                                                          |
| Est indexé             | Faux                                                                                         |
| Dans le catalogue global      | Vrai                                                                                          |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                                                                  |
| Range-Lower            | \-                                                                                            |
| Range-Upper            | \-                                                                                            |
| Search-Flags           | 0x00000000                                                                                    |
| System-Flags           | 0x00000010                                                                                    |
| Classes utilisées dans        | [**MSMQ-migrated-User**](c-msmqmigrateduser.md)<br/> [**Utilisateur**](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrée | Valeur |
|------------------------|-----------------------------------------------------------------------------------------------|
| ID de lien                | \-                                                                                            |
| MAPI-Id                | \-                                                                                            |
| System-Only            | Faux                                                                                         |
| Est de valeur unique       | Vrai                                                                                          |
| Est indexé             | Faux                                                                                         |
| Dans le catalogue global      | Vrai                                                                                          |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                                                                  |
| Range-Lower            | \-                                                                                            |
| Range-Upper            | \-                                                                                            |
| Search-Flags           | 0x00000000                                                                                    |
| System-Flags           | 0x00000010                                                                                    |
| Classes utilisées dans        | [**MSMQ-migrated-User**](c-msmqmigrateduser.md)<br/> [**Utilisateur**](c-user.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrée | Valeur |
|------------------------|-----------------------------------------------------------------------------------------------|
| ID de lien                | \-                                                                                            |
| MAPI-Id                | \-                                                                                            |
| System-Only            | Faux                                                                                         |
| Est de valeur unique       | Vrai                                                                                          |
| Est indexé             | Faux                                                                                         |
| Dans le catalogue global      | Vrai                                                                                          |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                                                                  |
| Range-Lower            | \-                                                                                            |
| Range-Upper            | \-                                                                                            |
| Search-Flags           | 0x00000000                                                                                    |
| System-Flags           | 0x00000010                                                                                    |
| Classes utilisées dans        | [**MSMQ-migrated-User**](c-msmqmigrateduser.md)<br/> [**Utilisateur**](c-user.md)<br/> |



 

 





