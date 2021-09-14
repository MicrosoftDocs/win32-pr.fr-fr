---
title: Accessibilité et support global
description: la plateforme Windows 7 facilite la création de solutions qui sont accessibles à davantage d’utilisateurs et qui répondent ou dépassent les normes de conformité d’accessibilité.
ms.assetid: bcad2f00-7885-461c-a2dc-0a0a176962b4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cea7f710850f419493c5a8435626d163361c8a03
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127293210"
---
# <a name="accessibility-and-global-support"></a>Accessibilité et support global

la plateforme Windows 7 facilite la création de solutions qui sont accessibles à davantage d’utilisateurs et qui répondent ou dépassent les normes de conformité d’accessibilité. La communauté des fournisseurs de technologies d’assistance (VTA) peut désormais créer des solutions pour un plus grand nombre d’applications clientes, et les développeurs d’applications trouveront plus facile de créer et de valider des interfaces utilisateur accessibles.

Windows 7 rend également la prise en charge de plusieurs langues globales plus facile que dans les versions précédentes de Windows. à partir du moment où un utilisateur sélectionne une langue et un emplacement, Windows 7 présente des dates, des chiffres, des calendriers, des classements et d’autres informations à l’aide des conventions culturelles que les clients attendent.

## <a name="windows-automation"></a>Windows Mati

Windows 7 offre une couche d’automatisation riche et normalisée qui est étendue pour les applications natives. Il s’appuie sur Microsoft Active Accessibility et Microsoft UI Automation. Il est également conçu pour fonctionner avec les normes du secteur, telles que les spécifications du W3C Web ARIA (accès à une application Internet riche accessible) et la *Section 508*.

UI Automation offre des performances améliorées en introduisant des proxies d’automatisation non gérés plus rapides pour les contrôles Microsoft Win32 et les applications Microsoft Active Accessibility (*MSAA*) héritées, ainsi que des inscriptions de proxy et des événements d’automatisation d’interface utilisateur améliorés et plus rapides. Les nouvelles fonctionnalités d’extensibilité étendent les modèles de contrôle, les propriétés et les événements personnalisés. (voir [API d’automatisation Windows : vue d’ensemble](../winauto/windows-automation-api-overview.md).)

## <a name="accessibility-support-tools"></a>Outils de support d’accessibilité

Le vérificateur d’accessibilité de l’interface utilisateur est un outil d’interface utilisateur graphique pratique qui permet aux développeurs et aux testeurs de vérifier rapidement si leur interface utilisateur est conforme aux exigences d’accessibilité clés, telles que *MSAA* (qui vérifie les relations parent-enfant ou les rectangles englobants) et l’accès par programmation UI Automation, la génération d’événements, la disposition et la navigation au clavier. (Voir [l’outil de vérification de l’accessibilité de l’interface utilisateur](https://www.codeplex.com/AccCheck).)

UIA Verify est une infrastructure d’automatisation des tests qui facilite les tests manuels et automatisés de l’implémentation du fournisseur UI Automation d’un contrôle ou d’une application. Ces deux nouveaux outils permettent aux développeurs de tester les implémentations et les fonctionnalités d’accessibilité dans les applications qui utilisent *MSAA* ou UI Automation. Les deux outils sont disponibles via [CodePlex](https://www.codeplex.com/), un site Web créé par Microsoft pour héberger des projets open source et mieux servir la communauté des développeurs. (Consultez [UI Automation Verify (UIA Verify) tester l’infrastructure d’automatisation](https://uiautomationverify.codeplex.com/).)

## <a name="improved-multi-language-user-interface-support-and-linguistic-services"></a>Amélioration de la prise en charge de l’interface utilisateur multilingue et des services linguistiques

Windows 7 offre aux développeurs une méthode standard pour préparer leurs applications au marché international en proposant une prise en charge améliorée de l’interface utilisateur multilingue et des services linguistiques qu’ils peuvent utiliser dans leurs applications.

les Services linguistiques étendus sont une nouvelle fonctionnalité de Windows 7 qui permet aux développeurs d’utiliser le même petit ensemble d’api pour tirer parti d’une large gamme de fonctionnalités linguistiques avancées. en utilisant des ServicesAPIs linguistiques étendues dans Windows 7, les développeurs peuvent détecter automatiquement la langue de n’importe quel élément de texte Unicode et utiliser ces informations pour faciliter le choix de l’expérience utilisateur pour les clients dans le monde entier. Les services linguistiques étendus proposent également une prise en charge de la translittération intégrée qui convertit le texte d’un système d’écriture en un autre. Par exemple, les développeurs peuvent désormais convertir automatiquement le texte entre le chinois simplifié et le chinois traditionnel pour aider les utilisateurs à communiquer entre eux à travers les limites linguistiques. En utilisant des ServicesAPIs linguistiques étendus, les développeurs peuvent utiliser les services linguistiques étendus existants et récupérer de nouveaux services à l’avenir sans apprendre de nouveau code. (Voir [services linguistiques étendus](../intl/extended-linguistic-services.md).)

 

 