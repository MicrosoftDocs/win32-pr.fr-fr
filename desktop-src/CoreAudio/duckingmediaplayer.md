---
description: Cet exemple d’application illustre l’atténuation du flux en implémentant un lecteur multimédia qui montre le comportement d’atténuation par défaut fourni par le système, qui ne permet pas d’encadrer des événements et implémente une gestion personnalisée lors de la réception d’événements.
ms.assetid: 667c8751-1d17-4b59-8ced-ed5f0c333ae9
title: DuckingMediaPlayer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f86952f1aa7b81c9a7dc711f0c4f36fc8531bd63
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/03/2021
ms.locfileid: "106539380"
---
# <a name="duckingmediaplayer"></a>DuckingMediaPlayer

Cet exemple d’application illustre l’atténuation du flux en implémentant un lecteur multimédia qui montre le comportement d’atténuation par défaut fourni par le système, qui ne permet pas d’encadrer des événements et implémente une gestion personnalisée lors de la réception d’événements. Cet exemple doit être utilisé avec [DuckingCaptureSample](duckingcapturesample.md). Pour plus d’informations sur l’utilisation de la canard ou de l’atténuation de flux, consultez l’expérience de l’utilisation de l' [environnement](stream-attenuation.md).

Cette rubrique contient les sections suivantes.

-   [Description](#description)
-   [Configuration requise](#requirements)
-   [Téléchargement de l’exemple](#downloading-the-sample)
-   [Génération de l'exemple](#building-the-sample)
-   [Exécution de l’exemple](#running-the-sample)
-   [Rubriques connexes](#related-topics)

## <a name="description"></a>Description

Cet exemple illustre les fonctionnalités suivantes.

-   DirectShow pour lire un fichier multimédia.
-   [WASAPI](wasapi.md) pour la gestion des flux et la gestion des événements de canard.

## <a name="requirements"></a>Configuration requise



| Produit                                                        | Version   |
|----------------------------------------------------------------|-----------|
| [SDK Windows](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | Windows 7 |
| Visual Studio                                                  | 2008      |



 

## <a name="downloading-the-sample"></a>Téléchargement de l’exemple

Cet exemple est disponible aux emplacements suivants.



| Emplacement    | Chemin d’accès/URL                                                                                            |
|-------------|-----------------------------------------------------------------------------------------------------|
| Kit de développement logiciel (SDK) Windows | \\Program Files \\ Microsoft SDK \\ Windows \\ v 7.0 \\ exemples \\ multimédia \\ audio \\ DuckingMediaPlayer \\ ... |



 

## <a name="building-the-sample"></a>Génération de l'exemple

Pour générer l’exemple DuckingMediaPlayer, procédez comme suit :

1.  Ouvrez DuckingMediaPlayer. sln dans Visual Studio 2008.
2.  À partir de la fenêtre, sélectionnez la configuration de la solution **Debug** ou **Release** , sélectionnez le menu **générer** dans la barre de menus, puis sélectionnez l’option **générer** . Si vous n’ouvrez pas Visual Studio à partir du shell CMD pour le kit de développement logiciel (SDK), Visual Studio n’aura pas accès à l’environnement de génération du kit de développement logiciel (SDK). Dans ce cas, l’exemple n’est pas généré, sauf si vous définissez explicitement la variable d’environnement MSSdk, qui est utilisée dans le fichier projet, DuckingMediaPlayer. vcproj.

## <a name="running-the-sample"></a>Exécution de l'exemple

Si vous générez l’application avec succès, un fichier exécutable, DuckingMediaPlayer.exe, est généré. Pour l’exécuter, sélectionnez **Démarrer le débogage** ou **Démarrer sans débogage** dans le menu **Déboguer** ou tapez `DuckingMediaPlayer` dans une fenêtre de commande.

Pour voir une démonstration de l’un des canards, vous devez exécuter DuckingMediaPlayer et DuckingCaptureSample simultanément. DuckingCaptureSample ouvre un flux de communication et signale au système qu’il doit générer un événement de canard. Le DuckingMediaPlayer est averti par le système lorsqu’un événement de canard se produit et que le lecteur multimédia effectue l’action demandée par l’utilisateur.

Pour désactiver le comportement de l’encanardment :

1.  Dans la fenêtre DuckingCaptureSample, sélectionnez **utiliser l’appareil d’entrée par défaut**, puis cliquez sur **Démarrer** pour démarrer une session de capture à partir de l’appareil de communication.
2.  Sur la DuckingMediaPlayer, sélectionnez un fichier multimédia à lire, puis spécifiez l’option de l’option de l’encadrement comme **refus de** l’encadrer.

Notez que le fichier multimédia est lu sans interruption. Les événements générés par le système lors de l’ouverture du flux de communication sont ignorés.

Pour illustrer le comportement de l’encodeur par défaut fourni par le système, procédez comme suit :

1.  Sélectionnez l’option **sons** dans le panneau de configuration. Sous l’onglet **communications** , sélectionnez **réduire le volume des autres sons de 80%**.
2.  Dans la fenêtre DuckingCaptureSample, sélectionnez **utiliser l’appareil d’entrée par défaut**, puis cliquez sur **Démarrer** pour démarrer une session de capture à partir de l’appareil de communication.
3.  Sur le DuckingMediaPlayer, sélectionnez un fichier multimédia à lire, sans choisir l’une des options d’encanardment.
4.  Dans la fenêtre DuckingCaptureSample, cliquez sur **arrêter** pour arrêter le flux de communication.

Notez que lorsque DuckingCaptureSample ouvre le flux de communication, le fichier multimédia joué par DuckingMediaPlayer est lu sans interruption, mais le niveau de volume est abaissé. Lorsque la session de communication est arrêtée, le volume est réinitialisé sur le paramètre d’origine. Ce comportement d’atténuation de flux est le comportement de mise en œuvre par défaut implémenté par le système.

Pour afficher un comportement de canardment personnalisé implémenté par le lecteur multimédia :

1.  Dans la fenêtre DuckingCaptureSample, sélectionnez **utiliser l’appareil d’entrée par défaut**, puis cliquez sur **Démarrer** pour démarrer une session de capture à partir de l’appareil de communication.
2.  Sur le DuckingMediaPlayer, sélectionnez un fichier multimédia à lire et spécifiez l’option de mise en forme en tant que mise en **pause sur le canard**.
3.  Dans la fenêtre DuckingCaptureSample, cliquez sur **arrêter** pour arrêter le flux de communication.

Notez que lorsque DuckingCaptureSample ouvre le flux de communication, le fichier multimédia lu par DuckingMediaPlayer est suspendu. La lecture reprend lorsque la session de communication est arrêtée. Ce comportement d’atténuation du flux est le comportement de l’enchaînement implémenté par le lecteur multimédia.

DuckingMediaPlayer montre également comment intégrer le contrôle du volume pour chaque application avec le mélangeur de volume.

Pour plus d’informations sur la fonctionnalité d’atténuation de flux, consultez l’expérience de l’utilisation de l' [environnement par défaut](stream-attenuation.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Exemples de SDK qui utilisent les API audio principales](sdk-samples-that-use-the-core-audio-apis.md)
</dt> </dl>

 

 



