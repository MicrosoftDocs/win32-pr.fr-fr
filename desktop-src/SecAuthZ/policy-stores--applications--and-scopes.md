---
description: Les magasins de stratégies d’autorisation, les applications et les étendues représentent différents niveaux d’organisation de la stratégie du gestionnaire d’autorisations.
ms.assetid: 235f236d-59c9-4a8c-aec6-60d1ddba4d5d
title: Magasins de stratégies, applications et étendues
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5db06b291ef81f391fed1a0094b73c9b31d0342f59bce22d93779c7bfa48a80b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119907569"
---
# <a name="policy-stores-applications-and-scopes"></a>Magasins de stratégies, applications et étendues

Les magasins de stratégies d’autorisation, les applications et les étendues représentent différents niveaux d’organisation de la stratégie du gestionnaire d’autorisations. Un magasin de stratégies peut contenir une ou plusieurs applications, et une application peut contenir une ou plusieurs étendues.

-   [Magasins de stratégies d’autorisation](#authorization-policy-stores)
-   [Applications](#policy-stores-applications-and-scopes)
-   [Étendues](#policy-stores-applications-and-scopes)
-   [La délégation](#delegation)
-   [Rubriques connexes](#related-topics)

## <a name="authorization-policy-stores"></a>Magasins de stratégies d’autorisation

Dans l’API du gestionnaire d’autorisations, un magasin de stratégies d’autorisation est représenté par un objet [**IAzAuthorizationStore**](/windows/desktop/api/Azroles/nn-azroles-iazauthorizationstore) . Le magasin de stratégies d’autorisation contient les définitions et les assignations des applications, des étendues, des opérations, des tâches, des rôles et des groupes d’utilisateurs.

Un magasin de stratégies d’autorisation peut être stocké en tant que fichier XML ou Active Directory.

Une application doit initialiser un magasin de stratégies d’autorisation avant de modifier les informations dans le magasin ou d’utiliser la stratégie de stockage pour vérifier l’accès client aux ressources.

Un magasin de stratégies d’autorisation peut contenir un ou plusieurs objets [**IAzApplication**](/windows/desktop/api/Azroles/nn-azroles-iazapplication) qui représentent chacun une stratégie d’autorisation pour une application spécifique.

## <a name="applications"></a>Applications

Dans l’API du gestionnaire d’autorisations, une application est représentée par un objet [**IAzApplication**](/windows/desktop/api/Azroles/nn-azroles-iazapplication) . Un magasin de stratégies d’autorisation peut contenir des informations de stratégie d’autorisation pour de nombreuses applications. L’utilisation d’objets **IAzApplication** vous permet de stocker différentes stratégies d’autorisation pour différentes applications dans un même magasin de stratégies.

Un magasin de stratégies d’autorisation doit contenir au moins une application.

## <a name="scopes"></a>Étendues

Dans l’API du gestionnaire d’autorisations, une étendue est représentée par un objet [**IAzScope**](/windows/desktop/api/Azroles/nn-azroles-iazscope) . Les étendues fournissent un niveau supplémentaire, facultatif d’organisation, pour une stratégie d’autorisation. Une application peut contenir une ou plusieurs étendues, mais elle n’a pas besoin d’en contenir (le gestionnaire d’autorisations fournit une étendue par défaut à l’échelle de l’application).

Une étendue est une sous-division au sein d’une application qui sépare les ressources des autres ressources utilisées par cette application. Si vous disposez de groupes du gestionnaire d’autorisations, d’attributions de rôles, de définitions de rôles ou de définitions de tâches que vous ne souhaitez pas appliquer à l’ensemble de l’application, vous pouvez les créer au niveau de l’étendue.

## <a name="delegation"></a>La délégation

Les magasins de stratégies d’autorisation stockés dans Active Directory prennent en charge la délégation de l’administration. L’administration peut être déléguée à des utilisateurs et à des groupes au niveau du magasin, de l’application ou de l’étendue. Chaque niveau définit des rôles d’administration pour la stratégie à ce niveau. Pour déléguer le contrôle à un utilisateur ou à un groupe, affectez-le au rôle administrateur ; pour autoriser un utilisateur ou un groupe à lire la stratégie, attribuez-le au rôle lecteur.

Les administrateurs d’un magasin, d’une application ou d’une étendue peuvent lire et modifier le magasin de stratégies au niveau délégué. Les lecteurs peuvent lire le magasin de stratégies au niveau délégué, mais ne peuvent pas modifier le magasin.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Création d’un objet du magasin de stratégies d’autorisation en C++](creating-an-authorization-policy-store-object-in-c--.md)
</dt> <dt>

[Création d’un objet d’application en C++](creating-an-application-object-in-c--.md)
</dt> <dt>

[Délégation de la définition des autorisations en C++](delegating-the-defining-of-permissions-in-c--.md)
</dt> </dl>

 

 



