---
title: Problèmes d’entrée vocale
description: Problèmes d’entrée vocale
ms.assetid: b42664a2-9615-4e15-97a6-115e9556096b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a7b29a85c79996eb0c01260c8e2b738fcd926f2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103939859"
---
# <a name="speech-input-problems"></a>Problèmes d’entrée vocale

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

### <a name="the-character-does-not-respond-to-my-spoken-input"></a>Le caractère ne répond pas à mon entrée parlée.

Ce symptôme peut être dû à un certain nombre de problèmes. Essayez ce qui suit pour isoler le problème :

-   Vérifiez que votre microphone est correctement branché. Il est judicieux de le tester avec une autre application d’entrée audio pour vous assurer qu’elle fonctionne correctement.
-   Vérifiez qu’un moteur de reconnaissance vocale compatible est installé. Sous Windows 95, Windows 98 et Windows NT 4,0, ouvrez le panneau de configuration. Si vous trouvez l’objet Speech ici, ouvrez-le et il répertorie les moteurs de reconnaissance vocale disponibles et installés sur votre système.
-   Vérifiez que votre carte son est compatible avec Microsoft Windows 95, Windows 98 ou Windows NT.

    La meilleure façon de procéder consiste à exécuter l’application magnétophone fournie avec Windows. Il se trouve généralement dans le menu Démarrer. Cliquez sur le bouton Démarrer, sur programmes, sur accessoires, sur multimédia, puis sur magnétophone. Lorsque la fenêtre de l’enregistreur audio s’affiche, cliquez sur le bouton **Enregistrer** et communiquez avec votre microphone. La ligne de la fenêtre doit s’animer en réponse à votre entrée vocale.

    Si l’application magnétophone ne fonctionne pas sur votre système, contactez le support technique du fabricant de la carte son pour obtenir de l’aide. Votre carte son n’est peut-être pas compatible avec Windows ou il y a peut-être un problème avec les pilotes logiciels de votre carte son.

-   Vérifiez que votre entrée audio pour l’entrée vocale est correctement définie.
    1.  Ouvrez l’objet entrée vocale dans le panneau de configuration. Si l’objet Speech n’est pas présent, installez-en un.
    2.  Sélectionnez le moteur d’entrée vocal que vous avez installé.
    3.  Cliquez sur le bouton de l’Assistant paramètres du microphone. Si ce bouton est désactivé, aucun moteur de reconnaissance vocale compatible n’est installé ou le moteur de reconnaissance vocale que vous avez installé ne prend peut-être pas en charge le réglage automatique.
-   Vérifiez que l’application activée par agent ou la page Web prend en charge l’entrée vocale. Toutes les pages (ou applications) ne prennent pas en charge l’entrée vocale. Appuyez sur la touche d’écoute et maintenez-la enfoncée. En général, il s’agit de la touche Arrêt défil, sauf si vous l’avez modifiée. Une fenêtre contextuelle doit apparaître sous le caractère. Le texte de l’info-bulle indique l’état d’écoute du caractère. Si aucun Conseil ne s’affiche, cela signifie que l’application ou la page Web ne prend pas en charge l’entrée vocale ou que vous n’avez pas de moteur de reconnaissance vocale compatible. Si l’info-bulle apparaît et indique que le caractère est à l’écoute, parlez-en une des commandes vocales du caractère. Si vous ne savez pas quelles commandes vocales sont disponibles, libérez la clé d’écoute et cliquez avec le bouton droit sur le caractère. Ensuite, choisissez Ouvrir la fenêtre commandes vocales dans le menu contextuel. Si la commande n’apparaît pas, la prise en charge de la reconnaissance vocale n’est pas disponible pour l’application ou la page Web que vous utilisez. S’il n’apparaît pas, appuyez de nouveau sur la touche d’écoute et maintenez-la enfoncée. Si l’info-bulle d’écoute apparaît sous le caractère et indique que le caractère est à l’écoute, parlez-en une des commandes listées dans la fenêtre. Si le caractère ne répond pas, passez à l’étape suivante.
-   Vérifiez qu’aucune autre application n’utilise actuellement l’appareil de sortie audio.
-   Vérifiez que l’utilisation d’MIDI par Microsoft Agent ne bloque pas le canal audio (voir les [applications qui jouent sur midi n’ont pas de sortie audio lorsque l’agent Microsoft est en cours d’exécution](output-problems.md)» dans la section problèmes de sortie).
-   Si vous avez suivi les étapes ci-dessus mais que vous rencontrez toujours des problèmes avec les entrées vocales, vérifiez que votre carte son et le logiciel du pilote sont compatibles avec le moteur de reconnaissance vocale que vous utilisez. Consultez le support technique de votre carte son et du fabricant de votre moteur de reconnaissance vocale.

### <a name="the-midi-tone-seems-to-disrupts-speech-input"></a>Le ton MIDI semble perturber l’entrée vocale.

Réduisez le volume MIDI en procédant comme suit.

1.  Ouvrez la fenêtre contrôle du volume en cliquant avec le bouton droit sur l’icône de haut-parleur dans la barre des tâches ou en ouvrant l’objet multimédia dans le panneau de configuration. Cliquez sur le bouton volume dans la section lecture de la page audio.
2.  Diminuez le volume MIDI en déplaçant le curseur vers le dessous.

### <a name="the-character-does-not-respond-to-voice-input-but-i-can-hear-my-voice-through-my-speakers-when-i-talk-into-my-microphone"></a>Ce caractère ne répond pas aux entrées vocales, mais je peux entendre ma voix dans mes orateurs quand je dialogue dans mon microphone.

Votre carte son n’est pas configurée correctement pour une utilisation avec Microsoft Agent. Choisissez l’Assistant paramètres du microphone sur la feuille de propriétés de l’objet Speech dans le panneau de configuration. Pour plus d’informations sur la façon d’accéder à ce bouton, consultez les étapes pour «[le caractère ne répond pas à mon entrée parlée](#the-character-does-not-respond-to-my-spoken-input)».

 

 




