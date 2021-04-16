---
description: Cette rubrique explique comment écrire un filtre source personnalisé pour DirectShow.
ms.assetid: 032f7624-2237-41cd-844a-18ed4a2e420d
title: Comment écrire un filtre source pour DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87af99595a43c86be0e2f4ecaa51768a211e9674
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104522519"
---
# <a name="how-to-write-a-source-filter-for-directshow"></a>Comment écrire un filtre source pour DirectShow

Cette rubrique explique comment écrire un filtre source personnalisé pour DirectShow.

> [!Note]  
> Cette rubrique décrit les sources Push uniquement. il ne décrit pas les sources de tirage, telles que le filtre de lecteur Async, ou les filtres de séparateur qui se connectent aux sources d’extraction. Pour la distinction entre les sources *Push* et *pull* , consultez [flux de données pour les développeurs de filtres](data-flow-for-filter-developers.md).

 

## <a name="the-directshow-streaming-model"></a>Modèle de diffusion en continu DirectShow

Lorsque vous écrivez un filtre source, il est important de comprendre qu’une source Push n’est pas la même chose qu’une source active. Une source active obtient des données à partir d’une source externe, telle qu’une caméra ou un flux réseau. En règle générale, une source dynamique ne peut pas contrôler le taux de données entrant. Si les filtres en aval ne consomment pas suffisamment de données, la source devra supprimer des échantillons.

Mais il n’est pas nécessaire qu’une source Push soit une source dynamique. Par exemple, une source Push peut lire des données à partir d’un fichier local. Dans ce cas, les filtres de convertisseur en aval déterminent la vitesse à laquelle ils consomment les données de la source, en fonction de l’horloge de référence et des horodatages de l’exemple. Le filtre source fournit des échantillons aussi rapidement que possible, mais le workflow réel est limité par les convertisseurs. Les mécanismes de déclenchement du workflow sont décrits dans la rubrique [Data Flow pour les développeurs de filtres](data-flow-for-filter-developers.md).

Chaque broche de sortie sur le filtre source crée un thread appelé *thread de streaming*. Le code PIN fournit des exemples sur le thread de streaming. En général, tout le décodage, le traitement et le rendu se produisent sur ce thread, bien que certains filtres en aval puissent créer des threads supplémentaires pour la mise en file d’attente de leurs exemples de sortie.

Le thread de streaming exécute une boucle avec la structure suivante :

``` syntax
until (stopped)
  1. Get a media sample from the allocator.
  2. Fill the sample with data.
  3. Time stamp the sample. 
  4. Deliver the sample downstream.
```

Si aucun échantillon n’est disponible, l’étape 1 se bloque jusqu’à ce qu’un exemple soit disponible. L’étape 4 peut également se bloquer ; par exemple, il peut se bloquer pendant que le graphique est suspendu.

La boucle s’exécute aussi rapidement que possible, mais elle est limitée par la vitesse à laquelle le filtre de convertisseur effectue le rendu de chaque échantillon. En supposant que le graphique de filtre a une horloge de référence, le taux est déterminé par les durées de présentation des échantillons. S’il n’y a pas d’horloge de référence, le convertisseur consomme les échantillons le plus rapidement possible.

## <a name="using-csource-and-csourcestream"></a>Utilisation de CSource et CSourceStream

Les classes de base DirectShow incluent deux classes qui prennent en charge les sources Push : [**CSource**](csource.md) et [**CSourceStream**](csourcestream.md).

-   [**CSource**](csource.md) est la classe de base pour le filtre et implémente l’interface [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) .
-   [**CSourceStream**](csourcestream.md) est la classe de base pour les broches de sortie et implémente l’interface [**IPIN**](/windows/desktop/api/Strmif/nn-strmif-ipin) .

### <a name="output-pins"></a>Broches de sortie

Un filtre source peut avoir plusieurs broches de sortie. Dans la méthode du constructeur de votre filtre, créez un ou plusieurs codes confidentiels dérivés de [**CSourceStream**](csourcestream.md) (un code confidentiel par flux de sortie). Vous n’avez pas besoin de stocker des pointeurs vers les broches. les codes confidentiels s’ajoutent automatiquement au filtre lorsqu’ils sont créés.

### <a name="output-formats"></a>Formats de sortie

La broche de sortie gère la négociation de format avec les méthodes [**CSourceStream**](csourcestream.md) suivantes :



| Méthode                                                 | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|--------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetMediaType**](csourcestream-getmediatype.md)     | Obtient un type de média à partir de la broche de sortie. <br/> Le code confidentiel doit proposer au moins un type de média, car le filtre en aval peut ne pas proposer de types. Dans la plupart des cas, le filtre en aval est un décodeur ou un convertisseur, selon que le filtre source fournit des données compressées ou non compressées. Un filtre de convertisseur requiert généralement un type de média complet, contenant toutes les informations de format nécessaires pour restituer le flux. Pour un décodeur, la quantité d’informations requises dans le type de média dépend beaucoup du format d’encodage.<br/> |
| [**CheckMediaType**](csourcestream-checkmediatype.md) | Vérifie si la broche de sortie accepte un type de média donné. La substitution de cette méthode est facultative, selon la manière dont vous implémentez [**GetMediaType**](csourcestream-getmediatype.md).                                                                                                                                                                                                                                                                                                                                                                                                         |



 

La méthode [**GetMediaType**](csourcestream-getmediatype.md) est surchargée :

-   [**GetMediaType**](csourcestream-getmediatype.md) (1) accepte un seul paramètre, un pointeur vers un objet [**CMediaType**](cmediatype.md) .
-   [**GetMediaType**](csourcestream-getmediatype2.md) (2) prend une variable d’index et un pointeur vers un objet [**CMediaType**](cmediatype.md) .

Si la broche de sortie du filtre source ne prend en charge qu’un seul format de média, vous devez remplacer (1) pour initialiser l’objet [**CMediaType**](cmediatype.md) avec ce format. Laissez l’implémentation par défaut de (2) et laissez également l’implémentation par défaut de [**CheckMediaType**](csourcestream-checkmediatype.md).

Si le code PIN prend en charge plusieurs formats, remplacez (2). Initialisez l’objet [**CMediaType**](cmediatype.md) en fonction de la valeur de la variable d’index. Le code confidentiel doit renvoyer les formats sous la forme d’une liste ordonnée. Dans ce cas, vous devez également remplacer [**CheckMediaType**](csourcestream-checkmediatype.md) pour vérifier le type de support par rapport à votre liste de formats.

Pour les formats vidéo non compressés, n’oubliez pas que le filtre en aval peut proposer des formats avec différentes valeurs Stride. Votre filtre doit accepter toute valeur Stride valide. Pour plus d’informations, consultez [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader).

Vous devez également substituer la méthode [**CBaseOutputPin ecidebuffersize ::D**](cbaseoutputpin-decidebuffersize.md) pure. Utilisez cette méthode pour définir la taille des exemples de mémoires tampons.

### <a name="streaming"></a>Diffusion en continu

La classe [**CSourceStream**](csourcestream.md) crée le thread de streaming pour le code confidentiel. La procédure de thread est implémentée dans la méthode [**CSourceStream ::D obufferprocessingloop**](csourcestream-dobufferprocessingloop.md) . Cette méthode appelle la méthode pure-virtual [**CSourceStream :: FillBuffer**](csourcestream-fillbuffer.md) , que la classe dérivée doit substituer. Cette méthode est l’endroit où le code confidentiel remplit la mémoire tampon avec des données. Par exemple, si votre filtre fournit une vidéo non compressée, c’est là que vous dessinez les images vidéo.

La classe de base démarre et arrête automatiquement la boucle de thread au moment approprié, lorsque le filtre est suspendu ou s’arrête. Dans ce cas, la classe [**CSourceStream**](csourcestream.md) appelle des méthodes pour notifier votre classe dérivée :

-   [**CSourceStream::OnThreadCreate**](csourcestream-onthreadcreate.md)
-   [**CSourceStream::OnThreadDestroy**](csourcestream-onthreaddestroy.md)
-   [**CSourceStream::OnThreadStartPlay**](csourcestream-onthreadstartplay.md)

Vous pouvez substituer ces méthodes si vous devez ajouter une gestion spéciale. Dans le cas contraire, les implémentations par défaut retournent simplement **S \_ OK**.

## <a name="seeking"></a>Cherche

Si vous avez un filtre source avec une broche de sortie, vous pouvez utiliser la classe [**CSourceSeeking**](csourceseeking.md) comme point de départ pour l’implémentation de la recherche. Hériter de votre classe pin de [**CSourceStream**](csourcestream.md) et **CSourceSeeking**.

> [!Note]  
> [**CSourceSeeking**](csourceseeking.md) n’est pas recommandé pour un filtre avec plus d’une broche de sortie. Le principal problème est que seul un code PIN doit répondre aux demandes de recherche. En général, cela nécessite une communication entre les codes confidentiels et le filtre.

 

La classe [**CSourceSeeking**](csourceseeking.md) gère la vitesse de lecture, l’heure de début, l’heure d’arrêt et la durée. Votre classe dérivée doit définir l’heure et la durée de l’arrêt initiales. Chaque fois que l’une de ces valeurs change, la méthode [**CSourceSeeking :: ChangeRate**](csourceseeking-changerate.md), [**CSourceSeeking :: modifiez l'**](csourceseeking-changestart.md)ou [**CSourceSeeking :: ChangeStop**](csourceseeking-changestop.md) est appelée, le cas échéant. Les méthodes sont toutes des méthodes virtuelles pures. La classe de code confidentiel dérivée remplace ces méthodes pour effectuer les opérations suivantes :

1.  Appelez [**IPIN :: BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) sur le code confidentiel en aval. Cela amène les filtres en aval à libérer des exemples qu’ils détiennent et rejettent de nouveaux exemples.
2.  Appelez [**CSourceStream :: Stop**](csourcestream-stop.md) pour arrêter le thread de diffusion en continu. Le filtre source interrompt la production de nouvelles données.
3.  Appelez [**IPIN :: EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) sur le code confidentiel en aval. Cela indique aux filtres en aval d’accepter de nouvelles données.
4.  Appelez [**IPIN :: NewSegment**](/windows/desktop/api/Strmif/nf-strmif-ipin-newsegment) avec les nouvelles dates et heures de début et de fin.
5.  Définissez la propriété discontinu sur l’exemple suivant.

Pour plus d’informations, consultez [prise en charge de la recherche dans un filtre source](supporting-seeking-in-a-source-filter.md).

Si votre filtre prend en charge la recherche, la position du flux est maintenant indépendante de l’heure de la présentation. Après une recherche, les horodatages sont remis à zéro. La formule générale pour les horodatages est la suivante :

-   heure de début de l’exemple = durée écoulée/vitesse de lecture
-   heure de fin de l’exemple = heure de début de l’exemple + (temps par cadre/vitesse de lecture)

le *temps écoulé* est le temps écoulé depuis le début de l’exécution du filtre ou depuis la dernière commande Seek.

### <a name="time-formats-for-seeking"></a>Formats d’heure pour la recherche

Par défaut, les commandes de recherche sont en unités de 100 nanosecondes. Votre filtre source peut prendre en charge des formats d’heure supplémentaires, tels que la recherche par numéro de trame. Chaque format d’heure est identifié par un GUID. consultez [**GUID de format d’heure**](time-format-guids.md).

Pour prendre en charge des formats d’heure supplémentaires, vous devez implémenter les méthodes suivantes sur votre code confidentiel de sortie :

-   [**IMediaSeeking::ConvertTimeFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-converttimeformat)
-   [**IMediaSeeking::GetTimeFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-gettimeformat)
-   [**IMediaSeeking::IsFormatSupported**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-isformatsupported)
-   [**IMediaSeeking::IsUsingTimeFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-isusingtimeformat)
-   [**IMediaSeeking::QueryPreferredFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-querypreferredformat)
-   [**IMediaSeeking::SetTimeFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-settimeformat)

Si l’application définit un nouveau format d’heure, tous les paramètres de position dans les méthodes [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) sont interprétés en fonction du nouveau format d’heure. Par exemple, si le format d’heure est frames, la méthode [**IMediaSeeking :: GetDuration**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getduration) doit retourner la durée dans les frames.

En pratique, peu de filtres DirectShow prennent en charge des formats d’heure supplémentaires et, par conséquent, peu d’applications DirectShow utilisent cette fonctionnalité.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Écriture de filtres source](writing-source-filters.md)
</dt> </dl>

 

 




