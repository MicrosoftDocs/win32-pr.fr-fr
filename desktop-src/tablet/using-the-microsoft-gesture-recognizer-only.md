---
description: 'Vous pouvez utiliser un collecteur d’encres (InkCollector, InkOverlay ou InkPicture) pour accéder directement à la reconnaissance de mouvement Microsoft par défaut. Pour utiliser un collecteur d’encres pour accéder au module de reconnaissance de mouvement : définissez la propriété CollectionMode du collecteur d’encre en mode InkAndGesture ou en mode GestureOnly. inkOverlay. CollectionMode = CollectionMode. GestureOnly ; Choisissez le geste que vous souhaitez prendre en charge. inkOverlay. SetGestureStatus (ApplicationGesture. AllGestures, true); implémentez un gestionnaire d’événements qui reçoit des notifications de mouvement. Dans le gestionnaire d’événements, vous devez implémenter l’action correspondant à chaque événement reçu. Remarque le mode mixte ne prend en charge que les gestes à trait simple. Le mode geste prend en charge les gestes à plusieurs traits. inkOverlay. geste + = New InkCollectorGestureEventHandler ( \_ mouvement inkOverlay); en mode InkAndGesture, chaque trait individuel est envoyé au module de reconnaissance de mouvement Microsoft. S’il est reconnu comme un geste que vous avez activé, une notification d’événement est envoyée. Si l’application accepte la notification d’événement, le trait est effacé. Si l’application n’accepte pas la notification ou si le trait n’est pas reconnu comme un mouvement, le trait est stocké dans l’objet Ink. En mode GestureOnly, les traits sont délimités par des délais d’attente avant et après les traits. Les traits collectés dans le délai d’expiration sont envoyés au module de reconnaissance. Si les traits sont reconnus comme un geste que vous avez activé, une notification d’événement est envoyée. L’application peut accepter ou refuser l’événement, ce qui a pour effet d’appliquer l’action correspondante. En mode de mouvement uniquement, les traits ne sont jamais enregistrés dans l’objet Ink.'
ms.assetid: 3f5f00a3-1f2c-4fa2-9738-bc5fb56e2208
title: Utilisation du module de reconnaissance de mouvement Microsoft uniquement
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08d7b27ae30e0bba98ee2c9db57cc0da2d6491932d0137cc5cd4d2b6f86420ea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118715176"
---
# <a name="using-the-microsoft-gesture-recognizer-only"></a>Utilisation du module de reconnaissance de mouvement Microsoft uniquement

Vous pouvez utiliser un collecteur d’encres ([**InkCollector**](inkcollector-class.md), [**InkOverlay**](inkoverlay-class.md)ou [InkPicture](inkpicture-control-reference.md)) pour accéder directement à la reconnaissance de mouvement Microsoft par défaut.

Pour utiliser un collecteur d’encres pour accéder au module de reconnaissance de mouvement :

-   Définissez la propriété [**CollectionMode**](/windows/desktop/api/msinkaut/ne-msinkaut-inkcollectionmode) du collecteur d’encre en mode **InkAndGesture** ou en mode **GestureOnly** .

`inkOverlay.CollectionMode = CollectionMode.GestureOnly;`

-   Choisissez le geste que vous souhaitez prendre en charge.

`inkOverlay.SetGestureStatus(ApplicationGesture.AllGestures, true);`

-   Implémentez un gestionnaire d’événements qui reçoit des notifications de mouvement. Dans le gestionnaire d’événements, vous devez implémenter l’action correspondant à chaque événement reçu.
    > [!Note]  
    > Le mode mixte ne prend en charge que les gestes à trait simple. Le mode geste prend en charge les gestes à plusieurs traits.

     

`inkOverlay.Gesture += new InkCollectorGestureEventHandler(inkOverlay_Gesture);`

En mode **InkAndGesture** , chaque trait individuel est envoyé au module de reconnaissance de mouvement Microsoft. S’il est reconnu comme un geste que vous avez activé, une notification d’événement est envoyée. Si l’application accepte la notification d’événement, le trait est effacé. Si l’application n’accepte pas la notification ou si le trait n’est pas reconnu comme un mouvement, le trait est stocké dans l’objet [**Ink**](inkdisp-class.md) .

En mode **GestureOnly** , les traits sont délimités par des délais d’attente avant et après les traits. Les traits collectés dans le délai d’expiration sont envoyés au module de reconnaissance. Si les traits sont reconnus comme un geste que vous avez activé, une notification d’événement est envoyée. L’application peut accepter ou refuser l’événement, ce qui a pour effet d’appliquer l’action correspondante. En mode de mouvement uniquement, les traits ne sont jamais enregistrés dans l’objet [**Ink**](inkdisp-class.md) .

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Microsoft. Ink. InkCollector. CollectionMode](/previous-versions/ms836497(v=msdn.10))
</dt> <dt>

[Microsoft. Ink. InkOverlay. CollectionMode](/previous-versions/ms833092(v=msdn.10))
</dt> <dt>

[Microsoft. Ink. InkPicture. CollectionMode](/previous-versions/ms582182(v=vs.100))
</dt> </dl>

 

 
