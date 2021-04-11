---
title: Attribut MS-DS-Replicas-NC-Reason
description: Attribut de l’objet ntdsConnection qui indique pourquoi (ou si) le KCC affiche la connexion est utile dans la topologie de réplication. Est à valeurs multiples et a une syntaxe DistName + Binary, où la partie binaire est un champ de bits de taille int.
ms.assetid: ba66e346-d288-4c0b-b41e-599c3f8e8405
ms.tgt_platform: multiple
keywords:
- Schéma AD de l’attribut MS-DS-Replicas-NC-Reason
- Schéma AD de l’attribut mS-DS-ReplicatesNCReason
topic_type:
- apiref
api_name:
- MS-DS-Replicates-NC-Reason
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1a45c587ef82773b5e7fd310e8e8591f18ad27ab
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104385339"
---
# <a name="ms-ds-replicates-nc-reason-attribute"></a>Attribut MS-DS-Replicas-NC-Reason

Attribut de l’objet ntdsConnection qui indique pourquoi (ou si) le KCC affiche la connexion est utile dans la topologie de réplication. Est à valeurs multiples et a une syntaxe DistName + Binary, où la partie binaire est un champ de bits de taille int.



| Entrée | Valeur |
|-------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| CN                | MS-DS-répliques-NC-raison                                                                                                                 |
| LDAP-Display-Name | mS-DS-ReplicatesNCReason                                                                                                                   |
| Taille              | Valeur de la partie binaire : 0 = aucune \_ raison, 1 = \_ topologie GC, 2 = \_ topologie en anneau, 4 = réduire \_ la \_ topologie des TRONÇONs, 8 = topologie des serveurs obsolètes \_ \_ . |
| Mettre à jour le privilège  | Cette valeur est définie par le système.                                                                                                           |
| Fréquence des mises à jour  | Peut changer en réponse aux modifications apportées à la topologie du réseau.                                                                                 |
| Attribute-Id      | 1.2.840.113556.1.4.1408                                                                                                                    |
| System-ID-GUID    | 0ea12b84-08b3-11d3-91bc-0000f87a57d4                                                                                                       |
| Syntaxe            | [**Object(DN-Binary)**](s-object-dn-binary.md)                                                                                            |



## <a name="implementations"></a>Implémentations

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**ADAM**](#adam)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server



| Entrée | Valeur |
|------------------------|--------------------------------------------------------|
| ID de lien                | \-                                                     |
| MAPI-Id                | \-                                                     |
| System-Only            | Faux                                                  |
| Est de valeur unique       | Faux                                                  |
| Est indexé             | Faux                                                  |
| Dans le catalogue global      | Faux                                                  |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                           |
| Range-Lower            | \-                                                     |
| Range-Upper            | \-                                                     |
| Search-Flags           | 0x00000000                                             |
| System-Flags           | 0x00000010                                             |
| Classes utilisées dans        | [**NTDS-connexion**](c-ntdsconnection.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Entrée | Valeur |
|------------------------|--------------------------------------------------------|
| ID de lien                | \-                                                     |
| MAPI-Id                | \-                                                     |
| System-Only            | Faux                                                  |
| Est de valeur unique       | Faux                                                  |
| Est indexé             | Faux                                                  |
| Dans le catalogue global      | Faux                                                  |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                           |
| Range-Lower            | \-                                                     |
| Range-Upper            | \-                                                     |
| Search-Flags           | 0x00000000                                             |
| System-Flags           | 0x00000010                                             |
| Classes utilisées dans        | [**NTDS-connexion**](c-ntdsconnection.md)<br/> |



## <a name="adam"></a>ADAM



| Entrée | Valeur |
|------------------------|--------------------------------------------------------|
| ID de lien                | \-                                                     |
| MAPI-Id                | \-                                                     |
| System-Only            | Faux                                                  |
| Est de valeur unique       | Faux                                                  |
| Est indexé             | Faux                                                  |
| Dans le catalogue global      | Faux                                                  |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                           |
| Range-Lower            | \-                                                     |
| Range-Upper            | \-                                                     |
| Search-Flags           | 0x00000000                                             |
| System-Flags           | 0x00000010                                             |
| Classes utilisées dans        | [**NTDS-connexion**](c-ntdsconnection.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrée | Valeur |
|------------------------|--------------------------------------------------------|
| ID de lien                | \-                                                     |
| MAPI-Id                | \-                                                     |
| System-Only            | Faux                                                  |
| Est de valeur unique       | Faux                                                  |
| Est indexé             | Faux                                                  |
| Dans le catalogue global      | Faux                                                  |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                           |
| Range-Lower            | \-                                                     |
| Range-Upper            | \-                                                     |
| Search-Flags           | 0x00000000                                             |
| System-Flags           | 0x00000010                                             |
| Classes utilisées dans        | [**NTDS-connexion**](c-ntdsconnection.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrée | Valeur |
|------------------------|--------------------------------------------------------|
| ID de lien                | \-                                                     |
| MAPI-Id                | \-                                                     |
| System-Only            | Faux                                                  |
| Est de valeur unique       | Faux                                                  |
| Est indexé             | Faux                                                  |
| Dans le catalogue global      | Faux                                                  |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                           |
| Range-Lower            | \-                                                     |
| Range-Upper            | \-                                                     |
| Search-Flags           | 0x00000000                                             |
| System-Flags           | 0x00000010                                             |
| Classes utilisées dans        | [**NTDS-connexion**](c-ntdsconnection.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrée | Valeur |
|------------------------|--------------------------------------------------------|
| ID de lien                | \-                                                     |
| MAPI-Id                | \-                                                     |
| System-Only            | Faux                                                  |
| Est de valeur unique       | Faux                                                  |
| Est indexé             | Faux                                                  |
| Dans le catalogue global      | Faux                                                  |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                           |
| Range-Lower            | \-                                                     |
| Range-Upper            | \-                                                     |
| Search-Flags           | 0x00000000                                             |
| System-Flags           | 0x00000010                                             |
| Classes utilisées dans        | [**NTDS-connexion**](c-ntdsconnection.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrée | Valeur |
|------------------------|--------------------------------------------------------|
| ID de lien                | \-                                                     |
| MAPI-Id                | \-                                                     |
| System-Only            | Faux                                                  |
| Est de valeur unique       | Faux                                                  |
| Est indexé             | Faux                                                  |
| Dans le catalogue global      | Faux                                                  |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                           |
| Range-Lower            | \-                                                     |
| Range-Upper            | \-                                                     |
| Search-Flags           | 0x00000000                                             |
| System-Flags           | 0x00000010                                             |
| Classes utilisées dans        | [**NTDS-connexion**](c-ntdsconnection.md)<br/> |



 

 





