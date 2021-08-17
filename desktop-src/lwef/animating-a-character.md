---
title: Animation d’un caractère
description: Animation d’un caractère
ms.assetid: ed42de30-acac-41e8-bacb-4caaff254724
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 937b970f1cdc9de9c973d298bbe963bfa70e4de3733869292e54d5d32742c722
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118976779"
---
# <a name="animating-a-character"></a>Animation d’un caractère

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

Une fois qu’un caractère est chargé, vous pouvez utiliser plusieurs méthodes de Microsoft Agent pour animer le caractère. La première que vous utilisez est généralement la méthode [**Show**](show-method.md) . **Afficher** rend le frame du caractère visible et lit l’animation affectée à l’état d' **affichage** du caractère.

Une fois que le frame du caractère est visible, vous pouvez utiliser la méthode [**Play**](play-method.md) , en spécifiant le nom d’une animation, pour lire cette animation. Les noms d’animation sont spécifiques à une définition de caractère. À mesure qu’une animation est lue, la forme de sa fenêtre change pour correspondre à l’image dans le cadre. Une image de graphique mobile, ou un *Sprite*, s’affiche par-dessus le bureau et toutes les fenêtres, ou l' *ordre de plan*.

Si le fichier du caractère est stocké localement, il vous suffit d’appeler la méthode [**Play**](play-method.md) . Dans d’autres cas, par exemple, lorsque vous avez chargé un. Caractère ACF à partir d’un serveur HTTP, vous devez utiliser la méthode d’extraction (ou de [**préparation**](/windows/desktop/lwef/iagentcharacter--prepare)) pour récupérer d' [**abord les données**](get-method.md) d’animation. L’agent demande alors le fichier d’animation sur le serveur et le stocke dans la mémoire tampon du navigateur sur l’ordinateur local.

La méthode [**Speak**](speak-method.md) vous permet de programmer le caractère à parler, en synchronisant automatiquement la sortie de la lèvre. Pour plus d’informations, reportez-vous à la section sortie de ce document.

Vous pouvez utiliser la méthode [**MoveTo**](moveto-method.md) pour positionner le caractère à un nouvel emplacement. Lorsque vous appelez la méthode **MoveTo** , Microsoft Agent lit automatiquement l’animation appropriée en fonction de l’emplacement actuel du caractère, puis déplace le cadre du caractère. De même, quand vous appelez [**GestureAt**](gestureat-method.md), Microsoft Agent lit l’animation gesturing appropriée en fonction de l’emplacement du caractère et de l’emplacement spécifié dans l’appel.

Pour masquer le caractère, appelez la méthode [Hide](hide-method.md) . Cela lit automatiquement le caractère associé à l’état de **masquage** du caractère, puis masque le frame du caractère. Toutefois, vous pouvez également masquer ou afficher un caractère en définissant la propriété [**visible**](visible-property.md) du caractère.

Microsoft Agent traite tous les appels d’animation, ou *demandes*, de manière asynchrone. Cela permet au code de votre application de continuer à gérer d’autres événements pendant le traitement de la requête. Par exemple, les appels à la méthode [**Play**](play-method.md) placent l’animation dans une file d’attente pour le caractère afin que les animations puissent être lues de manière séquentielle. Toutefois, cela signifie que vous ne pouvez pas supposer qu’un appel à d’autres fonctions s’exécutera nécessairement après l’animation qu’il suit dans votre code. Par exemple, en général, une instruction qui suit un appel à **Play** ou [**MoveTo**](moveto-method.md) s’exécute avant la fin de l’animation.

Vous pouvez synchroniser votre code avec des animations dans la file d’attente d’un caractère en créant une référence d’objet à la demande d’animation et, lorsque l’animation démarre ou se termine, en surveillant les événements de [requête](the-request-object.md) que le serveur utilise pour notifier les clients du caractère. Par exemple, si vous souhaitez qu’une boîte de message s’affiche lorsque le caractère termine une animation, vous pouvez placer l’appel de la boîte de message dans la sous-routine de gestion des événements [**RequestComplete**](requestcomplete-event.md) , en vérifiant l’ID de demande particulier.

Lorsqu’un caractère est masqué, le serveur ne joue pas les animations ; Toutefois, il met toujours en file d’attente et traite la demande d’animation (lit l’animation) et transmet à nouveau l’état de la demande au client. Dans l’état masqué, le caractère ne peut pas devenir en entrée-actif. Toutefois, si l’utilisateur parle du nom du caractère (lorsque l’entrée vocale est activée), le serveur affiche automatiquement le caractère.

Lorsque votre application cliente charge plusieurs caractères en même temps, les services d’animation de Microsoft agent vous permettent d’animer des caractères indépendamment ou d’utiliser les méthodes d' [**attente**](wait-method.md), d' [**interruption**](interrupt-method.md)ou d' [**arrêt**](stop-method.md) pour synchroniser leur animation les unes avec les autres.

Microsoft Agent est également en lecture automatique d’autres animations. Par exemple, si l’état du caractère n’a pas été modifié pendant plusieurs secondes, l’agent commence à exécuter les animations assignées aux animations au **ralenti** du personnage. De même, lorsque l’entrée vocale est activée, l’agent lit les animations d' **écoute** du personnage, puis émet **des animations lorsqu'** un énoncé est détecté. Ces animations gérées par le serveur sont appelées des *États* et sont définies lors de la création d’un caractère. Pour plus d’informations, consultez [conception de caractères pour Microsoft Agent](agent-states.md).

 

 