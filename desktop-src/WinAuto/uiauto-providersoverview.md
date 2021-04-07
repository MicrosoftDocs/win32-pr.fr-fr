---
title: Vue d'ensemble des fournisseurs UI Automation
description: Cette rubrique fournit une vue d’ensemble de la façon dont les développeurs de contrôles implémentent des fournisseurs UI Automation.
ms.assetid: 8928c889-0e0a-439f-87e8-a9d121fcf73f
keywords:
- UI Automation, vue d’ensemble des fournisseurs
- UI Automation, types de fournisseurs
- UI Automation, concepts du fournisseur
- fournisseurs, à propos de
- fournisseurs, types
- fournisseurs, concepts
- fournisseurs, éléments
- fournisseurs, navigation
- fournisseurs, vues
- fournisseurs, infrastructures
- fournisseurs, fragments
- fournisseurs, hôtes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21f70a806fe33b16eed2555c123cc50f1f2b28da
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103939847"
---
# <a name="ui-automation-providers-overview"></a>Vue d'ensemble des fournisseurs UI Automation

Un fournisseur Microsoft UI Automation est un objet logiciel qui expose un élément de l’interface utilisateur d’une application de sorte que les applications clientes d’accessibilité puissent récupérer des informations sur l’élément et appeler ses fonctionnalités. En général, chaque contrôle ou autre élément distinct d’une interface utilisateur a un fournisseur.

Microsoft propose un fournisseur pour chacun des contrôles standard fournis avec Microsoft Win32, Windows Forms et Windows Presentation Foundation (WPF). Cela signifie que les contrôles standard sont exposés automatiquement aux clients UI Automation. vous n’avez pas besoin d’implémenter d’interfaces d’accessibilité pour les contrôles standard.

Si votre application comprend des contrôles personnalisés, vous devez implémenter des fournisseurs UI Automation pour ces contrôles afin de les rendre accessibles aux applications clientes d’accessibilité. Vous devez également implémenter des fournisseurs pour les contrôles tiers qui n’incluent pas de fournisseur. Implémentez un fournisseur en implémentant des interfaces de fournisseur UI Automation et des interfaces de modèle de contrôle.

Cette rubrique fournit une vue d’ensemble de la façon dont les développeurs de contrôles implémentent des fournisseurs UI Automation. Il comprend les sections suivantes.

-   [Types de fournisseurs](#types-of-providers)
-   [Concepts de fournisseur UI Automation](#ui-automation-provider-concepts)
    -   [Éléments](#elements)
    -   [Frameworks](#frameworks)
    -   [Fragments](#fragments)
    -   [Hôtes](#hosts)
-   [Rubriques connexes](#related-topics)

## <a name="types-of-providers"></a>Types de fournisseurs

Les fournisseurs UI Automation se répartissent en deux catégories : les fournisseurs côté serveur et les fournisseurs côté client (ou *proxy*).

Un fournisseur côté serveur est un objet, tel qu’un contrôle personnalisé, qui contient sa propre implémentation native des interfaces de fournisseur UI Automation pertinentes. Un fournisseur côté serveur communique avec les applications clientes à travers la limite de processus en exposant son implémentation des interfaces de fournisseur au noyau UI Automation, qui traite les demandes des clients. Pour plus d’informations sur les fournisseurs côté serveur, consultez [implémentation d’un fournisseur UI Automation Server-Side](uiauto-serversideprovider.md).

Un fournisseur côté client, ou proxy, est un objet qui implémente des interfaces de fournisseur UI Automation pour le compte d’un contrôle ne comprend pas une implémentation complète de son propre fournisseur. Sans proxy, ce type de contrôle est largement opaque pour l’Automation d’interface utilisateur, qui peut fournir uniquement les informations de base disponibles à partir du handle de fenêtre (**HWND**), telles que l’emplacement du contrôle. En règle générale, les fournisseurs de proxy communiquent avec l’application à travers la limite de processus en envoyant et en recevant des messages Windows. Pour plus d’informations, consultez [implémentation d’un fournisseur UI Automation Client-Side (proxy)](uiauto-clientsideprovider.md).

## <a name="ui-automation-provider-concepts"></a>Concepts de fournisseur UI Automation

Cette section fournit de brèves explications sur certains concepts clés que vous devez comprendre pour pouvoir implémenter des fournisseurs UI Automation.

### <a name="elements"></a>Éléments

Les éléments UI Automation sont des parties de l’interface utilisateur, généralement des fenêtres ou des contrôles, qui sont visibles par les clients UI Automation. Les fenêtres d’application, les volets, les boutons, les info-bulles, les zones de liste et les éléments de liste en sont des exemples.

Les éléments UI Automation sont exposés aux clients sous la forme d’une arborescence. UI Automation construit l’arborescence en naviguant d’un élément à un autre. La navigation est activée par le fournisseur pour chaque élément. Chaque élément peut pointer vers son propre élément parent, ses éléments frères et ses premier et dernier éléments enfants.

Un client peut voir l’arborescence UI Automation dans trois vues principales, comme décrit dans le tableau suivant :



| Affichage         | Description                                                    |
|--------------|----------------------------------------------------------------|
| Affichage brut     | Comprend tous les éléments.                                         |
| Vue de contrôle | Comprend des éléments qui sont des contrôles.                           |
| Vue de contenu | Comprend des éléments de contrôle qui fournissent des informations à l’utilisateur. |



 

Il incombe à l’implémentation du fournisseur de définir un élément comme élément de contenu ou élément de contrôle. Les éléments de contrôle peuvent être ou non également des éléments de contenu, mais tous les éléments de contenu sont des éléments de contrôle.

Pour plus d’informations sur la vue client de l’arborescence, consultez [UI Automation Tree Overview](uiauto-treeoverview.md).

### <a name="frameworks"></a>Frameworks

Une infrastructure est un composant qui gère les contrôles enfants, les tests de positionnement et le rendu dans une zone de l’écran. Par exemple, une fenêtre Win32, souvent appelée **HWND**, peut servir d’infrastructure contenant plusieurs éléments UI Automation, tels qu’une barre de menus, une barre d’État et des boutons.

Les contrôles de conteneur Win32, tels que les zones de liste et les contrôles d’arborescence, sont considérés comme des infrastructures, car ils contiennent leur propre code pour restituer des éléments enfants et effectuer des tests de positionnement sur ces derniers. En revanche, une zone de liste WPF n’est pas une infrastructure, car le rendu et le test de positionnement sont gérés par la fenêtre conteneur.

L’interface utilisateur d’une application peut être composée de différentes infrastructures. Par exemple, un **HWND** dans une application peut contenir du HTML dynamique (DHTML) qui peut à son tour contenir un composant tel qu’une zone de liste déroulante dans un **HWND**.

### <a name="fragments"></a>Fragments

Une sous-arborescence complète d’éléments d’une infrastructure particulière est appelée un fragment. L’élément au niveau du nœud racine de la sous-arborescence est appelé racine de fragment. Une racine de fragment n’a pas de parent, mais elle est hébergée dans une autre infrastructure, généralement une fenêtre Win32 (**HWND**).

### <a name="hosts"></a>Hôtes

Le nœud racine de chaque fragment doit être hébergé dans un élément, généralement une fenêtre Win32 (**HWND**). Le bureau est une exception et il n’est hébergé dans aucun autre élément. L’hôte d’un contrôle personnalisé est le **HWND** du contrôle lui-même, et non la fenêtre d’application ou toute autre fenêtre qui peut contenir des groupes de contrôles de niveau supérieur.

L’hôte d’un fragment joue un rôle important dans la fourniture de services UI Automation. Il permet la navigation vers la racine de fragment et fournit des propriétés par défaut afin que le fournisseur personnalisé n’ait pas à les implémenter.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

**Méthodologique**
</dt> <dt>

[Implémentation d’un fournisseur UI Automation Client-Side](uiauto-clientsideprovider.md)
</dt> <dt>

[Implémentation d’un fournisseur UI Automation Server-Side](uiauto-serversideprovider.md)
</dt> <dt>

[Vue d’ensemble de l’arborescence UI Automation](uiauto-treeoverview.md)
</dt> </dl>

 

 




