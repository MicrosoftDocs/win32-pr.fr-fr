---
title: Mappage de l’interface utilisateur Objet utilisateur
description: Les tableaux suivants identifient les pages de propriétés fournies par le composant logiciel enfichable utilisateurs et ordinateurs Active Directory.
ms.assetid: f309c139-c957-40c4-b369-f527aa87157c
ms.tgt_platform: multiple
keywords:
- Mappage de l’interface utilisateur de l’objet utilisateur Active Directory
- Mappage de l’interface utilisateur Active Directory, objet User
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 656e8071b558b730ecb1fc0463834f6fbadb7eb9bf4c56b11640e2b95209735f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119024497"
---
# <a name="user-object-user-interface-mapping"></a>Mappage de l’interface utilisateur Objet utilisateur

Les tableaux suivants identifient les pages de propriétés fournies par le composant logiciel enfichable utilisateurs et ordinateurs Active Directory. Chaque table identifie les éléments de l’interface utilisateur de la page de propriétés et l’attribut associé à cet élément d’interface utilisateur. Étant donné que les pages de propriétés qui sont affichées par le composant logiciel enfichable utilisateurs et ordinateurs Active Directory peuvent être étendues, il n’est pas possible de fournir ces données pour toutes les pages affichées dans une feuille de propriétés.

## <a name="general-property-page"></a>Général, page de propriétés

Le tableau suivant répertorie les étiquettes de l’interface utilisateur de la page de propriétés **général** .



| Étiquette d’interface utilisateur         | Attribut dans Active Directory Domain Services                           |
|------------------|-------------------------------------------------------------------------|
| Prénom       | [**givenName**](/windows/desktop/ADSchema/a-givenname)                                   |
| Nom        | [**perso**](/windows/desktop/ADSchema/a-sn)                                                 |
| Initiales         | [**initiales**](/windows/desktop/ADSchema/a-initials)                                     |
| Nom d’affichage     | [**NomComplet**](/windows/desktop/ADSchema/a-displayname)                               |
| Description      | [**descriptive**](/windows/desktop/ADSchema/a-description)                               |
| Office           | [**physicalDeliveryOfficeName**](/windows/desktop/ADSchema/a-physicaldeliveryofficename) |
| Numéro de téléphone | [**telephoneNumber**](/windows/desktop/ADSchema/a-telephonenumber)                       |
| Téléphone : autre | [**otherTelephone**](/windows/desktop/ADSchema/a-othertelephone)                         |
| Courrier électronique           | [**Adresses de messagerie**](/windows/desktop/ADSchema/a-mail)                                 |
| Page Web         | [**wWWHomePage**](/windows/desktop/ADSchema/a-wwwhomepage)                               |
| Page Web : autre  | [**URL**](/windows/desktop/ADSchema/a-url)                                               |



 

## <a name="account-property-page"></a>Page de propriétés du compte

Le tableau suivant répertorie les étiquettes de l’interface utilisateur de la page de propriétés du **compte** .



| Étiquette d’interface utilisateur                                | Attribut dans Active Directory Domain Services                                                   | Commentaire                                                                                                                                                                                                                                                                                                                                                                                 |
|-----------------------------------------|-------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Nom de UserLogon                          | [**userPrincipalName**](/windows/desktop/ADSchema/a-userprincipalname)                                           | Ce champ est extrait de tous les éléments de l’attribut [**userPrincipalName**](/windows/desktop/ADSchema/a-userprincipalname) qui précèdent le dernier caractère « @ ». Le dernier caractère « @ » et tout ce qui suit est placé dans la zone de liste déroulante des suffixes.                                                                                                                                                      |
| nom d’ouverture de session de l’utilisateur (pré-Windows 2000)      | [**sAMAccountname**](/windows/desktop/ADSchema/a-samaccountname)                                                 | Aucun commentaire.                                                                                                                                                                                                                                                                                                                                                                             |
| Horaires d’accès                             | [**logonHours**](/windows/desktop/ADSchema/a-logonhours)                                                         | Aucun commentaire.                                                                                                                                                                                                                                                                                                                                                                             |
| Se connecter à                               | [**logonWorkstation**](/windows/desktop/ADSchema/a-logonworkstation)                                             | Aucun commentaire.                                                                                                                                                                                                                                                                                                                                                                             |
| Le compte est verrouillé                   | [**lockoutTime**](/windows/desktop/ADSchema/a-lockouttime) et [ **lockoutDuration**](/windows/desktop/ADSchema/a-lockoutduration) | Si l’attribut [**lockoutTime**](/windows/desktop/ADSchema/a-lockouttime) n’est pas égal à zéro, l’attribut [**lockoutDuration**](/windows/desktop/ADSchema/a-lockoutduration) est ajouté à **lockoutTime** et comparé à la date et à l’heure actuelles pour déterminer si le compte est verrouillé.                                                                                                                                |
| L’utilisateur doit changer de mot de passe à la prochaine ouverture de session | [**pwdLastSet**](/windows/desktop/ADSchema/a-pwdlastset)                                                         | Aucun commentaire.                                                                                                                                                                                                                                                                                                                                                                             |
| L’utilisateur ne peut pas changer de mot de passe             | N/A                                                                                             | Il s’agit du contrôle modifier le mot de passe dans la liste de contrôle d’accès.                                                                                                                                                                                                                                                                                                                                         |
| Autres options de compte                   | [**userAccountControl**](/windows/desktop/ADSchema/a-useraccountcontrol)                                         | Les éléments restants dans les options de compte basculent bits dans le masque de bits d’attribut [**UserAccountControl**](/windows/desktop/ADSchema/a-useraccountcontrol) (indicateurs dans une valeur DWORD).                                                                                                                                                                                                                                 |
| Expiration du compte                         | [**AccountExpires dans**](/windows/desktop/ADSchema/a-accountexpires)                                                 | Le contrôle **expiration du compte** affiche la date à laquelle le compte expire à la fin de. L’attribut [**AccountExpires dans**](/windows/desktop/ADSchema/a-accountexpires) est stocké en tant que date à laquelle le compte expire. Pour cette raison, la date affichée dans le contrôle **Expires du compte** s’affiche dans un jour antérieur à la date contenue dans l’attribut **AccountExpires dans** . |



 

## <a name="address-property-page"></a>Page de propriétés de l’adresse

Le tableau suivant répertorie les étiquettes de l’interface utilisateur de la page de propriétés **adresse** .



| Étiquette d’interface utilisateur        | Attribut dans Active Directory Domain Services                                                 | Commentaire                                                   |
|-----------------|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------|
| Rue          | [**streetAddress**](/windows/desktop/ADSchema/a-streetaddress)                                                 | Aucun commentaire.                                               |
| P. O. Box         | [**postOfficeBox**](/windows/desktop/ADSchema/a-postofficebox)                                                 | Aucun commentaire.                                               |
| City            | [**budget**](/windows/desktop/ADSchema/a-l)                                                                         | Le nom de l’attribut **l** est un « l » minuscule, comme dans les paramètres régionaux. |
| État/province  | [**St**](/windows/desktop/ADSchema/a-st)                                                                       | Aucun commentaire.                                               |
| Code postal | [**Postal**](/windows/desktop/ADSchema/a-postalcode)                                                       | Aucun commentaire.                                               |
| Pays/Région  | [**c**](/windows/desktop/ADSchema/a-c), [**co**](/windows/desktop/ADSchema/a-co)et [**CountryCode**](/windows/desktop/ADSchema/a-countrycode) | Aucun commentaire.                                               |



 

## <a name="member-of-property-page"></a>Membre de la page de propriétés

Le tableau suivant répertorie les étiquettes de l’interface utilisateur du **membre de** la page de propriétés.



| Étiquette d’interface utilisateur          | Attribut dans Active Directory Domain Services   | Commentaire                                                                                                                                                                    |
|-------------------|-------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Membre de         | [**memberOf**](/windows/desktop/ADSchema/a-memberof)             | Comprend tous les groupes de la liste des interfaces utilisateur, à l’exception du groupe principal, qui est représenté dans la publicité via l’attribut [**primaryGroupId**](/windows/desktop/ADSchema/a-primarygroupid) . |
| Définir le groupe principal | [**primaryGroupId**](/windows/desktop/ADSchema/a-primarygroupid) | LDAP : lié à [**primaryGroupToken**](/windows/desktop/ADSchema/a-primarygrouptoken) du groupe principal.                                                                                  |



 

## <a name="organization-property-page"></a>Page de propriétés de l’Organisation

Le tableau suivant présente les étiquettes de l’interface utilisateur de la page de propriétés **organisation** .



| Étiquette d’interface utilisateur       | Attribut dans Active Directory Domain Services | Commentaire     |
|----------------|-----------------------------------------------|-------------|
| Titre          | [**bonhomme**](/windows/desktop/ADSchema/a-title)                 | Aucun commentaire. |
| Service     | [**compétent**](/windows/desktop/ADSchema/a-department)       | Aucun commentaire. |
| Company        | [**entreprise**](/windows/desktop/ADSchema/a-company)             | Aucun commentaire. |
| Gestionnaire : nom   | [**gestion**](/windows/desktop/ADSchema/a-manager)             | Aucun commentaire. |
| Rapports directs | [**directReports**](/windows/desktop/ADSchema/a-directreports) | Aucun commentaire. |



 

## <a name="profile-property-page"></a>Page de propriétés du profil

Le tableau suivant répertorie les étiquettes de l’interface utilisateur de la page de propriétés du **Profil** .



| Étiquette d’interface utilisateur                | Attribut dans Active Directory Domain Services | Commentaire                                                                                                                 |
|-------------------------|-----------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| Chemin d’accès du profil            | [**profilePath**](/windows/desktop/ADSchema/a-profilepath)     | Aucun commentaire.                                                                                                             |
| Script d’ouverture de session            | [**scriptPath**](/windows/desktop/ADSchema/a-scriptpath)       | Aucun commentaire.                                                                                                             |
| Dossier de démarrage : chemin d’accès local | [**homeDirectory**](/windows/desktop/ADSchema/a-homedirectory) | Si le **chemin d’accès local** est sélectionné, le chemin d’accès local est stocké dans l’attribut [**HomeDirectory**](/windows/desktop/ADSchema/a-homedirectory) . |
| Dossier de démarrage : Connecter    | [**homeDrive**](/windows/desktop/ADSchema/a-homedrive)         | si **Connecter** est sélectionné, le lecteur mappé est stocké dans l’attribut [**homeDrive**](/windows/desktop/ADSchema/a-homedrive) .          |
| Dossier de démarrage : à         | [**homeDirectory**](/windows/desktop/ADSchema/a-homedirectory) | si **Connecter** est sélectionné, le chemin d’accès est stocké dans l’attribut [**homeDirectory**](/windows/desktop/ADSchema/a-homedirectory) .          |



 

## <a name="telephones-property-page"></a>Page de propriétés des téléphones

Le tableau suivant répertorie les éléments d’interface utilisateur de la page de propriétés des **téléphones** et leurs attributs de Active Directory correspondants.



| Étiquette d’interface utilisateur        | Attribut dans Active Directory Domain Services                                 |
|-----------------|-------------------------------------------------------------------------------|
| page d'accueil            | [**homePhone**](/windows/desktop/ADSchema/a-homephone)                                         |
| Page d’hébergement : autres     | [**otherHomePhone**](/windows/desktop/ADSchema/a-otherhomephone)                               |
| Récepteur de radiomessagerie           | [**destinés**](/windows/desktop/ADSchema/a-pager)                                                 |
| Radiomessagerie : Other    | [**otherPager**](/windows/desktop/ADSchema/a-otherpager)                                       |
| Mobile          | [**processeur**](/windows/desktop/ADSchema/a-mobile)                                               |
| Mobile : autres   | [**otherMobile**](/windows/desktop/ADSchema/a-othermobile)                                     |
| Fax             | [**facsimileTelephoneNumber**](/windows/desktop/ADSchema/a-facsimiletelephonenumber)           |
| Télécopie : autres      | [**otherFacsimileTelephoneNumber**](/windows/desktop/ADSchema/a-otherfacsimiletelephonenumber) |
| Téléphone IP        | [**ipPhone**](/windows/desktop/ADSchema/a-ipphone)                                             |
| Téléphone IP : autre | [**otherIpPhone**](/windows/desktop/ADSchema/a-otheripphone)                                   |
| Remarques           | [**méta**](/windows/desktop/ADSchema/a-info)                                                   |



 

## <a name="environment-sessions-remote-control-and-terminal-services-profile-property-pages"></a>Pages de propriétés environnement, sessions, contrôle à distance et profil des services Terminal Server

Les pages **environnement**, **sessions**, **contrôle à distance** et **profil des services Terminal Server** sont fournies pour un objet utilisateur qui prend en charge les services Terminal Server. Les éléments d’interface utilisateur pour ces pages ne correspondent pas à des attributs individuels. Au lieu de cela, les paramètres sont stockés dans des données privées dans Active Directory Domain Services. Vous pouvez accéder aux paramètres des services Terminal Server à l’aide de l’interface [**IADsTsUserEx**](/windows/desktop/api/tsuserex/nn-tsuserex-iadstsuserex) .

 

 