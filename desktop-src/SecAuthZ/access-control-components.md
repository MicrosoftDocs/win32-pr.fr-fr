---
description: Explique les parties du modèle de contrôle d’accès.
ms.assetid: cca78195-90f5-45ee-9d16-c445d87e9f5e
title: Parties du modèle de Access Control
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8bffdbf6542a9e29360437c50f47495d83467334e09c7aa55e8a136a8fc7556d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117785669"
---
# <a name="parts-of-the-access-control-model"></a>Parties du modèle de Access Control

Il existe deux parties principales du modèle de contrôle d’accès :

-   [Jetons d’accès](access-tokens.md), qui contiennent des informations sur un utilisateur connecté
-   [Descripteurs de sécurité](security-descriptors.md), qui contiennent les informations de sécurité qui protègent un [objet sécurisable](securable-objects.md)

Lorsqu’un utilisateur ouvre une session, le système [*authentifie*](/windows/desktop/SecGloss/a-gly) le nom et le mot de passe du compte de l’utilisateur. Si l’ouverture de session réussit, le système crée un jeton d’accès. Chaque [*processus*](/windows/desktop/SecGloss/p-gly) exécuté pour le compte de cet utilisateur aura une copie de ce jeton d’accès. Le jeton d’accès contient des [identificateurs de sécurité](security-identifiers.md) qui identifient le compte de l’utilisateur et les comptes de groupe auxquels l’utilisateur appartient. Le jeton contient également une liste des [privilèges](privileges.md) détenus par l’utilisateur ou les groupes de l’utilisateur. Le système utilise ce jeton pour identifier l’utilisateur associé lorsqu’un processus tente d’accéder à un objet sécurisable ou d’effectuer une tâche d’administration de système qui requiert des privilèges.

Lorsqu’un objet sécurisable est créé, le système lui assigne un [*descripteur de sécurité*](/windows/desktop/SecGloss/s-gly) qui contient les informations de sécurité spécifiées par son créateur, ou des informations de sécurité par défaut si aucun objet n’est spécifié. Les applications peuvent utiliser des fonctions pour récupérer et définir les informations de sécurité pour un objet existant.

Un descripteur de sécurité identifie le propriétaire de l’objet et peut également contenir les [listes de contrôle d’accès](access-control-lists.md)suivantes :

-   Liste de contrôle d’accès discrétionnaire (DACL, [*Discretionary Access Control List*](/windows/desktop/SecGloss/d-gly) ) qui identifie les utilisateurs et les groupes qui autorisent ou refusent l’accès à l’objet
-   Une [*liste de contrôle d’accès système*](/windows/desktop/SecGloss/s-gly) (SACL) qui contrôle la façon dont le système [audite](audit-generation.md) les tentatives d’accès à l’objet

Une liste ACL contient une liste d' [entrées de contrôle d’accès](access-control-entries.md) (ACE). Chaque ACE spécifie un ensemble de [droits d’accès](access-rights-and-access-masks.md) et contient un SID qui identifie un tiers de [confiance](trustees.md) pour lequel les droits sont autorisés, refusés ou audités. Un tiers de confiance peut être un compte d’utilisateur, un compte de groupe ou une [*ouverture de session*](/windows/desktop/SecGloss/l-gly).

Utilisez les fonctions pour manipuler le contenu des descripteurs de sécurité, des SID et des ACL au lieu d’y accéder directement. Cela permet de garantir que ces structures restent syntaxiquement précises et empêche les futures améliorations du système de sécurité d’interrompre le code existant.

Les rubriques suivantes fournissent des informations sur les parties du modèle de contrôle d’accès :

-   [Jetons d’accès](access-tokens.md)
-   [Descripteurs de sécurité](security-descriptors.md)
-   [Listes de Access Control](access-control-lists.md)
-   [Entrées Access Control](access-control-entries.md)
-   [Droits d’accès et masques d’accès](access-rights-and-access-masks.md)
-   [Fonctionnement de AccessCheck](how-dacls-control-access-to-an-object.md)
-   [Stratégie d’autorisation centralisée](centralized-authorization-policy.md)
-   [Identificateurs de sécurité](security-identifiers.md)

 

 
