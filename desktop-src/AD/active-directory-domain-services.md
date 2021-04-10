---
title: Services de domaine Active Directory
description: Microsoft Active Directory Domain Services sont la base des réseaux distribués basés sur les systèmes d’exploitation Windows 2000 Server, Windows Server 2003 et Microsoft Windows Server 2008 qui utilisent des contrôleurs de domaine.
ms.assetid: 9fc78c72-c59c-4c4d-ace5-00a431645c4b
ms.tgt_platform: multiple
keywords:
- Active Directory Domain Services Active Directory
- Active Directory Active Directory, page de démarrage
- Active Directory Domain Services Active Directory, page de démarrage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0270f331a68d23ad89a8e5a999f8cabd95487020
ms.sourcegitcommit: 73417d55867c804274a55abe5ca71bcba7006119
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/20/2020
ms.locfileid: "104032060"
---
# <a name="active-directory-domain-services"></a>Active Directory Domain Services

## <a name="purpose"></a>Objectif

Microsoft Active Directory Domain Services sont la base des réseaux distribués basés sur les systèmes d’exploitation Windows 2000 Server, Windows Server 2003 et Microsoft Windows Server 2008 qui utilisent des contrôleurs de domaine. Active Directory Domain Services fournir un stockage de données hiérarchique, sécurisé et structuré pour les objets d’un réseau, tels que les utilisateurs, les ordinateurs, les imprimantes et les services. Active Directory Domain Services prennent en charge la localisation et l’utilisation de ces objets.

Ce guide fournit une vue d’ensemble des Active Directory Domain Services et des exemples de code pour les tâches de base, telles que la recherche d’objets et la lecture des propriétés, pour des tâches plus avancées telles que la publication de service.

Windows 2000 Server et les systèmes d’exploitation ultérieurs fournissent une interface utilisateur permettant aux utilisateurs et aux administrateurs de travailler avec les objets et les données de Active Directory Domain Services. Ce guide décrit comment étendre et personnaliser cette interface utilisateur. Elle explique également comment étendre les Active Directory Domain Services en définissant de nouvelles classes et attributs d’objet.

> [!Note]  
> La documentation suivante est destinée aux programmeurs informatiques. Si vous êtes un utilisateur final qui tente de déboguer une erreur d’impression ou un problème de réseau à distance, consultez les forums de la [communauté Microsoft](https://answers.microsoft.com).

 

## <a name="where-applicable"></a>Le cas échéant

Les administrateurs réseau écrivent des scripts et des applications qui accèdent à Active Directory Domain Services pour automatiser les tâches administratives courantes, telles que l’ajout d’utilisateurs et de groupes, la gestion des imprimantes et la définition d’autorisations pour les ressources réseau.

Les éditeurs de logiciels indépendants et les développeurs d’utilisateurs finaux peuvent utiliser Active Directory Domain Services programmation pour activer l’annuaire de leurs produits et applications. Les services peuvent se publier eux-mêmes dans Active Directory Domain Services ; les clients peuvent utiliser Active Directory Domain Services pour rechercher des services, et les deux peuvent utiliser Active Directory Domain Services pour rechercher et utiliser d’autres objets sur un réseau.

## <a name="developer-audience"></a>Développeurs concernés

Les applications qui accèdent aux données dans Active Directory Domain Services peuvent être écrites à l’aide de l’API [interfaces de Service Active Directory](../adsi/active-directory-service-interfaces-adsi.md) , de l’API [Lightweight Directory Access Protocol](/previous-versions/windows/desktop/ldap/lightweight-directory-access-protocol-ldap-api) ou de l’espace de noms [System. DirectoryServices](/dotnet/api/system.directoryservices) .

## <a name="run-time-requirements"></a>Conditions d’exécution

Active Directory Domain Services s’exécuter sur les contrôleurs de domaine Windows 2000 et versions ultérieures. Toutefois, les applications clientes peuvent être écrites pour et s’exécuter sous Windows Vista, Windows Server 2003, Windows XP, Windows 2000, Windows NT 4,0, Windows 98 et Windows 95.

## <a name="in-this-section"></a>Dans cette section

<dl> <dt>

[À propos de Active Directory Domain Services](about-active-directory-domain-services.md)
</dt> <dd>

Informations générales sur Active Directory Domain Services.

</dd> <dt>

[Utilisation des services de domaine Active Directory](using-active-directory-domain-services.md)
</dt> <dd>

Guide de programmation Active Directory Domain Services.

</dd> <dt>

[Référence Active Directory Domain Services](active-directory-domain-services-reference.md)
</dt> <dd>

Référence de programmation de Active Directory Domain Services.

</dd> </dl>

 

 