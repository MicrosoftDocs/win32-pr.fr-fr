---
title: Vue d’ensemble de WinEvents et Active Accessibility
description: Les serveurs Microsoft Active Accessibility déclenchent WinEvents pour notifier les clients lorsqu’un objet accessible change.
ms.assetid: a2d486ee-84ef-4c44-a832-dbc0dae81542
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b351b1ce7b6337c4ca0ac0827daff2978c6611af
ms.sourcegitcommit: 85688bbfbe5b121bc05ddf112d54c23a469dfbc0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/29/2020
ms.locfileid: "103940633"
---
# <a name="winevents-and-active-accessibility"></a>WinEvents et Active Accessibility

Les serveurs Microsoft Active Accessibility déclenchent *winEvents* pour notifier les clients lorsqu’un objet accessible change. Dans de nombreuses conditions, un serveur avertit un client qu’une modification a été apportée. Chaque [constante d’événement](event-constants.md) définie par Microsoft Active Accessibility décrit une condition relative à la notification d’un client. Par exemple, WinEvents peut signaler :

- Lorsqu’un objet est créé ou détruit.
- Lorsqu’un objet reçoit ou perd le focus.
- Lorsque l’État ou l’emplacement d’un objet change.
- Lorsqu’une propriété d’un objet change.

Les applications clientes ne reçoivent pas automatiquement les notifications d’événements ; ils doivent spécifier les événements qu’ils souhaitent recevoir en appelant la fonction [**SetWinEventHook**](/windows/desktop/api/Winuser/nf-winuser-setwineventhook) . Avec **SetWinEventHook**, un client s’inscrit pour recevoir un ou plusieurs événements et définit une fonction de raccordement pour gérer les événements spécifiés. Les clients peuvent utiliser la même fonction de raccordement pour gérer plusieurs types d’événements, ou il peut utiliser des fonctions de raccordement multipe. Les clients appellent le **SetWinEventHook** une fois pour chaque fonction de raccordement qu’il doit inscrire.

Les fonctions de raccordement sont situées dans le corps du code du client, dans une DLL mappée au processus du client ou dans une DLL mappée dans le processus du serveur. Chacune de ces méthodes présente des avantages et des inconvénients. Pour plus d’informations, consultez [fonctions de raccordement in-context et hors contexte](in-context-and-out-of-context-hook-functions.md).

Pour informer les clients d’une occurrence d’événement, les serveurs appellent [**NotifyWinEvent**](/windows/desktop/api/Winuser/nf-winuser-notifywinevent). Le système vérifie si des applications clientes ont des fonctions de raccordement définies pour l’événement et appelle les fonctions de raccordement appropriées si nécessaire.

Quand la fonction de raccordement du client est appelée, elle reçoit un certain nombre de paramètres qui décrivent l’événement et l’objet qui a généré l’événement. Pour accéder à l’objet qui a généré l’événement, la fonction de raccordement client appelle [**AccessibleObjectFromEvent**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromevent).

> [!NOTE]
> Si aucun client n’est inscrit pour la réception de WinEvents, l’impact sur les performances sur un serveur pour appeler [**NotifyWinEvent**](/windows/desktop/api/Winuser/nf-winuser-notifywinevent) est négligeable.
>
> Les serveurs appellent [**NotifyWinEvent**](/windows/desktop/api/Winuser/nf-winuser-notifywinevent) pour les modifications uniquement dans leurs propres objets accessibles. ils n’appellent pas **NotifyWinEvent** pour les modifications apportées aux éléments d’interface utilisateur fournis par le système.

## <a name="event-driven-communication"></a>Communication Event-Driven

Les clients doivent inscrire un hook WinEvent avant de pouvoir recevoir des notifications WinEvent. Pour éviter les rappels inutiles et améliorer les performances, il est conseillé aux clients de s’inscrire uniquement pour les événements qu’ils doivent recevoir.

À l’intérieur de la procédure de Hook, le client peut appeler [**AccessibleObjectFromEvent**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromevent) pour récupérer un objet [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) pour l’élément auquel l’événement s’applique. Avec cet objet, le client peut commencer à appeler des méthodes **IAccessible** pour récupérer des informations ou interagir avec l’élément d’interface utilisateur.

## <a name="related-topics"></a>Rubriques connexes

[WinEvents](winevents-infrastructure.md)
