---
title: Présentation de l’architecture
description: cette vue d’ensemble de l’architecture fournit un contexte pour l’API Windows touch pour les Technologies tablette et touch et explique comment elle s’intègre à la plus grande architecture Windows 7.
ms.assetid: b284e96f-0998-408c-ae84-92a3acdc3014
keywords:
- Windows Touch, vue d’ensemble de l’architecture
- Windows Toucher, manipulations
- Windows Toucher, messages
- Windows Toucher, inertie
- Windows Toucher, mouvements
- mouvements, à propos de
- manipulations, à propos de
- inertie, à propos de
- processeur de manipulation, vue d’ensemble de l’architecture
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 36b5ce003c88a66e96072fa9f96bc6ae73bd91cb39f53e03ab3748dd14a194d1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119448651"
---
# <a name="architectural-overview"></a>Présentation de l’architecture

cette vue d’ensemble de l’architecture fournit un contexte pour l’API Windows touch pour les Technologies tablette et touch et explique comment elle s’intègre à la plus grande architecture Windows 7.

## <a name="messages-for-windows-touch-input-and-gestures"></a>Messages pour les entrées tactiles et les gestes Windows

les fonctionnalités de messagerie pour Windows Touch sont activées en écoutant et en interprétant les messages pendant l’exécution. l’illustration suivante montre comment les messages sont générés à partir du matériel et envoyés aux applications par Windows 7.

![Illustration montrant comment Windows 7 envoie des messages à partir d’un matériel tactile multipoint vers une application](images/wm-multitouch-messaging.png)

Dans la colonne la plus à gauche de l’illustration, le matériel tactile reçoit l’entrée d’un utilisateur. Un pilote communique ensuite entre le matériel et le système d’exploitation. Ensuite, le système d’exploitation génère un message [**de \_ mouvement**](wm-gesture.md) [**WM \_ Touch**](wm-touchdown.md) ou WM qui est ensuite envoyé au HWND d’une application. L’application met ensuite à jour l’interface utilisateur en fonction des informations encapsulées dans le message.

Par défaut, les applications reçoivent des mouvements. à moins qu’une application n’enregistre des messages d’entrée tactile Windows avec la fonction [**RegisterTouchWindow**](/windows/desktop/api/winuser/nf-winuser-registertouchwindow) , les notifications de mouvements (messages de [**\_ mouvement WM**](wm-gesture.md) ) sont créées par Windows et envoyées à cette fenêtre d’application. si une fenêtre d’application s’inscrit pour recevoir des messages tactiles, les notifications pour Windows entrée tactile (messages [**WM \_ touch**](wm-touchdown.md) ) sont envoyées à cette fenêtre d’application. Windows Les messages tactiles et de mouvement sont gourmands en ce sens qu’une fois le toucher effectué ou qu’un mouvement commence dans une fenêtre d’application, tous les messages sont envoyés à cette application jusqu’à ce que le mouvement soit terminé ou que la touche principale soit terminée.

pour la prise en charge héritée, Windows interprète les messages de [**\_ mouvement WM**](wm-gesture.md) s’ils sont propagés, puis envoie ou publie les messages appropriés qui mappent au geste. Pour éviter de rompre la prise en charge héritée, veillez à transférer \_ les messages de mouvement WM à l’aide de [DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca). pour plus d’informations sur la prise en charge héritée, consultez la section [vue d’ensemble des gestes Windows Touch](windows-touch-gestures-overview.md).

## <a name="manipulations-and-inertia"></a>Manipulations et inertie

Windows Les programmeurs tactiles doivent être en mesure d’interpréter les gestes de plusieurs sources d’une manière qui est explicite pour le mouvement en cours. Microsoft fournit l’API de manipulation pour effectuer ces calculs. Les manipulations sont essentiellement des mouvements avec des valeurs qui leur sont associées qui décrivent l’intégralité du mouvement. Une fois que vous avez connecté les données d’entrée au processeur de manipulation, vous pouvez récupérer les informations pertinentes pour l’action effectuée par l’utilisateur sur l’objet. La figure suivante illustre une façon d’utiliser des manipulations.

![Illustration montrant les messages tactiles Windows passés au processeur de manipulation d’un objet, qui gère les événements avec l' \- interface imanipulationevents](images/manipulation-arch.png)

Dans le coin supérieur gauche de l’illustration, l’utilisateur a touché l’écran, ce qui crée des messages tactiles. Ces messages contiennent une coordonnée x et une coordonnée y qui sont utilisées pour déterminer l’objet qui est actif. L’objet dans le focus contient un processeur de manipulation. Ensuite, sur le message [**WM \_ Touch**](wm-touchdown.md) avec l’indicateur **TOUCHEVENTF \_ up** , l’objet du focus de l’utilisateur est sélectionné, le processeur de manipulation est référencé et le message est envoyé au processeur de manipulation. Les messages **WM \_ Touch** suivants associés à ce contact sont envoyés au processeur de manipulation jusqu’à ce que le message **WM \_ Touch** avec l’indicateur **TOUCHEVENTF \_ up** soit reçu et que l’objet sélectionné soit déréférencé. Dans la section en bas à droite de l’illustration, un récepteur d’événements de manipulation qui implémente l’interface [**\_ IManipulationEvents**](/windows/win32/api/manipulations/nn-manipulations-_imanipulationevents) est utilisé pour gérer les événements de manipulation, qui sont déclenchés pendant la création des messages tactiles. Le récepteur d’événements peut effectuer des mises à jour de l’interface en fonction des événements de manipulation lorsqu’ils se produisent.

dans Windows applications tactiles, il est courant d’incorporer une physique simple afin que les objets arrivent facilement à l’arrêt, au lieu de s’arrêter brusquement lorsqu’ils ne sont plus touchées. Microsoft fournit l’API d’inertie pour effectuer les calculs pour ces simples physiques afin que votre application puisse se comporter de manière similaire à d’autres applications. Cela vous évite également d’avoir à créer des fonctionnalités physiques fiables. L’illustration suivante montre comment vous pouvez utiliser l’inertie.

![Illustration montrant des messages tactiles Windows passés à l’interface IInertiaProcessor d’un objet, qui déclenche des événements avec l' \- interface imanipulationevents](images/inertia-arch.png)

Notez les similitudes entre l’inertie et la manipulation. La seule différence entre les deux est que, en cas d’inertie, les messages interprétés sont transmis à un processeur d’inertie plutôt qu’à un processeur de manipulation et le processeur d’inertie déclenche les événements. Dans le coin supérieur gauche de l’illustration, sur le message [**WM \_ Touch**](wm-touchdown.md) avec l’indicateur **TOUCHEVENTF \_ up** , les messages tactiles sont utilisés pour identifier un objet qui contient un processeur d’inertie et un processeur de manipulation. Les messages **WM \_ Touch** suivants sont envoyés au processeur de manipulation et le processeur de manipulation effectue des mises à jour de l’interface utilisateur de l’application. Une fois la manipulation terminée, les valeurs de vélocité de la manipulation sont utilisées pour configurer un processeur d’inertie. Comme illustré dans la colonne du milieu, la méthode [**Process**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-process) ou [**ProcessTime**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-processtime) est appelée sur l’interface [**IInertiaProcessor**](/windows/desktop/api/manipulations/nn-manipulations-iinertiaprocessor) à l’aide d’un minuteur ou d’une autre boucle dans un thread séparé jusqu’à ce que les appels indiquent que le traitement du processeur est terminé. Pendant que ces appels sont effectués, les événements de manipulation sont déclenchés, qui sont gérés par un récepteur d’événements de manipulation basé sur l’interface [**\_ IManipulationEvents**](/windows/win32/api/manipulations/nn-manipulations-_imanipulationevents) . Dans la section en bas à droite de l’illustration, ce récepteur d’événements effectue ensuite des mises à jour de l’interface utilisateur de l’application en fonction des événements de manipulation lorsqu’ils se produisent par le biais de gestionnaires d’événements dans le récepteur d’événements.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Guide de programmation](programming-guide.md)
</dt> </dl>

 

 