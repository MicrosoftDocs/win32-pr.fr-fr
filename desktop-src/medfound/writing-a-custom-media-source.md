---
description: Cette rubrique décrit comment implémenter une source de média personnalisée dans Microsoft Media Foundation.
ms.assetid: 82db6f32-ad94-4563-b8bd-8a5072c5b221
title: Écriture d’une source de média personnalisée
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8769fa16d4dcbfd3438b66f9a9e78c34274735a5
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127313514"
---
# <a name="writing-a-custom-media-source"></a>Écriture d’une source de média personnalisée

Cette rubrique décrit comment implémenter une source de média personnalisée dans Microsoft Media Foundation. Il contient les sections suivantes :

-   [Création du descripteur de présentation](#creating-the-presentation-descriptor)
-   [Démarrage de la source du média](#starting-the-media-source)
    -   [Cherche](#seeking)
-   [Suspension de la source du média](#pausing-the-media-source)
-   [Génération de données sources](#generating-source-data)
    -   [Exemples de demandes](#sample-requests)
    -   [Allouer des exemples](#allocating-samples)
    -   [Écarts dans le flux](#gaps-in-the-stream)
-   [Arrêt de la source du média](#shutting-down-the-media-source)
-   [Sources en direct](#live-sources)
-   [Rubriques connexes](#related-topics)

## <a name="creating-the-presentation-descriptor"></a>Création du descripteur de présentation

La méthode [**IMFMediaSource :: CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor) retourne une copie du descripteur de présentation de la source. Pour créer le descripteur de présentation, vous devez connaître le nombre de flux dans le contenu source et les formats possibles de chaque flux. Pour chaque flux, créez un descripteur de flux comme suit :

1.  Créer un tableau de types de médias. Chaque type de média dans le tableau représente un format possible pour le flux. Pour plus d’informations sur la création de types de médias, consultez [types de médias](media-types.md).
2.  Appelez [**MFCreateStreamDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatestreamdescriptor) pour créer le descripteur de flux. Transmettez le tableau de types de média. La fonction retourne un pointeur [**IMFStreamDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamdescriptor) .
3.  Appelez [**IMFStreamDescriptor :: GetMediaTypeHandler**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamdescriptor-getmediatypehandler) pour récupérer le gestionnaire de type de média du descripteur de flux.
4.  Appelez [**IMFMediaTypeHandler :: SetCurrentMediaType**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-setcurrentmediatype) pour définir le format de flux par défaut. Utilisez l’un des types de médias que vous avez créés à l’étape 1. En règle générale, vous devez utiliser le format avec la qualité la plus élevée.
5.  Vous pouvez éventuellement définir des attributs sur le descripteur de flux. Pour obtenir la liste des attributs qui s’appliquent aux descripteurs de flux, consultez attributs du descripteur de [flux](stream-descriptor-attributes.md).

Maintenant, créez le descripteur de présentation :

1.  Appelez [**MFCreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepresentationdescriptor) et transmettez le tableau de descripteurs de flux. La fonction retourne un pointeur [**IMFPresentationDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor) .
2.  Choisissez la sélection de flux par défaut en appelant [**IMFPresentationDescriptor :: SelectStream**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-selectstream) pour sélectionner un ou plusieurs flux. Au moins un flux doit être sélectionné dans la configuration par défaut.
3.  Vous pouvez éventuellement définir des attributs sur le descripteur de présentation. Pour obtenir la liste des attributs qui s’appliquent aux descripteurs de flux, consultez attributs du descripteur de [Présentation](presentation-descriptor-attributes.md).

Vous devez créer le descripteur de présentation une seule fois, au démarrage ou une fois que la source a analysé suffisamment les données sources pour déterminer le contenu. La méthode [**CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor) doit retourner une copie du descripteur de présentation. Pour créer la copie, appelez [**IMFPresentationDescriptor :: Clone**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-clone). Le retour d’une copie empêche le client de modifier l’état du descripteur de présentation d’origine, tel que les attributs ou la sélection de flux. Toutefois, sachez que **clone** crée une copie superficielle, de sorte que le client peut potentiellement modifier les descripteurs de flux sous-jacents.

## <a name="starting-the-media-source"></a>Démarrage de la source du média

La méthode [**IMFMediaSource :: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) démarre la source du média ou cherche à une nouvelle position. Un appel à **Start** provoque une *recherche* lorsque l’état précédent a été suspendu ou en cours d’exécution, et une nouvelle heure de début est spécifiée. Dans le cas contraire, la méthode **Start** provoque un *démarrage*. Une fois l’opération de **démarrage** terminée, envoyez les événements suivants.

1.  Envoyez un événement [MENewStream](menewstream.md) pour chaque nouveau flux, autrement dit, chaque flux qui a été désélectionné précédemment et qui est maintenant sélectionné. Les données d’événement sont un pointeur vers le flux.
2.  Envoyez un événement [MEUpdatedStream](meupdatedstream.md) pour chaque flux précédemment sélectionné et est toujours sélectionné. Les données d’événement sont un pointeur vers le flux. (N’envoyez pas d’événement pour les flux désélectionnés.)
3.  Si la source recherche, envoyer un événement [MESourceSeeked](mesourceseeked.md) . Sinon, envoyer un événement [MESourceStarted](mesourcestarted.md) . Les données d’événement sont l’heure de début spécifiée dans la méthode [**Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) . Pour l’événement MESourceStarted, si l’heure de début est VT \_ vide, définissez l’attribut de [**\_ \_ \_ \_ démarrage réel**](mf-event-source-actual-start-attribute.md) de la source de l’événement MF sur l’événement. La valeur de l’attribut est l’heure de début réelle.
4.  Pour chaque flux, si la source recherche, envoyer un événement [MEStreamSeeked](mestreamseeked.md) . Sinon, envoyer un événement [MEStreamStarted](mestreamstarted.md) . Les données d’événement sont l’heure de début. (La source du média peut faire la file d’attente d’un événement sur le flux en appelant la méthode [**IMFMediaEventGenerator :: QueueEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-queueevent) du flux.)

Lorsqu’un flux est désélectionné, arrêtez le flux. Le flux ne doit pas défiler plus d’événements à ce stade.

Le format d’heure de la méthode [**Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) est indiqué dans le paramètre *pguidTimeFormat* . Le format d’heure standard, indiqué par le **GUID \_ null**, est de 100 à nanosecondes unités. Une source de média doit prendre en charge ce format d’heure.

### <a name="seeking"></a>Cherche

Lors de la recherche, la position de départ demandée peut ne pas se trouver sur une limite d’échantillon exacte. En outre, pour le contenu compressé, la position de début peut se situer entre les images clés. Un flux doit fournir des échantillons à partir du point le plus ancien nécessaire pour produire un exemple non compressé à la position de départ demandée. Pour la vidéo, cela signifie démarrer à partir de l’image clé précédente. Le pipeline est chargé de supprimer les frames supplémentaires du décodeur, afin que la lecture commence à l’heure demandée.

L’heure de début indiquée dans les événements source ([MESourceStarted](mesourcestarted.md), [MESourceSeeked](mesourceseeked.md), [MEStreamStarted](mestreamstarted.md)et [MEStreamSeeked](mestreamseeked.md)) est l’heure de début demandée (la valeur donnée dans la méthode [**Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) ), quelle que soit la position de début réelle.

Par exemple, supposons que les premières images d’un flux vidéo présentent les caractéristiques suivantes :



| Exemple     | 1       | 2       | 3        | 4        |
|------------|---------|---------|----------|----------|
| Temps       | 33 ms | 66 ms | 100 ms | 133 ms |
| Image clé ? | Oui     | Non      | Non       | Oui      |



 

Si la méthode [**Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) est appelée avec une valeur de 100 millisecondes, la source doit générer une vidéo à partir de l’image 1, la première image clé avant cette heure. L’événement de début indiquera toujours 100 millisecondes dans les données d’événement.

## <a name="pausing-the-media-source"></a>Suspension de la source du média

La méthode [**IMFMediaSource ::P ause**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-pause) interrompt la source du média.

Lorsque la source est suspendue, un flux peut créer de nouveaux exemples et les stocker dans une file d’attente, mais le flux ne remet pas les exemples. Voici quelques exceptions à cette règle :

-   Les sources dynamiques doivent supprimer les données pendant la suspension.
-   Si la source obtient des données à partir d’un réseau, elle peut suspendre le serveur.

Si le client appelle [**IMFMediaStream :: RequestSample**](/windows/desktop/api/mfidl/nf-mfidl-imfmediastream-requestsample) alors que la source est suspendue, la demande est également mise en file d’attente jusqu’à ce que la source soit de nouveau redémarrée. Les requêtes ne doivent pas être supprimées.

La suspension est autorisée uniquement à partir de l’état Démarré. Sinon, la [**suspension**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-pause) doit retourner **MF E une \_ \_ \_ \_ transition d’État non valide**.

## <a name="generating-source-data"></a>Génération de données sources

Media Foundation utilise un *modèle d’extraction*, ce qui signifie que les flux génèrent et fournissent des exemples en réponse aux demandes du pipeline. Un flux peut fournir des exemples lorsque la source du média est en cours d’exécution et que le flux est sélectionné. Un flux fournit des données uniquement lorsque le client demande un nouvel exemple.

### <a name="sample-requests"></a>Exemple de demande

Le client demande un nouvel exemple en appelant [**IMFMediaStream :: RequestSample**](/windows/desktop/api/mfidl/nf-mfidl-imfmediastream-requestsample). Voici la séquence des opérations :

1.  Le client appelle [**IMFMediaStream :: RequestSample**](/windows/desktop/api/mfidl/nf-mfidl-imfmediastream-requestsample). L’argument est un pointeur vers un objet de *jeton* facultatif que le client utilise pour effectuer le suivi de la requête. Le client implémente le jeton. Les jetons doivent exposer l’interface **IUnknown** . Le client peut également passer un pointeur NULL au lieu d’un jeton.
2.  Si le client a fourni un jeton, le flux multimédia appelle **AddRef** sur le jeton et le place dans une file d’attente premier entré, premier sorti. La méthode retourne, et les étapes restantes se produisent de manière asynchrone.

3.  Quand davantage de données sont disponibles, le flux de média crée un nouvel exemple. (Cette étape est décrite plus en détail dans la section suivante.)
4.  Le flux multimédia extrait le premier jeton de la file d’attente.
5.  Si le jeton n’est pas **null**, le flux de média définit l’attribut de [**\_ jeton MFSampleExtension**](mfsampleextension-token-attribute.md) sur l’exemple de support. La valeur de l’attribut est un pointeur vers le jeton.
6.  Le flux de média envoie un événement [MEMediaSample](memediasample.md) . Les données d’événement sont un pointeur vers l’interface [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) de l’exemple.
7.  Si le client a fourni un jeton, le flux multimédia appelle la **version finale** sur l’objet de jeton.

Si le flux de média ne peut pas satisfaire la requête [**RequestSample**](/windows/desktop/api/mfidl/nf-mfidl-imfmediastream-requestsample) du client, il extrait le jeton de la file d’attente et appelle la **libération** sur le jeton, mais n’envoie pas d’événement [MEMediaSample](memediasample.md) .

Le client peut utiliser le jeton pour suivre l’état de la demande. Lorsque le client reçoit l’événement [MEMediaSample](memediasample.md) , il peut obtenir le jeton de l’exemple et le mettre en correspondance avec la requête d’origine. Le client peut également utiliser le jeton pour déterminer si la source du média a supprimé la demande. Si le nombre de références du jeton est égal à zéro et que le flux de média n’envoie pas d’événement MEMediaSample, cela signifie que la requête a été supprimée.

Les étapes répertoriées ici supposent que la méthode [**RequestSample**](/windows/desktop/api/mfidl/nf-mfidl-imfmediastream-requestsample) est implémentée en tant qu’opération asynchrone. Si la méthode est synchrone, vous n’avez pas besoin de placer le jeton de requête dans une file d’attente. Toutefois, si la génération de données prend beaucoup de temps, une approche asynchrone est recommandée, par exemple, si la source lit les données à partir d’un flux d’octets.

Le flux est responsable de la mise en mémoire tampon des données qui s’accumulent entre les appels à [**RequestSample**](/windows/desktop/api/mfidl/nf-mfidl-imfmediastream-requestsample).

Lorsque le flux multimédia atteint la fin du flux, il envoie un événement [MEEndOfStream](meendofstream.md) après le dernier échantillon. Une fois que chaque flux est terminé, la source du média envoie un événement [MEEndOfPresentation](meendofpresentation.md) . Une fois qu’un flux de données multimédia envoie l’événement MEEndOfStream, la méthode [**RequestSample**](/windows/desktop/api/mfidl/nf-mfidl-imfmediastream-requestsample) retourne **MF \_ E \_ End \_ du \_ flux** jusqu’à ce que la source soit redémarrée.

### <a name="allocating-samples"></a>Allouer des exemples

Lorsque le flux est prêt à remplir un exemple de demande en attente, il crée un nouvel exemple et ajoute une ou plusieurs mémoires tampons de média à l’exemple. Pour plus d’informations sur la création de mémoires tampons de média, consultez [mémoires tampons de média](media-buffers.md).

Le flux doit définir l’horodatage et la durée, s’ils sont connus. L’horodatage est relatif à la source. Dans la plupart des cas, le début du contenu correspond à un horodatage de zéro. Par exemple, si la source lit à partir d’un fichier multimédia, le début du fichier aurait un horodatage égal à zéro.

L’horodatage de l’échantillon n’est pas nécessairement égal à l’heure de la présentation. La session multimédia se traduit de l’heure de la source à l’heure de la présentation. Pour les données compressées, le flux doit générer les données à partir de l’image clé la plus proche avant l’heure de début. Cela permet au décodeur de remettre le frame qui apparaît à l’heure de début demandée. (Sinon, le décodeur doit attendre l’image clé suivante.)

Si la vitesse de lecture est plus rapide ou plus lente que 1,0, le pipeline ajuste la vitesse de l’horloge de la présentation. La source n’ajuste pas les horodatages sur les échantillons.

La source peut définir des informations supplémentaires sur l’exemple en définissant des attributs. Pour obtenir la liste des exemples d’attributs, consultez [exemples d’attributs](sample-attributes.md).

### <a name="gaps-in-the-stream"></a>Écarts dans le flux

Si un flux contient un intervalle de longueur significative, il est recommandé que le flux envoie un événement [MEStreamTick](mestreamtick.md) . Cet événement avertit le client qu’un exemple est manquant. Les données d’événement sont l’horodatage de l’échantillon manquant, en unités de 100 nanosecondes (**VT \_ i8**). Cet événement peut enregistrer les composants en aval qui n’arrivent pas à attendre. Le flux peut envoyer autant d’événements MEStreamTick que nécessaire pour couvrir l’intervalle dans le flux.

## <a name="shutting-down-the-media-source"></a>Arrêt de la source du média

Lorsque le client a terminé à l’aide de la source du média, il appelle [**IMFMediaSource :: Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown). Dans cette méthode, la source du média doit rompre les nombres de références circulaires. En règle générale, il y aura des références circulaires entre la source du média et les flux multimédias.

Si vous utilisez la file d’attente d’événements pour implémenter [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator), appelez [**IMFMediaEventQueue :: Shutdown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventqueue-shutdown) dans la file d’attente d’événements. Cette méthode arrête la file d’attente des événements et signale à tout appelant qui attend un événement.

Après l’arrêt, toutes les méthodes sur la source retournent l' **\_ \_ arrêt MF E**, à l’exception des méthodes **IUnknown** .

## <a name="live-sources"></a>Sources en direct

à partir de Windows 7, Media Foundation prend automatiquement en charge les périphériques de capture audio et vidéo. Pour la vidéo, l’appareil doit fournir un minipilote de streaming de noyau (KS) dans la catégorie capture vidéo. Media Foundation utilise le chemin PnP pour énumérer l’appareil. pour l’audio, Media Foundation utilise l’API MMDevice (Windows Multimedia Device) pour énumérer les appareils de point de terminaison audio. Si l’appareil répond à ces critères, il n’est pas nécessaire d’implémenter une source de média personnalisée.

Toutefois, vous souhaiterez peut-être implémenter une source de média personnalisée pour un autre type d’appareil ou une autre source de données active. Il n’existe que quelques différences entre une source en direct et d’autres sources multimédias :

-   Dans la méthode [**IMFMediaSource :: GetCharacteristics**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-getcharacteristics) , retourne le **MFMEDIASOURCE \_ indicateur \_ Live** .
-   Le premier exemple doit avoir un horodatage égal à zéro.
-   Les États des événements et de la diffusion en continu sont gérés de la même façon que les sources de média, à l’exception de l’état suspendu.
-   Pendant la suspension, ne pas placer les exemples en file d’attente. Supprimer toutes les données générées pendant la suspension.
-   En règle générale, les sources en direct ne prennent pas en charge la recherche, la lecture inversée ou le contrôle du débit.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Sources multimédias](media-sources.md)
</dt> <dt>

[Didacticiel : écriture d’une source de média personnalisée](tutorial--writing-a-custom-media-source.md)
</dt> </dl>

 

 



