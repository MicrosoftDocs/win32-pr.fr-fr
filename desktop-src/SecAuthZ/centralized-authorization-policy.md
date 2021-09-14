---
description: Le scénario de Access Control dynamique (DAC) permet une administration de contrôle d’accès centralisée pour les scénarios de serveur de fichiers d’entreprise.
ms.assetid: 5A06B8D8-F14B-4D9E-9ED6-4246A26BF945
title: Stratégie d’autorisation centralisée
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e1e5798c477a69e80f325a35fd443df101a148c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127416546"
---
# <a name="centralized-authorization-policy"></a>Stratégie d’autorisation centralisée

Le [scénario de Access Control dynamique (DAC)](/previous-versions/windows/desktop/dacx/dynamic-access-control-developer-extensibility-roadmap) permet une administration de contrôle d’accès centralisée pour les scénarios de serveur de fichiers d’entreprise. La plupart des organisations disposent de plusieurs domaines dans lesquels elles souhaitent contrôler l’accès.

Voici quelques exemples :

-   Contrôle de l’accès aux informations sensibles, dans lequel les fichiers marqués comme sensibles disposent d’autorisations spécifiques
-   Contrôle de l’accès aux fichiers contenant des informations d’identification personnelle (PII).
-   Limitation de l’accès aux documents en fonction des stratégies de rétention des organisations.

Plusieurs nouvelles abstractions de stratégie d’autorisation sont fournies pour permettre à un administrateur de définir ces stratégies de manière centralisée et de simplifier le processus de définition en permettant à chacune de ces exigences d’accès d’être définies et gérées séparément, mais appliquées comme une seule stratégie.

Deux nouveaux objets de stratégie de Active Directory, une [stratégie d’autorisation centrale](central-authorization-policies.md) et une [règle de stratégie d’autorisation centrale](central-authorization-policy-rule.md) (CAPR) sont introduits dans Windows 8 pour définir et appliquer des stratégies d’autorisation centralisées basées sur des expressions de revendications et des attributs de ressource. lors de l’utilisation de ces objets, un administrateur définit un CAPR en tant que stratégie d’autorisation spécifique qui peut être appliquée à des ressources qui ont un certain attribut ou satisfont à une certaine condition d’applicabilité. par exemple, les documents intitulés « High Business impact ». les capes peuvent être définis pour chaque stratégie de contrôle d’accès souhaitée dans une organisation qui peut être exprimée, et les ressources auxquelles elle doit être appliquée peuvent être identifiées, en termes d’expressions DAC Windows 8. un capuchon est un ensemble de CAPRS qui peut être appliqué ensemble sur des ressources. le diagramme suivant montre les relations entre le Cap et le Cap et les étapes conceptuelles impliquées dans la définition et l’application de ces objets aux ressources de fichier. ![relation entre les capes et les majuscules](images/cap.png)

 

 
