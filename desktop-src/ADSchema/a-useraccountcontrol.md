---
title: Attribut User-Account-Control
description: Indicateurs qui contrôlent le comportement du compte d’utilisateur.
ms.assetid: fc81a16a-f537-44cc-957c-5d7ca66b9755
ms.tgt_platform: multiple
keywords:
- Schéma AD de l’attribut de contrôle de compte d’utilisateur
- Schéma AD d’attribut userAccountControl
topic_type:
- apiref
api_name:
- User-Account-Control
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f60297d22aad76b229c691a667ac22a87271402c
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104107923"
---
# <a name="user-account-control-attribute"></a>Attribut User-Account-Control

Indicateurs qui contrôlent le comportement du compte d’utilisateur.



| Entrée | Valeur |
|-------------------|---------------------------------------|
| CN                | Contrôle de compte d’utilisateur                  |
| LDAP-Display-Name | userAccountControl                    |
| Taille              | 4 octets.                              |
| Mettre à jour le privilège  | Cette valeur est définie par le système.      |
| Fréquence des mises à jour  | Chaque fois que la stratégie de compte change. |
| Attribute-Id      | 1.2.840.113556.1.4.8                  |
| System-ID-GUID    | bf967a68-0de6-11d0-a285-00aa003049e2  |
| Syntaxe            | [**Enumeration**](s-enumeration.md)  |



## <a name="implementations"></a>Implémentations

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server



| Entrée | Valeur |
|------------------------|-----------------------------------|
| ID de lien                | \-                                |
| MAPI-Id                | \-                                |
| System-Only            | Faux                             |
| Est de valeur unique       | Vrai                              |
| Est indexé             | Vrai                              |
| Dans le catalogue global      | Vrai                              |
| Descripteur de sécurité NT | O :BAG : BAD : S :                      |
| Range-Lower            | \-                                |
| Range-Upper            | \-                                |
| Search-Flags           | 0x00000019                        |
| System-Flags           | 0x00000012                        |
| Classes utilisées dans        | [**Utilisateur**](c-user.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Entrée | Valeur |
|------------------------|-----------------------------------|
| ID de lien                | \-                                |
| MAPI-Id                | \-                                |
| System-Only            | Faux                             |
| Est de valeur unique       | Vrai                              |
| Est indexé             | Vrai                              |
| Dans le catalogue global      | Vrai                              |
| Descripteur de sécurité NT | O :BAG : BAD : S :                      |
| Range-Lower            | \-                                |
| Range-Upper            | \-                                |
| Search-Flags           | 0x00000019                        |
| System-Flags           | 0x00000012                        |
| Classes utilisées dans        | [**Utilisateur**](c-user.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrée | Valeur |
|------------------------|-----------------------------------|
| ID de lien                | \-                                |
| MAPI-Id                | \-                                |
| System-Only            | Faux                             |
| Est de valeur unique       | Vrai                              |
| Est indexé             | Vrai                              |
| Dans le catalogue global      | Vrai                              |
| Descripteur de sécurité NT | O :BAG : BAD : S :                      |
| Range-Lower            | \-                                |
| Range-Upper            | \-                                |
| Search-Flags           | 0x00000019                        |
| System-Flags           | 0x00000012                        |
| Classes utilisées dans        | [**Utilisateur**](c-user.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrée | Valeur |
|------------------------|-----------------------------------|
| ID de lien                | \-                                |
| MAPI-Id                | \-                                |
| System-Only            | Faux                             |
| Est de valeur unique       | Vrai                              |
| Est indexé             | Vrai                              |
| Dans le catalogue global      | Vrai                              |
| Descripteur de sécurité NT | O :BAG : BAD : S :                      |
| Range-Lower            | \-                                |
| Range-Upper            | \-                                |
| Search-Flags           | 0x00000019                        |
| System-Flags           | 0x00000012                        |
| Classes utilisées dans        | [**Utilisateur**](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrée | Valeur |
|------------------------|-----------------------------------|
| ID de lien                | \-                                |
| MAPI-Id                | \-                                |
| System-Only            | Faux                             |
| Est de valeur unique       | Vrai                              |
| Est indexé             | Vrai                              |
| Dans le catalogue global      | Vrai                              |
| Descripteur de sécurité NT | O :BAG : BAD : S :                      |
| Range-Lower            | \-                                |
| Range-Upper            | \-                                |
| Search-Flags           | 0x00000019                        |
| System-Flags           | 0x00000012                        |
| Classes utilisées dans        | [**Utilisateur**](c-user.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrée | Valeur |
|------------------------|-----------------------------------|
| ID de lien                | \-                                |
| MAPI-Id                | \-                                |
| System-Only            | Faux                             |
| Est de valeur unique       | Vrai                              |
| Est indexé             | Vrai                              |
| Dans le catalogue global      | Vrai                              |
| Descripteur de sécurité NT | O :BAG : BAD : S :                      |
| Range-Lower            | \-                                |
| Range-Upper            | \-                                |
| Search-Flags           | 0x00000019                        |
| System-Flags           | 0x00000012                        |
| Classes utilisées dans        | [**Utilisateur**](c-user.md)<br/> |



## <a name="remarks"></a>Notes

Cette valeur d’attribut peut être zéro ou une combinaison d’une ou plusieurs des valeurs suivantes.



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Valeur hexadécimale</th>
<th>Identificateur (défini dans IADs. h)</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>0x00000001</td>
<td><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_SCRIPT</strong></a></td>
<td>Le script d’ouverture de session est exécuté.</td>
</tr>
<tr class="even">
<td>0x00000002</td>
<td><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_ACCOUNTDISABLE</strong></a></td>
<td>Le compte d’utilisateur est désactivé.</td>
</tr>
<tr class="odd">
<td>0x00000008</td>
<td><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_HOMEDIR_REQUIRED</strong></a></td>
<td>Le répertoire de départ est requis.</td>
</tr>
<tr class="even">
<td>0x00000010</td>
<td><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_LOCKOUT</strong></a></td>
<td>Le compte est actuellement verrouillé.</td>
</tr>
<tr class="odd">
<td>0x00000020</td>
<td><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_PASSWD_NOTREQD</strong></a></td>
<td>Aucun mot de passe n'est requis.</td>
</tr>
<tr class="even">
<td>0x00000040</td>
<td><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_PASSWD_CANT_CHANGE</strong></a></td>
<td>L’utilisateur ne peut pas modifier le mot de passe.
<blockquote>
[!Note]<br />
Vous ne pouvez pas assigner les paramètres d’autorisation de PASSWD_CANT_CHANGE en modifiant directement l’attribut UserAccountControl. Pour plus d’informations et pour obtenir un exemple de code qui montre comment empêcher un utilisateur de modifier le mot de passe, consultez l' <a href="/windows/desktop/ADSI/user-cannot-change-password">utilisateur ne peut pas changer de mot de passe</a>.
</blockquote>
<br/> :</td>
</tr>
<tr class="odd">
<td>0x00000080</td>
<td><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_ENCRYPTED_TEXT_PASSWORD_ALLOWED</strong></a></td>
<td>L’utilisateur peut envoyer un mot de passe chiffré.</td>
</tr>
<tr class="even">
<td>0x00000100</td>
<td><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_TEMP_DUPLICATE_ACCOUNT</strong></a></td>
<td>Il s’agit d’un compte pour les utilisateurs dont le compte principal se trouve dans un autre domaine. Ce compte fournit l’accès utilisateur à ce domaine, mais pas à un domaine qui approuve ce domaine. Également connu sous le nom de compte d’utilisateur local.</td>
</tr>
<tr class="odd">
<td>0x00000200</td>
<td><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_NORMAL_ACCOUNT</strong></a></td>
<td>Il s’agit d’un type de compte par défaut qui représente un utilisateur standard.</td>
</tr>
<tr class="even">
<td>0x00000800</td>
<td><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_INTERDOMAIN_TRUST_ACCOUNT</strong></a></td>
<td>Il s’agit d’un permis de faire confiance à un compte de domaine système qui approuve d’autres domaines.</td>
</tr>
<tr class="odd">
<td>0x00001000</td>
<td><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_WORKSTATION_TRUST_ACCOUNT</strong></a></td>
<td>Il s’agit d’un compte d’ordinateur pour un ordinateur qui est membre de ce domaine.</td>
</tr>
<tr class="even">
<td>0x00002000</td>
<td><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_SERVER_TRUST_ACCOUNT</strong></a></td>
<td>Il s’agit d’un compte d’ordinateur pour un contrôleur de domaine de sauvegarde du système qui est membre de ce domaine.</td>
</tr>
<tr class="odd">
<td>0x00004000</td>
<td>N/A</td>
<td>Non utilisé.</td>
</tr>
<tr class="even">
<td>0x00008000</td>
<td>N/A</td>
<td>Non utilisé.</td>
</tr>
<tr class="odd">
<td>0x00010000</td>
<td><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_DONT_EXPIRE_PASSWD</strong></a></td>
<td>Le mot de passe de ce compte n’expire jamais.</td>
</tr>
<tr class="even">
<td>0x00020000</td>
<td><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_MNS_LOGON_ACCOUNT</strong></a></td>
<td>Il s’agit d’un compte MNS Logon.</td>
</tr>
<tr class="odd">
<td>0x00040000</td>
<td><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_SMARTCARD_REQUIRED</strong></a></td>
<td>L’utilisateur doit se connecter à l’aide d’une carte à puce.</td>
</tr>
<tr class="even">
<td>0x00080000</td>
<td><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_TRUSTED_FOR_DELEGATION</strong></a></td>
<td>Le compte de service (compte d’utilisateur ou d’ordinateur), sous lequel un service s’exécute, est approuvé pour la délégation Kerberos. N’importe quel service peut emprunter l’identité d’un client qui demande le service.</td>
</tr>
<tr class="odd">
<td>0x00100000</td>
<td><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_NOT_DELEGATED</strong></a></td>
<td>Le contexte de sécurité de l’utilisateur ne sera pas délégué à un service même si le compte de service est défini comme approuvé pour la délégation Kerberos.</td>
</tr>
<tr class="even">
<td>0x00200000</td>
<td><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_USE_DES_KEY_ONLY</strong></a></td>
<td>Limitez ce principal pour qu’il utilise uniquement des types de chiffrement DES (Data Encryption Standard) pour les clés.</td>
</tr>
<tr class="odd">
<td>0x00400000</td>
<td><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_DONT_REQUIRE_PREAUTH</strong></a></td>
<td>Ce compte ne nécessite pas l’authentification préalable Kerberos pour l’ouverture de session.</td>
</tr>
<tr class="even">
<td>0x00800000</td>
<td><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_PASSWORD_EXPIRED</strong></a></td>
<td>Le mot de passe de l’utilisateur a expiré. Cet indicateur est créé par le système à l’aide des données de l’attribut <a href="a-pwdlastset.md"><strong>PWD-Last-Set</strong></a> et de la stratégie de domaine.</td>
</tr>
<tr class="odd">
<td>0x01000000</td>
<td><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_TRUSTED_TO_AUTHENTICATE_FOR_DELEGATION</strong></a></td>
<td>Le compte est activé pour la délégation. Il s’agit d’un paramètre sensible à la sécurité. les comptes pour lesquels cette option est activée doivent être contrôlés de manière stricte. Ce paramètre permet à un service s’exécutant sous le compte de supposer une identité client et de s’authentifier en tant qu’utilisateur sur d’autres serveurs distants sur le réseau.</td>
</tr>
</tbody>
</table>



 

