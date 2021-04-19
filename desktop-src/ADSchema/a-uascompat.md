---
title: Attribut UAS-Compat
description: Indique si le gestionnaire de compte de sécurité appliquera des tailles de données pour rendre les Active Directory compatibles avec le système de comptes d’utilisateur LanManager (UAS).
ms.assetid: 745e271e-28f4-4012-83a8-606d88de0221
ms.tgt_platform: multiple
keywords:
- Schéma AD d’attribut UAS-Compat
- Schéma AD de l’attribut uASCompat
topic_type:
- apiref
api_name:
- UAS-Compat
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f6bbf1088f48c697b03c4ef423930be2dbd24617
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "106514888"
---
# <a name="uas-compat-attribute"></a>Attribut UAS-Compat

Indique si le gestionnaire de compte de sécurité appliquera des tailles de données pour rendre les Active Directory compatibles avec le système de comptes d’utilisateur LanManager (UAS). Si cette valeur est égale à 0, aucune limite n’est appliquée. Si cette valeur est 1, les limites suivantes sont appliquées.



| Valeur                          | Longueur                         |
|--------------------------------|--------------------------------|
| Mot de passe<br/>            | 0 à 14 caractères<br/>  |
| Nom du compte<br/>        | de 0 à 20 caractères<br/>  |
| Nom de domaine<br/>         | de 0 à 15 caractères<br/>  |
| Nom d’ordinateur<br/>       | de 0 à 15 caractères<br/>  |
| Commentaires<br/>            | 0 à 48 caractères<br/>  |
| Répertoire de base<br/>      | 0 à 256 caractères<br/> |
| Chemin du script<br/>         | 0 à 256 caractères<br/> |
| Unités de temps par semaine<br/> | 168 bits (21 octets)<br/> |



 



| Entrée | Valeur |
|-------------------|--------------------------------------|
| CN                | UAS-Compat                           |
| LDAP-Display-Name | uASCompat                            |
| Taille              | \-                                   |
| Mettre à jour le privilège  | Effectuée par un administrateur.       |
| Fréquence des mises à jour  | \-                                   |
| Attribute-Id      | 1.2.840.113556.1.4.155               |
| System-ID-GUID    | bf967a61-0de6-11d0-a285-00aa003049e2 |
| Syntaxe            | [**Enumeration**](s-enumeration.md) |



## <a name="implementations"></a>Implémentations

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server



| Entrée | Valeur |
|------------------------|-------------------------------------------------------|
| ID de lien                | \-                                                    |
| MAPI-Id                | \-                                                    |
| System-Only            | Faux                                                 |
| Est de valeur unique       | Vrai                                                  |
| Est indexé             | Faux                                                 |
| Dans le catalogue global      | Faux                                                 |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                          |
| Range-Lower            | \-                                                    |
| Range-Upper            | \-                                                    |
| Search-Flags           | 0x00000000                                            |
| System-Flags           | 0x00000010                                            |
| Classes utilisées dans        | [**Sam-domaine-base**](c-samdomainbase.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Entrée | Valeur |
|------------------------|-------------------------------------------------------|
| ID de lien                | \-                                                    |
| MAPI-Id                | \-                                                    |
| System-Only            | Faux                                                 |
| Est de valeur unique       | Vrai                                                  |
| Est indexé             | Faux                                                 |
| Dans le catalogue global      | Faux                                                 |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                          |
| Range-Lower            | \-                                                    |
| Range-Upper            | \-                                                    |
| Search-Flags           | 0x00000000                                            |
| System-Flags           | 0x00000010                                            |
| Classes utilisées dans        | [**Sam-domaine-base**](c-samdomainbase.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrée | Valeur |
|------------------------|-------------------------------------------------------|
| ID de lien                | \-                                                    |
| MAPI-Id                | \-                                                    |
| System-Only            | Faux                                                 |
| Est de valeur unique       | Vrai                                                  |
| Est indexé             | Faux                                                 |
| Dans le catalogue global      | Faux                                                 |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                          |
| Range-Lower            | \-                                                    |
| Range-Upper            | \-                                                    |
| Search-Flags           | 0x00000000                                            |
| System-Flags           | 0x00000010                                            |
| Classes utilisées dans        | [**Sam-domaine-base**](c-samdomainbase.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrée | Valeur |
|------------------------|-------------------------------------------------------|
| ID de lien                | \-                                                    |
| MAPI-Id                | \-                                                    |
| System-Only            | Faux                                                 |
| Est de valeur unique       | Vrai                                                  |
| Est indexé             | Faux                                                 |
| Dans le catalogue global      | Faux                                                 |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                          |
| Range-Lower            | \-                                                    |
| Range-Upper            | \-                                                    |
| Search-Flags           | 0x00000000                                            |
| System-Flags           | 0x00000010                                            |
| Classes utilisées dans        | [**Sam-domaine-base**](c-samdomainbase.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrée | Valeur |
|------------------------|-------------------------------------------------------|
| ID de lien                | \-                                                    |
| MAPI-Id                | \-                                                    |
| System-Only            | Faux                                                 |
| Est de valeur unique       | Vrai                                                  |
| Est indexé             | Faux                                                 |
| Dans le catalogue global      | Faux                                                 |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                          |
| Range-Lower            | \-                                                    |
| Range-Upper            | \-                                                    |
| Search-Flags           | 0x00000000                                            |
| System-Flags           | 0x00000010                                            |
| Classes utilisées dans        | [**Sam-domaine-base**](c-samdomainbase.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrée | Valeur |
|------------------------|-------------------------------------------------------|
| ID de lien                | \-                                                    |
| MAPI-Id                | \-                                                    |
| System-Only            | Faux                                                 |
| Est de valeur unique       | Vrai                                                  |
| Est indexé             | Faux                                                 |
| Dans le catalogue global      | Faux                                                 |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                          |
| Range-Lower            | \-                                                    |
| Range-Upper            | \-                                                    |
| Search-Flags           | 0x00000000                                            |
| System-Flags           | 0x00000010                                            |
| Classes utilisées dans        | [**Sam-domaine-base**](c-samdomainbase.md)<br/> |



 

 





