---
title: MS-DNS-NSEC3-attribut sel utilisateur
description: Attribut qui définit une chaîne Salt NSEC3 spécifiée par l’utilisateur à utiliser lors de la signature de la zone DNS. S’il est vide, le Salt aléatoire est utilisé.
ms.assetid: b9829732-8a79-4f07-8644-9fe4ba05ba8f
ms.tgt_platform: multiple
keywords:
- Schéma AD de l’attribut de sel d’utilisateur MS-DNS-NSEC3
- Schéma AD de l’attribut msDNs-NSEC3UserSalt
topic_type:
- apiref
api_name:
- ms-DNS-NSEC3-User-Salt
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1dbd1725675487ae5a6812dd77c400745b6671de0ef7db360e1c1980dd25b1b1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119553019"
---
# <a name="ms-dns-nsec3-user-salt-attribute"></a>MS-DNS-NSEC3-attribut sel utilisateur

Attribut qui définit une chaîne Salt NSEC3 spécifiée par l’utilisateur à utiliser lors de la signature de la zone DNS. S’il est vide, le Salt aléatoire est utilisé.



| Entrée | Valeur |
|-------------------|---------------------------------------------|
| CN                | MS-DNS-NSEC3-utilisateur-Salt                      |
| LDAP-Display-Name | msDN-NSEC3UserSalt                         |
| Taille              | \-                                          |
| Mettre à jour le privilège  | \-                                          |
| Fréquence des mises à jour  | \-                                          |
| Attribute-Id      | 1.2.840.113556.1.4.2148                     |
| System-ID-GUID    | aff16770-9622-4fbc-a128-3088777605b9        |
| Syntaxe            | [**String(Unicode)**](s-string-unicode.md) |



## <a name="implementations"></a>Implémentations

-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-server-2012"></a>Windows Server 2012



| Entrée | Valeur |
|------------------------|------------------------------------------|
| ID de lien                | \-                                       |
| MAPI-Id                | \-                                       |
| System-Only            | Faux                                    |
| Est de valeur unique       | Vrai                                     |
| Est indexé             | Faux                                    |
| Dans le catalogue global      | Faux                                    |
| Descripteur de sécurité NT | O :BAG : BAD : S :                             |
| Range-Lower            | 0                                        |
| Range-Upper            | 510                                      |
| Search-Flags           | 0x00000008                               |
| System-Flags           | 0x00000010                               |
| Classes utilisées dans        | [**Zone DNS**](c-dnszone.md)<br/> |



 

 





