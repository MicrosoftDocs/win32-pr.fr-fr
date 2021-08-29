---
description: Cet exemple utilise les API audio de base pour capturer un flux vocal de haute qualité. l’exemple prend en charge l’annulation de l’écho acoustique et le traitement du tableau de microphone à l’aide de l’DMO AEC, également appelé DSP de capture vocale, fourni par Microsoft.
ms.assetid: 932d3442-1beb-4938-9382-031c61cd9b05
title: AECMicArray
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5d7960a1ff3163b936af949d605e7782f8a09890741f99e022c37a0aadc57a2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120059119"
---
# <a name="aecmicarray"></a>AECMicArray

Cet exemple utilise les API audio de base pour capturer un flux vocal de haute qualité. l’exemple prend en charge l’annulation de l’écho acoustique et le traitement du tableau de microphone à l’aide de l’DMO AEC, également appelé DSP de capture vocale, fourni par Microsoft.

Cette rubrique contient les sections suivantes.

-   [Description](#description)
-   [Requirements](#requirements)
-   [Téléchargement de l’exemple](#downloading-the-sample)
-   [Génération de l'exemple](#building-the-sample)
-   [Exécution de l’exemple](#running-the-sample)
-   [Rubriques connexes](#related-topics)

## <a name="description"></a>Description

Cet exemple illustre les fonctionnalités suivantes.

-   [MMDevice](mmdevice-api.md) pour l’énumération et la sélection des appareils multimédias.
-   [WASAPI](wasapi.md) pour les opérations de gestion de flux, telles que le démarrage et l’arrêt du flux, le basculement de flux.
-   [DeviceTopology](devicetopology-api.md) pour l’énumération des adaptateurs audio.
-   [EndpointVolume](endpointvolume-api.md) contrôle des niveaux de volume des [sessions audio](audio-sessions.md).

## <a name="requirements"></a>Configuration requise



| Produit                                                        | Version                     |
|----------------------------------------------------------------|-----------------------------|
| [SDK Windows](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | Windows Vista ou version ultérieure ;      |
| Visual Studio                                                  | 2005 (éditions non-Express) |



 

## <a name="downloading-the-sample"></a>Téléchargement de l’exemple

Cet exemple est disponible aux emplacements suivants.



| Emplacement    | Chemin d’accès/URL                                                                                     |
|-------------|----------------------------------------------------------------------------------------------|
| Kit de développement logiciel (SDK) Windows | \\Program Files \\ Microsoft sdk \\ Windows \\ v 7.0 \\ samples \\ \\ Audio Multimedia \\ AECMicArray \\ ... |



 

## <a name="building-the-sample"></a>Génération de l'exemple

Pour générer l’exemple AecSDKDemo, procédez comme suit :

1.  Ouvrez une fenêtre de commande du kit de développement logiciel (SDK).
2.  Tapez **CD% MSSDK% \\ Setup**.
3.  Exécutez VCIntegrate.exe.

    À partir de ce point, les fenêtres de commande auront les paramètres d’environnement appropriés pour créer une application qui tire parti du kit de développement logiciel (SDK).

4.  Générez l’exemple.

## <a name="running-the-sample"></a>Exécution de l'exemple

Si vous générez l’application de démonstration avec succès, un fichier exécutable, AecSDKDemo.exe est généré. Pour l’exécuter, tapez `AecSDKDemo` dans une fenêtre de commande suivie d’arguments obligatoires ou facultatifs, comme décrit ci-dessous.

`AecSDKDemo -out mic_out.pcm -mod system_mode [-option value] `

Le tableau suivant indique les arguments.

| Argument  | Description                                                                                                                           |
|-----------|---------------------------------------------------------------------------------------------------------------------------------------|
| -out      | Obligatoire. Spécifie le nom du fichier de sortie.                                                                                                 |
| -mod      | Obligatoire. Spécifie le mode système de capture vocale. pour plus d’informations, reportez-vous à la section « configuration de la DMO de capture vocale » dans le fichier lisezmoi de l’exemple. |
| -Feature     | Facultatif. Active le mode de fonctionnalité sur (1) ou sur OFF (0).                                                                                       |
| -NS       | Facultatif. Désactive la suppression du bruit sur (1) ou sur OFF (0). Le mode de fonctionnalité doit être activé pour pouvoir être spécifié.                                     |
| -AGC      | Facultatif. Active Digital AGC sur (1) ou sur OFF (0). Le mode de fonctionnalité doit être activé pour pouvoir être spécifié.                                           |
| -cntrclip | Facultatif. Active ou désactive le découpage du Centre (0). Le mode de fonctionnalité doit être activé pour pouvoir être spécifié.                                       |
| -spkdev   | Facultatif. Spécifie l’index de l’appareil de l’intervenant. S’il n’est pas spécifié, l’utilisateur est invité à sélectionner.                                         |
| -micdev   | Facultatif. Spécifie l’index du périphérique microphone. S’il n’est pas spécifié, l’utilisateur est invité à sélectionner.                                      |
| -Duration | Facultatif. Spécifie la durée d’exécution de l’application.                                                                                    |



 

Cet exemple d’application ne joue aucun signal. pour exécuter correctement la démonstration pour les modes activés AEC (mode 0 et 4), les utilisateurs doivent lire certains signaux audio via le même périphérique d’orateur spécifié pour le DMO (c’est-à-dire l’appareil spécifié par l’option « -spkdev »), ce qui simule la voix extrême dans un scénario de conversation bidirectionnel. Les utilisateurs peuvent utiliser n’importe quel joueur pour lire des signaux audio. s’il n’y a aucun flux de rendu actif sur le périphérique de l’intervenant sélectionné, le processus de DMO ne peut pas être traité.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Exemples de SDK qui utilisent les API audio principales](sdk-samples-that-use-the-core-audio-apis.md)
</dt> </dl>

 

 



