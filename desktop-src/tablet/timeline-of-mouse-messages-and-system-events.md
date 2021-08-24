---
description: Quand une action donnée est effectuée, les événements système (précédés de ISG \_ ) sont envoyés et reçus presque instantanément par l’application.
ms.assetid: deca6d17-fe2c-4130-88ca-d0605bcb6084
title: Chronologie des messages de la souris et des événements système
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 635147b3f30b8746c75901de78336102ac8d1b41a685919c27f990496f5f225d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119819602"
---
# <a name="timeline-of-mouse-messages-and-system-events"></a>Chronologie des messages de la souris et des événements système

Quand une action donnée est effectuée, les événements système (précédés de ISG \_ ) sont envoyés et reçus presque instantanément par l’application. les messages de la souris (précédés de WM \_ ) sont envoyés lors de l’exécution de l’action et sont reçus par l’application après le temps nécessaire au traitement de l’événement par le service de messagerie Microsoft Windows. En outre, **CursorDown** et **CursorUp** sont des événements PEN reçus du matériel Pen. Ils sont envoyés lorsque le stylet touche l’écran et lorsqu’il est levé à partir de l’écran, respectivement.

Les événements Pen et les messages de la souris ne sont pas synchronisés. Il n’y a aucune garantie que les messages de souris et les événements de stylet correspondants se produisent dans un ordre particulier. Le graphique suivant montre la séquence des événements système et souris attendus, mais pas toujours prévisibles, qui sont envoyés. Notez que, dans le graphique, les événements de souris sont retardés lorsque des événements de mouvement de système sont détectés.

![séquence attendue d’événements système et de souris pour l’entrée du stylet](images/ccdafa48-13c0-4af7-aec5-ed162be4bbe7.jpg)

## <a name="important-implementation-considerations"></a>Considérations importantes relatives à l’implémentation

Tenez compte des éléments suivants lors du développement pour les messages de souris et les événements système :

-   Les événements de stylet et les messages de la souris sont envoyés à une application, que le stylet ou la souris soit utilisé ou non.
-   Si votre application est à l’écoute des messages de stylet et de la souris, il est difficile de prédire la relation entre les messages et, par conséquent, le comportement éventuel. Les événements Pen et les messages de la souris ne sont pas synchronisés. Il n’existe aucune garantie que les messages de souris et les événements PEN correspondants (tels que WM \_ LBUTTONDOWN et **ISG \_ Tap**, ou WM \_ LBUTTONDBLCLK et **ISG \_ DBLTAP**) se produisent dans un ordre particulier. La relation entre ces messages est complexe.
-   Il est recommandé de ne pas associer les événements de souris et de stylet à la même fonctionnalité d’application. Par exemple, une fonctionnalité d’application qui répond à **CursorDown** et **MouseUp** peut ne pas se comporter comme prévu actuellement ou avec les futures versions du kit de développement logiciel (SDK) Tablet PC.
-   Dans le cas d’une séquence d’événements, si l’utilisateur fait glisser le stylet du Tablet PC avant la fin de la séquence, les événements envoyés correspondent à l’opération de glissement à gauche. Par exemple, lors du démarrage du glissement, **ISG \_ Drag** et WM \_ LBUTTONDOWN sont envoyés. Lorsque le stylet est levé, **CursorUp** et WM \_ LBUTTONUP sont envoyés. L’événement de mouvement système peut ne pas se déclencher immédiatement, car il doit déterminer le type d’événement qui se produit.
-   Le double-clic avec un stylet de tablette est souvent moins précis qu’un double-clic avec une souris. Cela provient de la nature inhérente de l’exécution d’un double-clic avec un stylet de tablette. Étant donné que l’utilisateur doit soulever le stylet pour effectuer un double-appui, le délai entre les pressions est souvent supérieur au temps correspondant entre les clics d’un double-clic. En outre, il est probable que les deux robinets du stylet se produisent à des coordonnées d’écran plus éloignées que celles des deux clics de la souris. pour tenir compte de cela, Windows XP édition Tablet PC possède des paramètres pour la distance temporelle et spatiale entre les deux pressions d’un double-appui qui sont séparées des paramètres de la souris pour un double-clic. ces paramètres peuvent être ajustés dans tablette et Pen Paramètres dans le panneau de configuration.

En raison de ces considérations, les applications doivent écouter un seul ensemble de messages plutôt que les deux. Si vous générez une application avec stylet, écoutez uniquement les messages du système et du stylet. Ces messages sont prévisibles et fonctionnent bien avec le stylet du Tablet PC. Si vous générez une application qui n’est pas activée pour le stylet, écoutez uniquement les messages de la souris.

 

 



