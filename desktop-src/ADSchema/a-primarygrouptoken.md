---
title: Attribut Primary-Group-Token
description: Attribut calculé utilisé pour récupérer la liste d’appartenance d’un groupe, par exemple les utilisateurs du domaine. L’appartenance complète de ces groupes n’est pas stockée explicitement pour des raisons de mise à l’échelle.
ms.assetid: b23d3b7f-074b-4f1b-bc06-b22738a8a79e
ms.tgt_platform: multiple
keywords:
- Schéma Active Directory de l’attribut Primary-Group-Token
- Schéma AD de l’attribut primaryGroupToken
topic_type:
- apiref
api_name:
- Primary-Group-Token
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fd83e89a25a81f6d62207e48053fff5cafd279e29b482a9b80cb02de580ad3fc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120065919"
---
# <a name="primary-group-token-attribute"></a>Attribut Primary-Group-Token

Attribut calculé utilisé pour récupérer la liste d’appartenance d’un groupe, par exemple les utilisateurs du domaine. L’appartenance complète de ces groupes n’est pas stockée explicitement pour des raisons de mise à l’échelle.



| Entrée | Valeur |
|-------------------|--------------------------------------------|
| CN                | Primary-Group-Token                        |
| LDAP-Display-Name | primaryGroupToken                          |
| Taille              | 4 octets                                    |
| Mettre à jour le privilège  | Cette valeur est définie par le système.           |
| Fréquence des mises à jour  | À chaque fois qu’un groupe principal d’objets change. |
| Attribute-Id      | 1.2.840.113556.1.4.1412                    |
| System-ID-GUID    | c0ed8738-7efd-4481-84d9-66d2db8be369       |
| Syntaxe            | [**Énumération**](s-enumeration.md)       |



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
|------------------------|-------------------------------------|
| ID de lien                | \-                                  |
| MAPI-Id                | \-                                  |
| System-Only            | Vrai                                |
| Est de valeur unique       | Vrai                                |
| Est indexé             | Faux                               |
| Dans le catalogue global      | Faux                               |
| Descripteur de sécurité NT | O :BAG : BAD : S :                        |
| Range-Lower            | \-                                  |
| Range-Upper            | \-                                  |
| Search-Flags           | 0x00000000                          |
| System-Flags           | 0x00000014                          |
| Classes utilisées dans        | [**Groupe**](c-group.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Entrée | Valeur |
|------------------------|-------------------------------------|
| ID de lien                | \-                                  |
| MAPI-Id                | \-                                  |
| System-Only            | Vrai                                |
| Est de valeur unique       | Vrai                                |
| Est indexé             | Faux                               |
| Dans le catalogue global      | Faux                               |
| Descripteur de sécurité NT | O :BAG : BAD : S :                        |
| Range-Lower            | \-                                  |
| Range-Upper            | \-                                  |
| Search-Flags           | 0x00000000                          |
| System-Flags           | 0x00000014                          |
| Classes utilisées dans        | [**Groupe**](c-group.md)<br/> |



## <a name="adam"></a>ADAM



| Entrée | Valeur |
|------------------------|-------------------------------------|
| ID de lien                | \-                                  |
| MAPI-Id                | \-                                  |
| System-Only            | Vrai                                |
| Est de valeur unique       | Vrai                                |
| Est indexé             | Faux                               |
| Dans le catalogue global      | Faux                               |
| Descripteur de sécurité NT | O :BAG : BAD : S :                        |
| Range-Lower            | \-                                  |
| Range-Upper            | \-                                  |
| Search-Flags           | 0x00000000                          |
| System-Flags           | 0x00000014                          |
| Classes utilisées dans        | [**Groupe**](c-group.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrée | Valeur |
|------------------------|-------------------------------------|
| ID de lien                | \-                                  |
| MAPI-Id                | \-                                  |
| System-Only            | Vrai                                |
| Est de valeur unique       | Vrai                                |
| Est indexé             | Faux                               |
| Dans le catalogue global      | Faux                               |
| Descripteur de sécurité NT | O :BAG : BAD : S :                        |
| Range-Lower            | \-                                  |
| Range-Upper            | \-                                  |
| Search-Flags           | 0x00000000                          |
| System-Flags           | 0x00000014                          |
| Classes utilisées dans        | [**Groupe**](c-group.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrée | Valeur |
|------------------------|-------------------------------------|
| ID de lien                | \-                                  |
| MAPI-Id                | \-                                  |
| System-Only            | Vrai                                |
| Est de valeur unique       | Vrai                                |
| Est indexé             | Faux                               |
| Dans le catalogue global      | Faux                               |
| Descripteur de sécurité NT | O :BAG : BAD : S :                        |
| Range-Lower            | \-                                  |
| Range-Upper            | \-                                  |
| Search-Flags           | 0x00000000                          |
| System-Flags           | 0x00000014                          |
| Classes utilisées dans        | [**Groupe**](c-group.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrée | Valeur |
|------------------------|-------------------------------------|
| ID de lien                | \-                                  |
| MAPI-Id                | \-                                  |
| System-Only            | Vrai                                |
| Est de valeur unique       | Vrai                                |
| Est indexé             | Faux                               |
| Dans le catalogue global      | Faux                               |
| Descripteur de sécurité NT | O :BAG : BAD : S :                        |
| Range-Lower            | \-                                  |
| Range-Upper            | \-                                  |
| Search-Flags           | 0x00000000                          |
| System-Flags           | 0x00000014                          |
| Classes utilisées dans        | [**Groupe**](c-group.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrée | Valeur |
|------------------------|-------------------------------------|
| ID de lien                | \-                                  |
| MAPI-Id                | \-                                  |
| System-Only            | Vrai                                |
| Est de valeur unique       | Vrai                                |
| Est indexé             | Faux                               |
| Dans le catalogue global      | Faux                               |
| Descripteur de sécurité NT | O :BAG : BAD : S :                        |
| Range-Lower            | \-                                  |
| Range-Upper            | \-                                  |
| Search-Flags           | 0x00000000                          |
| System-Flags           | 0x00000014                          |
| Classes utilisées dans        | [**Groupe**](c-group.md)<br/> |



 

 





