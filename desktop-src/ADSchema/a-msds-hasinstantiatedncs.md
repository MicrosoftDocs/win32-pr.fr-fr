---
title: attribut ms-DS-has-instancied-NC
description: Les informations d’état de la réplication DS, similaires à (et sur un sur-ensemble), les attributs existants hasMasterNCs et hasPartialReplicaNCs. À utiliser par le KCC lors de la configuration des partenaires de réplication.
ms.assetid: 00dda441-e382-4fb2-b735-ae547901c11f
ms.tgt_platform: multiple
keywords:
- Schéma AD de l’attribut ms-DS-a-instancié-NC
- Schéma Active Directory de l’attribut msDS-HasInstantiatedNCs
topic_type:
- apiref
api_name:
- ms-DS-Has-Instantiated-NCs
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: efde9ef1cd9a7230e4493d3e542e1f5f661ed33027ad3e9a88ded9679df812c7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119804050"
---
# <a name="ms-ds-has-instantiated-ncs-attribute"></a>attribut ms-DS-has-instancied-NC

Les informations d’état de la réplication DS, similaires à (et sur un sur-ensemble), les attributs existants hasMasterNCs et hasPartialReplicaNCs. À utiliser par le KCC lors de la configuration des partenaires de réplication.



| Entrée | Valeur |
|-------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| CN                | ms-DS-a-instancié-NC                                                                                                                                                                                  |
| LDAP-Display-Name | msDS-HasInstantiatedNCs                                                                                                                                                                                     |
| Taille              | 4 octets                                                                                                                                                                                                     |
| Mettre à jour le privilège  | Cette valeur est définie par le système.                                                                                                                                                                            |
| Fréquence des mises à jour  | Environ deux fois plus souvent que hasMasterNCs/hasPartialReplicaNCs. Ces attributs existants sont mis à jour uniquement lorsque le contrôleur de périphérique ajoute ou supprime une partition (par exemple, lors du passage de DC à GC ou vice versa). |
| Attribute-Id      | 1.2.840.113556.1.4.1709                                                                                                                                                                                     |
| System-ID-GUID    | 11e9a5bc-4517-4049-af9c-51554fb0fc09                                                                                                                                                                        |
| Syntaxe            | [**Object(DN-Binary)**](s-object-dn-binary.md)                                                                                                                                                             |



## <a name="implementations"></a>Implémentations

-   [**Windows Server 2003**](#windows-server-2003)
-   [**ADAM**](#adam)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-server-2003"></a>Windows Server 2003



| Entrée | Valeur |
|------------------------|------------------------------------------|
| ID de lien                | 2002                                     |
| MAPI-Id                | \-                                       |
| System-Only            | Vrai                                     |
| Est de valeur unique       | Faux                                    |
| Est indexé             | Faux                                    |
| Dans le catalogue global      | Faux                                    |
| Descripteur de sécurité NT | O :BAG : BAD : S :                             |
| Range-Lower            | 4                                        |
| Range-Upper            | 4                                        |
| Search-Flags           | 0x00000000                               |
| System-Flags           | 0x00000010                               |
| Classes utilisées dans        | [**NTDS-DSA**](c-ntdsdsa.md)<br/> |



## <a name="adam"></a>ADAM



| Entrée | Valeur |
|------------------------|------------------------------------------|
| ID de lien                | 2002                                     |
| MAPI-Id                | \-                                       |
| System-Only            | Vrai                                     |
| Est de valeur unique       | Faux                                    |
| Est indexé             | Faux                                    |
| Dans le catalogue global      | Faux                                    |
| Descripteur de sécurité NT | O :BAG : BAD : S :                             |
| Range-Lower            | 4                                        |
| Range-Upper            | 4                                        |
| Search-Flags           | 0x00000000                               |
| System-Flags           | 0x00000010                               |
| Classes utilisées dans        | [**NTDS-DSA**](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrée | Valeur |
|------------------------|------------------------------------------|
| ID de lien                | 2002                                     |
| MAPI-Id                | \-                                       |
| System-Only            | Vrai                                     |
| Est de valeur unique       | Faux                                    |
| Est indexé             | Faux                                    |
| Dans le catalogue global      | Faux                                    |
| Descripteur de sécurité NT | O :BAG : BAD : S :                             |
| Range-Lower            | 4                                        |
| Range-Upper            | 4                                        |
| Search-Flags           | 0x00000000                               |
| System-Flags           | 0x00000010                               |
| Classes utilisées dans        | [**NTDS-DSA**](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrée | Valeur |
|------------------------|------------------------------------------|
| ID de lien                | 2002                                     |
| MAPI-Id                | \-                                       |
| System-Only            | Vrai                                     |
| Est de valeur unique       | Faux                                    |
| Est indexé             | Faux                                    |
| Dans le catalogue global      | Faux                                    |
| Descripteur de sécurité NT | O :BAG : BAD : S :                             |
| Range-Lower            | 4                                        |
| Range-Upper            | 4                                        |
| Search-Flags           | 0x00000000                               |
| System-Flags           | 0x00000010                               |
| Classes utilisées dans        | [**NTDS-DSA**](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrée | Valeur |
|------------------------|------------------------------------------|
| ID de lien                | 2002                                     |
| MAPI-Id                | \-                                       |
| System-Only            | Vrai                                     |
| Est de valeur unique       | Faux                                    |
| Est indexé             | Faux                                    |
| Dans le catalogue global      | Faux                                    |
| Descripteur de sécurité NT | O :BAG : BAD : S :                             |
| Range-Lower            | 4                                        |
| Range-Upper            | 4                                        |
| Search-Flags           | 0x00000000                               |
| System-Flags           | 0x00000010                               |
| Classes utilisées dans        | [**NTDS-DSA**](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrée | Valeur |
|------------------------|------------------------------------------|
| ID de lien                | 2002                                     |
| MAPI-Id                | \-                                       |
| System-Only            | Vrai                                     |
| Est de valeur unique       | Faux                                    |
| Est indexé             | Faux                                    |
| Dans le catalogue global      | Faux                                    |
| Descripteur de sécurité NT | O :BAG : BAD : S :                             |
| Range-Lower            | 4                                        |
| Range-Upper            | 4                                        |
| Search-Flags           | 0x00000000                               |
| System-Flags           | 0x00000010                               |
| Classes utilisées dans        | [**NTDS-DSA**](c-ntdsdsa.md)<br/> |



 

 





