---
description: Lorsque vous utilisez plusieurs Viewports, appuyez sur testingdetermines les Viewports affectés par l’entrée de l’utilisateur en tenant l’emplacement de l’écran d’un contact et en déterminant le rectangle de la fenêtre d’affichage du contact.
ms.assetid: 960EF92D-F439-4A84-AAF9-1469E2830573
title: Utilisation de plusieurs Viewports dans DirectManipulation
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: 627a97a7c9563ca0af9decf79b18340343dda345
ms.sourcegitcommit: 3d718d8f69d3f86eaecf94c5705d761c5a9ef4a1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/20/2020
ms.locfileid: "104562072"
---
# <a name="using-multiple-viewports-in-directmanipulation"></a>Utilisation de plusieurs Viewports dans DirectManipulation

Lorsque vous utilisez plusieurs Viewports, le *test de positionnement* détermine les Viewports affectés par l’entrée d’utilisateur en tenant l’emplacement de l’écran d’un contact et en déterminant le rectangle de la fenêtre d’affichage du contact.

Un scénario courant de [manipulation directe](direct-manipulation-portal.md) consiste à placer une fenêtre d’affichage à l’intérieur d’une autre, également appelée « *fenêtres d’affichage*». Si le contact atteint plusieurs Viewports, l’ordre des appels  [**SetContact**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationviewport-setcontact) par le [*WndProc*](/previous-versions/windows/desktop/legacy/ms644975(v=vs.85)) de la fenêtre détermine la relation parent-enfant des Viewports imbriqués.

Règle : l’élément enfant doit appeler [**SetContact**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationviewport-setcontact)avant d’appeler le parent.

![Diagramme montrant les hiérarchies de test de positionnement](images/dm-art-8.png)

Un contact apparaît dans une fenêtre d’affichage. [**SetContact**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationviewport-setcontact) doit d’abord être appelé sur la fenêtre d’affichage orange (enfant), puis sur la fenêtre d’affichage verte (parent) pour établir la hiérarchie correcte.

## <a name="targeting-the-correct-viewport"></a>Ciblage de la fenêtre d’affichage correcte

Un contact peut être associé à un nombre quelconque de Viewports et chaque contact peut être attribué à un autre jeu de Viewports.

Chaque Viewport peut être configuré pour prendre en charge des interactions spécifiques, selon les besoins.

En fonction de ces paramètres, la [manipulation directe](direct-manipulation-portal.md) identifie la fenêtre d’affichage qui gère l’entrée. La fenêtre d’affichage la plus enfant dans la hiérarchie de test d’atteinte a la première chance de gérer l’entrée. Toutefois, le chaînage et la promotion parente peuvent modifier la fenêtre d’affichage qui gère l’entrée.

## <a name="chaining"></a>Chaînage

Lorsque la fin du contenu est atteinte pendant une manipulation, la [manipulation directe](direct-manipulation-portal.md) applique un effet de limite pour indiquer que le contenu ne peut pas aller plus loin. Toutefois, si une fenêtre d’affichage enfant est *chaînée* à une fenêtre d’affichage parent, cet effet est supprimé. Au lieu de cela, la fenêtre d’affichage ancêtre la plus proche dans la hiérarchie des tests de positionnement qui prend en charge la manipulation gère l’entrée. Si la direction de la manipulation est inversée de sorte que l’ancêtre retourne au point où le chaînage a été déclenché, la manipulation « déchaîne » et le contrôle sont renvoyés à la fenêtre d’affichage enfant.

![Diagramme montrant la manipulation chaînée](images/dm-art-9.png)

Lorsque l’utilisateur effectue un panoramique de la fenêtre d’affichage enfant jusqu’à la périphérie du contenu, la manipulation « chaînes » vers la fenêtre d’affichage parente et l’utilisateur commence à panoramiqueer le contenu parent à la place.

> [!Note]  
> Les axes des abscisses X et Y indépendamment les uns des autres. par conséquent, si un panoramique Diagonal atteint la limite x avant la limite y, la manipulation déplace le parent dans la direction x tout en continuant à déplacer l’enfant sur l’axe y. Pour activer ou désactiver le chaînage, appelez l’API [**SetChaining**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationviewport-setchaining) sur la fenêtre d’affichage enfant.

### <a name="rails"></a>Rail

La spécification des rails dans la configuration d’une fenêtre d’affichage affecte la façon dont l’entrée est chaînée à partir de la fenêtre d’affichage. Plus précisément, l’entrée ne peut pas être chaînée à son parent à partir d’une fenêtre d’affichage enfant avec rail dans le mode panoramique « non rail » des rails. Pour enchaîner les entrées lorsque les rails sont définis, l’utilisateur doit avoir panoramique verticalement ou horizontalement et être verrouillé sur les rails.

### <a name="zooming"></a>zoom ;

Si une fenêtre d’affichage enfant est imbriquée dans un parent et que les deux sont configurés pour le zoom, une manipulation de zoom peut être chaînée d’un enfant à un parent. Toutefois, si la manipulation se poursuit, elle fonctionne uniquement sur le parent et ne peut pas « déchaîner » sur l’enfant. Si l’utilisateur associe un zoom d’un enfant à un parent, la [manipulation directe](direct-manipulation-portal.md) interrompt l’enfant jusqu’à ce que tous les contacts associés à la manipulation soient supprimés de l’écran. À ce stade, l’enfant est libéré de la suspension et l’utilisateur peut effectuer un panoramique de la fenêtre d’affichage enfant.

## <a name="gesture-targeting-parent-promotion"></a>Ciblage du mouvement : promotion parente

Le *ciblage de mouvement* est le processus par lequel les groupes de [manipulation directs](direct-manipulation-portal.md) regroupent les contacts et déterminent la fenêtre d’affichage qui traite l’entrée. La *promotion parente* fait référence aux cas où l’entrée est transférée de l’enfant au parent. Par exemple, lorsqu’un utilisateur remet deux contacts et pinces au sein d’une fenêtre d’affichage enfant configurée uniquement pour le défilement, l’entrée est promue au parent afin que le zoom se produise. La promotion parente se produit, que le chaînage soit activé ou non sur la fenêtre d’affichage enfant.

Contrairement au chaînage, la promotion parente n’est pas inversée. La fenêtre d’affichage parent continue à traiter l’entrée d’interaction jusqu’à ce que tous les contacts soient levés (les fenêtres d’affichage enfants cessent de traiter l’entrée).
