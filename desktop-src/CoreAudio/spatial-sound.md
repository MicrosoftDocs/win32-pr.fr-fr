---
description: le son spatial microsoft est la solution au niveau de la plate-forme de microsoft pour la prise en charge des sons spatiaux sur Xbox, Windows et HoloLens 2, ce qui permet l’entourage et l’élévation (au-dessus ou en dessous de l’écouteur) des signaux audio.
ms.assetid: 4F962F1A-CA4A-4018-BA97-516EA3519650
title: Son spatial pour les développeurs
ms.custom: contperf-fy21q1
ms.topic: article
ms.date: 09/18/2020
ms.openlocfilehash: 361b45ab015f9604d2fca743714b6e6868635d2f858c22fa7e107234c66bd656
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120088339"
---
# <a name="spatial-sound-for-developers"></a>Son spatial pour les développeurs
> [!Note] 
> Cette documentation est destinée aux développeurs. Pour obtenir la prise en charge par l’utilisateur final de l’activation du son spatial sur votre appareil, consultez [Comment activer le son spatial dans Windows 10](https://support.microsoft.com/help/4563140/how-to-turn-on-spatial-sound-in-windows-10).

le son spatial microsoft est la solution au niveau de la plate-forme de microsoft pour la prise en charge des sons spatiaux sur Xbox, Windows et HoloLens 2, ce qui permet l’entourage et l’élévation (au-dessus ou en dessous de l’écouteur) des signaux audio. le son Spatial peut être utilisé par les applications Windows desktop (Win32) et les applications plateforme Windows universelle (UWP) sur les plateformes prises en charge. Les API de son spatial permettent aux développeurs de créer des objets audio qui émettent du son à partir de positions dans l’espace 3D. Les objets audio dynamiques vous permettent d’émettre du son à partir d’une position arbitraire dans l’espace, qui peut changer au fil du temps. Vous pouvez également spécifier que les objets audio émettent des sons à partir de l’un des 17 canaux statiques prédéfinis (8.1.4.4) qui peuvent représenter des intervenants réels ou virtualisés. Le format de sortie réel est sélectionné par l’utilisateur et peut être extrait des implémentations de son spatial Microsoft. l’audio sera présenté aux orateurs, casques et récepteurs Home Cinema existants, sans qu’il soit nécessaire de modifier le code ou le contenu. la plateforme prend entièrement en charge l’encodage Dolby Atmos en temps réel pour les sorties casque HDMI et stéréo, DTS : X pour les écouteurs et l’encodage Windows Sonic pour casque pour les casques stéréo. Enfin, les applications Microsoft spatiales sont conformes à la stratégie de mixage du système et leur contenu audio est également mélangé à des applications non spatialement sensibles. La prise en charge du son spatial Microsoft est également intégrée dans Media Foundation ; les applications qui utilisent Media Foundation peuvent lire du contenu Dolby Atmos sans implémentation supplémentaire.

Le son spatial avec le son spatial Microsoft prend en charge les téléviseurs, les théâtres et les barres de sons qui prennent en charge Dolby Atmos. le son Spatial peut également être utilisé avec n’importe quelle paire de casques que le consommateur peut posséder, avec l’audio rendu par la plateforme à l’aide de Windows Sonic pour casque, Dolby Atmos for Headphones ou du casque DTS : X.


## <a name="enabling-microsoft-spatial-sound"></a>Activation du son spatial Microsoft

Qu’il s’agisse d’un développeur ou d’un consommateur, un utilisateur doit activer le son spatial de Microsoft sur son appareil afin d’entendre un son spatial.

### <a name="windows"></a>Windows
sur Windows pc, cette opération est effectuée via la page propriétés pour un périphérique de sortie sonore donné. Dans le panneau de configuration du **son** , sélectionnez un périphérique de sortie, puis cliquez sur Propriétés de l' **appareil**. Dans la section **son spatial** de la page, si l’appareil prend en charge le son spatial, vous pouvez sélectionner l’un des formats disponibles dans la liste déroulante **format de son spatial** .

![activer le son spatial dans le panneau de contrôle du son](images/spatialsoundsettingswindows1.png)

Vous pouvez également activer le son spatial Microsoft en cliquant avec le bouton droit sur l’icône de **volume** dans la barre des tâches.

![activer le son spatial à partir de la barre des tâches](images/spatialsoundsettingswindows2.png)

### <a name="xbox-one"></a>Xbox One
sur Xbox One, les capacités de son Spatial Microsoft sont toujours disponibles pour le consommateur et sont activées via l’application Paramètres sous **général-> Volume & la sortie audio**.


![activer le son spatial sur Xbox 1 dans l’application paramètres ](images/audiosettingsbitstream.png)

Une fois que Dolby Atmos pour Home Theater est sélectionné comme « format de flux binaire », la prise en charge de ce format est vérifiée via les données EDID (Extended Display Identification) HDMI. Si l’appareil HDMI ne prend pas en charge le format, un message d’erreur s’affiche pour l’utilisateur. notez que si vous sélectionnez cette option pour la première fois, l’utilisateur doit télécharger l’application Dolby Access.

Si un format autre que « flux binaire » est sélectionné pour l' **Audio HDMI** , la liste déroulante **format de flux binaire** est désactivée.

![son spatial est désactivé sur Xbox 1 dans l’application paramètres ](images/audiosettingsplain.png)

sélectionnez Dolby Atmos for Headphones, le casque DTS : X ou Windows Sonic pour casque dans la liste déroulante **format du casque** sous **casque audio** .

![activer le son spatial pour les écouteurs sur Xbox 1 dans l’application paramètres ](images/audiosettingsheadphone.png)

Lorsque le son spatial Microsoft n’est pas disponible (par exemple, lors de la diffusion sur des enceintes stéréo d’ordinateur portable incorporées, ou si l’utilisateur n’a pas explicitement activé le son spatial Microsoft par-dessus), le nombre d’objets dynamiques disponibles renvoyés par [**ISpatialAudioClient :: GetMaxDynamicObjectCount**](/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioclient-getmaxdynamicobjectcount) à une application sera 0.

### <a name="hololens-2"></a>HoloLens 2

sur HoloLens 2, le son Spatial Microsoft est activé par défaut et utilise le déchargement matériel DSP conçu spécifiquement pour la Windows Sonic pour casque.

## <a name="microsoft-spatial-sound-and-audio-middleware"></a>Intergiciel Microsoft spatial et audio

De nombreux développeurs d’applications et de jeux utilisent des solutions de moteur de rendu audio tiers, qui incluent souvent des outils de création et d’audition sophistiqués. Microsoft a conclu un partenariat avec plusieurs de ces fournisseurs de solutions pour implémenter le son spatial dans leurs environnements de création existants. Cela signifie souvent que les API présentées ici sont extraites de la vue de l’application. ils sont encapsulés en tant que plug-ins de traitement de signal numérique (DSP) que l’application peut instancier, et que l’implémenteur audio de l’application peut utiliser pour mélanger à un lit de canal de son spatial Microsoft, une piste de mixage secondaire ou envoyer des voix individuelles aux plug-ins d’instance d’objet dynamique comme vous le souhaitez. Consultez votre fournisseur de solutions d’intergiciel audio pour leur niveau de prise en charge du son spatial Microsoft.

## <a name="microsoft-spatial-sound-for-audio-renderers"></a>Son spatial Microsoft pour les convertisseurs audio

de nombreux convertisseurs audio ciblent un point de terminaison de Windows WASAPI (audio Session API) [**IAudioClient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudioclient) , où l’application alimente les mémoires tampons de données audio en mode mixte et conformes au formatage sur un récepteur audio WASAPI. les mémoires tampons fournies sont ensuite consommées pour être mélangées avec d’autres clients, le traitement au niveau du système final et le rendu.

Les points de terminaison spatiaux de son spatial Microsoft sont implémentés en tant que [**ISpatialAudioClient**](/windows/desktop/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioclient), ce qui présente de nombreuses similarités avec **IAudioClient**. Il prend en charge les objets audio *statiques* formant un lit de canal, avec la prise en charge de canaux 8.1.4.4 (8 canaux autour de l’écouteur : gauche, droite, centré, côté gauche, côté droit, arrière-plan, arrière-plan, de droite et centre arrière ; 1 canal d’effets à faible fréquence ; 4 canaux au-dessus de l’écouteur Et il prend en charge les objets audio *dynamiques* , qui peuvent être positionnés arbitrairement dans l’espace 3D.

Le modèle général de codage de l’implémentation pour **ISpatialAudioClient** est le suivant :

-   Créer des objets audio statiques et/ou dynamiques.
-   Alimenter chaque image de la mémoire tampon audio de chaque objet afin que le système puisse la restituer.
-   Mettez à jour les positions 3D des objets dynamiques à la demande, aussi souvent (ou rarement) que l’application le souhaite.

Notez que le format de sortie actuel (haut-parleurs ou casque). Windows Sonic pour casque, Dolby Atmos ou le casque DTS : X) est extrait de l’implémentation ci-dessus : le développeur de l’application peut se concentrer sur le son spatial sans avoir besoin de pivoter en fonction du format. Les applications qui souhaitent que leur comportement divergent en fonction du format de sortie puissent interroger le format utilisé, mais l’abstraction signifie qu’une application n’est pas requise pour gérer ces formats.

## <a name="microsoft-spatial-sound-integration-with-audio-renderers"></a>Intégration du son spatial Microsoft avec les convertisseurs audio

Étant donné que [**ISpatialAudioClient**](/windows/desktop/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioclient) est un récepteur audio qui consomme des données, un convertisseur audio offre plusieurs options pour interagir avec et lui fournir des données audio. Il existe trois techniques d’intégration couramment utilisées (et pour les titres utilisant l’intergiciel audio, vous pouvez voir les plug-ins équivalents mis à disposition en fonction de ces options) :

-   **7.1.4 des pannes et de la parole de mastérisation**: les convertisseurs qui prennent déjà en charge les points de terminaison 7,1 peuvent choisir d’ajouter simplement la prise en charge des quatre canaux de hauteur supplémentaires pris en charge par la lit de canal statique **ISpatialAudioClient** . Tout panoramique de canal précédemment fait (probablement déjà en tirant parti des coordonnées x, y, z) peut être mis à jour pour inclure maintenant ces canaux de hauteur. Cela offre souvent le moins de perturbations pour les flux de travail de rendu et d’application audio, les signaux, les flux et le contrôle de combinaison. Au-dessus du casque, Notez que la combinaison d’applications complète sera spatiale, de sorte que même la musique stéréo peut être perçue comme « externalisée » de l’écouteur.
-   **Conserver le point de terminaison existant, et ajouter un bus 7.1.4 (et des pannes)**: certains titres peuvent choisir de gérer deux points de terminaison : leur point de terminaison WASAPI stéréo existant (pour le contenu « direct to Ears » non destiné à être spatial) et un lit de canal statique **ISpatialAudioClient** prenant en charge 7.1.4 (ou même jusqu’à 8.1.4.4). Bien entendu, la gestion des interactions entre deux mixages présente des défis supplémentaires pour les créateurs de contenu, bien que la synchronisation soit conservée, puisque les instances WASAPI et ISAC actives à un moment donné utilisent la même taille de mémoire tampon et l’horloge pour le traitement.
-   **Utilisez des objets de sons dynamiques pour certaines voix ou sous-mixages**: l’offre peut-être le positionnement le plus détaillé/précis, mais potentiellement la création d’une opacité mixte, cette technique implique l’utilisation d’objets audio dynamiques **ISpatialAudioClient** . Notez que les métadonnées plus la mémoire tampon audio sont remises au convertisseur, ce qui signifie que ces sons seront opaques au reste de la combinaison d’applications. En outre, étant donné qu’il y a un nombre limité d’objets sons dynamiques disponibles, le convertisseur devra envisager d’implémenter des techniques de hiérarchisation (élimination, colocalisation du son, fusion vers la vitre du canal statique, etc.). Les jeux ont souvent utilisé cette technique pour des sons « héros » individuels, tels qu’un hélicoptère qui se déplace au-dessus de l’écouteur.

Les convertisseurs peuvent également mélanger et faire correspondre entre ces approches.

## <a name="microsoft-spatial-sound-runtime-resource-implications"></a>Implications sur la ressource Microsoft spatial Sound Runtime

sur Windows et Xbox, le nombre de voix disponibles varie selon le format utilisé. Les formats Dolby Atmos prennent en charge 32 objets actifs au total (par conséquent, si un lit de canal 7.1.4 est en cours d’utilisation, 20 objets de son dynamique supplémentaires peuvent être actifs). Windows Sonic pour casque prend en charge le nombre total d’objets actifs 128, le canal des effets de faible fréquence (LFE) n’étant pas réellement compté comme un objet. ainsi, lorsqu’un lit de canal 8.1.4.4 est en cours d’utilisation, 112 objets de son dynamique peuvent être actifs.

pour les applications plateforme Windows universelle s’exécutant sur Xbox One consoles de jeu, le codage en temps réel (pour Dolby Atmos pour home theater, Dolby Atmos for Headphones, le casque DTS : X et Windows Sonic pour casque) est effectué dans le matériel sans coût d’uc.

| Format                       | Nombre maximal d’objets statiques (lit de canal) | Nombre maximal d’objets dynamiques <br> Xbox One | Nombre maximal d’objets dynamiques <br> Windows | Nombre maximal d’objets dynamiques <br> HoloLens 2
|------------------------------|----------------------------------|-------------------------------------------|------------------------------------------|------------------------------------------|
| Dolby Atmos (HDMI)           | 12 (7.1.4)                       | 20                                        | 20                                       | NA |
| Dolby Atmos (casque & enceintes intégrées)     | 17 (8.1.4.4)                     | 16                                        | 16                                       | NA |
| Casque DTS : X (casque) | 17 (8.1.4.4)        | 16                                        | 32                                      | NA |
| Windows Sonic pour casque | 17 (8.1.4.4)        | 15                                        | 112                                      | 31 |


Les applications doivent également prendre en compte les implications suivantes sur les ressources :

-   **Stockage de la bande passante/disc**: le contenu linéaire pré-créé vers 7.1.4 sera généralement plus grand que le contenu linéaire de 7,1 (bien que les codecs de perception tirent déjà souvent parti de la corrélation de canal pour que ce soit beaucoup moins que le nombre de 50% de données audio plus réelles)
-   **Autres coûts de traitement de signal numérique**: certains effets globaux précédemment peuvent désormais être instanciés par objet de son dynamique. En outre, certains créateurs de contenu peuvent souhaiter mettre à jour certains effets DSP pour prendre en charge des canaux supplémentaires ou les utiliser de manière unique.

## <a name="microsoft-spatial-sound-and-sound-spatialization-cues"></a>Signaux Spatialization et Sound spatial Microsoft

Le son spatial Microsoft est axé sur la simulation de positionnement du son sur une sphère idéale autour de l’écouteur. Windows Sonic pour casque, le casque DTS : X et Dolby Atmos implémentent le mappage et la virtualisation de haut-parleur sur un casque, mais notez que de nombreux autres aspects de la simulation spatiale de son, généralement implémentés en mode de création de contenu, sont laissés aux moteurs existants. Les créateurs de contenu continuent à utiliser les outils de jeu existants et les processus qu’ils ont déjà eu pour des indications spatiales comme Doppler, l’atténuation basée sur la distance et le filtrage, l’occlusion et l’obstruction, et l’environnement reverberation.

## <a name="additional-resources"></a>Ressources supplémentaires

-   [Référentiel GitHub d’exemples de son spatial Microsoft](https://github.com/Microsoft/Xbox-ATG-Samples/tree/master/UWPSamples/Audio)
-   dolby offre un certain nombre de ressources de support concernant dolby Atmos et l’application Dolby Access à l’adresse <https://developer.dolby.com> .

## <a name="spatial-sound-interfaces"></a>Interfaces son spatiales



| Interface                                                                              | Description                                                                                                                    |
|----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| [**ISpatialAudioClient**](/windows/desktop/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioclient)                                     | Permet à un client de créer des flux audio qui émettent du son à partir d’une position dans l’espace 3D.                                          |
| [**ISpatialAudioObject**](/windows/desktop/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioobject)                                     | Représente un objet qui fournit des données audio à rendre à partir d’une position dans l’espace 3D, par rapport à l’utilisateur.                |
| [**ISpatialAudioObjectRenderStream**](/windows/desktop/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioobjectrenderstream)             | Fournit des méthodes pour contrôler un flux de rendu d’objet audio spatial, y compris le démarrage, l’arrêt et la réinitialisation du flux. |
| [**ISpatialAudioObjectRenderStreamNotify**](/windows/desktop/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioobjectrenderstreamnotify) | Fournit des notifications pour que les clients de son spatial répondent aux modifications de l’état d’un ISpatialAudioObjectRenderStream.     |



 

> [!Note]  
> lorsque vous utilisez les interfaces [**ISpatialAudioClient**](/windows/desktop/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioclient) sur un titre de Kit de développement Xbox One (XDK), vous devez d’abord appeler **EnableSpatialAudio** avant d’appeler [**IMMDeviceEnumerator :: EnumAudioEndpoints**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-enumaudioendpoints) ou [**IMMDeviceEnumerator :: GetDefaultAudioEndpoint**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint). Dans le cas contraire, une \_ erreur E nointerface est retournée à partir de l’appel à Activate. **EnableSpatialAudio** est uniquement disponible pour les titres XDK et n’a pas besoin d’être appelé pour les applications plateforme Windows universelle s’exécutant sur Xbox One, ni pour les appareils non-Xbox One.

 

## <a name="spatial-sound-structures"></a>Structures de son spatial



| Structure                                                                                                 | Description                                                                  |
|-----------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| [**SpatialAudioObjectRenderStreamActivationParams**](/windows/desktop/api/spatialaudioclient/ns-spatialaudioclient-spatialaudioobjectrenderstreamactivationparams) | Représente les paramètres d’activation pour un flux de rendu audio spatial.          |
| [**SpatialAudioClientActivationParams**](/windows/desktop/api/spatialaudioclient/ns-spatialaudioclient-spatialaudioclientactivationparams)                          | Représente les paramètres d’activation facultatifs pour un flux de rendu audio spatial. |



 

## <a name="spatial-sound-enumerations"></a>Énumérations de sons spatiaux



| Énumération                                | Description                                   |
|--------------------------------------------|-----------------------------------------------|
| [**AudioObjectType**](/windows/desktop/api/spatialaudioclient/ne-spatialaudioclient-audioobjecttype) | Spécifie le type d’un ISpatialAudioObject. |



 

 

 



