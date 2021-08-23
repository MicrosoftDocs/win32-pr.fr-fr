---
title: Attribut title
description: Contient la fonction de l’utilisateur. Cette propriété est couramment utilisée pour indiquer la fonction formelle, telle que le programmeur senior, plutôt que la classe professionnelle, comme le programmeur. Il n’est généralement pas utilisé pour les titres de suffixe tels que Esq. ou DDS.
ms.assetid: 4a6899a7-ddbf-4dd0-b088-3739716f33df
ms.tgt_platform: multiple
keywords:
- Attribut titre-schéma AD
- attribut titre-schéma AD
topic_type:
- apiref
api_name:
- Title
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c8885a557e8fbec17d6d58d68fdea0f99039f0e09e34a8da01954dc7b4979fc3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119645029"
---
# <a name="title-attribute-ad-schema"></a>Attribut title (schéma Active Directory)

Contient la fonction de l’utilisateur. Cette propriété est couramment utilisée pour indiquer la fonction formelle, telle que le programmeur senior, plutôt que la classe professionnelle, comme le programmeur. Il n’est généralement pas utilisé pour les titres de suffixe tels que Esq. ou DDS.



| Entrée | Valeur |
|-------------------|---------------------------------------------------------------------------|
| CN                | Titre                                                                     |
| LDAP-Display-Name | title                                                                     |
| Taille              | \-                                                                        |
| Mettre à jour le privilège  | Administrateur de domaine ou propriétaire du compte.                                    |
| Fréquence des mises à jour  | Lorsque l’enregistrement de l’utilisateur est créé et chaque fois que le titre doit être modifié. |
| Attribute-Id      | 2.5.4.12                                                                  |
| System-ID-GUID    | bf967a55-0de6-11d0-a285-00aa003049e2                                      |
| Syntaxe            | [**String(Unicode)**](s-string-unicode.md)                               |



## <a name="implementations"></a>Implémentations

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server



| Entrée | Valeur |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| ID de lien                | \-                                                                                                                              |
| MAPI-Id                | 0x3A17                                                                                                                          |
| System-Only            | Faux                                                                                                                           |
| Est de valeur unique       | Vrai                                                                                                                            |
| Est indexé             | Faux                                                                                                                           |
| Dans le catalogue global      | Faux                                                                                                                           |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                                                                                                    |
| Range-Lower            | 1                                                                                                                               |
| Range-Upper            | 64                                                                                                                              |
| Search-Flags           | 0x00000000                                                                                                                      |
| System-Flags           | 0x00000010                                                                                                                      |
| Classes utilisées dans        | [**Organizational-Person**](c-organizationalperson.md)<br/> [**Personne privée**](c-residentialperson.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Entrée | Valeur |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| ID de lien                | \-                                                                                                                              |
| MAPI-Id                | 0x3A17                                                                                                                          |
| System-Only            | Faux                                                                                                                           |
| Est de valeur unique       | Vrai                                                                                                                            |
| Est indexé             | Faux                                                                                                                           |
| Dans le catalogue global      | Faux                                                                                                                           |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                                                                                                    |
| Range-Lower            | 1                                                                                                                               |
| Range-Upper            | 64                                                                                                                              |
| Search-Flags           | 0x00000000                                                                                                                      |
| System-Flags           | 0x00000010                                                                                                                      |
| Classes utilisées dans        | [**Organizational-Person**](c-organizationalperson.md)<br/> [**Personne privée**](c-residentialperson.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrée | Valeur |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| ID de lien                | \-                                                                                                                              |
| MAPI-Id                | 0x3A17                                                                                                                          |
| System-Only            | Faux                                                                                                                           |
| Est de valeur unique       | Vrai                                                                                                                            |
| Est indexé             | Faux                                                                                                                           |
| Dans le catalogue global      | Faux                                                                                                                           |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                                                                                                    |
| Range-Lower            | 1                                                                                                                               |
| Range-Upper            | 64                                                                                                                              |
| Search-Flags           | 0x00000000                                                                                                                      |
| System-Flags           | 0x00000010                                                                                                                      |
| Classes utilisées dans        | [**Organizational-Person**](c-organizationalperson.md)<br/> [**Personne privée**](c-residentialperson.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrée | Valeur |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| ID de lien                | \-                                                                                                                              |
| MAPI-Id                | 0x3A17                                                                                                                          |
| System-Only            | Faux                                                                                                                           |
| Est de valeur unique       | Vrai                                                                                                                            |
| Est indexé             | Faux                                                                                                                           |
| Dans le catalogue global      | Faux                                                                                                                           |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                                                                                                    |
| Range-Lower            | 1                                                                                                                               |
| Range-Upper            | 128                                                                                                                             |
| Search-Flags           | 0x00000000                                                                                                                      |
| System-Flags           | 0x00000010                                                                                                                      |
| Classes utilisées dans        | [**Organizational-Person**](c-organizationalperson.md)<br/> [**Personne privée**](c-residentialperson.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrée | Valeur |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| ID de lien                | \-                                                                                                                              |
| MAPI-Id                | 0x3A17                                                                                                                          |
| System-Only            | Faux                                                                                                                           |
| Est de valeur unique       | Vrai                                                                                                                            |
| Est indexé             | Faux                                                                                                                           |
| Dans le catalogue global      | Faux                                                                                                                           |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                                                                                                    |
| Range-Lower            | 1                                                                                                                               |
| Range-Upper            | 128                                                                                                                             |
| Search-Flags           | 0x00000000                                                                                                                      |
| System-Flags           | 0x00000010                                                                                                                      |
| Classes utilisées dans        | [**Organizational-Person**](c-organizationalperson.md)<br/> [**Personne privée**](c-residentialperson.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrée | Valeur |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| ID de lien                | \-                                                                                                                              |
| MAPI-Id                | 0x3A17                                                                                                                          |
| System-Only            | Faux                                                                                                                           |
| Est de valeur unique       | Vrai                                                                                                                            |
| Est indexé             | Faux                                                                                                                           |
| Dans le catalogue global      | Faux                                                                                                                           |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                                                                                                    |
| Range-Lower            | 1                                                                                                                               |
| Range-Upper            | 128                                                                                                                             |
| Search-Flags           | 0x00000000                                                                                                                      |
| System-Flags           | 0x00000010                                                                                                                      |
| Classes utilisées dans        | [**Organizational-Person**](c-organizationalperson.md)<br/> [**Personne privée**](c-residentialperson.md)<br/> |



 

 





