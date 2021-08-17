---
title: Attribut SPN-Mappings
description: Cet attribut à valeurs multiples contient une liste de noms de principal du service (SPN) pour indiquer l’équivalence des types SPN.
ms.assetid: 6d37618d-426d-4e7b-8475-c912adb595ee
ms.tgt_platform: multiple
keywords:
- Schéma AD d’attribut SPN-Mappings
- Schéma AD de l’attribut sPNMappings
topic_type:
- apiref
api_name:
- SPN-Mappings
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 451f8d3f98984f725915410e964e39a66905f29c1ccbcf9156b55d7ba51d3e5f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118960048"
---
# <a name="spn-mappings-attribute"></a>Attribut SPN-Mappings

Cet attribut à valeurs multiples contient une liste de noms de principal du service (SPN) pour indiquer l’équivalence des types SPN. Le SPN est le nom qu’un client utilise pour identifier de manière unique une instance d’un service. Si vous installez plusieurs instances d'un service sur les ordinateurs d'une forêt, chaque instance doit posséder son propre SPN. Une instance de service donnée peut posséder plusieurs noms SPN si les clients peuvent utiliser plusieurs noms pour l'authentification. Par exemple, « LDAP/... » Les noms de principal du service (SPN) peuvent être mappés pour qu’ils soient équivalents à « Host/... » SPN.



| Entrée | Valeur |
|-------------------|--------------------------------------------------------------------------------------------------------------------|
| CN                | SPN-Mappings                                                                                                       |
| LDAP-Display-Name | sPNMappings                                                                                                        |
| Taille              | \-                                                                                                                 |
| Mettre à jour le privilège  | Cette valeur est définie lors de l’installation du produit. Il peut être modifié par l’administrateur système ultérieurement. |
| Fréquence des mises à jour  | \-                                                                                                                 |
| Attribute-Id      | 1.2.840.113556.1.4.1347                                                                                            |
| System-ID-GUID    | 2ab0e76c-7041-11d2-9905-0000f87a57d4                                                                               |
| Syntaxe            | [**String(Unicode)**](s-string-unicode.md)                                                                        |



## <a name="implementations"></a>Implémentations

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server



| Entrée | Valeur |
|------------------------|--------------------------------------------------|
| ID de lien                | \-                                               |
| MAPI-Id                | \-                                               |
| System-Only            | Faux                                            |
| Est de valeur unique       | Faux                                            |
| Est indexé             | Faux                                            |
| Dans le catalogue global      | Faux                                            |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                     |
| Range-Lower            | \-                                               |
| Range-Upper            | \-                                               |
| Search-Flags           | 0x00000000                                       |
| System-Flags           | 0x00000010                                       |
| Classes utilisées dans        | [**NTDS-service**](c-ntdsservice.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Entrée | Valeur |
|------------------------|--------------------------------------------------|
| ID de lien                | \-                                               |
| MAPI-Id                | \-                                               |
| System-Only            | Faux                                            |
| Est de valeur unique       | Faux                                            |
| Est indexé             | Faux                                            |
| Dans le catalogue global      | Faux                                            |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                     |
| Range-Lower            | \-                                               |
| Range-Upper            | \-                                               |
| Search-Flags           | 0x00000000                                       |
| System-Flags           | 0x00000010                                       |
| Classes utilisées dans        | [**NTDS-service**](c-ntdsservice.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrée | Valeur |
|------------------------|--------------------------------------------------|
| ID de lien                | \-                                               |
| MAPI-Id                | \-                                               |
| System-Only            | Faux                                            |
| Est de valeur unique       | Faux                                            |
| Est indexé             | Faux                                            |
| Dans le catalogue global      | Faux                                            |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                     |
| Range-Lower            | \-                                               |
| Range-Upper            | \-                                               |
| Search-Flags           | 0x00000000                                       |
| System-Flags           | 0x00000010                                       |
| Classes utilisées dans        | [**NTDS-service**](c-ntdsservice.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrée | Valeur |
|------------------------|--------------------------------------------------|
| ID de lien                | \-                                               |
| MAPI-Id                | \-                                               |
| System-Only            | Faux                                            |
| Est de valeur unique       | Faux                                            |
| Est indexé             | Faux                                            |
| Dans le catalogue global      | Faux                                            |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                     |
| Range-Lower            | \-                                               |
| Range-Upper            | \-                                               |
| Search-Flags           | 0x00000000                                       |
| System-Flags           | 0x00000010                                       |
| Classes utilisées dans        | [**NTDS-service**](c-ntdsservice.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrée | Valeur |
|------------------------|--------------------------------------------------|
| ID de lien                | \-                                               |
| MAPI-Id                | \-                                               |
| System-Only            | Faux                                            |
| Est de valeur unique       | Faux                                            |
| Est indexé             | Faux                                            |
| Dans le catalogue global      | Faux                                            |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                     |
| Range-Lower            | \-                                               |
| Range-Upper            | \-                                               |
| Search-Flags           | 0x00000000                                       |
| System-Flags           | 0x00000010                                       |
| Classes utilisées dans        | [**NTDS-service**](c-ntdsservice.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrée | Valeur |
|------------------------|--------------------------------------------------|
| ID de lien                | \-                                               |
| MAPI-Id                | \-                                               |
| System-Only            | Faux                                            |
| Est de valeur unique       | Faux                                            |
| Est indexé             | Faux                                            |
| Dans le catalogue global      | Faux                                            |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                     |
| Range-Lower            | \-                                               |
| Range-Upper            | \-                                               |
| Search-Flags           | 0x00000000                                       |
| System-Flags           | 0x00000010                                       |
| Classes utilisées dans        | [**NTDS-service**](c-ntdsservice.md)<br/> |



 

 





