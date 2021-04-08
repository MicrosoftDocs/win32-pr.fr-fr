---
title: Propriété User-Account-restrictions définies
description: Jeu de propriétés contenant les attributs utilisateur qui décrivent les restrictions de compte.
ms.assetid: 5616fede-12b1-41bd-b445-11c0e1ff66db
ms.tgt_platform: multiple
keywords:
- Propriété compte d’utilisateur-restrictions définir le schéma AD
topic_type:
- apiref
api_name:
- User-Account-Restrictions
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a8c3c39c80c83f321c654e675ccd87950cfd4bcf
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "103942969"
---
# <a name="user-account-restrictions-property-set"></a>Propriété User-Account-restrictions définies

Jeu de propriétés contenant les attributs utilisateur qui décrivent les restrictions de compte.



| Entrée | Valeur |
|--------------|--------------------------------------|
| CN           | Compte d’utilisateur-restrictions            |
| Display-Name | Restrictions de compte                 |
| Rights-GUID  | 4c164200-20c0-11d0-a768-00aa006e0529 |



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
|-------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Applies-To              | [**Utilisateur**](c-user.md)<br/> [**Computer**](c-computer.md)<br/>                                                                                                                                                   |
| Localisation-Display-ID | 9                                                                                                                                                                                                                             |
| Membres du jeu de propriétés    | [**Compte-expire**](a-accountexpires.md)<br/> [**Pwd-dernier jeu**](a-pwdlastset.md)<br/> [**Contrôle de compte d’utilisateur**](a-useraccountcontrol.md)<br/> [**Paramètres utilisateur**](a-userparameters.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Entrée | Valeur |
|-------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Applies-To              | [**Utilisateur**](c-user.md)<br/> [**Computer**](c-computer.md)<br/> [**inetOrgPerson**](c-inetorgperson.md)<br/>                                                                                                                                                                                              |
| Localisation-Display-ID | 9                                                                                                                                                                                                                                                                                                                            |
| Membres du jeu de propriétés    | [**Compte-expire**](a-accountexpires.md)<br/> [**ms-DS-utilisateur-compte-contrôle-calculé**](a-msds-user-account-control-computed.md)<br/> [**Pwd-dernier jeu**](a-pwdlastset.md)<br/> [**Contrôle de compte d’utilisateur**](a-useraccountcontrol.md)<br/> [**Paramètres utilisateur**](a-userparameters.md)<br/> |



## <a name="adam"></a>ADAM



| Entrée | Valeur |
|-------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Applies-To              | \-                                                                                                                                                                                                    |
| Localisation-Display-ID | 9                                                                                                                                                                                                     |
| Membres du jeu de propriétés    | [**Compte-expire**](a-accountexpires.md)<br/> [**ms-DS-utilisateur-compte-contrôle-calculé**](a-msds-user-account-control-computed.md)<br/> [**Pwd-dernier jeu**](a-pwdlastset.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrée | Valeur |
|-------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Applies-To              | [**Utilisateur**](c-user.md)<br/> [**Computer**](c-computer.md)<br/> [**inetOrgPerson**](c-inetorgperson.md)<br/>                                                                                                                                                                                              |
| Localisation-Display-ID | 9                                                                                                                                                                                                                                                                                                                            |
| Membres du jeu de propriétés    | [**Compte-expire**](a-accountexpires.md)<br/> [**ms-DS-utilisateur-compte-contrôle-calculé**](a-msds-user-account-control-computed.md)<br/> [**Pwd-dernier jeu**](a-pwdlastset.md)<br/> [**Contrôle de compte d’utilisateur**](a-useraccountcontrol.md)<br/> [**Paramètres utilisateur**](a-userparameters.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrée | Valeur |
|-------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Applies-To              | [**Utilisateur**](c-user.md)<br/> [**Computer**](c-computer.md)<br/> [**inetOrgPerson**](c-inetorgperson.md)<br/>                                                                                                                                                                                                                                                                                                   |
| Localisation-Display-ID | 9                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| Membres du jeu de propriétés    | [**Compte-expire**](a-accountexpires.md)<br/> [**ms-DS-utilisateur-compte-contrôle-calculé**](a-msds-user-account-control-computed.md)<br/> [**ms-DS-utilisateur-expiration du mot de passe-heure de calcul**](a-msds-userpasswordexpirytimecomputed.md)<br/> [**Pwd-dernier jeu**](a-pwdlastset.md)<br/> [**Contrôle de compte d’utilisateur**](a-useraccountcontrol.md)<br/> [**Paramètres utilisateur**](a-userparameters.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrée | Valeur |
|-------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Applies-To              | [**Utilisateur**](c-user.md)<br/> [**Computer**](c-computer.md)<br/> [**ms-DS-Managed-service-account**](c-msds-managedserviceaccount.md)<br/> [**inetOrgPerson**](c-inetorgperson.md)<br/>                                                                                                                                                                                                                  |
| Localisation-Display-ID | 9                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| Membres du jeu de propriétés    | [**Compte-expire**](a-accountexpires.md)<br/> [**ms-DS-utilisateur-compte-contrôle-calculé**](a-msds-user-account-control-computed.md)<br/> [**ms-DS-utilisateur-expiration du mot de passe-heure de calcul**](a-msds-userpasswordexpirytimecomputed.md)<br/> [**Pwd-dernier jeu**](a-pwdlastset.md)<br/> [**Contrôle de compte d’utilisateur**](a-useraccountcontrol.md)<br/> [**Paramètres utilisateur**](a-userparameters.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrée | Valeur |
|-------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Applies-To              | [**Utilisateur**](c-user.md)<br/> [**Computer**](c-computer.md)<br/> [**ms-DS-Managed-service-account**](c-msds-managedserviceaccount.md)<br/> [**inetOrgPerson**](c-inetorgperson.md)<br/>                                                                                                                                                                                                                  |
| Localisation-Display-ID | 9                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| Membres du jeu de propriétés    | [**Compte-expire**](a-accountexpires.md)<br/> [**ms-DS-utilisateur-compte-contrôle-calculé**](a-msds-user-account-control-computed.md)<br/> [**ms-DS-utilisateur-expiration du mot de passe-heure de calcul**](a-msds-userpasswordexpirytimecomputed.md)<br/> [**Pwd-dernier jeu**](a-pwdlastset.md)<br/> [**Contrôle de compte d’utilisateur**](a-useraccountcontrol.md)<br/> [**Paramètres utilisateur**](a-userparameters.md)<br/> |



 

 





