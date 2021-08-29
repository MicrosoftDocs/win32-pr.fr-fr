---
description: Cet exemple d’application utilise les API audio de base pour capturer des données audio à partir d’un périphérique d’entrée spécifié par l’utilisateur et les écrit dans un fichier. wav portant un nom unique dans le répertoire actif. Cet exemple illustre la mise en mémoire tampon pilotée par les événements.
ms.assetid: 6ff3bc23-550e-41b7-b37c-35d552b29e20
title: CaptureSharedEventDriven
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d8d71739c6e308ee9be79263dc5cdd5bbc693775722f14a35567b6a70138c8e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119758979"
---
# <a name="capturesharedeventdriven"></a>CaptureSharedEventDriven

Cet exemple d’application utilise les API audio de base pour capturer des données audio à partir d’un périphérique d’entrée spécifié par l’utilisateur et les écrit dans un fichier. wav portant un nom unique dans le répertoire actif. Cet exemple illustre la mise en mémoire tampon pilotée par les événements.

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
-   [WASAPI](wasapi.md) pour les opérations de gestion de flux, telles que le démarrage et l’arrêt du flux et le basculement de flux.

## <a name="requirements"></a>Configuration requise



| Produit                                                        | Version   |
|----------------------------------------------------------------|-----------|
| [SDK Windows](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | Windows 7 |
| Visual Studio                                                  | 2008      |



 

## <a name="downloading-the-sample"></a>Téléchargement de l’exemple

Cet exemple est disponible aux emplacements suivants.



| Emplacement    | Chemin d’accès/URL                                                                                                  |
|-------------|-----------------------------------------------------------------------------------------------------------|
| Kit de développement logiciel (SDK) Windows | \\Program Files \\ Microsoft sdk \\ Windows \\ v 7.0 \\ samples \\ \\ Audio Multimedia \\ CaptureSharedEventDriven \\ ... |



 

## <a name="building-the-sample"></a>Génération de l'exemple

Pour générer l’exemple CaptureSharedEventDriven, procédez comme suit :

1.  ouvrez l’interpréteur de commandes pour le SDK Windows et accédez au répertoire d’exemple CaptureSharedEventDriven.
2.  exécutez la commande `start WASAPICaptureSharedEventDriven.sln` dans le répertoire CaptureSharedEventDriven pour ouvrir le projet WASAPICaptureSharedEventDriven dans la fenêtre Visual Studio.
3.  À partir de la fenêtre, sélectionnez la configuration de la solution **Debug** ou **Release** , sélectionnez le menu **générer** dans la barre de menus, puis sélectionnez l’option **générer** . si vous n’ouvrez pas Visual Studio à partir du shell CMD pour le kit de développement logiciel (sdk), Visual Studio n’aura pas accès à l’environnement de génération du kit de développement logiciel (sdk). Dans ce cas, l’exemple n’est pas généré, sauf si vous définissez explicitement la variable d’environnement MSSdk, qui est utilisée dans le fichier projet, WASAPICaptureSharedEventDriven. vcproj.

## <a name="running-the-sample"></a>Exécution de l'exemple

Si vous générez l’application de démonstration avec succès, un fichier exécutable, WASAPICaptureSharedEventDriven.exe, est généré. Pour l’exécuter, tapez `WASAPICaptureSharedEventDriven` dans une fenêtre de commande suivie d’arguments obligatoires ou facultatifs. L’exemple suivant montre comment exécuter l’exemple en spécifiant la durée de capture sur le périphérique multimédia par défaut.

`WASAPICaptureSharedEventDriven.exe -d 20 -multimedia`

Le tableau suivant indique les arguments.

| Argument        | Description                                                |
|-----------------|------------------------------------------------------------|
| -?              | Affiche l’aide.                                                |
| -H              | Affiche l’aide.                                                |
| -l              | Latence de capture audio en millisecondes.                     |
| -d              | Durée de capture audio en secondes.                         |
| -M              | Désactive l’utilisation de MMCSS.                                 |
| -Console        | Utilisez l’appareil de la console par défaut.                            |
| -Communications | Utilisez l’appareil de communication par défaut.                      |
| -multimédia     | Utilisez l’appareil multimédia par défaut.                         |
| -point de terminaison       | Utilisez l’identificateur de point de terminaison spécifié dans la valeur de commutateur. |



 

Si l’application est exécutée sans arguments, elle énumère les périphériques disponibles et invite l’utilisateur à sélectionner un appareil pour la session de capture. La console, la communication et les périphériques multimédias par défaut sont répertoriés suivis des appareils et des identificateurs de point de terminaison. Si aucune durée n’est spécifiée, le flux audio de l’appareil spécifié est capturé pendant 10 secondes. L’application écrit les données capturées dans un fichier. wav portant un nom unique.

CaptureSharedEventDriven illustre la mise en mémoire tampon pilotée par les événements. Le client audio instancié pour cet exemple est configuré pour s’exécuter en mode partagé et le traitement du client de la mémoire tampon audio est rendu déclenché par l’événement en définissant l’indicateur **AUDCLNT \_ STREAMFLAGS \_ EventCallback suivante** dans l’appel à [**IAudioClient :: Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize). L’exemple montre comment le client doit fournir un handle d’événement au système en appelant la méthode [**IAudioClient :: SetEventHandle**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-seteventhandle) . Après le début de la session de capture et le démarrage du flux, le moteur audio signale le handle d’événement fourni pour notifier le client chaque fois qu’une mémoire tampon est prête à être traitée par le client. Les données audio peuvent également être traitées dans une boucle pilotée par une minuterie. Ce mode est demostrated dans l’exemple [CaptureSharedTimerDriven](capturesharedtimerdriven.md) .

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Exemples de SDK qui utilisent les API audio principales](sdk-samples-that-use-the-core-audio-apis.md)
</dt> </dl>

 

 



