---
title: À propos de Direct2D
description: Introduit Direct2D, une API qui fournit aux développeurs Win32 la possibilité d’effectuer des tâches de rendu graphiques 2D avec des performances et une qualité visuel supérieures.
ms.assetid: 05cc230e-6fec-4a15-8e28-c68397392fc5
keywords:
- Direct2D, à propos de
- Direct2D, interopérabilité
- Direct2D, performances
- Direct2D, disponibilité
- Direct2D, applications
- interopérabilité, Direct2D
- performances pour Direct2D
- disponibilité pour Direct2D
- applications pour Direct2D
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 486c83b7a83ef82983e189977f9f99254b0a1977
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127113306"
---
# <a name="about-direct2d"></a>À propos de Direct2D

Cette rubrique présente Direct2D, une API qui fournit aux développeurs Win32 la possibilité d’effectuer des tâches de rendu graphiques 2D avec des performances et une qualité visuelle supérieures.

## <a name="what-is-direct2d"></a>Qu’est-ce que Direct2D ?

Direct2D est une API graphique en 2D en mode immédiat, accélérée par le matériel, qui offre des performances élevées et un rendu de haute qualité pour la géométrie 2D, les bitmaps et le texte. l’API Direct2D est conçue pour interagir avec le code existant qui utilise GDI, GDI+ ou Direct3D.

Direct2D est principalement conçu pour être utilisé par les classes de développeurs suivantes :

-   Développeurs de grandes applications natives à l’échelle de l’entreprise.
-   Les développeurs qui créent des outils de contrôle et des bibliothèques pour la consommation par les développeurs en aval.
-   Développeurs qui ont besoin d’un rendu côté serveur d’un graphique 2D.
-   Les développeurs qui utilisent les graphiques Direct3D et ont besoin d’un mode de rendu de texte et 2D simple et hautes performances pour les menus, les éléments d’interface utilisateur et les affichages de tête haut (HUDs).

## <a name="why-direct2d"></a>Pourquoi Direct2D ?

les principales motivations pour créer une nouvelle API graphics 2d dans Microsoft Windows sont les suivantes :

-   pour suivre le niveau d’évolution de la richesse visuelle que Windows utilisateurs sont habitués.
-   Pour permettre aux développeurs d’écrire un code de rendu 2D qui s’adapte directement au matériel de traitement graphique du PC sur lequel il s’exécute.
-   Pour permettre aux développeurs d’écrire du code pour afficher des graphiques 2D qui peuvent s’exécuter dans le contexte d’un service.

Au cours des dernières années, les utilisateurs finaux ont commencé à s’attendre à une plus grande fidélité visuelle dans les expériences numériques. Cette tendance est reflétée dans l’électronique grand public. Les périphériques GPS, les périphériques de lecture multimédia, les téléphones mobiles et les appareils photo numériques offrent des expériences plus riches en permanence à l’issue de l’année. Cette tendance peut également être consultée dans la diversité du contenu graphique des films, des téléviseurs, des jeux vidéo et sur le Web. pour suivre ces changements, les développeurs sont invités à mettre leurs applications de Windows existantes au niveau supérieur de la richesse visuelle.

les processeurs graphiques des pc Windows modernes évoluent régulièrement, en passant par des avancées dans les graphiques de jeux vidéo et des parties de l’expérience Windows comme Windows Media Center et Aero. certaines applications Windows peuvent tirer parti des gpu modernes à l’aide de Microsoft Direct3D et Windows Presentation Foundation (WPF). bien que Direct3D serve des applications graphiques 3d haut de gamme et que WPF réponde aux besoins des développeurs .net, il existe des lacunes pour les développeurs qui ont des codes base existants volumineux de rendu de code basés sur GDI et GDI+ ou qui souhaitent incorporer des graphiques 2d de haute qualité dans leurs applications basées sur Direct3D.

Enfin, la nécessité d’une API Graphics pouvant être utilisée dans un service est devenue une exigence émergente pour les développeurs qui travaillent dans des scénarios d’entreprise et de développement Web. Les API de rendu existantes se concentrent sur le rendu côté client dans une session mono-utilisateur. Par conséquent, ils peuvent être très courts dans des domaines de robustesse et d’extensibilité lorsqu’ils sont utilisés dans un contexte de service. Une nouvelle API est requise pour résoudre ce cas de figure.

## <a name="high-performance-with-maximum-availability"></a>Haute performance avec une disponibilité maximale

Direct2D est une bibliothèque de mode utilisateur créée à l’aide de l’API Direct3D 10,1. Cela signifie que les applications Direct2D bénéficient d’un rendu accéléré par le matériel sur les GPU standard modernes. L’accélération matérielle est également réalisée sur un matériel Direct3D 9 antérieur à l’aide du rendu Direct3D 10-niveau 9. cette combinaison offre d’excellentes performances sur le matériel graphique sur les pc Windows existants.

> [!Note]  
> à partir de Windows 8, Direct2D est construit à l’aide de l’API Direct3D 11,1.

 

Le diagramme suivant illustre l’architecture en couches de Direct2D.

![diagramme de l’architecture en couches Direct2D](images/direct2d-architectual-layering.png)

Pour les scénarios où l’utilisation de l’accélération matérielle n’est pas possible, Direct2D comprend un rastériseur logiciel à hautes performances. lors du rendu dans le logiciel, les applications qui utilisent l’expérience de Direct2D ont de meilleures performances de rendu qu’avec GDI+ et avec une qualité visuelle similaire. Le rastériseur logiciel est également conçu pour être utilisé dans un contexte de service.

le contenu rendu à l’aide de Direct2D peut également être affiché à distance à l’aide de l’infrastructure protocole RDP (Remote Desktop Protocol) (RDP) dans le système d’exploitation Windows 7. Les développeurs peuvent choisir si le rendu est géré par le GPU sur l’ordinateur d’affichage ou s’il est rendu localement et transmis en tant que bitmaps. Ce choix peut être effectué en fonction du taux de remplissage requis et de la quantité de primitives graphiques qui sont restituées. lorsque l’ordinateur d’affichage exécute un système d’exploitation antérieur à Windows 7, le rendu d’affichage à distance est effectué en transmettant des bitmaps sur le réseau.

En fournissant une API unique qui associe les performances de Direct3D et de High Availability en fournissant une solution de secours logicielle, un bureau à distance et un rendu de service, Direct2D permet aux développeurs d’avoir une implémentation unique pour un rendu hautes performances dans de nombreux scénarios différents.

## <a name="visual-quality"></a>Qualité visuelle

Les applications qui utilisent Direct2D pour les graphiques peuvent offrir une meilleure qualité visuelle que ce que vous pouvez obtenir à l’aide de GDI. Direct2D utilise l’anticrénelage par primitive pour fournir des courbes et des lignes à l’allure plus lisses dans le contenu rendu. Il existe également une prise en charge complète de la transparence et de la fusion alpha lors du rendu de primitives 2D. Les images suivantes comparent le contenu avec alias rendu à l’aide de GDI (à gauche) avec un contenu avec anticrénelage rendu par Direct2D (à droite).

![illustration des courbes et des lignes qui sont rendues dans GDI et dans Direct2D](images/rendering-curves-and-lines.png)

Les développeurs peuvent spécifier un rendu par alias des graphiques vectoriels. Cela est utilisé dans les scénarios où l’alignement sur les limites de pixels physiques est requis, comme les éléments d’interface utilisateur tels que les pointeurs ou les règles, si le style GDI de sortie doit être mis en correspondance, ou si l’anticrénelage est effectué en aval dans le processus de rendu via l’anticrénelage à plusieurs échantillons ou un autre mécanisme.

## <a name="interoperability"></a>Interopérabilité

L’intégration du rendu basé sur Direct2D est facilitée pour les développeurs grâce à l’interopérabilité des niveaux de surface avec GDI et Direct3D. les Applications qui restituent du contenu principalement avec GDI, GDI+ ou Direct3D peuvent commencer à utiliser Direct2D pour afficher des zones spécifiques de leur application, et au fil du temps, passer à un modèle où le rendu est réalisé principalement via Direct2D, en utilisant GDI principalement pour les plug-ins ou l’extensibilité héritée.

Direct2D facilite également l’utilisation de [DirectWrite](/windows/desktop/DirectWrite/direct-write-portal) pour le texte de haute qualité et les fonctionnalités de création d’images avancées du [composant Microsoft Windows imaging Component (WIC)](https://msdn.microsoft.com/library/ms737408.aspx).

Pour plus d’informations sur l’interopérabilité de Direct2D, consultez la [section interopérabilité du kit de développement logiciel (SDK) Direct2D.](interoperability.md)

## <a name="summary"></a>Résumé

Microsoft Direct2D permet aux développeurs de créer des fonctionnalités graphiques 2D dans leurs applications qui offrent une meilleure qualité visuelle sur GDI et des caractéristiques de performances qui évoluent avec les GPU modernes. le modèle d’interopérabilité Direct2D permet aux développeurs de migrer de manière sélective des parties de leur application à un moment donné, avec GDI, GDI+ ou un rendu basé sur Direct3D.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Démarrage rapide de Direct2D pour Windows 8](direct2d-quickstart-with-device-context.md)
</dt> <dt>

[Vue d’ensemble de l’API Direct2D](the-direct2d-api.md).
</dt> </dl>

 

 