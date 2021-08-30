---
title: Install-attribut au niveau de l’interface utilisateur
description: Cet attribut contient des informations sur le type (niveau) d’installation utilisé pour l’interface utilisateur.
ms.assetid: 718e04c7-ea96-4519-b312-12534ffd66df
ms.tgt_platform: multiple
keywords:
- Installer-attribut au niveau de l’interface utilisateur schéma AD
- Schéma AD de l’attribut installUiLevel
topic_type:
- apiref
api_name:
- Install-Ui-Level
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 87c692c20a42c843bfa9b56b81a263b7f1dfa41404e22b3509de812af3faa87e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119925289"
---
# <a name="install-ui-level-attribute"></a>Install-attribut au niveau de l’interface utilisateur

Cet attribut contient des informations sur le type (niveau) d’installation utilisé pour l’interface utilisateur. Les niveaux d’installation possibles sont les suivants : 2 INSTALLUILEVEL \_ aucun (installation sans assistance) 3 INSTALLUILEVEL \_ de base (installation simple avec gestion des erreurs) 4 INSTALLUILEVEL \_ réduit (IU créée, boîtes de dialogue de l’Assistant supprimées) 5 INSTALLUILEVEL \_ complet (interface utilisateur créée avec les assistants, progression, erreurs)



| Entrée | Valeur |
|-------------------|--------------------------------------|
| CN                | Installer-au niveau de l’interface utilisateur                     |
| LDAP-Display-Name | installUiLevel                       |
| Taille              | \-                                   |
| Mettre à jour le privilège  | \-                                   |
| Fréquence des mises à jour  | \-                                   |
| Attribute-Id      | 1.2.840.113556.1.4.847               |
| System-ID-GUID    | 96a7dd64-9118-11d1-aebc-0000f80367c1 |
| Syntaxe            | [**Énumération**](s-enumeration.md) |



## <a name="implementations"></a>Implémentations

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server



| Entrée | Valeur |
|------------------------|------------------------------------------------------------------|
| ID de lien                | \-                                                               |
| MAPI-Id                | \-                                                               |
| System-Only            | Faux                                                            |
| Est de valeur unique       | Vrai                                                             |
| Est indexé             | Faux                                                            |
| Dans le catalogue global      | Faux                                                            |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                                     |
| Range-Lower            | \-                                                               |
| Range-Upper            | \-                                                               |
| Search-Flags           | 0x00000000                                                       |
| System-Flags           | 0x00000010                                                       |
| Classes utilisées dans        | [**Inscription de packages**](c-packageregistration.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Entrée | Valeur |
|------------------------|------------------------------------------------------------------|
| ID de lien                | \-                                                               |
| MAPI-Id                | \-                                                               |
| System-Only            | Faux                                                            |
| Est de valeur unique       | Vrai                                                             |
| Est indexé             | Faux                                                            |
| Dans le catalogue global      | Faux                                                            |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                                     |
| Range-Lower            | \-                                                               |
| Range-Upper            | \-                                                               |
| Search-Flags           | 0x00000000                                                       |
| System-Flags           | 0x00000010                                                       |
| Classes utilisées dans        | [**Inscription de packages**](c-packageregistration.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrée | Valeur |
|------------------------|------------------------------------------------------------------|
| ID de lien                | \-                                                               |
| MAPI-Id                | \-                                                               |
| System-Only            | Faux                                                            |
| Est de valeur unique       | Vrai                                                             |
| Est indexé             | Faux                                                            |
| Dans le catalogue global      | Faux                                                            |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                                     |
| Range-Lower            | \-                                                               |
| Range-Upper            | \-                                                               |
| Search-Flags           | 0x00000000                                                       |
| System-Flags           | 0x00000010                                                       |
| Classes utilisées dans        | [**Inscription de packages**](c-packageregistration.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrée | Valeur |
|------------------------|------------------------------------------------------------------|
| ID de lien                | \-                                                               |
| MAPI-Id                | \-                                                               |
| System-Only            | Faux                                                            |
| Est de valeur unique       | Vrai                                                             |
| Est indexé             | Faux                                                            |
| Dans le catalogue global      | Faux                                                            |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                                     |
| Range-Lower            | \-                                                               |
| Range-Upper            | \-                                                               |
| Search-Flags           | 0x00000000                                                       |
| System-Flags           | 0x00000010                                                       |
| Classes utilisées dans        | [**Inscription de packages**](c-packageregistration.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrée | Valeur |
|------------------------|------------------------------------------------------------------|
| ID de lien                | \-                                                               |
| MAPI-Id                | \-                                                               |
| System-Only            | Faux                                                            |
| Est de valeur unique       | Vrai                                                             |
| Est indexé             | Faux                                                            |
| Dans le catalogue global      | Faux                                                            |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                                     |
| Range-Lower            | \-                                                               |
| Range-Upper            | \-                                                               |
| Search-Flags           | 0x00000000                                                       |
| System-Flags           | 0x00000010                                                       |
| Classes utilisées dans        | [**Inscription de packages**](c-packageregistration.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrée | Valeur |
|------------------------|------------------------------------------------------------------|
| ID de lien                | \-                                                               |
| MAPI-Id                | \-                                                               |
| System-Only            | Faux                                                            |
| Est de valeur unique       | Vrai                                                             |
| Est indexé             | Faux                                                            |
| Dans le catalogue global      | Faux                                                            |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                                     |
| Range-Lower            | \-                                                               |
| Range-Upper            | \-                                                               |
| Search-Flags           | 0x00000000                                                       |
| System-Flags           | 0x00000010                                                       |
| Classes utilisées dans        | [**Inscription de packages**](c-packageregistration.md)<br/> |



 

 





