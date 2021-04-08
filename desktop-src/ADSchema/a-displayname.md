---
title: Attribut Display-Name
description: Nom complet d’un objet.
ms.assetid: 0ecf5ede-0351-4d59-bdbf-44baf729f2e2
ms.tgt_platform: multiple
keywords:
- Schéma AD d’attribut Display-Name
- Schéma AD attribut displayName
topic_type:
- apiref
api_name:
- Display-Name
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b4fe662ccbdf2157c7ed51a311739cf7d16273b
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "103744260"
---
# <a name="display-name-attribute"></a>Attribut Display-Name

Nom complet d’un objet. Il s’agit généralement de la combinaison du prénom, de l’initiale du deuxième prénom et du nom de famille des utilisateurs.



| Entrée | Valeur |
|-------------------|------------------------------------------------------------------------------|
| CN                | Display-Name                                                                 |
| LDAP-Display-Name | displayName                                                                  |
| Taille              | \-                                                                           |
| Mettre à jour le privilège  | Administrateur de domaine ou propriétaire du compte.                                       |
| Fréquence des mises à jour  | Lorsque l’enregistrement de l’utilisateur est créé et que le nom d’affichage doit être modifié. |
| Attribute-Id      | 1.2.840.113556.1.2.13                                                        |
| System-ID-GUID    | bf967953-0de6-11d0-a285-00aa003049e2                                         |
| Syntaxe            | [**String(Unicode)**](s-string-unicode.md)                                  |



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
|------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID de lien                | \-                                                                                                                                                                                                                                                                                                                                               |
| MAPI-Id                | \-                                                                                                                                                                                                                                                                                                                                               |
| System-Only            | Faux                                                                                                                                                                                                                                                                                                                                            |
| Est de valeur unique       | Vrai                                                                                                                                                                                                                                                                                                                                             |
| Est indexé             | Vrai                                                                                                                                                                                                                                                                                                                                             |
| Dans le catalogue global      | Vrai                                                                                                                                                                                                                                                                                                                                             |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                                                                                                                                                                                                                                                                                                                     |
| Range-Lower            | 0                                                                                                                                                                                                                                                                                                                                                |
| Range-Upper            | 256                                                                                                                                                                                                                                                                                                                                              |
| Search-Flags           | 0x00000005                                                                                                                                                                                                                                                                                                                                       |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                       |
| Classes utilisées dans        | [**Adresse-conteneur de livres**](c-addressbookcontainer.md)<br/> [**Modèle d’adresse**](c-addresstemplate.md)<br/> [**PKI-Certificate-modèle**](c-pkicertificatetemplate.md)<br/> [**Classe de service**](c-serviceclass.md)<br/> [**Instance de service**](c-serviceinstance.md)<br/> [**Retour au début**](c-top.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Entrée | Valeur |
|------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID de lien                | \-                                                                                                                                                                                                                                                                                                                                                                                                   |
| MAPI-Id                | \-                                                                                                                                                                                                                                                                                                                                                                                                   |
| System-Only            | Faux                                                                                                                                                                                                                                                                                                                                                                                                |
| Est de valeur unique       | Vrai                                                                                                                                                                                                                                                                                                                                                                                                 |
| Est indexé             | Vrai                                                                                                                                                                                                                                                                                                                                                                                                 |
| Dans le catalogue global      | Vrai                                                                                                                                                                                                                                                                                                                                                                                                 |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                                                                                                                                                                                                                                                                                                                                                                         |
| Range-Lower            | 0                                                                                                                                                                                                                                                                                                                                                                                                    |
| Range-Upper            | 256                                                                                                                                                                                                                                                                                                                                                                                                  |
| Search-Flags           | 0x00000005                                                                                                                                                                                                                                                                                                                                                                                           |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                                                           |
| Classes utilisées dans        | [**Adresse-conteneur de livres**](c-addressbookcontainer.md)<br/> [**Modèle d’adresse**](c-addresstemplate.md)<br/> [**inetOrgPerson**](c-inetorgperson.md)<br/> [**PKI-Certificate-modèle**](c-pkicertificatetemplate.md)<br/> [**Classe de service**](c-serviceclass.md)<br/> [**Instance de service**](c-serviceinstance.md)<br/> [**Retour au début**](c-top.md)<br/> |



## <a name="adam"></a>ADAM



| Entrée | Valeur |
|------------------------|---------------------------------|
| ID de lien                | \-                              |
| MAPI-Id                | \-                              |
| System-Only            | Faux                           |
| Est de valeur unique       | Vrai                            |
| Est indexé             | Vrai                            |
| Dans le catalogue global      | Vrai                            |
| Descripteur de sécurité NT | O :BAG : BAD : S :                    |
| Range-Lower            | 0                               |
| Range-Upper            | 256                             |
| Search-Flags           | 0x00000005                      |
| System-Flags           | 0x00000010                      |
| Classes utilisées dans        | [**Retour au début**](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrée | Valeur |
|------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID de lien                | \-                                                                                                                                                                                                                                                                                                                                                                                                   |
| MAPI-Id                | \-                                                                                                                                                                                                                                                                                                                                                                                                   |
| System-Only            | Faux                                                                                                                                                                                                                                                                                                                                                                                                |
| Est de valeur unique       | Vrai                                                                                                                                                                                                                                                                                                                                                                                                 |
| Est indexé             | Vrai                                                                                                                                                                                                                                                                                                                                                                                                 |
| Dans le catalogue global      | Vrai                                                                                                                                                                                                                                                                                                                                                                                                 |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                                                                                                                                                                                                                                                                                                                                                                         |
| Range-Lower            | 0                                                                                                                                                                                                                                                                                                                                                                                                    |
| Range-Upper            | 256                                                                                                                                                                                                                                                                                                                                                                                                  |
| Search-Flags           | 0x00000005                                                                                                                                                                                                                                                                                                                                                                                           |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                                                           |
| Classes utilisées dans        | [**Adresse-conteneur de livres**](c-addressbookcontainer.md)<br/> [**Modèle d’adresse**](c-addresstemplate.md)<br/> [**inetOrgPerson**](c-inetorgperson.md)<br/> [**PKI-Certificate-modèle**](c-pkicertificatetemplate.md)<br/> [**Classe de service**](c-serviceclass.md)<br/> [**Instance de service**](c-serviceinstance.md)<br/> [**Retour au début**](c-top.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrée | Valeur |
|------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID de lien                | \-                                                                                                                                                                                                                                                                                                                                                                                                   |
| MAPI-Id                | \-                                                                                                                                                                                                                                                                                                                                                                                                   |
| System-Only            | Faux                                                                                                                                                                                                                                                                                                                                                                                                |
| Est de valeur unique       | Vrai                                                                                                                                                                                                                                                                                                                                                                                                 |
| Est indexé             | Vrai                                                                                                                                                                                                                                                                                                                                                                                                 |
| Dans le catalogue global      | Vrai                                                                                                                                                                                                                                                                                                                                                                                                 |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                                                                                                                                                                                                                                                                                                                                                                         |
| Range-Lower            | 0                                                                                                                                                                                                                                                                                                                                                                                                    |
| Range-Upper            | 256                                                                                                                                                                                                                                                                                                                                                                                                  |
| Search-Flags           | 0x00000005                                                                                                                                                                                                                                                                                                                                                                                           |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                                                           |
| Classes utilisées dans        | [**Adresse-conteneur de livres**](c-addressbookcontainer.md)<br/> [**Modèle d’adresse**](c-addresstemplate.md)<br/> [**inetOrgPerson**](c-inetorgperson.md)<br/> [**PKI-Certificate-modèle**](c-pkicertificatetemplate.md)<br/> [**Classe de service**](c-serviceclass.md)<br/> [**Instance de service**](c-serviceinstance.md)<br/> [**Retour au début**](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrée | Valeur |
|------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID de lien                | \-                                                                                                                                                                                                                                                                                                                                                                                                   |
| MAPI-Id                | \-                                                                                                                                                                                                                                                                                                                                                                                                   |
| System-Only            | Faux                                                                                                                                                                                                                                                                                                                                                                                                |
| Est de valeur unique       | Vrai                                                                                                                                                                                                                                                                                                                                                                                                 |
| Est indexé             | Vrai                                                                                                                                                                                                                                                                                                                                                                                                 |
| Dans le catalogue global      | Vrai                                                                                                                                                                                                                                                                                                                                                                                                 |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                                                                                                                                                                                                                                                                                                                                                                         |
| Range-Lower            | 0                                                                                                                                                                                                                                                                                                                                                                                                    |
| Range-Upper            | 256                                                                                                                                                                                                                                                                                                                                                                                                  |
| Search-Flags           | 0x00000005                                                                                                                                                                                                                                                                                                                                                                                           |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                                                           |
| Classes utilisées dans        | [**Adresse-conteneur de livres**](c-addressbookcontainer.md)<br/> [**Modèle d’adresse**](c-addresstemplate.md)<br/> [**inetOrgPerson**](c-inetorgperson.md)<br/> [**PKI-Certificate-modèle**](c-pkicertificatetemplate.md)<br/> [**Classe de service**](c-serviceclass.md)<br/> [**Instance de service**](c-serviceinstance.md)<br/> [**Retour au début**](c-top.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrée | Valeur |
|------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID de lien                | \-                                                                                                                                                                                                                                                                                                                                                                                                   |
| MAPI-Id                | \-                                                                                                                                                                                                                                                                                                                                                                                                   |
| System-Only            | Faux                                                                                                                                                                                                                                                                                                                                                                                                |
| Est de valeur unique       | Vrai                                                                                                                                                                                                                                                                                                                                                                                                 |
| Est indexé             | Vrai                                                                                                                                                                                                                                                                                                                                                                                                 |
| Dans le catalogue global      | Vrai                                                                                                                                                                                                                                                                                                                                                                                                 |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                                                                                                                                                                                                                                                                                                                                                                         |
| Range-Lower            | 0                                                                                                                                                                                                                                                                                                                                                                                                    |
| Range-Upper            | 256                                                                                                                                                                                                                                                                                                                                                                                                  |
| Search-Flags           | 0x00000005                                                                                                                                                                                                                                                                                                                                                                                           |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                                                           |
| Classes utilisées dans        | [**Adresse-conteneur de livres**](c-addressbookcontainer.md)<br/> [**Modèle d’adresse**](c-addresstemplate.md)<br/> [**inetOrgPerson**](c-inetorgperson.md)<br/> [**PKI-Certificate-modèle**](c-pkicertificatetemplate.md)<br/> [**Classe de service**](c-serviceclass.md)<br/> [**Instance de service**](c-serviceinstance.md)<br/> [**Retour au début**](c-top.md)<br/> |



 

 





