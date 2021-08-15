---
title: Attribut MSMQ-Sign-Certificates
description: Cet attribut contient un certain nombre de certificats. Un utilisateur peut générer un certificat par ordinateur. Pour chaque certificat, nous conservons également un condensé.
ms.assetid: 70e182c7-3544-43d7-b27a-6e8d03bd2d47
ms.tgt_platform: multiple
keywords:
- Schéma AD des attributs de certificats de signature MSMQ
- Schéma AD de l’attribut mSMQSignCertificates
topic_type:
- apiref
api_name:
- MSMQ-Sign-Certificates
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 89ee82a5a2bf64acc315dfb535ca6897261ef0cb26f5e249a8c8593cc492b53c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119081743"
---
# <a name="msmq-sign-certificates-attribute"></a>Attribut MSMQ-Sign-Certificates

Cet attribut contient un certain nombre de certificats. Un utilisateur peut générer un certificat par ordinateur. Pour chaque certificat, nous conservons également un condensé.



| Entrée | Valeur |
|-------------------|----------------------------------------------------------------------------------------|
| CN                | Certificats de signature MSMQ                                                                 |
| LDAP-Display-Name | mSMQSignCertificates                                                                   |
| Taille              | Le type d’attribut est un objet BLOB, la taille n’est pas limitée et les données sont conservées dans notre propre format. |
| Mettre à jour le privilège  | \-                                                                                     |
| Fréquence des mises à jour  | \-                                                                                     |
| Attribute-Id      | 1.2.840.113556.1.4.947                                                                 |
| System-ID-GUID    | 9a0dc33b-c100-11d1-bbc5-0080c76670c0                                                   |
| Syntaxe            | [**Object(Replica-Link)**](s-object-replica-link.md)                                  |



## <a name="implementations"></a>Implémentations

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
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



 

 





