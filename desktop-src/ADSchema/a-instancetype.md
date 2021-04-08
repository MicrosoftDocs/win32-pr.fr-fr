---
title: Attribut Instance-Type
description: Champ de champ binaire qui détermine la façon dont l’objet est instancié sur un serveur particulier.
ms.assetid: ed77c302-3d80-4292-8e48-bfc6cb5079ee
ms.tgt_platform: multiple
keywords:
- Schéma AD d’attribut Instance-Type
- Schéma Active Directory de l’attribut instanceType
topic_type:
- apiref
api_name:
- Instance-Type
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e31eec3c5a7a189f4623e8e77badb3b1e83e0cd4
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "103744836"
---
# <a name="instance-type-attribute"></a>Attribut Instance-Type

Champ de champ binaire qui détermine la façon dont l’objet est instancié sur un serveur particulier. La valeur de cet attribut peut différer sur différents réplicas même si les réplicas sont synchronisés.

Cet attribut peut avoir la valeur zéro ou une combinaison d’une ou plusieurs des valeurs suivantes.

| Valeur      | Description                                                                                        |
|------------|----------------------------------------------------------------------------------------------------|
| 0x00000001 | Le début du contexte d’appellation.                                                                        |
| 0x00000002 | Ce réplica n’est pas instancié.                                                                  |
| 0x00000004 | L’objet est accessible en écriture dans ce répertoire.                                                          |
| 0x00000008 | Le contexte d’appellation au-dessus de celui-ci est conservé sur ce répertoire.                                       |
| 0x00000010 | Le contexte d’appellation est en cours de construction pour la première fois à l’aide de la réplication. |
| 0x00000020 | Le contexte d’appellation est en cours de suppression du DSA local.                          |



 



| Entrée | Valeur |
|-------------------|------------------------------------------------|
| CN                | Instance-Type                                  |
| LDAP-Display-Name | instanceType                                   |
| Taille              | 4 octets.                                       |
| Mettre à jour le privilège  | Cette valeur est définie par l’administrateur de schéma. |
| Fréquence des mises à jour  | Lorsque l’objet est créé.                    |
| Attribute-Id      | 1.2.840.113556.1.2.1                           |
| System-ID-GUID    | bf96798c-0de6-11d0-a285-00aa003049e2           |
| Syntaxe            | [**Enumeration**](s-enumeration.md)           |



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
|------------------------|---------------------------------|
| ID de lien                | \-                              |
| MAPI-Id                | 0x80BD                          |
| System-Only            | Vrai                            |
| Est de valeur unique       | Vrai                            |
| Est indexé             | Faux                           |
| Dans le catalogue global      | Vrai                            |
| Descripteur de sécurité NT | O :BAG : BAD : S :                    |
| Range-Lower            | \-                              |
| Range-Upper            | \-                              |
| Search-Flags           | 0x00000008                      |
| System-Flags           | 0x00000012                      |
| Classes utilisées dans        | [**Retour au début**](c-top.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Entrée | Valeur |
|------------------------|---------------------------------|
| ID de lien                | \-                              |
| MAPI-Id                | 0x80BD                          |
| System-Only            | Vrai                            |
| Est de valeur unique       | Vrai                            |
| Est indexé             | Faux                           |
| Dans le catalogue global      | Vrai                            |
| Descripteur de sécurité NT | O :BAG : BAD : S :                    |
| Range-Lower            | \-                              |
| Range-Upper            | \-                              |
| Search-Flags           | 0x00000008                      |
| System-Flags           | 0x00000012                      |
| Classes utilisées dans        | [**Retour au début**](c-top.md)<br/> |



## <a name="adam"></a>ADAM



| Entrée | Valeur |
|------------------------|---------------------------------|
| ID de lien                | \-                              |
| MAPI-Id                | 0x80BD                          |
| System-Only            | Vrai                            |
| Est de valeur unique       | Vrai                            |
| Est indexé             | Faux                           |
| Dans le catalogue global      | Vrai                            |
| Descripteur de sécurité NT | O :BAG : BAD : S :                    |
| Range-Lower            | \-                              |
| Range-Upper            | \-                              |
| Search-Flags           | 0x00000008                      |
| System-Flags           | 0x00000012                      |
| Classes utilisées dans        | [**Retour au début**](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrée | Valeur |
|------------------------|---------------------------------|
| ID de lien                | \-                              |
| MAPI-Id                | 0x80BD                          |
| System-Only            | Vrai                            |
| Est de valeur unique       | Vrai                            |
| Est indexé             | Faux                           |
| Dans le catalogue global      | Vrai                            |
| Descripteur de sécurité NT | O :BAG : BAD : S :                    |
| Range-Lower            | \-                              |
| Range-Upper            | \-                              |
| Search-Flags           | 0x00000008                      |
| System-Flags           | 0x00000012                      |
| Classes utilisées dans        | [**Retour au début**](c-top.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrée | Valeur |
|------------------------|---------------------------------|
| ID de lien                | \-                              |
| MAPI-Id                | 0x80BD                          |
| System-Only            | Vrai                            |
| Est de valeur unique       | Vrai                            |
| Est indexé             | Faux                           |
| Dans le catalogue global      | Vrai                            |
| Descripteur de sécurité NT | O :BAG : BAD : S :                    |
| Range-Lower            | \-                              |
| Range-Upper            | \-                              |
| Search-Flags           | 0x00000008                      |
| System-Flags           | 0x00000012                      |
| Classes utilisées dans        | [**Retour au début**](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrée | Valeur |
|------------------------|---------------------------------|
| ID de lien                | \-                              |
| MAPI-Id                | 0x80BD                          |
| System-Only            | Vrai                            |
| Est de valeur unique       | Vrai                            |
| Est indexé             | Faux                           |
| Dans le catalogue global      | Vrai                            |
| Descripteur de sécurité NT | O :BAG : BAD : S :                    |
| Range-Lower            | \-                              |
| Range-Upper            | \-                              |
| Search-Flags           | 0x00000008                      |
| System-Flags           | 0x00000012                      |
| Classes utilisées dans        | [**Retour au début**](c-top.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrée | Valeur |
|------------------------|---------------------------------|
| ID de lien                | \-                              |
| MAPI-Id                | 0x80BD                          |
| System-Only            | Vrai                            |
| Est de valeur unique       | Vrai                            |
| Est indexé             | Faux                           |
| Dans le catalogue global      | Vrai                            |
| Descripteur de sécurité NT | O :BAG : BAD : S :                    |
| Range-Lower            | \-                              |
| Range-Upper            | \-                              |
| Search-Flags           | 0x00000008                      |
| System-Flags           | 0x00000012                      |
| Classes utilisées dans        | [**Retour au début**](c-top.md)<br/> |



 

 





