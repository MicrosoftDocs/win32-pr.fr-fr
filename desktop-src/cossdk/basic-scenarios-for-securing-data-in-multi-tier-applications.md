---
description: Cette rubrique présente quelques scénarios de bloc de construction, illustrant les critères décrits dans décider où appliquer la sécurité.
ms.assetid: e9820e53-8891-4bff-a333-00ad2dbb03a4
title: Scénarios de base pour la sécurisation des données dans les applications multiniveau
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f9c4bafb0334bb9e5f124eb184f6ebf2d17f4f0dc40ef04421162dc6604f531
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118308741"
---
# <a name="basic-scenarios-for-securing-data-in-multi-tier-applications"></a>Scénarios de base pour la sécurisation des données dans les applications multiniveau

Cette rubrique présente quelques scénarios de bloc de construction, illustrant les critères décrits dans [décider où appliquer la sécurité](deciding-where-to-enforce-security.md).

## <a name="trusted-server-scenario"></a>Scénario de serveur approuvé

-   La base de données fait confiance entièrement à l’application COM+ pour authentifier et autoriser les utilisateurs finaux à accéder aux données de la base de données.
-   De préférence, la base de données est sécurisée par rapport à tout accès sauf via l’application.
-   L’application COM+ utilise la sécurité basée sur les rôles pour autoriser les utilisateurs.
-   Les connexions s’ouvrent sous l’identité de l’application COM+ et sont entièrement regroupées.
-   L’audit et la journalisation peuvent être effectuées par l’application COM+, ou ces informations peuvent être transmises à la base de données par l’application.

Ce scénario fonctionne mieux pour les données accessibles par des catégories prévisibles d’utilisateurs qui peuvent être encapsulées dans des rôles. Par exemple, seuls les « responsables », les « responsables » et les « comptables » sont autorisés à accéder aux comptes. La logique métier de ce que chaque est autorisé à faire est appliquée dans la couche intermédiaire.

## <a name="impersonation-scenario"></a>Scénario d’emprunt d’identité

-   La base de données effectue sa propre authentification et autorisation des utilisateurs finaux pour limiter l’accès aux données de la base de données.
-   L’application COM+ emprunte l’identité des clients chaque fois qu’ils accèdent à la base de données.
-   Les connexions sont établies par appel et ne peuvent pas être réutilisées.

Ce scénario fonctionne mieux pour les données étroitement liées à de très petites classes d’utilisateurs. Par exemple, chaque employé peut accéder uniquement à son propre fichier personnel, et chaque responsable peut accéder uniquement aux fichiers de personnel de ses rapports.

## <a name="hybrid-scenario"></a>Scénario hybride

Une combinaison des deux scénarios précédents, où l’emprunt d’identité est utilisé uniquement lorsque cela est nécessaire.

Ce scénario fonctionne mieux dans les situations où vous avez des relations de données utilisateur hybrides. Par exemple, vous avez des « responsables », des « responsables », des « comptables » et des milliers de clients Web individuels qui peuvent accéder à leurs propres comptes uniquement. Vous pouvez séparer les chemins logiques via l’application, éventuellement avec des composants distincts, pour gérer la dernière classe d’utilisateurs, en particulier lorsque les hypothèses de performances pour ces utilisateurs sont différentes.

## <a name="trusted-scenario-using-microsoft-sql-server-roles"></a>scénario approuvé à l’aide de rôles de Microsoft SQL Server

-   Microsoft SQL Server 7,0 et versions ultérieures peuvent autoriser l’accès à des lignes spécifiques à l’aide de rôles, mais il fait confiance à l’application COM+ pour authentifier et autoriser les utilisateurs et les mapper aux rôles appropriés dans la base de données.
-   L’application COM+ autorise les utilisateurs à utiliser la sécurité basée sur les rôles, et les rôles d’application correspondent bien aux rôles de base de données.
-   Des connexions spécifiques à un rôle de base de données particulier peuvent être ouvertes. Ces connexions peuvent être réutilisées si elles sont conservées par des objets regroupés dans les applications COM+. Pour plus d’informations sur la façon de procéder, consultez mise en [pool d’objets com+](com--object-pooling.md).
-   L’audit et la journalisation peuvent être effectuées par l’application COM+, ou ces informations peuvent être transmises à la base de données par l’application.

Ce scénario fonctionne mieux pour généralement les mêmes types d’utilisateurs et de données que dans le premier scénario de serveur approuvé, car l’application COM+ est toujours largement fiable pour gérer correctement l’autorisation. Toutefois, il permet de protéger la base de données contre tout accès non autorisé, tout en autorisant l’accès à partir de plusieurs sources en dehors de l’application COM+, sans entraîner de pénalités de mise à l’échelle et de performances dans le scénario d’emprunt d’identité.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Choix de l’emplacement de l’application de la sécurité](deciding-where-to-enforce-security.md)
</dt> <dt>

[Sécurité des applications multiniveau](multi-tier-application-security.md)
</dt> </dl>

 

 



