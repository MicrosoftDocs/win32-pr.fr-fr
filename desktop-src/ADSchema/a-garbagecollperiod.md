---
title: Attribut de période de garbage-coll.
description: Cet attribut se trouve dans le service d’annuaire CN, CN Windows NT, CN Services, CN Configuration,... dessin. Il représente le temps, en heures, entre les exécutions de garbage collection du service d’annuaire.
ms.assetid: 982a75f9-04b5-489e-99b3-a9fd3fb280c8
ms.tgt_platform: multiple
keywords:
- Schéma AD d’attribut de période de nettoyage de la mémoire
- Schéma AD de l’attribut garbageCollPeriod
topic_type:
- apiref
api_name:
- Garbage-Coll-Period
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 034b4612565bea508979ab91958a76d974c50e0d5ac9f17d0f0af388c8f149d7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119323289"
---
# <a name="garbage-coll-period-attribute"></a>Attribut de période de garbage-coll.

Cet attribut se trouve dans le dossier CN = Directory Service, CN = Windows NT, CN = Services, CN = Configuration,... dessin. Il représente le temps, en heures, entre les exécutions de garbage collection du service d’annuaire.



| Entrée | Valeur |
|-------------------|--------------------------------------|
| CN                | Garbage-coll-period                  |
| LDAP-Display-Name | garbageCollPeriod                    |
| Taille              | 4 octets                              |
| Mettre à jour le privilège  | Administrateur de domaine                 |
| Fréquence des mises à jour  | Très rare.                           |
| Attribute-Id      | 1.2.840.113556.1.2.301               |
| System-ID-GUID    | 5fd424a1-1262-11d0-a060-00aa006c33ed |
| Syntaxe            | [**Énumération**](s-enumeration.md) |



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
|------------------------|-------------------------------------------------------------------------------------------------------|
| ID de lien                | \-                                                                                                    |
| MAPI-Id                | 0x80AF                                                                                                |
| System-Only            | Faux                                                                                                 |
| Est de valeur unique       | Vrai                                                                                                  |
| Est indexé             | Faux                                                                                                 |
| Dans le catalogue global      | Faux                                                                                                 |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                                                                          |
| Range-Lower            | \-                                                                                                    |
| Range-Upper            | \-                                                                                                    |
| Search-Flags           | 0x00000000                                                                                            |
| System-Flags           | 0x00000010                                                                                            |
| Classes utilisées dans        | [**E-mail-destinataire**](c-mailrecipient.md)<br/> [**NTDS-service**](c-ntdsservice.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Entrée | Valeur |
|------------------------|-------------------------------------------------------------------------------------------------------|
| ID de lien                | \-                                                                                                    |
| MAPI-Id                | 0x80AF                                                                                                |
| System-Only            | Faux                                                                                                 |
| Est de valeur unique       | Vrai                                                                                                  |
| Est indexé             | Faux                                                                                                 |
| Dans le catalogue global      | Faux                                                                                                 |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                                                                          |
| Range-Lower            | \-                                                                                                    |
| Range-Upper            | \-                                                                                                    |
| Search-Flags           | 0x00000000                                                                                            |
| System-Flags           | 0x00000010                                                                                            |
| Classes utilisées dans        | [**E-mail-destinataire**](c-mailrecipient.md)<br/> [**NTDS-service**](c-ntdsservice.md)<br/> |



## <a name="adam"></a>ADAM



| Entrée | Valeur |
|------------------------|--------------------------------------------------|
| ID de lien                | \-                                               |
| MAPI-Id                | 0x80AF                                           |
| System-Only            | Faux                                            |
| Est de valeur unique       | Vrai                                             |
| Est indexé             | Faux                                            |
| Dans le catalogue global      | Faux                                            |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                     |
| Range-Lower            | \-                                               |
| Range-Upper            | \-                                               |
| Search-Flags           | 0x00000000                                       |
| System-Flags           | 0x00000010                                       |
| Classes utilisées dans        | [**NTDS-service**](c-ntdsservice.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrée | Valeur |
|------------------------|-------------------------------------------------------------------------------------------------------|
| ID de lien                | \-                                                                                                    |
| MAPI-Id                | 0x80AF                                                                                                |
| System-Only            | Faux                                                                                                 |
| Est de valeur unique       | Vrai                                                                                                  |
| Est indexé             | Faux                                                                                                 |
| Dans le catalogue global      | Faux                                                                                                 |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                                                                          |
| Range-Lower            | \-                                                                                                    |
| Range-Upper            | \-                                                                                                    |
| Search-Flags           | 0x00000000                                                                                            |
| System-Flags           | 0x00000010                                                                                            |
| Classes utilisées dans        | [**E-mail-destinataire**](c-mailrecipient.md)<br/> [**NTDS-service**](c-ntdsservice.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrée | Valeur |
|------------------------|-------------------------------------------------------------------------------------------------------|
| ID de lien                | \-                                                                                                    |
| MAPI-Id                | 0x80AF                                                                                                |
| System-Only            | Faux                                                                                                 |
| Est de valeur unique       | Vrai                                                                                                  |
| Est indexé             | Faux                                                                                                 |
| Dans le catalogue global      | Faux                                                                                                 |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                                                                          |
| Range-Lower            | \-                                                                                                    |
| Range-Upper            | \-                                                                                                    |
| Search-Flags           | 0x00000000                                                                                            |
| System-Flags           | 0x00000010                                                                                            |
| Classes utilisées dans        | [**E-mail-destinataire**](c-mailrecipient.md)<br/> [**NTDS-service**](c-ntdsservice.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrée | Valeur |
|------------------------|-------------------------------------------------------------------------------------------------------|
| ID de lien                | \-                                                                                                    |
| MAPI-Id                | 0x80AF                                                                                                |
| System-Only            | Faux                                                                                                 |
| Est de valeur unique       | Vrai                                                                                                  |
| Est indexé             | Faux                                                                                                 |
| Dans le catalogue global      | Faux                                                                                                 |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                                                                          |
| Range-Lower            | \-                                                                                                    |
| Range-Upper            | \-                                                                                                    |
| Search-Flags           | 0x00000000                                                                                            |
| System-Flags           | 0x00000010                                                                                            |
| Classes utilisées dans        | [**E-mail-destinataire**](c-mailrecipient.md)<br/> [**NTDS-service**](c-ntdsservice.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrée | Valeur |
|------------------------|-------------------------------------------------------------------------------------------------------|
| ID de lien                | \-                                                                                                    |
| MAPI-Id                | 0x80AF                                                                                                |
| System-Only            | Faux                                                                                                 |
| Est de valeur unique       | Vrai                                                                                                  |
| Est indexé             | Faux                                                                                                 |
| Dans le catalogue global      | Faux                                                                                                 |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                                                                          |
| Range-Lower            | \-                                                                                                    |
| Range-Upper            | \-                                                                                                    |
| Search-Flags           | 0x00000000                                                                                            |
| System-Flags           | 0x00000010                                                                                            |
| Classes utilisées dans        | [**E-mail-destinataire**](c-mailrecipient.md)<br/> [**NTDS-service**](c-ntdsservice.md)<br/> |



 

 





