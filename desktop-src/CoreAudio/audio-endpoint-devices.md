---
description: Périphériques de point de terminaison audio
ms.assetid: 773714fb-3b00-4f03-988f-05c5835f87cf
title: Périphériques de point de terminaison audio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d11145227ff4f6cf4eb7dd11342e28b3a8260aac95c41b32faed6b2d6bd414dd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118407328"
---
# <a name="audio-endpoint-devices"></a>Périphériques de point de terminaison audio

Le terme « *appareil de point de terminaison* » fait référence à un périphérique matériel qui se trouve à une extrémité d’un chemin de données qui est à l’origine ou se termine au niveau d’un programme d’application. Voici quelques exemples d’appareils de point de terminaison audio : les haut-parleurs, les casques, les microphones et les lecteurs de CD. Les données audio qui se déplacent sur le chemin de données peuvent traverser un certain nombre de composants logiciels et matériels au cours de leur trajet entre l’application et l’appareil de point de terminaison. Bien que ces composants soient essentiels au fonctionnement du périphérique de point de terminaison, ils ont tendance à être invisibles pour les utilisateurs. Les utilisateurs sont plus susceptibles de penser en termes d’appareils de point de terminaison qu’ils manipulent directement plutôt qu’en termes d’appareils sur les cartes audio que les appareils de point de terminaison connectent ou en termes de composants logiciels qui traitent les flux audio qui circulent vers et à partir de ces adaptateurs.

Pour éviter toute confusion avec les appareils de point de terminaison, cette documentation fait référence à un appareil sur une carte audio en tant que *périphérique adaptateur*.

Le diagramme suivant illustre la différence entre les périphériques de point de terminaison audio et les périphériques d’adaptateur.

![exemples d’appareils de point de terminaison audio et d’adaptateurs](images/devices.jpg)

Dans le diagramme ci-dessus, voici quelques exemples d’appareils de point de terminaison :

-   Haut-parleurs
-   Microphone
-   Périphérique d’entrée auxiliaire

Voici quelques exemples de périphériques d’adaptateur :

-   Appareil de sortie Wave (contient le convertisseur numérique-analogique)
-   Périphérique de contrôle de sortie (contient les contrôles volume et muet)
-   Périphérique d’entrée Wave (contient un convertisseur analogique-numérique)
-   Périphérique de contrôle d’entrée (contient le contrôle du volume et le multiplexeur)

En règle générale, les interfaces utilisateur des applications audio font référence aux périphériques de point de terminaison audio, et non aux périphériques d’adaptateur. Windows Vista simplifie la conception d’applications conviviales en prenant directement en charge l’abstraction des appareils de point de terminaison.

Certains périphériques de point de terminaison peuvent se connecter de façon permanente à un périphérique d’adaptateur. Par exemple, un ordinateur peut contenir des appareils internes tels qu’un lecteur de CD, un microphone ou des haut-parleurs intégrés dans le châssis du système. En règle générale, l’utilisateur ne supprime pas physiquement ces appareils de point de terminaison.

D’autres périphériques de point de terminaison peuvent se connecter à une carte audio par le biais de prises audio. L’utilisateur se connecte et déconnecte ces périphériques externes. Par exemple, un périphérique de point de terminaison audio, tel qu’un microphone externe ou un casque, se trouve à une extrémité d’un câble dont l’autre se connecte à un Jack sur un appareil d’adaptateur.

L’adaptateur communique avec le processeur système via un bus système (en général, PCI ou PCI Express) ou un bus externe (USB ou IEEE 1394) qui prend en charge Plug-and-Play (PnP). Au cours de l’énumération des appareils, le gestionnaire de Plug-and-Play identifie les périphériques de la carte audio et inscrit ces périphériques pour qu’ils soient disponibles pour une utilisation par le système d’exploitation et par les applications.

Contrairement à la connexion entre un adaptateur et un bus externe comme USB ou le bus IEEE 1394, la connexion entre un périphérique de point de terminaison et un périphérique d’adaptateur ne prend pas en charge la détection de périphérique PnP. Toutefois, certains adaptateurs audio prennent en charge la détection de la *présence du Jack*: lorsqu’un plug est inséré ou supprimé d’une prise Jack, le matériel génère une interruption pour informer le pilote de l’adaptateur de la modification de la configuration matérielle. le gestionnaire des points de terminaison de Windows Vista peut exploiter cette fonctionnalité matérielle pour informer les applications des périphériques de point de terminaison présents à tout moment. De cette façon, l’opération du gestionnaire de points de terminaison est analogue à celle du gestionnaire de Plug-and-Play, qui effectue le suivi des périphériques d’adaptateur présents dans le système.

dans Windows Vista, le système audio effectue le suivi des appareils de point de terminaison et des périphériques d’adaptateur. Le gestionnaire des points de terminaison inscrit les appareils de point de terminaison et le gestionnaire de Plug-and-Play inscrit les périphériques d’adaptateur. L’inscription des appareils de point de terminaison permet aux applications conviviales de permettre aux utilisateurs de faire référence aux appareils de point de terminaison que les utilisateurs manipulent directement au lieu de faire référence à des appareils d’adaptateur qui peuvent être masqués à l’intérieur du châssis de l’ordinateur. Les appareils de point de terminaison signalés par le système d’exploitation effectuent fidèlement le suivi des modifications dynamiques dans la configuration du matériel audio qui a la détection de la présence de la prise en forme. Lorsqu’un périphérique de point de terminaison reste branché, le système énumère ce périphérique. Lorsque l’utilisateur déconnecte un périphérique de point de terminaison, le système cesse de l’énumérer.

dans les versions antérieures de Windows, y compris Windows 98, Windows Me, Windows 2000 et Windows XP, le système présente explicitement uniquement les périphériques PnP aux applications. Ainsi, les applications doivent déduire l’existence d’appareils de point de terminaison. Un système d’exploitation qui ne dispose pas d’une prise en charge explicite des appareils de point de terminaison oblige les applications clientes à effectuer eux-mêmes ce travail. Par exemple, une application de capture audio doit effectuer les étapes suivantes pour activer la capture à partir d’un microphone externe :

1.  Énumérer tous les périphériques de capture audio (périphériques d’adaptateur) précédemment enregistrés par le Gestionnaire PnP.
2.  après avoir sélectionné un périphérique de capture, ouvrez un flux de capture sur l’appareil en appelant la fonction **waveInOpen** ou en utilisant l’API **DirectSoundCapture** ou DirectShow.
3.  Appelez la fonction mixerOpen et utilisez les autres fonctions **mixerXxx** pour rechercher une ligne de \_ microphone MIXERLINE COMPONENTTYPE \_ src \_ qui correspond au périphérique de capture ouvert à l’étape 2. Il s’agit d’une hypothèse éclairée.
4.  Débloquez le chemin de données à partir du microphone. Si le chemin d’accès aux données comprend un nœud muet, le client doit désactiver la sourdine du signal à partir du microphone. Si l’appareil de capture contient un multiplexeur pour la sélection parmi plusieurs entrées, le client doit sélectionner l’entrée microphone.

Ce processus est sujet aux erreurs, car le logiciel qui effectue ces opérations peut échouer s’il rencontre une configuration matérielle que ses concepteurs n’ont pas anticipées ou pour lesquelles il n’a pas été testé.

dans Windows Vista, qui prend en charge les appareils de point de terminaison, le processus de connexion au même appareil de point de terminaison est bien plus simple :

1.  Sélectionnez un microphone dans une collection d’appareils de point de terminaison.
2.  Activez une interface de capture audio sur ce microphone.

Le système d’exploitation effectue toutes les tâches nécessaires pour identifier et activer l’appareil de point de terminaison. Par exemple, si le chemin d’accès aux données du microphone comprend un multiplexeur, le système sélectionne automatiquement l’entrée du microphone dans le multiplexeur.

Le comportement du sous-système audio est plus fiable et déterministe si les applications, au lieu d’implémenter leurs propres algorithmes d’identification de point de terminaison, peuvent reléguer la tâche d’identification des appareils de point de terminaison au système d’exploitation. Les fournisseurs de logiciels n’ont plus besoin de vérifier que leurs algorithmes d’identification de point de terminaison fonctionnent correctement avec tous les périphériques et configurations matériels audio disponibles. ils peuvent simplement s’appuyer sur le système d’exploitation pour identifier les points de terminaison. De même, les fournisseurs de matériel n’ont plus besoin de vérifier que chaque application cliente appropriée peut facilement identifier tout périphérique de point de terminaison connecté à son adaptateur audio. il n’a besoin que de vérifier que le système d’exploitation peut identifier un périphérique de point de terminaison connecté à son adaptateur audio.

Les rubriques suivantes fournissent des informations supplémentaires sur les périphériques de point de terminaison audio :

-   [À propos de l’API MMDevice](mmdevice-api.md)
-   [Énumération des périphériques audio](enumerating-audio-devices.md)
-   [Chaînes ID du point de terminaison](endpoint-id-strings.md)
-   [Propriétés de l’appareil](device-properties.md)
-   [Événements de l’appareil](device-events.md)
-   [Rôles d’appareil](device-roles.md)
-   [Formats d’appareil](device-formats.md)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Guide de programmation](programming-guide.md)
</dt> </dl>

 

 



