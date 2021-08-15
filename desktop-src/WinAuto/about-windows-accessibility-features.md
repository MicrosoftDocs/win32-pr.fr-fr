---
title: Fonctionnalités d’accessibilité Windows
description: 'Windows l’accessibilité prend en charge deux catégories de fonctionnalités pour les développeurs de Windows : les api Win32 et les Paramètres utilisateur.'
ms.assetid: 823bbc5b-062b-43ef-9f3e-822dc6f55c5d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fac63f4bf021888ee96cb180e423f55b07190959ad8c8b7966f1a4a7ae395119
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118994419"
---
# <a name="windows-accessibility-features"></a>Fonctionnalités d’accessibilité Windows

Windows l’accessibilité prend en charge deux catégories de fonctionnalités pour aider Windows développeurs à concevoir des applications accessibles, les développeurs de technologie d’assistance peuvent créer des outils tels que les lecteurs d’écran et les loupes, et les ingénieurs de test de logiciel créent des scripts automatisés pour tester les applications Windows.

## <a name="settings"></a>Paramètres

Deux types de paramètres sont disponibles pour les utilisateurs (par le biais de la facilité d’accès du panneau de configuration) qui sont également exposés aux développeurs :

- [Paramètres d’accessibilité](accessibility-parameters.md). Lorsqu’ils sont définis, ces paramètres indiquent que les applications doivent modifier leur comportement par défaut. Les applications peuvent vérifier l’état d’un paramètre d’accessibilité pour déterminer si l’utilisateur souhaite un comportement spécial qui peut être fourni de manière spécifique à l’application. Par exemple, le paramètre son texte indique qu’une application qui utilise généralement un son pour transmettre des informations importantes doit également fournir les informations visuellement.
- [Fonctionnalités d’accessibilité intégrées](built-in-accessibility-features.md). Ces fonctionnalités sont intégrées au système ou fournies en tant qu’extension au système. Elles affectent la manière dont l’utilisateur fournit une entrée de clavier et de souris à l’ordinateur. Lorsqu’elles sont activées, leurs fonctionnalités sont disponibles, quelles que soient les applications en cours d’exécution. C’est le cas, par exemple, d’un filtre de clavier qui permet aux utilisateurs ayant des handicaps de mouvement de taper des combinaisons de touches comme CTRL + ALT + SUPPR.

Chaque paramètre d’accessibilité et chaque fonctionnalité d’accessibilité intégrée correspond à un paramètre système qui peut être défini ou interrogé avec la fonction [SystemParametersInfo](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) .

## <a name="win32-apis"></a>API Win32

Les API Win32 fournissent des fonctionnalités d’accessibilité et d’automatisation pour aider les développeurs à créer des applications et des infrastructures d’interface utilisateur, des outils de développement de technologies d’assistance, des testeurs garantissant des implémentations de qualité, et les personnes handicapées utilisent leurs ordinateurs et appareils.

## <a name="related-topics"></a>Rubriques connexes

[Considérations relatives à la sécurité pour les technologies d’assistance](uiauto-securityoverview.md)