---
description: Cette rubrique décrit comment les objets de pipeline personnalisés peuvent prendre en charge des vitesses de lecture variables, y compris la lecture inversée. Pour plus d’informations sur l’utilisation du contrôle de taux d’une application, consultez la section contrôle de la fréquence.
ms.assetid: 077678db-ca5a-423b-9430-93497113d639
title: Mise en œuvre du contrôle de taux
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5fd78cbbb95316a0d4ed12a50c9d3aa8954fe8a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127531893"
---
# <a name="implementing-rate-control"></a>Mise en œuvre du contrôle de taux

Cette rubrique décrit comment les objets de pipeline personnalisés peuvent prendre en charge des vitesses de lecture variables, y compris la lecture inversée. Pour plus d’informations sur l’utilisation du contrôle de taux d’une application, consultez la section contrôle de la [fréquence](rate-control.md).

Cette rubrique contient les sections suivantes :

-   [Sources multimédias](#media-sources)
-   [Transformations de Media Foundation](#media-foundation-transforms)
    -   [Lecture inversée](#reverse-playback)
-   [Récepteurs de médias](#media-sinks)
-   [Rubriques connexes](#related-topics)

Si vous écrivez un objet de pipeline Microsoft Media Foundation (une source multimédia, une transformation ou un récepteur multimédia), vous devrez peut-être prendre en charge des taux de lecture variables. Pour ce faire, implémentez les interfaces suivantes :

1.  Implémentez l’interface [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice) .
2.  Prendre en charge le service de contrôle de la **\_ Vitesse \_ \_ MF** . (Voir [interfaces de service](service-interfaces.md).)
3.  Implémentez l’interface [**IMFRateSupport**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport) , qui obtient les vitesses de lecture prises en charge par l’objet.
4.  Implémentez l’interface [**IMFRateControl**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol) , qui obtient ou définit la vitesse de lecture.

## <a name="media-sources"></a>Sources multimédias

Si une source de média prend en charge le contrôle de fréquence, elle doit implémenter à la fois [**IMFRateSupport**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport) et [**IMFRateControl**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol). Dans le cas contraire, la session multimédia signale que la vitesse de lecture minimale et maximale est 1,0, quels que soient les autres composants du pipeline.

La vitesse de lecture n’affecte pas les durées de présentation des échantillons, de sorte que la source du média ne doit pas ajuster ses horodatages. Au lieu de cela, l’horloge de la présentation s’exécute à une vitesse plus rapide ou plus lente. Pour la lecture inversée, la source remet les échantillons dans l’ordre inverse, avec des horodateurs réduits.

Le paramètre *fThin* de la méthode [**IMFRateControl ::**](/windows/desktop/api/mfidl/nf-mfidl-imfratecontrol-setrate) sesupported indique si la source du média doit *Finer* le contenu. L’affinage s’applique principalement aux flux vidéo. En mode éclairci, la source supprime les images Delta et ne remet que les images clés. À des taux de lecture très élevés, la source peut ignorer certaines images clés (par exemple, remettre toutes les autres images clés).

La source n’a pas besoin de déposer des échantillons audio en mode éclairci. Toutefois, avec des taux de lecture très élevés, la source peut ne pas être en mesure de lire des données rapides nough pour remplir les exemples de demandes du pipeline. Dans ce cas, il se peut que la source doive supprimer des données audio. Dans ce cas, il doit tenter de remettre des échantillons audio qui sont proches des exemples de vidéos (en supposant que la source a les deux types de flux).

Lorsqu’un flux passe du mode éclairci et non dilué, il envoie un événement [MEStreamThinMode](mestreamthinmode.md) .

Lorsque la source du média termine un appel [**à**](/windows/desktop/api/mfidl/nf-mfidl-imfratecontrol-setrate)sesupport, elle envoie l’événement [MESourceRateChanged](mesourceratechanged.md) .

Pendant la lecture inversée :

-   La source du média fournit des échantillons dans l’ordre inverse, sans ajuster les horodatages.
-   Les horodatages dans un flux doivent diminuer de façon monotone.
-   Le début du contenu est considéré comme la fin du flux. Une fois que chaque flux multimédia remet le premier échantillon dans le flux (autrement dit, l’heure de la présentation = 0), il envoie l’événement [MEEndOfStream](meendofstream.md) .

## <a name="media-foundation-transforms"></a>Transformations de Media Foundation

En général, une Media Foundation Transform (MFT) n’a pas besoin d’une prise en charge explicite du contrôle de la fréquence, sauf si la table MFT implémente une lecture inversée non fine.

Si une MFT n’implémente pas l’interface [**IMFRateSupport**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport) , la session multimédia suppose les points suivants :

-   La table MFT prend en charge les vitesses de lecture arbitraire pour la lecture en avant, à la fois fine et non fine.
-   La table MFT prend en charge la lecture inverse fine, mais ne prend pas en charge la lecture inversée non fine.

Si l’une de ces conditions n’est pas remplie, la table MFT doit implémenter [**IMFRateSupport**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport) et [**IMFRateControl**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol).

### <a name="reverse-playback"></a>Lecture inversée

La session multimédia peut être lue en sens inverse même si une ou plusieurs transformations du pipeline ne prennent pas en charge explicitement la lecture inversée.

Si une MFT n’expose pas l’interface [**IMFRateSupport**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport) , la session multimédia *utilise l'* affinage pour la lecture inversée, comme suit :

-   La session multimédia envoie les images clés à la MFT de la manière habituelle, en appelant [**IMFTransform ::P rocessinput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput).

-   La session multimédia supprime les images Delta et les remplace par les événements [MEStreamTick](mestreamtick.md) .

-   Entre chaque exemple, la session de média vide la MFT, afin d’éviter toute erreur provoquée par le fait que les horodatages diminuent.

Un exemple est considéré comme une image clé si l’attribut [MFSampleExtension \_ CleanPoint](mfsampleextension-cleanpoint-attribute.md) est défini sur **true**, et est considéré comme un frame Delta si cet attribut a la valeur **false** ou n’est pas défini.

Si la table MFT implémente [**IMFRateSupport**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport), la session multimédia utilise cette interface pour déterminer si la table MFT prend en charge la lecture inversée non fine. Si la MFT prend en charge la lecture inversée non fine, la session multimédia remet tous les exemples, dans l’ordre inverse, sans supprimer les échantillons ni vider la MFT.

Si une table MFT prend en charge la lecture inversée non fine, elle doit implémenter l’interface [**IMFRateControl**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol) . La session multimédia utilise cette interface pour notifier la table MFT en cas de lecture inversée. À ce stade, la MFT doit être préparée pour que les horodatages diminuent et que les images Delta arrivent dans l’ordre inverse. Un décodeur doit généralement mettre en mémoire tampon des échantillons jusqu’à ce qu’il ait reçu un groupe entier d’images, puis décoder l’ensemble du groupe d’images et sortir les images décodées dans l’ordre (inverse) correct.

## <a name="media-sinks"></a>Récepteurs de médias

Si un récepteur multimédia est sans *débit*, la session de média suppose que le récepteur multimédia peut gérer n’importe quel taux de lecture. Le récepteur multimédia n’a pas besoin d’implémenter [**IMFRateSupport**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport). (Un récepteur multimédia à débit retourne le MEDIASINK \_ Indicateur de débit à partir de la méthode [**IMFMediaSink :: GetCharacteristics**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-getcharacteristics) .)

Dans le cas contraire, un récepteur multimédia doit implémenter [**IMFRateSupport**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport) s’il peut gérer des vitesses de lecture autres que 1,0.

Les récepteurs multimédias ne doivent pas implémenter [**IMFRateControl**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol). Lorsque la vitesse de lecture change, l’horloge de la présentation appelle la méthode [**IMFClockStateSink :: OnClockSetRate**](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclocksetrate) du récepteur multimédia.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Contrôle de la fréquence](rate-control.md)
</dt> <dt>

[recherche, Avance rapide et la lecture inversée](seeking--fast-forward--and-reverse-play.md)
</dt> </dl>

 

 



