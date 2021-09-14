---
description: Enregistrement de bouclage
ms.assetid: 71c567f7-fffa-4b75-897a-63ed30c4c9b0
title: Enregistrement de bouclage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 374da7497096118905f5e4c79bbacda832a42a7b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127114902"
---
# <a name="loopback-recording"></a>Enregistrement de bouclage

En mode de bouclage, un client de WASAPI peut capturer le flux audio qui est lu par un périphérique de point de terminaison de rendu. Pour ouvrir un flux en mode de bouclage, le client doit :

-   Obtenez une interface [**IMMDevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) pour l’appareil de point de terminaison de rendu.
-   Initialisez un flux de capture en mode de bouclage sur le périphérique de point de terminaison de rendu.

Après avoir effectué ces étapes, le client peut appeler la méthode [**IAudioClient :: GetService**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getservice) pour obtenir une interface [**IAudioCaptureClient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudiocaptureclient) sur l’appareil de point de terminaison de rendu.

WASAPI fournit le mode de bouclage principalement pour prendre en charge l’annulation de l’écho acoustique (AEC). Toutefois, d’autres types d’applications audio peuvent être utiles en mode de bouclage pour capturer la combinaison de systèmes jouée par le moteur audio.

Dans l’exemple de code de [capture d’un flux](capturing-a-stream.md), la fonction RecordAudioStream peut être facilement modifiée pour configurer un flux de capture en mode de bouclage. Les modifications requises sont les suivantes :

-   Dans l’appel à la méthode [**IMMDeviceEnumerator :: GetDefaultAudioEndpoint**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint) , modifiez le premier paramètre (*flux* de données) de eCapture en eRender.
-   Dans l’appel à la méthode [**IAudioClient :: Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize) , modifiez la valeur du deuxième paramètre (*StreamFlags*) de 0 à AUDCLNT \_ StreamFlags \_ Loopback.

dans les versions de Windows antérieures à Windows 10 1703, le client de capture en mode pull ne reçoit aucun événement lorsqu’un flux est initialisé avec une mise en mémoire tampon pilotée par les événements et qu’il est activé pour la boucle. Pour contourner ce contournement, initialisez un flux de rendu en mode piloté par les événements. Chaque fois que le client reçoit un événement pour le flux de rendu, il doit signaler au client de capture d’exécuter le thread de capture qui lit le jeu d’exemples suivant dans la mémoire tampon du point de terminaison de capture. dans Windows 10 versions 1703 et ultérieures, les clients de bouclage piloté par les événements sont pris en charge et n’ont plus besoin de la solution de contournement impliquant le flux de rendu.  

Un client peut activer le mode de bouclage uniquement pour un flux en mode partagé (AUDCLNT \_ SHAREMODE \_ partagé). Les flux en mode exclusif ne peuvent pas fonctionner en mode de bouclage.

L’implémentation du bouclage par WASAPI dépend des fonctionnalités du matériel. Si le matériel prend en charge un code confidentiel de bouclage sur le point de terminaison de rendu, WASAPI utilise le son fourni sur ce code PIN pour le flux de bouclage. Lorsque le matériel ne prend pas en charge un code confidentiel de bouclage, WASAPI copie le flux de sortie du moteur audio dans la mémoire tampon de capture de l’application de bouclage, en plus de copier les données audio sur la broche de rendu du matériel.

Certains fournisseurs de matériel implémentent des périphériques de bouclage (par opposition à épingler des instances sur des appareils de rendu) dans leurs adaptateurs audio. Bien que les périphériques de bouclage matériel soient similaires en fonctionnement au mode de bouclage WASAPI, ils peuvent être plus difficiles à utiliser.

Les périphériques de bouclage matériel présentent les inconvénients suivants pour les applications audio :

-   Les cartes audio n’ont pas toutes des périphériques de bouclage. Ainsi, les applications qui en dépendent ne fonctionneront pas sur tous les systèmes.
-   Avant qu’une application puisse enregistrer à partir d’un périphérique de bouclage, l’utilisateur doit identifier le périphérique de bouclage et l’activer pour l’utiliser.

Différents fournisseurs attribuent des noms différents à leurs périphériques de bouclage matériels. Les noms suivants sont des exemples :

-   Combinaison stéréo
-   WaveOut Mix
-   Sortie mixte
-   Ce que vous entendez

L’absence de noms standardisés peut amener les utilisateurs à avoir des difficultés à identifier un périphérique de bouclage dans une liste de noms d’appareils.

Un périphérique de bouclage matériel est un périphérique de capture. Ainsi, si un adaptateur prend en charge un périphérique de bouclage, une application audio peut enregistrer à partir de l’appareil de la même manière qu’il enregistre depuis n’importe quel autre périphérique de capture.

Par exemple, si vous sélectionnez un périphérique de bouclage matériel comme périphérique de capture par défaut, vous pouvez utiliser la fonction RecordAudioStream (sans modification) dans l’exemple de code de [capture d’un flux](capturing-a-stream.md) pour capturer le flux de l’appareil. (vous pouvez également utiliser une API audio héritée, telle que les Windows fonctions **waveInXxx** multimédias, pour capturer le flux de données à partir de l’appareil.)

si votre carte audio contient un périphérique de bouclage matériel, vous pouvez utiliser le panneau de configuration Windows multimédia, Mmsys.cpl, pour désigner l’appareil comme périphérique de capture par défaut. La procédure comporte trois étapes :

1.  Pour exécuter Mmsys.cpl, ouvrez une fenêtre d’invite de commandes et entrez la commande suivante :

    ```C++
    control mmsys.cpl,,1
    ```

    

    Vous pouvez également exécuter Mmsys.cpl en cliquant avec le bouton droit sur l’icône de haut-parleur dans la zone de notification, située sur le côté droit de la barre des tâches, puis en sélectionnant **périphériques d’enregistrement**.

2.  Une fois la fenêtre de Mmsys.cpl ouverte, cliquez avec le bouton droit n’importe où dans la liste des périphériques d’enregistrement et vérifiez que l’option **afficher les périphériques désactivés** est cochée. (Dans le cas contraire, si le périphérique de bouclage est désactivé, il n’apparaîtra pas dans la liste.)
3.  Parcourez la liste des périphériques d’enregistrement pour localiser le périphérique de bouclage (s’il existe). Si le périphérique de bouclage est désactivé, activez-le en cliquant avec le bouton droit sur l’appareil et en cliquant sur **activer**.
4.  Enfin, pour sélectionner le périphérique de bouclage comme périphérique de capture par défaut, cliquez avec le bouton droit sur l’appareil, puis cliquez sur **définir en tant qu’appareil par défaut**.

WASAPI prend en charge l’enregistrement de bouclage, que le matériel audio contienne ou non un périphérique de bouclage, ou que l’utilisateur ait activé l’appareil.

Windows Vista fournit la gestion des droits numériques (DRM). Les fournisseurs de contenu s’appuient sur DRM pour protéger leur musique propriétaire ou tout autre contenu contre toute copie non autorisée et toute autre utilisation illégale. De même, un pilote audio approuvé n’autorise pas un périphérique de bouclage à capturer des flux numériques contenant du contenu protégé. Windows Vista autorise uniquement les pilotes approuvés à lire du contenu protégé. pour plus d’informations sur les pilotes approuvés et la DRM, consultez la documentation Windows DDK.

Le bouclage WASAPI contient la combinaison de tout le son en cours de lecture, quelle que soit la session des services Terminal Server à partir de laquelle le son provient. Par exemple, vous pouvez exécuter un client de bouclage dans un service s’exécutant dans la session 0 et capturer l’audio de toutes les sessions utilisateur, ainsi que le son lu à partir de la session 0.

Bureau à distance permet de rediriger l’audio vers le client. Cela est implémenté par la création de nouveaux périphériques audio qui apparaissent uniquement pour cette session.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Gestion de flux](stream-management.md)
</dt> </dl>

 

 



