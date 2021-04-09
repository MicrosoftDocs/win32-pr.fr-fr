---
title: Test d’une interface utilisateur
description: Cette section décrit en détail certaines des tâches associées au test d’une interface utilisateur pour une application Windows.
ms.assetid: d628e530-7a0b-4a8d-9a9f-253aec275fa9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2e86282c03502642541c0ea1318b8ccaf6d16b2
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103941281"
---
# <a name="testing-a-user-interface"></a>Test d’une interface utilisateur

Cette section décrit en détail certaines des tâches associées au test d’une interface utilisateur pour une application Windows.

-   [Introduction](#introduction)
-   [Tests de la facilité d'utilisation](#usability-testing)
-   [Test d’accessibilité](#accessibility-testing)

## <a name="introduction"></a>Introduction

Pour déterminer complètement l’efficacité et la facilité d’utilisation de l’interface utilisateur d’une application, elle doit être testée. Les tests exposent la facilité ou la difficulté de l’interface utilisateur pour l’audience la plus large possible. Le temps nécessaire au test d’une application vaut bien.

Cette rubrique se concentre sur trois principaux scénarios de test : convivialité générale, accessibilité et automatisation.

## <a name="usability-testing"></a>Tests de la facilité d'utilisation

Le test d’utilisabilité offre la possibilité d’évaluer un produit en étudiant la manière dont les utilisateurs réels utilisent réellement le produit. Cette analyse permet de s’assurer que les hypothèses clés relatives aux utilisateurs prévus et aux conceptions d’interface sont prises en charge (ou Challenge) avec des données réelles. La collecte de ces données empiriques vous permet uniquement de déterminer la façon dont l’interface utilisateur d’un produit répond aux besoins et aux attentes de vos utilisateurs.

En observant l’interaction de l’utilisateur avec le produit et en écoutant les commentaires des utilisateurs, des fonctionnalités importantes qui peuvent être difficiles à trouver et à utiliser sont identifiées. En fonction de ces résultats, les ajustements peuvent être apportés à l’interface utilisateur selon les besoins. Il est presque impossible de créer un produit utile sans un certain niveau de test d’utilisation, car les résultats fournissent la base pour prendre de meilleures décisions sur le produit et améliorer l’expérience globale de l’utilisateur.

Le test d’utilisabilité offre une rentabilité significative uniquement lorsqu’il est bien intégré à l’ensemble du cycle de vie du projet. Une étude d’utilisabilité unique peut identifier des problèmes, mais sans tests de suivi, il est difficile de déterminer si les solutions ont résolu ces problèmes ou en ont introduit de nouvelles.

Les principaux scénarios de test d’utilisation sont les suivants :

-   Si vous êtes un fournisseur de produits logiciels, le test des utilisateurs réels de votre produit signifie que vous évaluez la conception. En fonction de la façon dont vous avez conçu l’application, les utilisateurs peuvent-ils effectuer les tâches qu’ils ont besoin d’effectuer ? Le test des véritables utilisateurs qui effectuent des tâches réelles peut également indiquer si les instructions d’interface utilisateur que vous suivez fonctionnent dans le contexte de votre produit, et lorsque la cohérence contribue ou entrave la capacité d’un utilisateur à effectuer son travail.
-   Si vous êtes un acheteur de produits logiciels, vous pouvez effectuer des tests d’utilisation pour évaluer un produit à des fins d’achat. Par exemple, votre entreprise peut envisager d’acheter un produit pour ses employés de 20000. Avant que l’entreprise ne passe son argent, elle souhaite s’assurer que le produit en question permettra vraiment aux employés d’améliorer leur travail. Le test d’utilisabilité peut également être utile pour déterminer si l’application proposée suit les règles de style d’interface utilisateur publiées (internes ou externes). Il est préférable d’utiliser les instructions de l’interface utilisateur comme source d’information auxiliaire plutôt que principale pour prendre des décisions d’achat.

Pour plus d’informations, consultez [convivialité dans la pratique : test de la convivialité](/archive/msdn-magazine/2009/brownfield/usability-in-practice-usability-testing).

## <a name="accessibility-testing"></a>Test d’accessibilité

Le test d’accessibilité englobe deux zones de conception de l’interface utilisateur : la prise en charge des utilisateurs handicapés et l’accès par programme par les infrastructures de test automatisées.

S’assurer qu’une application est accessible aux utilisateurs avec handicap implique de tester :

-   Conformité : l’application respecte-t-elle les différentes exigences légales en matière d’accessibilité ?
-   Efficacité : les utilisateurs handicapés peuvent-ils utiliser l’application ?
-   Utilité : l’application expose-t-elle les fonctionnalités adéquates pour les utilisateurs handicapés ?
-   Satisfaction : comment l’application est-elle perçue par les utilisateurs handicapés ?

Le test de ces aspects d’une application peut être effectué via un audit d’accessibilité, ce qui implique une révision manuelle de l’application par un expert en accessibilité et une étude d’utilisabilité ciblée des utilisateurs désactivés et des appareils de technologie d’assistance.

Bien qu’apparemment sans rapport, il existe une corrélation étroite entre les exigences d’accès par programmation des infrastructures de test automatisées et celles des appareils de technologie d’assistance. La prise en charge d’une offre l’avantage supplémentaire de l’activation de l’autre. Pour plus d’informations sur l’accessibilité et l’automatisation des tests dans les applications Windows, consultez [accessibilité](/windows/desktop/accessibility), [outils de test](/windows/desktop/WinAuto/testing-tools)et [API d’automatisation Windows](/windows/desktop/WinAuto/windows-automation-api-portal).

 

 