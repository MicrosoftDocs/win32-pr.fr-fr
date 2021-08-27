---
description: Cet exemple d’application utilise les API audio de base pour afficher les données audio sur un périphérique de sortie, spécifié par l’utilisateur.
ms.assetid: 92e644be-df8b-415d-ac8e-c0c30c85f844
title: RenderSharedEventDriven
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aafab0e2a9d073a963653ebaf53106ee737327a516df300a810632b0822c26f1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120109408"
---
# <a name="rendersharedeventdriven"></a>RenderSharedEventDriven

Cet exemple d’application utilise les API audio de base pour afficher les données audio sur un périphérique de sortie, spécifié par l’utilisateur. Cet exemple illustre la mise en mémoire tampon pilotée par les événements pour un client de rendu en mode partagé. Pour un flux en mode partagé, le client partage la mémoire tampon du point de terminaison avec le moteur audio.

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
-   WASAPI pour les opérations de gestion de flux.

## <a name="requirements"></a>Configuration requise



| Produit                                                        | Version   |
|----------------------------------------------------------------|-----------|
| [SDK Windows](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | Windows 7 |
| Visual Studio                                                  | 2008      |



 

## <a name="downloading-the-sample"></a>Téléchargement de l’exemple

Cet exemple est disponible aux emplacements suivants.



| Emplacement    | Chemin d’accès/URL                                                                                                 |
|-------------|----------------------------------------------------------------------------------------------------------|
| Kit de développement logiciel (SDK) Windows | \\Program Files \\ Microsoft sdk \\ Windows \\ v 7.0 \\ samples \\ \\ Audio Multimedia \\ RenderSharedEventDriven \\ ... |



 

## <a name="building-the-sample"></a>Génération de l'exemple

Pour générer l’exemple RenderSharedEventDriven, procédez comme suit :

1.  ouvrez l’interpréteur de commandes pour le SDK Windows et accédez au répertoire d’exemple RenderSharedEventDriven.
2.  exécutez la commande `start WASAPIRenderSharedEventDriven.sln` dans le répertoire RenderSharedEventDriven pour ouvrir le projet WASAPIRenderSharedEventDriven dans la fenêtre Visual Studio.
3.  À partir de la fenêtre, sélectionnez la configuration de la solution **Debug** ou **Release** , sélectionnez le menu **générer** dans la barre de menus, puis sélectionnez l’option **générer** . si vous n’ouvrez pas Visual Studio à partir du shell CMD pour le kit de développement logiciel (sdk), Visual Studio n’aura pas accès à l’environnement de génération du kit de développement logiciel (sdk). Dans ce cas, l’exemple n’est pas généré, sauf si vous définissez explicitement la variable d’environnement MSSdk, qui est utilisée dans le fichier projet, WASAPIRenderSharedEventDriven. vcproj.

## <a name="running-the-sample"></a>Exécution de l'exemple

Si vous générez l’application de démonstration avec succès, un fichier exécutable, WASAPIRenderSharedEventDriven.exe, est généré. Pour l’exécuter, tapez `WASAPIRenderSharedEventDriven` dans une fenêtre de commande suivie d’arguments obligatoires ou facultatifs. L’exemple suivant montre comment exécuter l’exemple en spécifiant la durée de lecture sur le périphérique multimédia par défaut.

`WASAPIRenderSharedEventDriven.exe -d 20 -multimedia`

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

RenderSharedEventDriven illustre la mise en mémoire tampon pilotée par les événements. L’exemple montre comment effectuer les opérations suivantes :

-   Instanciez un client audio, configurez-le pour qu’il s’exécute en mode exclusif et activez la mise en mémoire tampon pilotée par les événements en définissant l’indicateur **AUDCLNT \_ STREAMFLAGS \_ EventCallback suivante** dans l’appel à [**IAudioClient :: Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize).
-   Associez le client aux exemples qui sont prêts à être rendus en fournissant un handle d’événement au système en appelant la méthode [**IAudioClient :: SetEventHandle**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-seteventhandle) .
-   Créez un thread de rendu pour effectuer des exemples de traitement à partir du moteur audio.
-   Vérifiez le format Mix du point de terminaison de l’appareil pour déterminer si les exemples peuvent être rendus. Si l’appareil ne prend pas en charge le format Mix, les données sont converties en PCM.
-   Gérer le basculement de flux.

Après le début de la session de rendu et le démarrage du flux, le moteur audio signale le handle d’événement fourni pour notifier le client chaque fois qu’une mémoire tampon est prête pour le traitement du client. Les données audio peuvent également être traitées dans une boucle pilotée par une minuterie. Ce mode est illustré dans l’exemple [RenderSharedTimerDriven](rendersharedtimerdriven.md) .

Pour plus d’informations sur le rendu d’un flux, consultez [rendu d’un flux](rendering-a-stream.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Exemples de SDK qui utilisent les API audio principales](sdk-samples-that-use-the-core-audio-apis.md)
</dt> </dl>

 

 



