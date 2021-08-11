---
title: Attribut Domain-Component
description: Attribut de nom pour les objets Domain et DNS. Généralement affiché en tant que DC DomainName.
ms.assetid: 1d674af1-ed2f-4266-9704-8c6ed5a9bdd8
ms.tgt_platform: multiple
keywords:
- Schéma AD d’attribut Domain-Component
- Schéma AD d’attribut de contrôleur de domaine
topic_type:
- apiref
api_name:
- Domain-Component
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fe93b6629ac176452edbe5cdf13bf35afa955890cde369273f87990034bcd3e1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118177767"
---
# <a name="domain-component-attribute"></a>Attribut Domain-Component

Attribut de nom pour les objets Domain et DNS. Généralement affiché sous la forme DC = DomainName.



| Entrée | Valeur |
|-------------------|---------------------------------------------|
| CN                | Domain-Component                            |
| LDAP-Display-Name | dc                                          |
| Taille              | \-                                          |
| Mettre à jour le privilège  | Administrateur de domaine                        |
| Fréquence des mises à jour  | Lors de la création du domaine.                 |
| Attribute-Id      | 0.9.2342.19200300.100.1.25                  |
| System-ID-GUID    | 19195a55-6da0-11d0-afd3-00c04fd930c9        |
| Syntaxe            | [**String(Unicode)**](s-string-unicode.md) |



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
|------------------------|-------------------------------------------------------------------------------------------------------------------------|
| ID de lien                | \-                                                                                                                      |
| MAPI-Id                | \-                                                                                                                      |
| System-Only            | False                                                                                                                   |
| Est de valeur unique       | True                                                                                                                    |
| Est indexé             | False                                                                                                                   |
| Dans le catalogue global      | True                                                                                                                    |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                                                                                            |
| Range-Lower            | 1                                                                                                                       |
| Range-Upper            | 255                                                                                                                     |
| Search-Flags           | 0x00000000                                                                                                              |
| System-Flags           | 0x00000012                                                                                                              |
| Classes utilisées dans        | [**Nœud DNS**](c-dnsnode.md)<br/> [**Zone DNS**](c-dnszone.md)<br/> [**Domain**](c-domain.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Entrée | Valeur |
|------------------------|-------------------------------------------------------------------------------------------------------------------------|
| ID de lien                | \-                                                                                                                      |
| MAPI-Id                | \-                                                                                                                      |
| System-Only            | False                                                                                                                   |
| Est de valeur unique       | True                                                                                                                    |
| Est indexé             | False                                                                                                                   |
| Dans le catalogue global      | True                                                                                                                    |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                                                                                            |
| Range-Lower            | 1                                                                                                                       |
| Range-Upper            | 255                                                                                                                     |
| Search-Flags           | 0x00000000                                                                                                              |
| System-Flags           | 0x00000012                                                                                                              |
| Classes utilisées dans        | [**Nœud DNS**](c-dnsnode.md)<br/> [**Zone DNS**](c-dnszone.md)<br/> [**Domain**](c-domain.md)<br/> |



## <a name="adam"></a>ADAM



| Entrée | Valeur |
|------------------------|---------------------------------------|
| ID de lien                | \-                                    |
| MAPI-Id                | \-                                    |
| System-Only            | False                                 |
| Est de valeur unique       | True                                  |
| Est indexé             | False                                 |
| Dans le catalogue global      | True                                  |
| Descripteur de sécurité NT | O :BAG : BAD : S :                          |
| Range-Lower            | 1                                     |
| Range-Upper            | 255                                   |
| Search-Flags           | 0x00000000                            |
| System-Flags           | 0x00000012                            |
| Classes utilisées dans        | [**Domain**](c-domain.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrée | Valeur |
|------------------------|-------------------------------------------------------------------------------------------------------------------------|
| ID de lien                | \-                                                                                                                      |
| MAPI-Id                | \-                                                                                                                      |
| System-Only            | False                                                                                                                   |
| Est de valeur unique       | True                                                                                                                    |
| Est indexé             | False                                                                                                                   |
| Dans le catalogue global      | True                                                                                                                    |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                                                                                            |
| Range-Lower            | 1                                                                                                                       |
| Range-Upper            | 255                                                                                                                     |
| Search-Flags           | 0x00000000                                                                                                              |
| System-Flags           | 0x00000012                                                                                                              |
| Classes utilisées dans        | [**Nœud DNS**](c-dnsnode.md)<br/> [**Zone DNS**](c-dnszone.md)<br/> [**Domain**](c-domain.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrée | Valeur |
|------------------------|-------------------------------------------------------------------------------------------------------------------------|
| ID de lien                | \-                                                                                                                      |
| MAPI-Id                | \-                                                                                                                      |
| System-Only            | False                                                                                                                   |
| Est de valeur unique       | True                                                                                                                    |
| Est indexé             | False                                                                                                                   |
| Dans le catalogue global      | True                                                                                                                    |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                                                                                            |
| Range-Lower            | 1                                                                                                                       |
| Range-Upper            | 255                                                                                                                     |
| Search-Flags           | 0x00000000                                                                                                              |
| System-Flags           | 0x00000012                                                                                                              |
| Classes utilisées dans        | [**Nœud DNS**](c-dnsnode.md)<br/> [**Zone DNS**](c-dnszone.md)<br/> [**Domain**](c-domain.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrée | Valeur |
|------------------------|-------------------------------------------------------------------------------------------------------------------------|
| ID de lien                | \-                                                                                                                      |
| MAPI-Id                | \-                                                                                                                      |
| System-Only            | False                                                                                                                   |
| Est de valeur unique       | True                                                                                                                    |
| Est indexé             | False                                                                                                                   |
| Dans le catalogue global      | True                                                                                                                    |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                                                                                            |
| Range-Lower            | 1                                                                                                                       |
| Range-Upper            | 255                                                                                                                     |
| Search-Flags           | 0x00000000                                                                                                              |
| System-Flags           | 0x00000012                                                                                                              |
| Classes utilisées dans        | [**Nœud DNS**](c-dnsnode.md)<br/> [**Zone DNS**](c-dnszone.md)<br/> [**Domain**](c-domain.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrée | Valeur |
|------------------------|-------------------------------------------------------------------------------------------------------------------------|
| ID de lien                | \-                                                                                                                      |
| MAPI-Id                | \-                                                                                                                      |
| System-Only            | False                                                                                                                   |
| Est de valeur unique       | True                                                                                                                    |
| Est indexé             | False                                                                                                                   |
| Dans le catalogue global      | True                                                                                                                    |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                                                                                            |
| Range-Lower            | 1                                                                                                                       |
| Range-Upper            | 255                                                                                                                     |
| Search-Flags           | 0x00000000                                                                                                              |
| System-Flags           | 0x00000012                                                                                                              |
| Classes utilisées dans        | [**Nœud DNS**](c-dnsnode.md)<br/> [**Zone DNS**](c-dnszone.md)<br/> [**Domain**](c-domain.md)<br/> |



 

 





