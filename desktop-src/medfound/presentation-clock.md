---
description: Horloge de présentation
ms.assetid: cb8bb62a-ef80-4de0-9a44-3bb77edc9dd5
title: Horloge de présentation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f0219b6384373fd75bc8a424935e502841071f69eaa9ae719ec6ed35c950218
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118239157"
---
# <a name="presentation-clock"></a>Horloge de présentation

L' *horloge de présentation* est un objet qui génère l’heure de l’horloge d’une présentation. L’heure indiquée par l’horloge de la présentation est appelée heure de la *Présentation*. Tous les flux d’une présentation sont synchronisés avec l’heure de la présentation. L’horloge de présentation expose les interfaces suivantes.



| Interface                                            | Description                                         |
|------------------------------------------------------|-----------------------------------------------------|
| [**IMFPresentationClock**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationclock) | Interface principale pour l’utilisation de l’horloge de présentation. |
| [**IMFRateControl**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol)             | Contrôle le taux d’horloge.                            |
| [**IMFTimer**](/windows/desktop/api/mfidl/nn-mfidl-imftimer)                         | Fournit un rappel de minuterie.                          |
| [**IMFShutdown**](/windows/desktop/api/mfidl/nn-mfidl-imfshutdown)                   | Arrête l’horloge de la présentation.                  |



 

Les récepteurs multimédias utilisent l’heure de présentation pour planifier le moment du rendu des exemples. Chaque fois qu’un récepteur multimédia reçoit un nouvel exemple, il obtient l’horodatage de l’échantillon et restitue l’échantillon à l’heure indiquée, ou aussi près que possible de cette heure. Étant donné que tous les récepteurs multimédia d’une topologie partagent la même horloge de présentation, plusieurs flux (tels que l’audio et la vidéo) sont synchronisés. Les sources et les transformations multimédias n’utilisent pas l’horloge de présentation, car elles ne planifient pas le moment où les exemples doivent être fournis. Au lieu de cela, ils produisent des exemples chaque fois que le pipeline demande un nouvel échantillon.

Si vous utilisez la session multimédia pour la lecture, la session multimédia gère tous les détails de la création de l’horloge de présentation, la sélection d’une source de temps et la notification des récepteurs de médias. Votre application peut utiliser l’horloge de présentation pour atteindre l’heure de présentation actuelle pendant la lecture, mais elle n’appelle aucune méthode sur l’horloge de présentation.

## <a name="clock-time-and-clock-states"></a>Horloge et état de l’horloge

Pour vous procurer l’heure de l’horloge la plus récente à partir de l’horloge de présentation, appelez [**IMFPresentationClock :: getTime**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationclock-gettime). Les temps d’horloge sont toujours en unités de 100 nanosecondes, donc une seconde est 10 millions (10 ^ 7) cycles. Cela correspond à une fréquence de 10 MHz.

L’horloge de la présentation a trois États : en cours d’exécution, en pause et arrêtée.

-   Pour exécuter l’horloge, appelez [**IMFPresentationClock :: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationclock-start). La méthode **Start** spécifie l’heure de début de l’horloge. Lorsque l’horloge est en cours d’exécution, l’heure de l’horloge s’incrémente de l’heure de début, à la fréquence d’horloge actuelle.
-   Pour suspendre l’horloge, appelez [**IMFPresentationClock ::P ause**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationclock-pause). Lorsque l’horloge est suspendue, l’heure de l’horloge n’avance pas, et [**getTime**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationclock-gettime) retourne l’heure à laquelle l’horloge a été suspendue.
-   Pour arrêter l’horloge, appelez [**IMFPresentationClock :: Stop**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationclock-stop). Lorsque l’horloge est arrêtée, l’heure de l’horloge n’avance pas et la fonction [**getTime**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationclock-gettime) retourne la valeur zéro.

Par défaut, l’horloge avance à un taux de 1,0, ce qui signifie 1 graduation par 100 nanosecondes. Pour modifier la vitesse d’avance de l’horloge, interrogez l’horloge de présentation pour l’interface [**IMFRateControl**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol) et appelez [**IMFRateControl ::**](/windows/desktop/api/mfidl/nf-mfidl-imfratecontrol-setrate)se.

Les objets peuvent recevoir des notifications de changements d’État (y compris les changements de taux) à partir de l’horloge de la présentation. Pour recevoir des notifications, implémentez l’interface [**IMFClockStateSink**](/windows/desktop/api/mfidl/nn-mfidl-imfclockstatesink) et appelez [**IMFPresentationClock :: AddClockStateSink**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationclock-addclockstatesink) sur l’horloge de présentation. Avant de fermer, appelez [**IMFPresentationClock :: RemoveClockStateSink**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationclock-removeclockstatesink) pour annuler l’inscription de l’objet. Les récepteurs de médias utilisent ce mécanisme pour recevoir des notifications de l’horloge.

## <a name="presentation-times"></a>Durées de présentation

Un récepteur multimédia tente de planifier chaque exemple afin que l’exemple soit rendu à l’heure correcte ou aussi près que possible de l’heure correcte. Les définitions suivantes s’appliquent :

-   *Heure de la présentation.* Heure à laquelle un échantillon doit être rendu. L’heure est donnée en unités de nanosecondes de 100.
-   *Heure du média.* Heure relative au début du contenu. Par exemple, si un fichier vidéo a une longueur de 10 secondes, le point moyen du fichier est de 5 secondes.
-   *Horodatage.* Heure marquée sur un échantillon de média. Pour connaître l’horodatage, appelez [**IMFSample :: GetSampleTime**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-getsampletime). Lorsqu’une source de média produit un exemple, elle définit l’horodatage comme étant égal à l’heure du support. La session multimédia traduit la date et l’heure de la présentation.

Par défaut, l’heure du média et l’heure de la présentation sont les mêmes, par exemple, si une image vidéo apparaît 5 secondes dans le fichier source, l’heure du support et l’heure de la présentation sont toutes les cinq secondes. Si vous utilisez la [source Sequencer](sequencer-source.md), le modèle de minutage est un peu plus compliqué pour permettre des transitions lisses entre les segments. Pour plus d’informations sur le modèle de minutage de la source de Sequencer, consultez [durée de présentation des séquences](sequence-presentation-times.md).

La source du média définit toujours l’horodatage comme étant égal à l’heure du support. Si l’heure de présentation n’est pas alignée sur l’heure du média, la session multimédia convertit les horodatages sur les échantillons de support. Au moment où le récepteur reçoit un échantillon, l’horodatage de l’exemple a été converti en heure de présentation. Le récepteur planifie l’exemple en fonction de l’heure actuelle de l’horloge de la présentation. (Les récepteurs de débit sont une exception, car ils ignorent l’horloge de présentation.)

Si l’application cherche à une nouvelle position, la session multimédia redémarre l’horloge de la présentation à l’heure de recherche spécifiée. Par exemple, si l’application cherche à la position de 5 secondes dans le fichier, la session multimédia démarre l’horloge à 5 secondes. La source du média peut fournir des échantillons avec un horodatage légèrement antérieur si le temps de recherche ne se situe pas dans une limite d’image clé. Cela est nécessaire pour que les décodeurs puissent décoder tous les frames. La session multimédia supprime ou tronque les échantillons avant qu’ils n’atteignent les récepteurs multimédia, afin de correspondre à l’heure de recherche demandée. Par exemple, si le temps de recherche est de 5 secondes, le premier échantillon audio peut commencer à 4,5 secondes. La session multimédia découpera les 0,5 premières secondes du premier exemple audio décodé.

## <a name="creating-the-presentation-clock"></a>Création de l’horloge de présentation

Pour créer l’horloge de présentation, appelez [**MFCreatePresentationClock**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepresentationclock). Pour arrêter l’horloge, interrogez l’interface [**IMFShutdown**](/windows/desktop/api/mfidl/nn-mfidl-imfshutdown) et appelez [**IMFShutdown :: Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfshutdown-shutdown). L’appelant de **MFCreatePresentationClock** est chargé d’appeler **Shutdown**; dans la plupart des cas, il s’agit de la session multimédia plutôt que de l’application.

## <a name="presentation-time-sources"></a>Sources de temps de présentation

En dépit de son nom, l’horloge de présentation n’implémente pas réellement une horloge. Au lieu de cela, il obtient les heures d’horloge d’un autre objet, appelé *source de temps de présentation*. La source de temps peut être n’importe quel objet qui génère des battements d’horloge précis et expose l’interface [**IMFPresentationTimeSource**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationtimesource) . L'illustration ci-dessous montre ce processus.

![Diagramme montrant la relation entre l’horloge de présentation et la source de temps de présentation](images/dedc255c-eb6d-49fc-8892-7b6076ed4488.gif)

Lorsque l’horloge de présentation est créée pour la première fois, elle n’a pas de source de temps. Pour définir la source de temps, appelez [**IMFPresentationClock :: SetTimeSource**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationclock-settimesource) avec un pointeur vers l’interface [**IMFPresentationTimeSource**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationtimesource) de la source de temps. Une source de temps prend en charge les mêmes États que l’horloge de présentation (en cours d’exécution, suspendue et arrêt) et doit implémenter l’interface [**IMFClockStateSink**](/windows/desktop/api/mfidl/nn-mfidl-imfclockstatesink) . L’horloge de présentation utilise cette interface pour notifier la source de temps quand modifier l’État. De cette façon, la source de temps fournit les battements d’horloge, mais l’horloge de présentation lance les changements d’état de l’horloge.

Certains récepteurs multimédias ont accès à une horloge précise et, par conséquent, exposent l’interface [**IMFPresentationTimeSource**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationtimesource) . En particulier, le convertisseur audio peut utiliser la fréquence de la carte audio comme une horloge. Dans la lecture audio, il est utile que le convertisseur audio agisse en tant que source de temps, de sorte que la vidéo est synchronisée avec la vitesse de lecture audio. Cela produit généralement de meilleurs résultats que de tenter de faire correspondre l’audio à une horloge externe.

Media Foundation fournit également une source de temps de présentation basée sur l’horloge système. Pour créer cet objet, appelez [**MFCreateSystemTimeSource**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatesystemtimesource). La source de temps système peut être utilisée quand aucun récepteur multimédia ne fournit de source de temps.

En général, un récepteur multimédia doit utiliser l’horloge de présentation qui lui est fournie, quelle que soit la source de temps utilisée par l’horloge de présentation. Cette règle s’applique même lorsqu’un récepteur multimédia implémente [**IMFPresentationTimeSource**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationtimesource). Si l’horloge de la présentation utilise une autre source de temps, le récepteur multimédia doit suivre cette source de temps, et non sa propre horloge interne.

Il existe deux situations dans lesquelles un récepteur multimédia ne suivra pas l’horloge de présentation :

-   Certains récepteurs multimédias ne sont pas *débités*. Si un récepteur multimédia est sans débit, il consomme les échantillons le plus rapidement possible, sans les planifier en fonction de l’horloge de la présentation. En règle générale, les récepteurs de débit écrivent les données dans un fichier. il est donc préférable d’effectuer l’opération aussi rapidement que possible. Un récepteur sans débit retourne l’indicateur MEDIASINK sans \_ débit dans sa méthode [**IMFMediaSink :: GetCharacteristics**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-getcharacteristics) . Lorsque tous les récepteurs d’une topologie sont sans débit, la session de média transmet les données via le pipeline aussi rapidement que possible.

-   Certains récepteurs multimédias ne peuvent pas faire correspondre les taux à une source de temps autre qu’eux-mêmes. Si c’est le cas, le récepteur retourne l' \_ indicateur MEDIASINK ne peut pas correspondre à l' \_ \_ indicateur Clock dans sa méthode [**GetCharacteristics**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-getcharacteristics) . Le pipeline peut toujours utiliser une autre source de temps, mais les résultats ne seront pas optimaux. Le récepteur sera probablement en retard et provoquera des problèmes lors de la lecture.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[API de plateforme Media Foundation](media-foundation-platform-apis.md)
</dt> </dl>

 

 



