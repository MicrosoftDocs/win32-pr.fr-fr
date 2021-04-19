---
description: La classe CTransformFilter est une classe de base pour l’implémentation de filtres de transformation.
ms.assetid: 99db8252-a8db-4995-b4be-a6cf944be869
title: CTransformFilter, classe (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d24c305b28641fcee366b4e906b87008decac014
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106539207"
---
# <a name="ctransformfilter-class"></a>CTransformFilter, classe

![hiérarchie de la classe ctransformfilter](images/tfrm03.png)

La `CTransformFilter` classe est une classe de base pour l’implémentation de filtres de transformation. Cette classe est conçue pour implémenter un filtre de transformation avec une broche d’entrée et une broche de sortie. Il utilise des allocateurs distincts pour la broche d’entrée et la broche de sortie. Pour créer un filtre qui traite les données en place, utilisez la classe [**CTransInPlaceFilter**](ctransinplacefilter.md) .

Ce filtre utilise la classe [**CTransformInputPin**](ctransforminputpin.md) pour sa broche d’entrée et la classe [**CTransformOutputPin**](ctransformoutputpin.md) pour sa broche de sortie. En règle générale, vous n’avez pas besoin de remplacer ces classes pin. La plupart des méthodes PIN appellent les méthodes correspondantes sur la `CTransformFilter` classe, ce qui vous permet de substituer les méthodes de filtre si nécessaire. Le filtre crée les deux codes confidentiels dans la méthode [**CTransformFilter :: GetPin**](ctransformfilter-getpin.md) . Si vous remplacez les classes de code confidentiel, vous devez remplacer **GetPin** pour créer vos codes confidentiels personnalisés.

Pour utiliser cette classe, dérivez une nouvelle classe de `CTransformFilter` et implémentez les méthodes suivantes :

-   [**CTransformFilter::CheckInputType**](ctransformfilter-checkinputtype.md)
-   [**CTransformFilter::CheckTransform**](ctransformfilter-checktransform.md)
-   [**CTransformFilter ::D ecideBufferSize**](ctransformfilter-decidebuffersize.md)
-   [**CTransformFilter::GetMediaType**](ctransformfilter-getmediatype.md)
-   [**CTransformFilter :: Transform**](ctransformfilter-transform.md)

Vous devrez peut-être substituer d’autres méthodes, en fonction des exigences de votre filtre.

## <a name="media-types"></a>Types de médias

La broche d’entrée de ce filtre ne propose aucun type de média ; Il s’appuie sur le filtre amont pour proposer les types de média pour la connexion. La raison de cette conception est que, dans la plupart des cas, le filtre en amont peut fournir plus d’informations sur le format. Par exemple, avec les formats vidéo, le filtre amont connaît les dimensions de la vidéo et la fréquence d’images, tandis que le filtre de transformation n’a aucun moyen de déterminer ces informations. Si vous souhaitez modifier ce comportement, remplacez la méthode [**GetMediaType**](ctransformfilter-getmediatype.md) de la broche d’entrée. Lorsque le filtre amont propose un type de média, la broche d’entrée appelle la méthode [**CheckInputType**](ctransformfilter-checkinputtype.md) du filtre (virtuel pur).

Tant que la broche d’entrée n’est pas connectée, la broche de sortie refuse toutes les connexions et ne retourne aucun type de média préféré. Une fois que la broche d’entrée est connectée, la broche de sortie retourne une liste de types préférés en appelant la méthode [**GetMediaType**](ctransformfilter-getmediatype.md) du filtre. Il vérifie les types de sortie pour la connexion via la méthode [**CheckTransform**](ctransformfilter-checktransform.md) du filtre. (Les deux méthodes sont virtuelles pures.) En règle générale, le type d’entrée détermine en partie les types de sortie acceptables.

Selon le filtre, vous souhaiterez peut-être inscrire certains des types de média pris en charge par le filtre, afin que l’objet [Mappeur de filtre](filter-mapper.md) puisse localiser votre filtre. Pour plus d’informations, consultez [comment inscrire des filtres DirectShow](how-to-register-directshow-filters.md).

## <a name="streaming"></a>Diffusion en continu

Cette classe ne met pas en file d’attente les données de sortie. Chaque exemple de sortie est remis à l’intérieur de la méthode [**IMemInputPin :: Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) . La méthode **Receive** appelle la méthode [**Transform**](ctransformfilter-transform.md) du filtre (également pure virtual) pour traiter les données.

Pour plus d’informations sur l’utilisation de cette classe, consultez [écriture de filtres de transformation](writing-transform-filters.md).



| Variables membres protégées                                                | Description                                                                                             |
|---------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------|
| [**m \_ bEOSDelivered**](ctransformfilter-m-beosdelivered.md)              | Indicateur qui spécifie si le filtre a envoyé une notification de fin de flux.                          |
| [**m \_ bSampleSkipped**](ctransformfilter-m-bsampleskipped.md)            | Indicateur qui spécifie si l’échantillon le plus récent a été supprimé.                                         |
| [**m \_ bQualityChanged**](ctransformfilter-m-bqualitychanged.md)          | Indicateur qui signale si la qualité a changé.                                                    |
| [**m \_ csFilter**](ctransformfilter-m-csfilter.md)                        | Section critique qui protège l’état du filtre.                                                        |
| [**m \_ csReceive**](ctransformfilter-m-csreceive.md)                      | Section critique qui protège l’état de diffusion en continu.                                                     |
| [**m \_ pInput**](ctransformfilter-m-pinput.md)                            | Pointeur vers la broche d’entrée.                                                                               |
| [**m \_ pOutput**](ctransformfilter-m-poutput.md)                          | Pointeur vers la broche de sortie.                                                                              |
| M&#233;thodes publiques                                                            | Description                                                                                             |
| [**CTransformFilter**](ctransformfilter-ctransformfilter.md)             | Méthode de constructeur.                                                                                     |
| [**~ CTransformFilter**](ctransformfilter--ctransformfilter.md)          | Méthode de destructeur.                                                                                      |
| [**GetPinCount**](ctransformfilter-getpincount.md)                       | Récupère le nombre de broches sur le filtre. Virtuels.                                                    |
| [**GetPin**](ctransformfilter-getpin.md)                                 | Récupère un code confidentiel. Virtuels.                                                                               |
| [**Transform**](ctransformfilter-transform.md)                           | Transforme un exemple d’entrée pour produire un échantillon de sortie. Virtuels.                                        |
| [**StartStreaming**](ctransformfilter-startstreaming.md)                 | Appelé lorsque le filtre bascule à l’état suspendu. Virtuels.                                           |
| [**StopStreaming**](ctransformfilter-stopstreaming.md)                   | Appelé lorsque le filtre bascule à l’état arrêté. Virtuels.                                          |
| [**AlterQuality**](ctransformfilter-alterquality.md)                     | Notifie le filtre qu’une modification de qualité est demandée. Virtuels.                                        |
| [**SetMediaType**](ctransformfilter-setmediatype.md)                     | Appelé lorsque le type de média est défini sur l’un des codes confidentiels du filtre. Virtuels.                                 |
| [**CheckConnect**](ctransformfilter-checkconnect.md)                     | Détermine si une connexion de code confidentiel est appropriée. Virtuels.                                               |
| [**BreakConnect**](ctransformfilter-breakconnect.md)                     | Libère un code confidentiel d’une connexion. Virtuels.                                                              |
| [**CompleteConnect**](ctransformfilter-completeconnect.md)               | Termine une connexion de code confidentiel. Virtuels.                                                                    |
| [**Çoive**](ctransformfilter-receive.md)                               | Reçoit un exemple de support, le traite et remet un échantillon de sortie au filtre en aval. Virtuels. |
| [**InitializeOutputSample**](ctransformfilter-initializeoutputsample.md) | Récupère un nouvel exemple de sortie et l’initialise.                                                       |
| [**EndOfStream**](ctransformfilter-endofstream.md)                       | Notifie le filtre qu’aucune donnée supplémentaire n’est attendue à partir de la broche d’entrée. Virtuels.                    |
| [**BeginFlush**](ctransformfilter-beginflush.md)                         | Commence une opération de vidage. Virtuels.                                                                      |
| [**EndFlush**](ctransformfilter-endflush.md)                             | Termine une opération de vidage. Virtuels.                                                                        |
| [**NewSegment**](ctransformfilter-newsegment.md)                         | Notifie le filtre que les exemples de supports reçus après cet appel sont regroupés en tant que segment. Virtuels.      |
| Méthodes virtuelles pures                                                      | Description                                                                                             |
| [**CheckInputType**](ctransformfilter-checkinputtype.md)                 | Vérifie si un type de média spécifié est acceptable pour l’entrée.                                          |
| [**CheckTransform**](ctransformfilter-checktransform.md)                 | Vérifie si un type de média d’entrée est compatible avec un type de média de sortie.                             |
| [**DecideBufferSize**](ctransformfilter-decidebuffersize.md)             | Définit les exigences de mémoire tampon de la broche de sortie.                                                              |
| [**GetMediaType**](ctransformfilter-getmediatype.md)                     | Récupère un type de média par défaut pour la broche de sortie.                                                    |
| Méthodes IMediaFilter                                                      | Description                                                                                             |
| [**Erreur**](ctransformfilter-stop.md)                                     | Arrête le filtre.                                                                                       |
| [**Suspendre**](ctransformfilter-pause.md)                                   | Suspend le filtre.                                                                                      |
| Méthodes IBaseFilter                                                       | Description                                                                                             |
| [**FindPin**](ctransformfilter-findpin.md)                               | Récupère le code confidentiel avec l’identificateur spécifié.                                                        |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Transfrm. h (include streams. h)</dt> </dl>                                                                                  |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



 

 




