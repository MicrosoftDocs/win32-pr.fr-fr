---
title: ms-DS-addition-DNS-Host-Name (attribut)
description: L’attribut est utilisé pour stocker le nom d’hôte DNS supplémentaire d’un objet ordinateur. Cet attribut est utilisé au moment où un contrôleur de périphérique est renommé.
ms.assetid: ea06f756-d9b6-409d-a008-0e3a1874ad94
ms.tgt_platform: multiple
keywords:
- Schéma AD de l’attribut ms-DS-Additional-DNS-Host-Name
- Schéma Active Directory de l’attribut msDS-AdditionalDnsHostName
topic_type:
- apiref
api_name:
- ms-DS-Additional-Dns-Host-Name
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 957829d688b1b89af59695a7929ed89d004fe2de9b7bf04c4478ad008f88a57b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119804229"
---
# <a name="ms-ds-additional-dns-host-name-attribute"></a>ms-DS-addition-DNS-Host-Name (attribut)

L’attribut est utilisé pour stocker le nom d’hôte DNS supplémentaire d’un objet ordinateur. Cet attribut est utilisé au moment où un ordinateur est renommé, ou les noms sont gérés avec « NETDOM ComputerName ».



| Entrée | Valeur |
|-------------------|-----------------------------------------------------------------------------|
| CN                | ms-DS-supplémentaire-DNS-Host-Name                                              |
| LDAP-Display-Name | msDS-AdditionalDnsHostName                                                  |
| Taille              | Chaque valeur peut être de 2048 caractères. Le nombre de valeurs correspond à la limite de la base de données d’environ 1200 valeurs. |
| Mettre à jour le privilège  | Cette valeur est définie par le système.                                            |
| Fréquence des mises à jour  | Lorsqu’un ordinateur est renommé.                                                 |
| Attribute-Id      | 1.2.840.113556.1.4.1717                                                     |
| System-ID-GUID    | 80863791-dbe9-4EB8-837e-7f0ab55d9ac7                                        |
| Syntaxe            | [**String(Unicode)**](s-string-unicode.md)                                 |



## <a name="implementations"></a>Implémentations

-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-server-2003"></a>Windows Server 2003



| Entrée | Valeur |
|------------------------|-------------------------------------------|
| ID de lien                | \-                                        |
| MAPI-Id                | \-                                        |
| System-Only            | Vrai                                      |
| Est de valeur unique       | Faux                                     |
| Est indexé             | Faux                                     |
| Dans le catalogue global      | Faux                                     |
| Descripteur de sécurité NT | O :BAG : BAD : S :                              |
| Range-Lower            | 0                                         |
| Range-Upper            | 2 048                                      |
| Search-Flags           | 0x00000000                                |
| System-Flags           | 0x00000010                                |
| Classes utilisées dans        | [**Computer**](c-computer.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrée | Valeur |
|------------------------|-------------------------------------------|
| ID de lien                | \-                                        |
| MAPI-Id                | \-                                        |
| System-Only            | Vrai                                      |
| Est de valeur unique       | Faux                                     |
| Est indexé             | Faux                                     |
| Dans le catalogue global      | Faux                                     |
| Descripteur de sécurité NT | O :BAG : BAD : S :                              |
| Range-Lower            | 0                                         |
| Range-Upper            | 2 048                                      |
| Search-Flags           | 0x00000000                                |
| System-Flags           | 0x00000010                                |
| Classes utilisées dans        | [**Computer**](c-computer.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrée | Valeur |
|------------------------|-------------------------------------------|
| ID de lien                | \-                                        |
| MAPI-Id                | \-                                        |
| System-Only            | Vrai                                      |
| Est de valeur unique       | Faux                                     |
| Est indexé             | Faux                                     |
| Dans le catalogue global      | Faux                                     |
| Descripteur de sécurité NT | O :BAG : BAD : S :                              |
| Range-Lower            | 0                                         |
| Range-Upper            | 2 048                                      |
| Search-Flags           | 0x00000000                                |
| System-Flags           | 0x00000010                                |
| Classes utilisées dans        | [**Computer**](c-computer.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrée | Valeur |
|------------------------|-------------------------------------------|
| ID de lien                | \-                                        |
| MAPI-Id                | \-                                        |
| System-Only            | Vrai                                      |
| Est de valeur unique       | Faux                                     |
| Est indexé             | Faux                                     |
| Dans le catalogue global      | Faux                                     |
| Descripteur de sécurité NT | O :BAG : BAD : S :                              |
| Range-Lower            | 0                                         |
| Range-Upper            | 2 048                                      |
| Search-Flags           | 0x00000000                                |
| System-Flags           | 0x00000010                                |
| Classes utilisées dans        | [**Computer**](c-computer.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrée | Valeur |
|------------------------|-------------------------------------------|
| ID de lien                | \-                                        |
| MAPI-Id                | \-                                        |
| System-Only            | Vrai                                      |
| Est de valeur unique       | Faux                                     |
| Est indexé             | Faux                                     |
| Dans le catalogue global      | Faux                                     |
| Descripteur de sécurité NT | O :BAG : BAD : S :                              |
| Range-Lower            | 0                                         |
| Range-Upper            | 2 048                                      |
| Search-Flags           | 0x00000000                                |
| System-Flags           | 0x00000010                                |
| Classes utilisées dans        | [**Computer**](c-computer.md)<br/> |



 

 





