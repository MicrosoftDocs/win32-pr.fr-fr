---
description: Les récepteurs de médias sont les objets de pipeline qui reçoivent des données multimédias.
ms.assetid: a0fbce1b-0a16-4449-9eca-906fd9056a1c
title: Récepteurs de médias
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9394cbfd49a631d59b9296202a2b6ca7a868869
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/03/2021
ms.locfileid: "104321474"
---
# <a name="media-sinks"></a>Récepteurs de médias

Les *récepteurs de médias* sont les objets de pipeline qui reçoivent des données multimédias. Un récepteur multimédia est la destination d’un ou plusieurs flux multimédias. Les récepteurs de médias se répartissent en deux catégories générales :

-   Un *convertisseur* est un récepteur multimédia qui présente des données pour la lecture. Le convertisseur vidéo amélioré (EVR) affiche des images vidéo et le convertisseur audio lit les flux audio par le biais de la carte son ou d’un autre périphérique audio.

-   Un *récepteur d’archives* est un récepteur multimédia qui écrit des données dans un fichier ou un autre stockage.

La principale différence réside dans le fait qu’un récepteur d’archive ne consomme pas les données à un taux de lecture fixe. Au lieu de cela, il écrit les données qu’il reçoit le plus rapidement possible.

Les récepteurs multimédias exposent l’interface [**IMFMediaSink**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink) . Chaque récepteur multimédia contient un ou plusieurs *récepteurs de flux*. Chaque récepteur de flux reçoit les données d’un flux. Les récepteurs de flux exposent l’interface [**IMFStreamSink**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamsink) . En général, une application ne crée pas directement des récepteurs multimédias. Au lieu de cela, l’application crée un ou plusieurs objets d’activation, que la session multimédia utilise pour créer le récepteur. Toutes les autres opérations sur le récepteur sont gérées par la session multimédia, et l’application n’appelle aucune méthode sur le récepteur multimédia ou l’un des récepteurs de flux. Pour plus d’informations sur les objets d’activation, consultez [objets d’activation](activation-objects.md).

Vous devez lire le reste de cette rubrique si vous écrivez un récepteur multimédia personnalisé ou si vous souhaitez utiliser un récepteur multimédia directement sans la session multimédia.

-   [Récepteurs de flux](#stream-sinks)
-   [Horloge de présentation](#presentation-clock)
-   [Formats de flux](#stream-formats)
-   [Flux de données](#data-flow)
-   [Marqueurs](#markers)
-   [Modifications d’État](#state-changes)
-   [En cours de finalisation](#finalizing)
-   [Arrêt en cours](#shutting-down)
-   [Interfaces du récepteur multimédia](#media-sink-interfaces)
-   [Interfaces du récepteur de flux](#stream-sink-interfaces)
-   [Événements du récepteur de flux](#stream-sink-events)
-   [Rubriques connexes](#related-topics)

## <a name="stream-sinks"></a>Récepteurs de flux

Un récepteur multimédia peut avoir un nombre fixe de récepteurs de flux, ou il peut prendre en charge l’ajout et la suppression de récepteurs de flux. S’il a un nombre fixe de récepteurs de flux, la méthode [**IMFMediaSink :: GetCharacteristics**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-getcharacteristics) retourne l' \_ indicateur de \_ flux fixe MEDIASINK. Dans le cas contraire, vous pouvez ajouter et supprimer des récepteurs de flux. Pour ajouter un nouveau récepteur de flux, appelez [**IMFMediaSink :: AddStreamSink**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-addstreamsink). Pour supprimer un récepteur de flux, appelez [**IMFMediaSink :: RemoveStreamSink**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-removestreamsink). L' \_ indicateur MEDIASINK \_ Streams Fixed indique que le récepteur multimédia ne prend pas en charge ces deux méthodes. (Cela peut prendre en charge une autre façon de configurer le nombre de flux, par exemple en définissant des paramètres d’initialisation lors de la création du récepteur.) La liste des récepteurs de flux est triée. Pour les énumérer par valeur d’index, appelez la méthode [**IMFMediaSink :: GetStreamSinkByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-getstreamsinkbyindex) .

Les récepteurs de flux ont également des identificateurs. Les identificateurs de flux sont uniques dans le récepteur multimédia, mais n’ont pas besoin d’être consécutifs. En fonction du récepteur multimédia, les identificateurs de flux peuvent avoir une signification liée au contenu. Par exemple, un récepteur d’archive peut écrire les identificateurs de flux dans l’en-tête de fichier. Dans le cas contraire, ils sont arbitraires. Pour obtenir un récepteur de flux par son identificateur, appelez [**IMFMediaSink :: GetStreamSinkById**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-getstreamsinkbyid).

## <a name="presentation-clock"></a>Horloge de présentation

La vitesse à laquelle un récepteur multimédia consomme des échantillons est contrôlée par l' [horloge de présentation](presentation-clock.md). La session multimédia sélectionne l’horloge de la présentation et la définit sur le récepteur multimédia en appelant la méthode [**IMFMediaSink :: SetPresentationClock**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-setpresentationclock) du récepteur multimédia. L’horloge de la présentation doit être définie sur le récepteur multimédia avant que la diffusion en continu puisse commencer. Chaque récepteur multimédia nécessite une horloge de présentation pour s’exécuter. Le récepteur multimédia utilise l’horloge de présentation pour deux raisons :

-   Pour recevoir des notifications au démarrage ou à l’arrêt de la diffusion en continu. Le récepteur multimédia reçoit ces notifications par le biais de l’interface [**IMFClockStateSink**](/windows/desktop/api/mfidl/nn-mfidl-imfclockstatesink) , que tous les récepteurs multimédias doivent implémenter.

-   Pour déterminer quand il doit restituer des exemples. Lorsque le récepteur multimédia reçoit un nouvel exemple, il obtient l’horodatage de l’échantillon et tente d’afficher l’échantillon à l’heure de la présentation.

L’horloge de présentation dérive les temps d’horloge d’un autre objet appelé *source de temps de présentation*. Les sources de temps de présentation exposent l’interface [**IMFPresentationTimeSource**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationtimesource) . Certains récepteurs multimédias ont accès à une horloge précise, de sorte qu’ils exposent cette interface. Cela signifie qu’un récepteur multimédia peut planifier des échantillons par rapport à une heure fournie par sa propre horloge. Toutefois, le récepteur multimédia ne peut pas supposer que c’est le cas. Elle doit toujours utiliser l’heure de l’horloge de présentation, que l’horloge de la présentation soit pilotée par le récepteur multimédia lui-même ou par une autre horloge.

Si un récepteur multimédia ne peut pas faire correspondre les vitesses avec une horloge autre que son propre, la méthode [**GetCharacteristics**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-getcharacteristics) retourne le MEDIASINK \_ ne peut pas \_ correspondre à l' \_ indicateur d’horloge. Si cet indicateur est présent et que l’horloge de présentation utilise une autre source de durée de présentation, le récepteur multimédia risque de mal fonctionner. Par exemple, il peut être en cours de lecture.

Un récepteur de *débit* est un récepteur multimédia qui ignore les horodatages sur les échantillons et consomme des données dès que chaque exemple arrive. Un récepteur de médias sans débit retourne l' \_ indicateur de débit MEDIASINK de la méthode [**GetCharacteristics**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-getcharacteristics) . En général, cet indicateur s’applique aux récepteurs d’archive. Si chaque récepteur multimédia du pipeline est sans débit, la session multimédia utilise une horloge de présentation spéciale sans frais. Cette horloge s’exécute aussi rapidement que les récepteurs consomment des échantillons.

## <a name="stream-formats"></a>Formats de flux

Pour que le récepteur multimédia puisse recevoir des exemples, le client doit définir le type de média sur les récepteurs de flux. Pour définir le type de média, appelez la méthode [**IMFStreamSink :: GetMediaTypeHandler**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamsink-getmediatypehandler) du récepteur de flux. Cette méthode retourne un pointeur vers l’interface [**IMFMediaTypeHandler**](/windows/desktop/api/mfidl/nn-mfidl-imfmediatypehandler) . Utilisez cette interface pour récupérer la liste des types de média préférés, récupérer le type de média actuel et définir le type de média.

Pour afficher la liste des types de média préférés, appelez [**IMFMediaTypeHandler :: GetMediaTypeByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-getmediatypebyindex). Les types préférés doivent être considérés comme un indicateur pour le client. La liste peut être incomplète ou inclure des types de média partiels. Un type de média partiel est un type qui n’a pas tous les attributs nécessaires pour décrire un format valide. Par exemple, un type de vidéo partiel peut spécifier l’espace de couleurs et la profondeur de bits, mais pas la largeur ou la hauteur de l’image. Un type audio partiel peut spécifier le format de compression et le taux d’échantillonnage, mais pas le nombre de canaux audio.

Pour récupérer le type de média actuel du récepteur de flux, appelez [**IMFMediaTypeHandler :: GetCurrentMediaType**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-getcurrentmediatype). Lorsqu’un récepteur de flux est créé, il peut avoir un type de média par défaut déjà défini, ou il n’a peut-être pas de type de média tant que le client n’en a pas défini un.

Pour définir le type de média, appelez [**IMFMediaTypeHandler :: SetCurrentMediaType**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-setcurrentmediatype). Certains récepteurs de flux peuvent ne pas prendre en charge la modification du type après que a été défini. Par conséquent, il est utile de tester les types de médias avant de les définir. Pour vérifier si le récepteur multimédia accepte un type de média (sans définir le type), appelez [**IMFMediaTypeHandler :: IsMediaTypeSupported**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-ismediatypesupported).

## <a name="data-flow"></a>Data Flow

Les récepteurs de médias utilisent un *modèle d’extraction*, ce qui signifie que le flux reçoit les données de demande en fonction de leurs besoins. Le client doit répondre en temps opportun pour éviter tout problème.

Certains récepteurs multimédias prennent en charge la *prérestauration*. La prérestauration est le processus qui consiste à fournir des données au récepteur multimédia avant le démarrage de l’horloge de présentation. Si un récepteur multimédia prend en charge la prérestauration, le récepteur multimédia expose l’interface [**IMFMediaSinkPreroll**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasinkpreroll) et la méthode [**GetCharacteristics**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-getcharacteristics) retourne l' \_ \_ indicateur de préroll MEDIASINK. Le prérollment garantit que le récepteur multimédia est prêt à présenter le premier exemple au démarrage de l’horloge de présentation. Il est recommandé que le client soit toujours préroll si le récepteur multimédia le prend en charge, car il peut empêcher des problèmes ou des failles pendant la lecture.

Le déplacement de données vers un récepteur multimédia fonctionne comme suit :

1.  Le client définit les types de médias et l’horloge de présentation. Le récepteur multimédia s’inscrit lui-même avec l’horloge de présentation pour recevoir des notifications sur les modifications de l’état de l’horloge.
2.  Le cas échéant, le client interroge [**IMFMediaSinkPreroll**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasinkpreroll). Si le récepteur multimédia expose cette interface, le client appelle [**IMFMediaSinkPreroll :: NotifyPreroll**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasinkpreroll-notifypreroll). Dans le cas contraire, le client passe à l’étape 5.
3.  Chaque récepteur de flux envoie un ou plusieurs événements [MEStreamSinkRequestSample](mestreamsinkrequestsample.md) . En réponse à chacun de ces événements, le client obtient l’exemple suivant de données pour ce flux et appelle [**IMFStreamSink ::P rocesssample**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamsink-processsample).
4.  Lorsque chaque récepteur de flux reçoit suffisamment de données de préroll, il envoie un événement [MEStreamSinkPrerolled](mestreamsinkprerolled.md) .
5.  Le client appelle [**IMFPresentationClock :: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationclock-start) pour démarrer l’horloge de la présentation.
6.  L’horloge de présentation informe le récepteur multimédia que l’horloge démarre, en appelant [**IMFClockStateSink :: OnClockStart**](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockstart).
7.  Pour obtenir plus de données, chaque récepteur de flux envoie des événements [MEStreamSinkRequestSample](mestreamsinkrequestsample.md) . En réponse à chacun de ces événements, le client obtient l’exemple suivant et appelle [**ProcessSample**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamsink-processsample). Cette étape est répétée jusqu’à la fin de la présentation.

La plupart des récepteurs de média traitent les exemples de manière asynchrone, de sorte que les récepteurs de flux peuvent envoyer plusieurs exemples de demandes à la fois.

Pendant la diffusion en continu, le client peut appeler [**IMFStreamSink ::P lacemarker**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamsink-placemarker) et [**IMFStreamSink :: Flush**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamsink-flush) à tout moment. Les marqueurs sont décrits dans la section suivante. Le vidage provoque la suppression, par le récepteur de flux, des exemples qu’il a mis en file d’attente mais pas encore rendus.

## <a name="markers"></a>Marqueurs

Les marqueurs permettent au client d’indiquer des points spécifiques dans le flux. Un marqueur se compose des informations suivantes :

-   Type de marqueur, défini en tant que membre de l’énumération du [**\_ \_ type de marqueur MFSTREAMSINK**](/windows/desktop/api/mfidl/ne-mfidl-mfstreamsink_marker_type) .
-   Données associées au marqueur. La signification des données dépend du type de marqueur. Certains types de marqueur n’ont pas de données.
-   Données facultatives pour l’utilisation du client.

Pour placer un marqueur, le client appelle [**IMFStreamSink ::P lacemarker**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamsink-placemarker). Le récepteur de flux termine le traitement des échantillons qu’il a reçus avant l’appel **PlaceMarker** , puis envoie un événement [MEStreamSinkMarker](mestreamsinkmarker.md) .

La plupart des récepteurs de média conservent une file d’attente d’exemples en attente, qu’ils traitent de façon asynchrone. Les événements de marqueur doivent être sérialisés avec le traitement de l’échantillon, afin que le récepteur multimédia doive placer les marqueurs dans la même file d’attente. Par exemple, supposons que le client effectue les appels de méthode suivants :

1.  [**ProcessSample**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamsink-processsample) (exemple \# 1)
2.  [**ProcessSample**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamsink-processsample) (exemple \# 2)
3.  [**PlaceMarker**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamsink-placemarker) (marqueur \# 1)
4.  [**ProcessSample**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamsink-processsample) (exemple \# 3)
5.  [**PlaceMarker**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamsink-placemarker) (marqueur \# 2)

Dans cet exemple, le récepteur de flux doit envoyer l’événement [MEStreamSinkMarker](mestreamsinkmarker.md) pour le marqueur \# 1 après le traitement de l’exemple \# 2, et l’événement pour le marqueur \# 2 après le traitement de l’exemple \# 3.

Si le client vide un récepteur de flux, le récepteur de flux traite immédiatement tous les marqueurs qui se trouvaient dans la file d’attente. Il définit le code d’État sur E \_ Abort sur ces événements.

Certains marqueurs contiennent des informations qui s’appliquent au récepteur multimédia :

-   **MFSTREAMSINK \_ \_Graduation du marqueur**: indique qu’il y a un intervalle dans le flux. L’exemple suivant est une discontinuité.
-   **MFSTREAMSINK \_ MARKER \_ ENDOFSEGMENT**: indique la fin d’un segment ou la fin d’un flux. L’exemple suivant (le cas échéant) peut être une discontinuité.
-   **MFSTREAMSINK \_ \_Événement marqueur**: contient un événement. En fonction du type d’événement et de l’implémentation du récepteur multimédia, le récepteur multimédia peut gérer l’événement ou l’ignorer.

## <a name="state-changes"></a>Changements d'état

Un récepteur multimédia est informé des changements d’État dans l’horloge de la présentation via l’interface [**IMFClockStateSink**](/windows/desktop/api/mfidl/nn-mfidl-imfclockstatesink) du récepteur multimédia. Lorsque le client définit l’horloge de présentation, le récepteur multimédia appelle [**IMFPresentationClock :: AddClockStateSink**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationclock-addclockstatesink) pour s’inscrire pour les notifications à partir de l’horloge. Le tableau suivant résume la façon dont un récepteur multimédia se comporte en réponse aux modifications de l’état de l’horloge.



| Changement d’état de l’horloge                                         | Traitement de l’échantillon                                                                                                                                                                                                                                             | Traitement des marqueurs                                                                                                                                                                                   |
|------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**OnClockStart**](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockstart)     | Les exemples de processus dont l’horodatage est supérieur ou égal à l’heure de début de l’horloge.                                                                                                                                                                              | Envoyez l’événement [MEStreamSinkMarker](mestreamsinkmarker.md) lorsque tous les exemples reçus avant que le marqueur ait été traité.                                                                 |
| [**OnClockPause**](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockpause)     | Le récepteur multimédia peut échouer [**ProcessSample**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamsink-processsample) pendant la suspension.<br/> Si le récepteur multimédia accepte des exemples en pause, il doit les placer en file d’attente jusqu’au redémarrage de l’horloge. Ne traitez aucun échantillon mis en file d’attente pendant la suspension.<br/> | S’il existe des échantillons mis en file d’attente, placez les marqueurs dans la même file d’attente. Envoyer l’événement de marqueur lorsque l’horloge redémarre.<br/> Sinon, envoyez immédiatement l’événement du marqueur.<br/>                    |
| [**OnClockRestart**](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockrestart) | Traitez les exemples qui ont été mis en file d’attente pendant la suspension, puis traitez le même que [**OnClockStart**](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockstart).                                                                                                                         | Envoyer des événements [MEStreamSinkMarker](mestreamsinkmarker.md) pour les marqueurs en file d’attente (sérialisés avec traitement de l’échantillon), puis traiter le même que [**OnClockStart**](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockstart). |
| [**OnClockStop**](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockstop)       | Supprimer tous les échantillons mis en file d’attente. D’autres appels à [**ProcessSample**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamsink-processsample) peuvent échouer.                                                                                                                                                      | Envoyer des événements de marqueur en file d’attente. Lors des appels suivants à [**PlaceMarker**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamsink-placemarker), envoyez immédiatement l’événement marqueur.                                                              |



 

En outre, les récepteurs de flux doivent envoyer les événements suivants lorsqu’ils ont terminé les transitions d’État :

-   [**OnClockStart**](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockstart), [**OnClockRestart**](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockrestart): [MEStreamSinkStarted](mestreamsinkstarted.md) , événement
-   [**OnClockPause**](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockpause): événement [MEStreamSinkPaused](mestreamsinkpaused.md)
-   [**OnClockStop**](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockstop): événement [MEStreamSinkStopped](mestreamsinkstopped.md)

## <a name="finalizing"></a>En cours de finalisation

Certains récepteurs multimédia nécessitent une étape de traitement supplémentaire après la remise du dernier échantillon. En général, cette exigence s’applique aux récepteurs d’archive, qui doivent écrire des en-têtes ou des index dans le fichier. Si un récepteur multimédia requiert un traitement final, il expose l’interface [**IMFFinalizableMediaSink**](/windows/desktop/api/mfidl/nn-mfidl-imffinalizablemediasink) .

Une fois que le client remet le dernier échantillon, le client interroge cette interface. Si le récepteur multimédia prend en charge l’interface, le client appelle [**IMFFinalizableMediaSink :: BeginFinalize**](/windows/desktop/api/mfidl/nf-mfidl-imffinalizablemediasink-beginfinalize) pour effectuer le traitement final de manière asynchrone. Cette méthode suit le modèle asynchrone Media Foundation standard, décrit dans [méthodes de rappel asynchrones](asynchronous-callback-methods.md). Le récepteur multimédia peut supposer que le client appellera **BeginFinalize**. L’échec de l’appel de **BeginFinalize** peut entraîner un fichier créé de manière incorrecte.

## <a name="shutting-down"></a>Arrêt en cours

Lorsque le client a terminé à l’aide du récepteur multimédia, le client appelle [**IMFMediaSink :: Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-shutdown). Au sein de cette méthode, le récepteur multimédia doit rompre les nombres de références circulaires. En règle générale, il y aura des références circulaires entre le récepteur multimédia et les récepteurs de flux.

Si vous utilisez l’objet d’assistance de la file d’attente d’événements pour implémenter [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator), appelez [**IMFMediaEventQueue :: Shutdown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventqueue-shutdown) dans la file d’attente d’événements. Cette méthode arrête la file d’attente des événements et signale à tout appelant qui attend un événement.

Après l’arrêt, toutes les méthodes sur le récepteur multimédia retournent l' \_ arrêt MF E \_ , à l’exception des méthodes **IUnknown** .

## <a name="media-sink-interfaces"></a>Interfaces du récepteur multimédia

Le tableau suivant répertorie les interfaces standard que les récepteurs multimédias peuvent exposer via **QueryInterface**. Les récepteurs multimédias peuvent également exposer des interfaces personnalisées.



| Interface                                                      | Description                                                                                   |
|----------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| [**IMFMediaSink**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink)                           | Interface principale pour les récepteurs multimédias. (Obligatoire.)                                            |
| [**IMFClockStateSink**](/windows/desktop/api/mfidl/nn-mfidl-imfclockstatesink)                 | Utilisé pour notifier le récepteur multimédia lorsque l’horloge de présentation change d’État. (Obligatoire.)              |
| [**IMFFinalizableMediaSink**](/windows/desktop/api/mfidl/nn-mfidl-imffinalizablemediasink)     | Implémentez si le récepteur multimédia doit effectuer une dernière étape de traitement. (Facultatif.)                 |
| [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice)                         | Implémentez si le récepteur multimédia expose des interfaces de service. (Facultatif.)                       |
| [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator)       | Implémentez si le récepteur multimédia envoie des événements. (Facultatif.)                                     |
| [**IMFMediaSinkPreroll**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasinkpreroll)             | Implémentez si le récepteur multimédia prend en charge le préroll. (Facultatif.)                                     |
| [**IMFPresentationTimeSource**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationtimesource) | Implémentez si le récepteur multimédia peut fournir une source de temps pour l’horloge de présentation. (Facultatif.) |
| [**IMFQualityAdvise**](/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise)                   | Implémentez si le récepteur multimédia peut ajuster la qualité de la lecture. (Facultatif.)                          |



 

Éventuellement, un récepteur multimédia peut implémenter l’interface suivante en tant que service.



| Interface de service                        | Description                                    |
|------------------------------------------|------------------------------------------------|
| [**IMFRateSupport**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport) | Indique la plage des taux de lecture pris en charge. |



 

Pour plus d’informations sur les interfaces de service et les [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice), consultez [interfaces de service](service-interfaces.md).

## <a name="stream-sink-interfaces"></a>Interfaces du récepteur de flux

Les récepteurs de flux doivent exposer les interfaces suivantes via **QueryInterface**.



| Interface                                                | Description                                                                                              |
|----------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| [**IMFStreamSink**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamsink)                   | Interface principale pour les récepteurs de flux. (Obligatoire.)                                                      |
| [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) | Met en file d’attente les événements. L’interface [**IMFStreamSink**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamsink) hérite de cette interface. (Obligatoire.) |



 

Aucune interface de service n’est actuellement définie pour les récepteurs de flux.

## <a name="stream-sink-events"></a>Événements du récepteur de flux

Le tableau suivant répertorie les événements qui sont définis pour les récepteurs de flux génériques. Les récepteurs de flux peuvent également envoyer des événements personnalisés qui ne sont pas répertoriés ici.



| Événement                                                                  | Description                                                  |
|------------------------------------------------------------------------|--------------------------------------------------------------|
| [MEStreamSinkFormatChanged](mestreamsinkformatchanged.md)             | Le type de média du récepteur de flux n’est plus valide. (Facultatif.) |
| [MEStreamSinkMarker](mestreamsinkmarker.md)                           | Un marqueur a été traité. (Obligatoire.)                          |
| [MEStreamSinkPaused](mestreamsinkpaused.md)                           | Le récepteur de flux est suspendu. (Obligatoire.)                      |
| [MEStreamSinkPrerolled](mestreamsinkprerolled.md)                     | Le préroll est terminé. (Facultatif.)                             |
| [MEStreamSinkRateChanged](mestreamsinkratechanged.md)                 | Le récepteur de flux a changé de vitesse de lecture. (Facultatif.)       |
| [MEStreamSinkRequestSample](mestreamsinkrequestsample.md)             | Un nouvel exemple est demandé. (Obligatoire.)                       |
| [MEStreamSinkScrubSampleComplete](mestreamsinkscrubsamplecomplete.md) | Une demande de nettoyage est terminée. (Facultatif.)                   |
| [MEStreamSinkStarted](mestreamsinkstarted.md)                         | Le récepteur de flux a démarré. (Obligatoire.)                     |
| [MEStreamSinkStopped](mestreamsinkstopped.md)                         | Le récepteur de flux s’est arrêté. (Obligatoire.)                     |



 

Actuellement, aucun événement à usage général n’est défini pour les récepteurs multimédias. Certains récepteurs multimédias peuvent envoyer des événements personnalisés.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Pipeline Media Foundation](media-foundation-pipeline.md)
</dt> <dt>

[Architecture Media Foundation](media-foundation-architecture.md)
</dt> </dl>

 

 




