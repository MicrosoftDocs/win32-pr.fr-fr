---
description: améliorations de la lecture de DVD dans Windows Vista
ms.assetid: b3cf043f-c974-4240-8291-5c717bd8afaa
title: améliorations de la lecture de DVD dans Windows Vista
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d5757f5dd73dc547ae123490fd8de84b0606d1ade8490c9600486df0b846541
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119148712"
---
# <a name="dvd-playback-enhancements-in-windows-vista"></a>améliorations de la lecture de DVD dans Windows Vista

cette section décrit les améliorations apportées à la lecture et à la navigation sur DVD dans Windows Vista.

**Spécification d’un décodeur**

dans les versions antérieures de DirectShow, il était difficile de spécifier un décodeur MPEG-2 particulier lors de la création d’un graphique de lecture DVD. à partir de Windows Vista, une application peut spécifier le décodeur comme suit :

1.  Ajoutez le décodeur au graphique avant d’appeler [**IDvdGraphBuilder :: RenderDvdVideoVolume**](/windows/desktop/api/Strmif/nf-strmif-idvdgraphbuilder-renderdvdvideovolume).
2.  Appelez **RenderDvdVideoVolume** et définissez l' \_ \_ indicateur do DVD do \_ not \_ Clear. Le navigateur DVD donne la préférence au décodeur que vous avez ajouté.

**Prise en charge du convertisseur vidéo amélioré**

il est recommandé que les applications écrites pour Windows Vista ou versions ultérieures utilisent le [**convertisseur vidéo amélioré**](enhanced-video-renderer-filter.md) (EVR) pour la lecture vidéo. Pour utiliser EVR dans une application de lecture de DVD, définissez l' \_ indicateur AM DVD \_ EVR \_ only quand vous appelez **RenderDvdVideoVolume**.

Pour configurer EVR avant de générer le graphique, appelez [**IDvdGraphBuilder :: GetDvdInterface**](/windows/desktop/api/Strmif/nf-strmif-idvdgraphbuilder-getdvdinterface) et recherchez l’interface **IEVRFilterConfig** ou **IMFVideoRenderer** . (Ces interfaces sont documentées dans la documentation du kit de développement logiciel (SDK) Media Foundation.) Pour plus d’informations sur la configuration du convertisseur vidéo dans un graphique de lecture DVD, consultez [génération du filtre de dvd Graph](building-the-dvd-filter-graph.md).

Le navigateur DVD n’utilise pas le EVR, sauf si la méthode [**IAMDecoderCaps :: GetDecoderCaps**](/windows/desktop/api/Strmif/nf-strmif-iamdecodercaps-getdecodercaps) du décodeur retourne \_ l' \_ indicateur \_ de \_ prise en charge de la requête am GETDECODERCAP EVR. Cet indicateur est défini pour s’assurer que les applications sont compatibles avec les décodeurs existants. Si **RenderDvdVideoVolume** échoue en utilisant l' \_ indicateur AM DVD \_ EVR \_ only, revenez à un autre convertisseur vidéo en appelant la méthode à nouveau sans l’indicateur.

**Lecture inversée fluide**

Le navigateur DVD peut désormais effectuer une lecture inversée en douceur. Dans le cadre de la lecture en sens inverse, le navigateur DVD envoie l’intégralité des unités d’objet vidéo (VOBUs) au décodeur, et le décodeur émet les frames dans l’ordre inverse. Cette fonctionnalité nécessite que les décodeurs prennent en charge la lecture inversée en douceur.

Lorsque l’application définit la vitesse de lecture sur une valeur négative, le navigateur DVD interroge les décodeurs pour la propriété [**\_ \_ ReverseMaxFullDataRate am rate**](am-rate-reversemaxfulldatarate-property.md) . La valeur de cette propriété est la valeur absolue de la vitesse inversée maximale x 10000. Par exemple, si la vitesse inversée maximale est-2,0, la valeur est 20000.

Si le décodeur vidéo prend en charge la propriété, le navigateur DVD utilise la lecture inversée en douceur. Le flux audio est lu en sens inverse si le décodeur audio prend en charge la propriété ; dans le cas contraire, le flux audio est muet. Si le décodeur vidéo ne prend pas en charge la propriété, ou si la vitesse de lecture dépasse la vitesse d’inversion maximale du décodeur vidéo, le navigateur DVD bascule en *mode d’analyse*. En mode de numérisation, le navigateur DVD envoie uniquement les images I au décodeur et supprime toutes les images B et P.

Pendant la lecture en sens inverse, le navigateur DVD envoie des VOBUs complets au décodeur. Le navigateur DVD envoie le VOBUs dans l’ordre inverse, mais envoie les trames dans chaque VOBU dans leur ordre normal. Au début de chaque VOBU, le navigateur DVD définit l’indicateur AM \_ ReverseBlockStart sur l’exemple. À la fin de l’VOBU, le navigateur DVD envoie un exemple vide avec l' \_ indicateur AM ReverseBlockEnd. Pour récupérer ces indicateurs, appelez [**IMediaSample2 :: GetProperties**](/windows/desktop/api/Strmif/nf-strmif-imediasample2-getproperties) sur l’exemple. Les indicateurs sont définis dans le membre **dwTypeSpecificFlags** de la structure de [**\_ \_ Propriétés am SAMPLE2**](/windows/win32/api/strmif/ns-strmif-am_sample2_properties) .

Le décodeur met en cache les données vidéo jusqu’à ce qu’il reçoive l’exemple avec l' \_ indicateur AM ReverseBlockEnd. À ce stade, le décodeur fournit des frames décodés dans l’ordre inverse. Par exemple, si VOBU 1 contient les trames 1 à 4 et VOBU 2 les images 5 à 8, le navigateur DVD envoie les images dans l’ordre suivant :

(Début de bloc) F5 F6 F7 F8 (fin de bloc) (début de bloc) F1 F2 F3 F4 (fin de bloc)

Le décodeur doit traiter les frames comme suit :

1.  Décodez VOBU 2.
2.  Frames de sortie : F8 F7 F6 F5
3.  Décodez VOBU 1.
4.  Frames de sortie : F4 F3 F2 F1

Le navigateur DVD définit l’horodatage sur le premier échantillon dans le VOBU (F1 et F5 dans cet exemple), mais l’horodatage contient l’heure de présentation du début du bloc, de sorte que le décodeur doit appliquer cette fois au dernier échantillon du bloc (F4 et F8). Augmentation des durées de présentation pendant la lecture inversée.

En général, un VOBU contient jusqu’à 42 images et peut contenir plusieurs groupes d’images (GOP). Pour permettre le décodage de la totalité du VOBU, le décodeur doit mettre en cache les images I et P décodées. VOBUs sur les DVD ne sont pas fermés GOP secondes, donc un frame B dans un groupe d’images peut nécessiter le décodage de tous les frames de référence dans le groupe d’images précédent. Si le décodeur n’a pas suffisamment de surfaces pour contenir toutes les trames décodées, il peut être nécessaire de recoder les frames sélectionnés.

**Modifications des taux**

Par défaut, le navigateur DVD vide le graphique entre les changements de taux. Toutefois, si le décodeur prend en charge la propriété [**\_ \_ ResetOnTimeDisc am rate**](am-rate-resetontimedisc-property.md) , le navigateur DVD n’efface pas le graphique, ce qui entraîne une transition plus lisse entre les vitesses de lecture.

Le navigateur DVD horodate toujours les échantillons pour la lecture à une vitesse 1x, quelle que soit la vitesse réelle de lecture. Le décodeur doit mettre à l’échelle les horodatages sur les échantillons décodés pour correspondre à la vitesse de lecture réelle. (Pour plus d’informations, consultez [**am \_ rate \_ SimpleRateChange Property**](am-rate-simpleratechange-property.md).) Par conséquent, lorsque vous jouez à des vitesses autres que 1x, les horodatages sur les images décodées divergent de ceux sur les images encodées. Chaque fois que le navigateur DVD définit \_ l' \_ indicateur AM Sample TIMEDISCONTINUITY sur un échantillon, le décodeur doit resynchroniser ses horodatages. En d’autres termes, la trame décodée doit avoir le même horodatage que le frame d’entrée. Pour récupérer l' \_ \_ indicateur TIMEDISCONTINUITY AM, appelez [**IMediaSample2 :: GetProperties**](/windows/desktop/api/Strmif/nf-strmif-imediasample2-getproperties) sur l’exemple. L’indicateur est défini dans le membre **dwSampleFlags** de la structure de [**\_ \_ Propriétés am SAMPLE2**](/windows/win32/api/strmif/ns-strmif-am_sample2_properties) .

**Gestion de l’alimentation**

dans Windows Vista, le navigateur DVD offre les améliorations suivantes à la gestion de l’alimentation :

-   Résolution de l’horloge supérieure
-   Plus grand cache de données

**Résolution du minuteur**: les applications peuvent demander une résolution minimale de la minuterie en appelant la fonction **timeBeginPeriod** . Une résolution supérieure (période plus petite) augmente la réactivité du système aux événements périodiques, tels que les délais d’attente, mais peut également augmenter la fréquence des changements de contexte de thread.

par défaut, l’horloge de référence dans DirectShow définit la résolution de la minuterie sur 1 milliseconde. À cette résolution, le processeur n’entrera pas en mode d’économie d’énergie. à partir de Windows Vista, le navigateur DVD remplace le comportement par défaut de l’horloge de référence en appelant [**IReferenceClockTimerControl :: SetDefaultTimerResolution**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclocktimercontrol-setdefaulttimerresolution) sur l’horloge de référence. Cela supprime la demande de l’horloge pour une résolution de minuteur de 1 milliseconde. Cela peut permettre au processeur de passer en mode d’économie d’énergie.

La résolution de la minuterie est un paramètre global ; Windows sélectionne la valeur la plus faible demandée. Les filtres de convertisseur de mixage vidéo (VMR-7 et VMR-9) définissent la résolution de la minuterie sur 1 milliseconde. Le EVR définit généralement la résolution sur une valeur comprise entre 4 et 8 millisecondes, en fonction de la façon dont la composition du Bureau est activée et si le EVR est en mode plein écran. D’autres applications peuvent également définir la résolution.

**Taille du cache**: les applications peuvent spécifier la quantité de données que le navigateur DVD met en cache en définissant l' \_ option CacheSizeInMB DVD dans la méthode [**IDvdControl2 :: SetOption**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-setoption) . Si l’application définit cet indicateur sur une valeur élevée (> 50 Mo), le lecteur de DVD peut s’arrêter après la pré-extraction initiale, en fonction du matériel, ce qui peut réduire la consommation d’énergie.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Applications DVD](dvd-applications.md)
</dt> </dl>

 

 



