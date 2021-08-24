---
title: Vue d’ensemble du développement d’interface utilisateur
description: Cette section décrit les trois phases de conception de l’interface utilisateur et présente les tâches qui sont généralement associées à chaque phase.
ms.assetid: ab544cb9-eed3-4575-a8dd-2f5d7b5c575f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a3c7c965c5c7bfd0250c2116ee23bd91b2125ae5ea6bf15bd714ed13d58e000d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119589139"
---
# <a name="overview-of-the-user-interface-development-process"></a>Vue d’ensemble du processus de développement de l’interface utilisateur

Cette section décrit les trois phases de conception de l’interface utilisateur et présente les tâches qui sont généralement associées à chaque phase.

## <a name="the-application-user-interface-and-the-user-experience"></a>L’interface utilisateur de l’application et l’expérience utilisateur

Pour commencer, vous devez préciser les termes « interface utilisateur » et « expérience utilisateur ».

L’interface utilisateur d’une application implique généralement les objets qu’un utilisateur voit et interagit directement sur son écran. Par exemple, ces objets incluent l’espace de document, les menus, les boîtes de dialogue, les icônes, les images et les animations.

Toutefois, l’interface utilisateur d’une application n’est qu’un aspect de l’expérience utilisateur globale. Les autres aspects de l’expérience utilisateur qui ne sont pas visibles par l’utilisateur, mais qui sont intégrés à une application et qui sont essentiels à son utilisation, incluent le temps de démarrage, la latence, la gestion des erreurs et les tâches automatisées qui sont terminées sans interaction directe de l’utilisateur.

En général, une interface utilisateur requiert une action d’un utilisateur pour accomplir une tâche, tandis qu’une expérience utilisateur exceptionnelle peut être obtenue sans aucune interface utilisateur.

## <a name="user-interface-development"></a>Développement de l’interface utilisateur

Fournir une expérience utilisateur réussie nécessite une approche équilibrée tout au long du cycle de vie du développement. Pour garantir cet équilibre, vous devez non seulement vous concentrer sur l’implémentation des fonctionnalités requises pour effectuer une tâche, mais également sur la façon dont la tâche est exposée par le biais de l’interface utilisateur. Rappelez-vous que l’interface utilisateur ne doit pas être fonctionnelle, elle doit également être utilisable.

L’exemple suivant présente les phases typiques du processus de Dvelopment de l’interface utilisateur :

### <a name="designing"></a>Conception

-   Spécifications fonctionnelles : Déterminez les exigences et les objectifs initiaux de l’application.
-   Analyse utilisateur : Identifiez les scénarios utilisateur et comprenez les besoins et les attentes des utilisateurs pour chaque scénario.
-   Conception conceptuelle : modélisez l’entreprise sous-jacente que l’application doit prendre en charge.
-   Conception logique : concevez le processus et le workflow d’informations de l’application.
-   Conception physique : Déterminez comment la conception logique sera implémentée sur des plateformes physiques spécifiques.

### <a name="implementing"></a>Conféré

-   Prototype : développez des maquettes de papier ou d’écran interactif qui se concentrent sur l’interface et n’incluez pas d’éléments de conception visuelle gênants.
-   Construct : générez l’application et préparez les demandes de modification de conception.

### <a name="testing"></a>Test

-   Test d’utilisabilité : Testez l’application avec divers utilisateurs et scénarios.
-   Test d’accessibilité : Testez l’application avec des technologies accessibles et des outils de test automatisés.

 

 




