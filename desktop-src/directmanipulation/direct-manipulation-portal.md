---
description: Les API de manipulation directe vous permettent de créer des expériences utilisateur panoramiques, de zoom et de glissement. Pour ce faire, il traite les entrées tactiles sur une région ou un objet, génère des transformations de sortie et applique les transformations aux éléments d’interface utilisateur.
ms.assetid: 26358bc5-71e9-40f0-9243-9bddd961a0e5
title: Manipulation directe
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: f449079a1772fd6dd43b51a2e5af3920ab3e173e1dc8590567ed4555b6deaf31
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120022583"
---
# <a name="direct-manipulation"></a>Manipulation directe

Les API de manipulation directe vous permettent de créer des expériences utilisateur panoramiques, de zoom et de glissement. Pour ce faire, il traite les entrées tactiles sur une région ou un objet, génère des transformations de sortie et applique les transformations aux éléments d’interface utilisateur. Vous pouvez utiliser la manipulation directe pour optimiser la réactivité et réduire la latence par le biais du traitement d’entrée hors thread, du test de positionnement d’entrée hors thread facultatif et de la prédiction d’entrée/sortie.

toutes les applications qui utilisent la Manipulation directe pour traiter les interactions tactiles affichent le fluide Windows 8 les animations et les comportements de commentaires d’interaction qui se conforment aux [instructions relatives aux interactions utilisateur courantes](/windows/uwp/design/input/).

## <a name="developer-audience"></a>Public de développeurs

l’API de Manipulation directe est destinée aux développeurs expérimentés qui connaissent C/C++, qui ont une bonne compréhension du [modèle COM (component Object Model)](../com/component-object-model--com--portal.md)et connaissent Windows concepts de programmation.

## <a name="run-time-requirements"></a>Conditions d’exécution

La manipulation directe a été introduite dans Windows 8. Il est inclus à la fois dans les versions 32 bits et 64 bits.

## <a name="why-use-directmanipulation"></a>Pourquoi utiliser DirectManipulation

### <a name="handles-interactions-in-a-straightforward-and-consistent-manner"></a>Gère les interactions de manière simple et cohérente

La manipulation directe fonctionne en prédéclarant les comportements et les interactions pour une région ou un objet. Par exemple, une page Web est souvent configurée pour le panoramique et le zoom. Lors de l’exécution, l’entrée est ensuite associée à cette région/cet objet via un appel d’API simple. À partir de ce point, la manipulation directe fait le plus gros du traitement de l’entrée, de l’application des contraintes et de la personnalité, et de la génération des transformations de sortie.

### <a name="build-responsive-touch-applications"></a>Créer des applications tactiles réactives

Pour optimiser la réactivité et réduire la latence, le traitement de manipulation directe se produit sur un thread indépendant distinct du thread d’interface utilisateur. Par conséquent, les transformations de sortie peuvent s’exécuter en parallèle à l’activité sur le thread d’interface utilisateur. L’activité de thread d’interface utilisateur peut inclure la logique d’application, le rendu, la disposition et toute autre chose qui consomme des cycles sur le processeur.

### <a name="implementation-flexibility"></a>Flexibilité d’implémentation

Les interfaces incluses avec la manipulation directe fournissent une prise en charge complète de la gestion des entrées, de la reconnaissance des interactions, des notifications de commentaires et des mises à jour de l’interface utilisateur. Les interfaces incorporent également des services système tels que [DirectComposition](../directcomp/directcomposition-portal.md).

## <a name="basic-concepts"></a>Concepts de base

L’implémentation de la manipulation directe la plus simple se compose d’une *fenêtre d’affichage*, de *contenu* et d' *interactions*. La *fenêtre d’affichage* est une région qui est en mesure de recevoir et traiter les entrées des utilisateurs. Il s’agit également de la région du contenu qui est visible par l’utilisateur final. Le *contenu* est l’objet réel que les utilisateurs finaux peuvent voir et indique ce qui se déplace ou évolue en réponse à une interaction de l’utilisateur. Les *interactions* de l’utilisateur principal (également appelées « *manipulations*») prises en charge par la manipulation directe sont le panoramique et le zoom. Ces interactions appliquent une transformation de translation ou d’échelle au contenu dans la fenêtre d’affichage, respectivement. Plusieurs Viewports (chacun avec son propre contenu) peuvent être configurés dans une seule fenêtre pour créer une expérience d’interface utilisateur riche.

Cette figure illustre une implémentation de base de la manipulation directe avant et après le panoramique.

![implémentation de base de la manipulation directe avant et après le panoramique.](images/dm-art-1.png)

Pendant l’initialisation de la manipulation directe, un objet **DCompDirectManipulationCompositor** est instancié et est associé à une manipulation directe. Cet objet est un wrapper autour de [DirectComposition](../directcomp/directcomposition-portal.md), qui est le compositeur système. L’objet est chargé d’appliquer les transformations de sortie et de piloter les mises à jour visuelles.

Un contact représente un point tactile identifié par le **pointerId** fourni dans le message [WM/_POINTERDOWN](../inputmsg/wm-pointerdown.md) . Lorsqu’un message **WM \_ POINTERDOWN** est reçu, l’application appelle [**SetContact**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationviewport-setcontact). L’application indique à Manipulationabout directe les contacts qui doivent être gérés et les Viewports qui doivent réagir à ces contacts. Les entrées au clavier et à la souris ont des valeurs **pointerId** spéciales afin qu’elles puissent être gérées de manière appropriée par manipulation directe.

Dans le cas de base ci-dessus, lorsque [**SetContact**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationviewport-setcontact) est appelé, plusieurs événements se produisent :

- Lorsque l’utilisateur effectue une panoramisation, un message [WM/_POINTERCAPTURECHANGED](../inputmsg/wm-pointercapturechanged.md) est envoyé à l’application pour notifier que le contact a été consommé par manipulation directe.
- Lorsque l’utilisateur déplace les déplacements, la fenêtre d’affichage déclenche des événements de mise à jour qui sont utilisés par le wrapper [DirectComposition](../directcomp/directcomposition-portal.md) pour piloter les mises à jour visuelles à l’écran. Pour effectuer un panoramique utilisateur dans une fenêtre d’affichage, le contenu s’affiche pour se déplacer correctement sous le contact.
- Lorsque l’utilisateur soulève le contact, il voit que le contenu continue à se déplacer lorsqu’il passe à une animation d’inertie, ce qui ralentit progressivement jusqu’à ce qu’il atteigne son emplacement de repos final.

## <a name="processing-keyboard-and-mouse-input"></a>Traitement de l’entrée du clavier et de la souris

La manipulation directe autorise le transfert manuel des messages du clavier et de la souris à partir du thread d’interface utilisateur de l’application via l’API [**ProcessInput**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationmanager-processinput) , de façon à ce qu’ils puissent être gérés de manière appropriée par manipulation directe.

## <a name="directmanipulation-and-the-hwnd"></a>DirectManipulation et HWND

La manipulation directe est associée à un HWND Win32 afin de recevoir et traiter des messages d’entrée de pointeur pour cette fenêtre. Lorsque la manipulation directe calcule des valeurs de sortie, elle effectue des rappels asynchrones aux objets [com (Component Object Model)](../com/component-object-model--com--portal.md) de manipulation directe qui sont implémentés dans l’application. Ces rappels informent l’application de la transformation appliquée aux objets. La manipulation directe est activée sur le HWND spécifié en appelant [**Activate**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationmanager-activate).

## <a name="supporting-documentation"></a>Documentation de prise en charge

- [Viewports et contenu](directmanipulation-viewports-and-content.md)
- [Utilisation de plusieurs Viewports dans DirectManipulation](directmanipulation-multiple-vieports.md)
- [Traitement des entrées avec DirectManipulation](directmanipulation-processing-input-with-directmanipulation.md)
- [Moteur de composition](directmanipulation-composition-engine.md)
- [Référence de manipulation directe](direct-manipulation-reference.md)

- [BUILD 2013 : WCL-022 : créez votre application de bureau avec le toucher, la souris et le stylet](https://channel9.msdn.com/Events/Build/2013/4-022)
- [Traitement des entrées tactiles avec manipulation directe, exemple](https://github.com/microsoft/Windows-classic-samples/tree/1d363ff4bd17d8e20415b92e2ee989d615cc0d91/Samples/TouchInputDirectManipulation)
