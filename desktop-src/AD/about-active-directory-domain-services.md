---
title: À propos de Active Directory Domain Services
description: Ce guide fournit des informations essentielles pour l’intégration de Microsoft Active Directory dans des applications distribuées conçues pour les systèmes d’exploitation qui prennent en charge Active Directory.
ms.assetid: cc6c63dd-ae22-40a7-8312-0a4648bb92bd
ms.tgt_platform: multiple
keywords:
- Active Directory Active Directory, à propos de
- Active Directory Active Directory Domain Services, à propos de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e4ef886409b435e1687d8ca6cf530b940852f3569818bb3afab69f57ab6b97c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117841073"
---
# <a name="about-active-directory-domain-services"></a>À propos de Active Directory Domain Services

## <a name="writing-powerful-applications-that-use-active-directory-domain-services"></a>Écrire des applications puissantes qui utilisent Active Directory Domain Services

Ce guide fournit des informations essentielles pour l’intégration de Active Directory Domain Services dans des applications distribuées conçues pour les systèmes d’exploitation qui prennent en charge Active Directory Domain Services, notamment :

-   Windows Server 2008
-   Windows Server 2008 R2
-   Windows Server 2012
-   Windows Server 2012 R2
-   Windows Server 2016

> [!Note]  
> Ces rubriques concernent les développeurs de logiciels. Pour les problèmes de support, consultez [support Microsoft](https://windows.microsoft.com/windows/support#1tc). Pour plus d’informations sur l’administration de Active Directory, consultez [Active Directory Domain Services](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc770946(v=ws.10)) sur TechNet.

 

## <a name="fundamental-directory-features"></a>Fonctionnalités d’annuaire fondamentales

Un service d’annuaire est un service fondamental pour les applications distribuées. Un service d’annuaire doit fournir les fonctionnalités indiquées dans le tableau suivant.



| Fonctionnalité               | Description                                                                                         |
|-----------------------|-----------------------------------------------------------------------------------------------------|
| Transparence de l’emplacement | En mesure de trouver l’utilisateur, le groupe, le service en réseau ou la ressource, les données sans l’adresse de l’objet           |
| Données d’objet           | Possibilité de stocker des données d’utilisateur, de groupe, d’organisation et de service dans une arborescence hiérarchique                    |
| Requête enrichie            | En mesure de localiser un objet en interrogeant les propriétés de l’objet                                          |
| Haute disponibilité     | Possibilité de localiser un réplica du répertoire à un emplacement efficace pour les opérations de lecture/écriture |



 

## <a name="advanced-features-of-active-directory-domain-services"></a>Fonctionnalités avancées de Active Directory Domain Services

Active Directory Domain Services fournit les fonctionnalités listées dans le tableau suivant.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Fonctionnalité</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Prise en charge des normes Internet</td>
<td>Active Directory Domain Services implémente ses fonctionnalités conformément aux normes Internet publiées, telles que LDAP et DNS.</td>
</tr>
<tr class="even">
<td>Sécurité étroitement intégrée et flexible</td>
<td>Les avantages sont notamment les suivants :<br/>
<ul>
<li>Choix des packages d’authentification. Kerberos, SSL (Secure Sockets Layer) (SSL) ou une combinaison ; par exemple, établissez un canal SSL pour le chiffrement, puis utilisez Kerberos pour l’authentification.</li>
<li>Gestion centralisée de l’accès aux services et aux ressources à l’aide des utilisateurs et des groupes dans Active Directory Domain Services.</li>
<li>Délégation de l’administration afin que les administrateurs centraux puissent déléguer des tâches d’administration telles que la modification de mot de passe ou la création et la suppression d’objets spécifiques.</li>
<li>le serveur Active Directory utilise les mêmes mécanismes de contrôle d’accès que ceux utilisés sur les systèmes de fichiers dans les systèmes d’exploitation Windows. Ainsi, les outils qui gèrent le contrôle d’accès sur un système de fichiers fonctionnent pour Active Directory Domain Services.</li>
<li>Infrastructure de clé publique complète. Le serveur de certificats Microsoft et la prise en charge des cartes à puce sont intégrés à Active Directory Domain Services pour fournir la gestion des certificats et des ouvertures de session par carte à puce.</li>
</ul></td>
</tr>
<tr class="odd">
<td>Facile à programmer</td>
<td>Le serveur Active Directory peut être accessible par programmation et administré à l’aide de l’API des <a href="/windows/desktop/ADSI/active-directory-service-interfaces-adsi">interfaces de Service Active Directory</a> , de l’API <a href="/previous-versions/windows/desktop/ldap/lightweight-directory-access-protocol-ldap-api">Lightweight Directory Access Protocol</a> ou de l’espace de noms <a href="/dotnet/api/system.directoryservices">System. DirectoryServices</a> .</td>
</tr>
<tr class="even">
<td>Services système activés pour les annuaires</td>
<td>votre application cliente peut être facilement déployée sur des bureaux distribués en créant un package Windows Installer et en utilisant la fonctionnalité de déploiement d’application disponible dans les systèmes d’exploitation Windows.</td>
</tr>
<tr class="odd">
<td>Intégration d’application clé</td>
<td>les applications distribuées de clés, telles que les Exchange, sont intégrées à Active Directory Domain Services. Ainsi, les entreprises peuvent réduire le nombre de services d’annuaire à gérer.</td>
</tr>
<tr class="even">
<td>Schéma riche et extensible</td>
<td>Le schéma définit les objets et les propriétés qui peuvent être écrits et lus à partir d’un service d’annuaire. Le schéma Active Directory est riche. La plupart des objets et propriétés nécessaires à un service sont disponibles. Si ce n’est pas le cas, une application distribuée peut étendre le schéma pour prendre en charge les spécifications de l’application.</td>
</tr>
</tbody>
</table>



 

Pour plus d’informations sur Active Directory Domain Services, consultez :

-   [Concepts de base de Active Directory Domain Services](core-concepts-of-active-directory-domain-services.md)
-   [Architecture Active Directory](active-directory-domain-services-architecture.md)
-   [Schéma Active Directory](active-directory-schema.md)

