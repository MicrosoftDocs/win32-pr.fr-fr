---
title: Attribut X509-Cert
description: Contient les certificats X. 509v3 encodés DER émis à l’utilisateur. Notez que cette propriété contient les certificats de clé publique émis à cet utilisateur par le service de certificats Microsoft.
ms.assetid: bdd6b9a4-c402-462c-be2c-8e7e582a899a
ms.tgt_platform: multiple
keywords:
- Schéma AD d’attribut X509-Cert
- Schéma AD de l’attribut userCertificate
topic_type:
- apiref
api_name:
- X509-Cert
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d0d6d95ab05047c19ba978a02957dca3870c2f93cf26b323bd6aa55c2f35472a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119644589"
---
# <a name="x509-cert-attribute"></a>Attribut X509-Cert

Contient les certificats X. 509v3 encodés DER émis à l’utilisateur. Notez que cette propriété contient les certificats de clé publique émis à cet utilisateur par le service de certificats Microsoft.



| Entrée | Valeur |
|-------------------|-------------------------------------------------------------------------------------------------------------------------|
| CN                | X509-Cert                                                                                                               |
| LDAP-Display-Name | userCertificate                                                                                                         |
| Taille              | Cet attribut nécessite environ 4 Ko pour chaque certificat de l’agent de récupération de clé émis par l’autorité de certification à l’aide de l’instance KRA. |
| Mettre à jour le privilège  | Administrateur de domaine                                                                                                    |
| Fréquence des mises à jour  | Chaque fois qu’un certificat est émis.                                                                                      |
| Attribute-Id      | 2.5.4.36                                                                                                                |
| System-ID-GUID    | bf967a7f-0de6-11d0-a285-00aa003049e2                                                                                    |
| Syntaxe            | [**Object(Replica-Link)**](s-object-replica-link.md)                                                                   |



## <a name="implementations"></a>Implémentations

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server



| Entrée | Valeur |
|------------------------|----------------------------------------------------------------------------------------|
| ID de lien                | \-                                                                                     |
| MAPI-Id                | 0x8C6A                                                                                 |
| System-Only            | Faux                                                                                  |
| Est de valeur unique       | Faux                                                                                  |
| Est indexé             | Faux                                                                                  |
| Dans le catalogue global      | Vrai                                                                                   |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                                                           |
| Range-Lower            | \-                                                                                     |
| Range-Upper            | \-                                                                                     |
| Search-Flags           | 0x00000000                                                                             |
| System-Flags           | 0x00000010                                                                             |
| Classes utilisées dans        | [**E-mail-destinataire**](c-mailrecipient.md)<br/> [**Utilisateur**](c-user.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Entrée | Valeur |
|------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID de lien                | \-                                                                                                                                                                                                                                 |
| MAPI-Id                | 0x8C6A                                                                                                                                                                                                                             |
| System-Only            | Faux                                                                                                                                                                                                                              |
| Est de valeur unique       | Faux                                                                                                                                                                                                                              |
| Est indexé             | Faux                                                                                                                                                                                                                              |
| Dans le catalogue global      | Vrai                                                                                                                                                                                                                               |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                                                                                                                                                                                                       |
| Range-Lower            | \-                                                                                                                                                                                                                                 |
| Range-Upper            | \-                                                                                                                                                                                                                                 |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                         |
| System-Flags           | 0x00000010                                                                                                                                                                                                                         |
| Classes utilisées dans        | [**inetOrgPerson**](c-inetorgperson.md)<br/> [**E-mail-destinataire**](c-mailrecipient.md)<br/> [**MS-PKI-privé-clé-Recovery-agent**](c-mspki-privatekeyrecoveryagent.md)<br/> [**Utilisateur**](c-user.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrée | Valeur |
|------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID de lien                | \-                                                                                                                                                                                                                                 |
| MAPI-Id                | 0x8C6A                                                                                                                                                                                                                             |
| System-Only            | Faux                                                                                                                                                                                                                              |
| Est de valeur unique       | Faux                                                                                                                                                                                                                              |
| Est indexé             | Faux                                                                                                                                                                                                                              |
| Dans le catalogue global      | Vrai                                                                                                                                                                                                                               |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                                                                                                                                                                                                       |
| Range-Lower            | \-                                                                                                                                                                                                                                 |
| Range-Upper            | \-                                                                                                                                                                                                                                 |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                         |
| System-Flags           | 0x00000010                                                                                                                                                                                                                         |
| Classes utilisées dans        | [**inetOrgPerson**](c-inetorgperson.md)<br/> [**E-mail-destinataire**](c-mailrecipient.md)<br/> [**MS-PKI-privé-clé-Recovery-agent**](c-mspki-privatekeyrecoveryagent.md)<br/> [**Utilisateur**](c-user.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrée | Valeur |
|------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID de lien                | \-                                                                                                                                                                                                                                 |
| MAPI-Id                | 0x8C6A                                                                                                                                                                                                                             |
| System-Only            | Faux                                                                                                                                                                                                                              |
| Est de valeur unique       | Faux                                                                                                                                                                                                                              |
| Est indexé             | Faux                                                                                                                                                                                                                              |
| Dans le catalogue global      | Vrai                                                                                                                                                                                                                               |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                                                                                                                                                                                                       |
| Range-Lower            | \-                                                                                                                                                                                                                                 |
| Range-Upper            | \-                                                                                                                                                                                                                                 |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                         |
| System-Flags           | 0x00000010                                                                                                                                                                                                                         |
| Classes utilisées dans        | [**inetOrgPerson**](c-inetorgperson.md)<br/> [**E-mail-destinataire**](c-mailrecipient.md)<br/> [**MS-PKI-privé-clé-Recovery-agent**](c-mspki-privatekeyrecoveryagent.md)<br/> [**Utilisateur**](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrée | Valeur |
|------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID de lien                | \-                                                                                                                                                                                                                                 |
| MAPI-Id                | 0x8C6A                                                                                                                                                                                                                             |
| System-Only            | Faux                                                                                                                                                                                                                              |
| Est de valeur unique       | Faux                                                                                                                                                                                                                              |
| Est indexé             | Faux                                                                                                                                                                                                                              |
| Dans le catalogue global      | Vrai                                                                                                                                                                                                                               |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                                                                                                                                                                                                       |
| Range-Lower            | \-                                                                                                                                                                                                                                 |
| Range-Upper            | \-                                                                                                                                                                                                                                 |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                         |
| System-Flags           | 0x00000010                                                                                                                                                                                                                         |
| Classes utilisées dans        | [**inetOrgPerson**](c-inetorgperson.md)<br/> [**E-mail-destinataire**](c-mailrecipient.md)<br/> [**MS-PKI-privé-clé-Recovery-agent**](c-mspki-privatekeyrecoveryagent.md)<br/> [**Utilisateur**](c-user.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrée | Valeur |
|------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID de lien                | \-                                                                                                                                                                                                                                 |
| MAPI-Id                | 0x8C6A                                                                                                                                                                                                                             |
| System-Only            | Faux                                                                                                                                                                                                                              |
| Est de valeur unique       | Faux                                                                                                                                                                                                                              |
| Est indexé             | Faux                                                                                                                                                                                                                              |
| Dans le catalogue global      | Vrai                                                                                                                                                                                                                               |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                                                                                                                                                                                                       |
| Range-Lower            | \-                                                                                                                                                                                                                                 |
| Range-Upper            | \-                                                                                                                                                                                                                                 |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                         |
| System-Flags           | 0x00000010                                                                                                                                                                                                                         |
| Classes utilisées dans        | [**inetOrgPerson**](c-inetorgperson.md)<br/> [**E-mail-destinataire**](c-mailrecipient.md)<br/> [**MS-PKI-privé-clé-Recovery-agent**](c-mspki-privatekeyrecoveryagent.md)<br/> [**Utilisateur**](c-user.md)<br/> |



 

 





