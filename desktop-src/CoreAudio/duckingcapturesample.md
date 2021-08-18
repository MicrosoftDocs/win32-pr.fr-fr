---
description: Cet exemple d’application montre l’ouverture et la fermeture de flux de communication et la mise en place d’événements de canard qu’une application peut atteindre pour implémenter l’atténuation du flux.
ms.assetid: 9a2131b2-ec4a-492a-a277-bd26ec8d67e5
title: DuckingCaptureSample
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76515f9d20e31bf4583b715e09da38c29bfdac34f6c975087f64bf2617696542
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119018457"
---
# <a name="duckingcapturesample"></a>DuckingCaptureSample

Cet exemple d’application montre l’ouverture et la fermeture de flux de communication et la mise en place d’événements de canard qu’une application peut atteindre pour implémenter l’atténuation du flux. Cette application implémente un client de conversation qui utilise des API audio de base pour lire les données audio à partir d’un périphérique de communication et les lire sur le périphérique de sortie.

Cette rubrique contient les sections suivantes.

-   [Description](#description)
-   [Requirements](#requirements)
-   [Téléchargement de l’exemple](#downloading-the-sample)
-   [Génération de l'exemple](#building-the-sample)
-   [Exécution de l’exemple](#running-the-sample)
-   [Rubriques connexes](#related-topics)

## <a name="description"></a>Description

Cet exemple illustre les fonctionnalités suivantes.

-   [API MMDevice](mmdevice-api.md) pour l’énumération et la sélection des appareils multimédias.
-   [WASAPI](wasapi.md) permettant d’accéder à la capture de communications et à l’appareil de rendu, aux opérations de gestion de flux et à la gestion des événements de canard.
-   [API Wave](/previous-versions//ms713499(v=vs.85)) permettant d’accéder au périphérique de communication et de capturer l’entrée audio.

## <a name="requirements"></a>Configuration requise



| Produit                                                        | Version   |
|----------------------------------------------------------------|-----------|
| [SDK Windows](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | Windows 7 |
| Visual Studio 2008                                             |           |



 

## <a name="downloading-the-sample"></a>Téléchargement de l’exemple

Cet exemple est disponible aux emplacements suivants.



| Emplacement    | Chemin d’accès/URL                                                                                              |
|-------------|-------------------------------------------------------------------------------------------------------|
| Kit de développement logiciel (SDK) Windows | \\Program Files \\ Microsoft sdk \\ Windows \\ v 7.0 \\ samples \\ \\ Audio Multimedia \\ DuckingCaptureSample \\ ... |



 

## <a name="building-the-sample"></a>Génération de l'exemple

Pour générer l’exemple DuckingCaptureSample, procédez comme suit :

1.  ouvrez DuckingCaptureSample. sln dans Visual Studio 2008.
2.  À partir de la fenêtre, sélectionnez la configuration de la solution **Debug** ou **Release** , sélectionnez le menu **générer** dans la barre de menus, puis sélectionnez l’option **générer** . si vous n’ouvrez pas Visual Studio à partir du shell CMD pour le kit de développement logiciel (sdk), Visual Studio n’aura pas accès à l’environnement de génération du kit de développement logiciel (sdk). Dans ce cas, l’exemple n’est pas généré, sauf si vous définissez explicitement la variable d’environnement MSSdk, qui est utilisée dans le fichier projet, DuckingCaptureSample. vcproj.

## <a name="running-the-sample"></a>Exécution de l'exemple

Si vous générez l’application avec succès, un fichier exécutable, DuckingCaptureSample.exe, est généré. Pour l’exécuter, sélectionnez **Démarrer le débogage** ou **Démarrer sans débogage** dans le menu **Déboguer** ou tapez `DuckingCaptureSample` dans une fenêtre de commande.

DuckingCaptureSample fournit à l’utilisateur deux implémentations pour capturer l’audio de l’appareil de console par défaut : les API WASAPI et Wave. Pour démarrer une session de capture, sélectionnez un mode, puis cliquez sur **Démarrer** dans l’interface utilisateur de l’application. Pour mettre fin à la session, cliquez sur **arrêter**. En fonction de l’appareil spécifié par l’utilisateur (entrée ou sortie), l’application utilise l’API MMDevice pour obtenir une référence au périphérique de communication de rendu ou de capture par défaut. Une fois que l’utilisateur a démarré une session de conversation, l’application effectue les tâches suivantes :

-   Crée et initialise un client audio en mode piloté par les événements.
-   Associe le client au handle d’événement qui signale que les exemples sont prêts pour la capture ou le rendu.
-   Configure un client de capture et un client de rendu pour le transport.
-   Crée le thread de conversation et démarre le moteur audio.

Pour la capture de données audio, avec chaque passe de traitement, l’exemple utilise le client de capture pour obtenir la quantité totale de données capturées disponibles dans la mémoire tampon, lire des données à partir de l’appareil d’entrée par défaut et libérer le paquet et rendre le tampon disponible pour lire le jeu suivant de données capturées.

Pour le rendu, l’application détermine la quantité de données mises en file d’attente dans la mémoire tampon du point de terminaison de capture. En conséquence, il écrit dans la mémoire tampon et libère la mémoire tampon en vue de la réussite du traitement suivant, jusqu’à ce que toutes les données aient été écrites. Pour le rendu, les trames silencieuses sont préinscrites pour empêcher le moteur audio de se lancer au démarrage. DuckingCaptureSample indique également comment masquer le flux de rendu à partir du mélangeur de volume.

Pour plus d’informations sur la fonctionnalité d’atténuation de flux, consultez [utilisation d’un appareil de communication](using-the-communication-device.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Exemples de SDK qui utilisent les API audio principales](sdk-samples-that-use-the-core-audio-apis.md)
</dt> </dl>

 

 
