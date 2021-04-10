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
ms.openlocfilehash: a97a6958d51c6e0e29f70685b2624fb194d42e05
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104107149"
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
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server



| Entrée | Valeur |
|------------------------|-------------------------------------------------------------------------------------------------------------------------|
| ID de lien                | \-                                                                                                                      |
| MAPI-Id                | \-                                                                                                                      |
| System-Only            | Faux                                                                                                                   |
| Est de valeur unique       | Vrai                                                                                                                    |
| Est indexé             | Faux                                                                                                                   |
| Dans le catalogue global      | Vrai                                                                                                                    |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                                                                                            |
| Range-Lower            | 1                                                                                                                       |
| Range-Upper            | 255                                                                                                                     |
| Search-Flags           | 0x00000000                                                                                                              |
| System-Flags           | 0x00000012                                                                                                              |
| Classes utilisées dans        | [**Nœud DNS**](c-dnsnode.md)<br/> [**Zone DNS**](c-dnszone.md)<br/> [**Domaine**](c-domain.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Entrée | Valeur |
|------------------------|-------------------------------------------------------------------------------------------------------------------------|
| ID de lien                | \-                                                                                                                      |
| MAPI-Id                | \-                                                                                                                      |
| System-Only            | Faux                                                                                                                   |
| Est de valeur unique       | Vrai                                                                                                                    |
| Est indexé             | Faux                                                                                                                   |
| Dans le catalogue global      | Vrai                                                                                                                    |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                                                                                            |
| Range-Lower            | 1                                                                                                                       |
| Range-Upper            | 255                                                                                                                     |
| Search-Flags           | 0x00000000                                                                                                              |
| System-Flags           | 0x00000012                                                                                                              |
| Classes utilisées dans        | [**Nœud DNS**](c-dnsnode.md)<br/> [**Zone DNS**](c-dnszone.md)<br/> [**Domaine**](c-domain.md)<br/> |



## <a name="adam"></a>ADAM



| Entrée | Valeur |
|------------------------|---------------------------------------|
| ID de lien                | \-                                    |
| MAPI-Id                | \-                                    |
| System-Only            | Faux                                 |
| Est de valeur unique       | Vrai                                  |
| Est indexé             | Faux                                 |
| Dans le catalogue global      | Vrai                                  |
| Descripteur de sécurité NT | O :BAG : BAD : S :                          |
| Range-Lower            | 1                                     |
| Range-Upper            | 255                                   |
| Search-Flags           | 0x00000000                            |
| System-Flags           | 0x00000012                            |
| Classes utilisées dans        | [**Domaine**](c-domain.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrée | Valeur |
|------------------------|-------------------------------------------------------------------------------------------------------------------------|
| ID de lien                | \-                                                                                                                      |
| MAPI-Id                | \-                                                                                                                      |
| System-Only            | Faux                                                                                                                   |
| Est de valeur unique       | Vrai                                                                                                                    |
| Est indexé             | Faux                                                                                                                   |
| Dans le catalogue global      | Vrai                                                                                                                    |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                                                                                            |
| Range-Lower            | 1                                                                                                                       |
| Range-Upper            | 255                                                                                                                     |
| Search-Flags           | 0x00000000                                                                                                              |
| System-Flags           | 0x00000012                                                                                                              |
| Classes utilisées dans        | [**Nœud DNS**](c-dnsnode.md)<br/> [**Zone DNS**](c-dnszone.md)<br/> [**Domaine**](c-domain.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrée | Valeur |
|------------------------|-------------------------------------------------------------------------------------------------------------------------|
| ID de lien                | \-                                                                                                                      |
| MAPI-Id                | \-                                                                                                                      |
| System-Only            | Faux                                                                                                                   |
| Est de valeur unique       | Vrai                                                                                                                    |
| Est indexé             | Faux                                                                                                                   |
| Dans le catalogue global      | Vrai                                                                                                                    |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                                                                                            |
| Range-Lower            | 1                                                                                                                       |
| Range-Upper            | 255                                                                                                                     |
| Search-Flags           | 0x00000000                                                                                                              |
| System-Flags           | 0x00000012                                                                                                              |
| Classes utilisées dans        | [**Nœud DNS**](c-dnsnode.md)<br/> [**Zone DNS**](c-dnszone.md)<br/> [**Domaine**](c-domain.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrée | Valeur |
|------------------------|-------------------------------------------------------------------------------------------------------------------------|
| ID de lien                | \-                                                                                                                      |
| MAPI-Id                | \-                                                                                                                      |
| System-Only            | Faux                                                                                                                   |
| Est de valeur unique       | Vrai                                                                                                                    |
| Est indexé             | Faux                                                                                                                   |
| Dans le catalogue global      | Vrai                                                                                                                    |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                                                                                            |
| Range-Lower            | 1                                                                                                                       |
| Range-Upper            | 255                                                                                                                     |
| Search-Flags           | 0x00000000                                                                                                              |
| System-Flags           | 0x00000012                                                                                                              |
| Classes utilisées dans        | [**Nœud DNS**](c-dnsnode.md)<br/> [**Zone DNS**](c-dnszone.md)<br/> [**Domaine**](c-domain.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrée | Valeur |
|------------------------|-------------------------------------------------------------------------------------------------------------------------|
| ID de lien                | \-                                                                                                                      |
| MAPI-Id                | \-                                                                                                                      |
| System-Only            | Faux                                                                                                                   |
| Est de valeur unique       | Vrai                                                                                                                    |
| Est indexé             | Faux                                                                                                                   |
| Dans le catalogue global      | Vrai                                                                                                                    |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                                                                                            |
| Range-Lower            | 1                                                                                                                       |
| Range-Upper            | 255                                                                                                                     |
| Search-Flags           | 0x00000000                                                                                                              |
| System-Flags           | 0x00000012                                                                                                              |
| Classes utilisées dans        | [**Nœud DNS**](c-dnsnode.md)<br/> [**Zone DNS**](c-dnszone.md)<br/> [**Domaine**](c-domain.md)<br/> |



 

 





