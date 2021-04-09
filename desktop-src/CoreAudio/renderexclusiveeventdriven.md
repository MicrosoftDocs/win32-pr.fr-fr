---
description: Cet exemple d’application utilise les API audio de base pour afficher les données audio sur un périphérique de sortie spécifié par l’utilisateur.
ms.assetid: 3a2e3fa6-2d6a-4ab0-a531-d1c968458e96
title: RenderExclusiveEventDriven
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d3b94fa423cd4d4e7dc7121e927696529bfadf9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104033706"
---
# <a name="renderexclusiveeventdriven"></a>RenderExclusiveEventDriven

Cet exemple d’application utilise les API audio de base pour afficher les données audio sur un périphérique de sortie spécifié par l’utilisateur. Cet exemple illustre la mise en mémoire tampon pilotée par les événements pour un client de rendu en mode exclusif. Pour un flux en mode exclusif, le client partage la mémoire tampon du point de terminaison avec le périphérique audio.

Cette rubrique contient les sections suivantes.

-   [Description](#description)
-   [Configuration requise](#requirements)
-   [Téléchargement de l’exemple](#downloading-the-sample)
-   [Génération de l'exemple](#building-the-sample)
-   [Exécution de l’exemple](#running-the-sample)
-   [Rubriques connexes](#related-topics)

## <a name="description"></a>Description

Cet exemple illustre les fonctionnalités suivantes.

-   [API MMDevice](mmdevice-api.md) pour l’énumération et la sélection des appareils multimédias.
-   WASAPI pour les opérations de gestion de flux.

## <a name="requirements"></a>Configuration requise



| Produit                                                        | Version   |
|----------------------------------------------------------------|-----------|
| [SDK Windows](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | Windows 7 |
| Visual Studio                                                  | 2008      |



 

## <a name="downloading-the-sample"></a>Téléchargement de l’exemple

Cet exemple est disponible aux emplacements suivants.



| Emplacement    | Chemin d’accès/URL                                                                                                    |
|-------------|-------------------------------------------------------------------------------------------------------------|
| Kit de développement logiciel (SDK) Windows | \\Program Files \\ Microsoft SDK \\ Windows \\ v 7.0 \\ exemples \\ multimédia \\ audio \\ RenderExclusiveEventDriven \\ ... |



 

## <a name="building-the-sample"></a>Génération de l'exemple

Pour générer l’exemple RenderExclusiveEventDriven, procédez comme suit :

1.  Ouvrez l’interpréteur de commandes pour le SDK Windows et accédez au répertoire d’exemple RenderExclusiveEventDriven.
2.  Exécutez la commande `start WASAPIRenderExclusiveEventDriven.sln` dans le répertoire RenderExclusiveEventDriven pour ouvrir le projet WASAPIRenderExclusiveEventDriven dans la fenêtre Visual Studio.
3.  À partir de la fenêtre, sélectionnez la configuration de la solution **Debug** ou **Release** , sélectionnez le menu **générer** dans la barre de menus, puis sélectionnez l’option **générer** . Si vous n’ouvrez pas Visual Studio à partir du shell CMD pour le kit de développement logiciel (SDK), Visual Studio n’aura pas accès à l’environnement de génération du kit de développement logiciel (SDK). Dans ce cas, l’exemple n’est pas généré, sauf si vous définissez explicitement la variable d’environnement MSSdk, qui est utilisée dans le fichier projet, WASAPIRenderExclusiveEventDriven. vcproj.

## <a name="running-the-sample"></a>Exécution de l'exemple

Si vous générez l’application de démonstration avec succès, un fichier exécutable, WASAPIRenderExclusiveEventDriven.exe, est généré. Pour l’exécuter, tapez `WASAPIRenderExclusiveEventDriven` dans une fenêtre de commande suivie d’arguments obligatoires ou facultatifs. L’exemple suivant montre comment exécuter l’exemple en spécifiant la durée de lecture sur le périphérique multimédia par défaut.

`WASAPIRenderExclusiveEventDriven.exe -d 20 -multimedia`

Le tableau suivant indique les arguments.

| Argument        | Description                                                |
|-----------------|------------------------------------------------------------|
| -?              | Affiche l’aide.                                                |
| -H              | Affiche l’aide.                                                |
| -f              | Fréquence des vagues sinusoïdales en Hz.                                 |
| -l              | Latence du rendu audio en millisecondes.                      |
| -d              | Durée de l’onde sinusoïdale en secondes.                             |
| -M              | Désactive l’utilisation de MMCSS.                                 |
| -Console        | Utilisez l’appareil de la console par défaut.                            |
| -Communications | Utilisez l’appareil de communication par défaut.                      |
| -multimédia     | Utilisez l’appareil multimédia par défaut.                         |
| -point de terminaison       | Utilisez l’identificateur de point de terminaison spécifié dans la valeur de commutateur. |



 

Si l’application est exécutée sans arguments, elle énumère les périphériques disponibles et invite l’utilisateur à sélectionner un appareil pour la session de rendu. Une fois que l’utilisateur a spécifié un appareil, l’application affiche une vague sinusoïdale à 440 Hz pendant 10 secondes. Ces valeurs peuvent être modifiées en spécifiant des valeurs de commutateur-f et-d.

L’exemple RenderExclusiveEventDriven illustre la mise en mémoire tampon pilotée par les événements. L’exemple montre comment effectuer les opérations suivantes :

-   Instanciez un client audio, configurez-le pour qu’il s’exécute en mode exclusif et activez la mise en mémoire tampon pilotée par les événements en définissant l’indicateur **AUDCLNT \_ STREAMFLAGS \_ EventCallback suivante** dans l’appel à [**IAudioClient :: Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize).
-   Associez le client aux exemples qui sont prêts à être rendus en fournissant un handle d’événement au système en appelant la méthode [**IAudioClient :: SetEventHandle**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-seteventhandle) .
-   Créez un thread de rendu pour traiter des exemples à partir du moteur audio.
-   Alignez correctement les mémoires tampons sur une limite de 128 octets avant de les envoyer à l’appareil. Cela s’effectue en ajustant la périodicité du moteur.
-   Vérifiez le format Mix du point de terminaison de l’appareil pour déterminer si les exemples peuvent être rendus. Si l’appareil ne prend pas en charge le format Mix, les données sont converties en PCM.
-   Gérer le basculement de flux.

Après le début de la session de rendu et le démarrage du flux, le moteur audio signale le handle d’événement fourni pour notifier le client chaque fois qu’une mémoire tampon est prête pour le traitement du client. Les données audio peuvent également être traitées dans une boucle pilotée par une minuterie. Ce mode est illustré dans l’exemple [RenderExclusiveTimerDriven](renderexclusivetimerdriven.md) .

Pour plus d’informations sur le rendu d’un flux, consultez [rendu d’un flux](rendering-a-stream.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Exemples de SDK qui utilisent les API audio principales](sdk-samples-that-use-the-core-audio-apis.md)
</dt> </dl>

 

 



