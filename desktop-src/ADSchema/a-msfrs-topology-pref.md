---
title: MS-FRS-Topology-attribut pref
description: L’attribut ms-FRS-Topology-pref est utilisé pour enregistrer les paramètres de topologie NTFRS préférés.
ms.assetid: 2804ad8a-bec8-491b-84ea-bdff1c8635d0
ms.tgt_platform: multiple
keywords:
- Schéma Active Directory MS-FRS-Topology-pref Attribute
- Schéma AD d’attribut msFRS-Topology-pref
topic_type:
- apiref
api_name:
- ms-FRS-Topology-Pref
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de417b03385e51d6a97fd68097f81bcc0cb6b9db
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "103744668"
---
# <a name="ms-frs-topology-pref-attribute"></a>MS-FRS-Topology-attribut pref

L’attribut **MS-FRS-Topology-pref** est utilisé pour enregistrer les paramètres de topologie NTFRS préférés. Lorsqu’un membre FRS est ajouté ou supprimé au jeu de réplicas, ces attributs sont référencés et les modifications sont apportées aux connexions entre le reste des membres FRS dans le jeu de réplicas.

Les valeurs valides pour cet attribut sont les suivantes.

| Valeur | Description                              |
|-------|------------------------------------------|
| 1     | \_anneau RSTOPOLOGYPREF \_ FRS<br/>     |
| 2     | \_RSTOPOLOGYPREF FRS \_ HUBSPOKE<br/> |
| 3     | \_RSTOPOLOGYPREF FRS \_ FULLMESH<br/> |
| 4     | \_RSTOPOLOGYPREF FRS \_ personnalisé<br/>   |



 



| Entrée | Valeur |
|-------------------|--------------------------------------------------------------------|
| CN                | MS-FRS-Topology-préférences                                               |
| LDAP-Display-Name | msFRS-Topology-pref                                                |
| Taille              | \-                                                                 |
| Mettre à jour le privilège  | Administrateur de domaine                                               |
| Fréquence des mises à jour  | Lors de la création du jeu de réplicas ou de la modification de la topologie par défaut. |
| Attribute-Id      | 1.2.840.113556.1.4.1692                                            |
| System-ID-GUID    | 92aa27e0-5c50-402d-9ec1-ee847def9788                               |
| Syntaxe            | [**String(Unicode)**](s-string-unicode.md)                        |



## <a name="implementations"></a>Implémentations

-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-server-2003"></a>Windows Server 2003



| Entrée | Valeur |
|------------------------|-----------------------------------------------------------|
| ID de lien                | \-                                                        |
| MAPI-Id                | \-                                                        |
| System-Only            | Faux                                                     |
| Est de valeur unique       | Vrai                                                      |
| Est indexé             | Faux                                                     |
| Dans le catalogue global      | Faux                                                     |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                              |
| Range-Lower            | \-                                                        |
| Range-Upper            | \-                                                        |
| Search-Flags           | 0x00000000                                                |
| System-Flags           | 0x00000000                                                |
| Classes utilisées dans        | [**NTFRS-jeu de réplicas**](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrée | Valeur |
|------------------------|-----------------------------------------------------------|
| ID de lien                | \-                                                        |
| MAPI-Id                | \-                                                        |
| System-Only            | Faux                                                     |
| Est de valeur unique       | Vrai                                                      |
| Est indexé             | Faux                                                     |
| Dans le catalogue global      | Faux                                                     |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                              |
| Range-Lower            | \-                                                        |
| Range-Upper            | \-                                                        |
| Search-Flags           | 0x00000000                                                |
| System-Flags           | 0x00000000                                                |
| Classes utilisées dans        | [**NTFRS-jeu de réplicas**](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrée | Valeur |
|------------------------|-----------------------------------------------------------|
| ID de lien                | \-                                                        |
| MAPI-Id                | \-                                                        |
| System-Only            | Faux                                                     |
| Est de valeur unique       | Vrai                                                      |
| Est indexé             | Faux                                                     |
| Dans le catalogue global      | Faux                                                     |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                              |
| Range-Lower            | \-                                                        |
| Range-Upper            | \-                                                        |
| Search-Flags           | 0x00000000                                                |
| System-Flags           | 0x00000000                                                |
| Classes utilisées dans        | [**NTFRS-jeu de réplicas**](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrée | Valeur |
|------------------------|-----------------------------------------------------------|
| ID de lien                | \-                                                        |
| MAPI-Id                | \-                                                        |
| System-Only            | Faux                                                     |
| Est de valeur unique       | Vrai                                                      |
| Est indexé             | Faux                                                     |
| Dans le catalogue global      | Faux                                                     |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                              |
| Range-Lower            | \-                                                        |
| Range-Upper            | \-                                                        |
| Search-Flags           | 0x00000000                                                |
| System-Flags           | 0x00000000                                                |
| Classes utilisées dans        | [**NTFRS-jeu de réplicas**](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrée | Valeur |
|------------------------|-----------------------------------------------------------|
| ID de lien                | \-                                                        |
| MAPI-Id                | \-                                                        |
| System-Only            | Faux                                                     |
| Est de valeur unique       | Vrai                                                      |
| Est indexé             | Faux                                                     |
| Dans le catalogue global      | Faux                                                     |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                              |
| Range-Lower            | \-                                                        |
| Range-Upper            | \-                                                        |
| Search-Flags           | 0x00000000                                                |
| System-Flags           | 0x00000000                                                |
| Classes utilisées dans        | [**NTFRS-jeu de réplicas**](c-ntfrsreplicaset.md)<br/> |



 

 





