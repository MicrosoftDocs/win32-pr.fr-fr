---
description: Configuration du codec DMOs
ms.assetid: 431b33f1-ceb0-4f1b-a9f2-72e88b63f973
title: Configuration du codec DMOs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4040c0a16c0311d14b0553336e1d9b70a7a6c1fd28a0f01277c955eea55ec7f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119958329"
---
# <a name="configuring-codec-dmos"></a>Configuration du codec DMOs

Cette rubrique décrit le processus de configuration du codec DMOs. Chaque codec a des procédures spécifiques, mais les informations communes à toutes sont décrites ici.

## <a name="configuring-dmo-inputs-and-outputs"></a>configuration des entrées et des sorties DMO

chaque DMO prend en charge des types d’entrée et de sortie spécifiques. Vous pouvez récupérer les types pris en charge pour les entrées et les sorties en appelant [**IMediaObject :: GetInputType**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-getinputtype) pour les entrées et [**IMediaObject :: GetOutputType**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-getoutputtype) pour les sorties. Vous pouvez énumérer les formats pris en charge en effectuant des appels répétés à l’une ou l’autre des méthodes, en incrémentant l’index de type avec chaque appel. lorsque l’index dépasse celui du type final pris en charge, l’appel retourne DMO \_ E \_ pas d' \_ autres \_ éléments.

Pour les codecs vidéo, un seul type de sortie ou type d’entrée est énuméré pour un sous-type de média donné. Pour les codecs audio, chaque type pris en charge est énuméré. Pour plus d’informations sur les types pris en charge pour les codecs individuels, consultez Utilisation de l' [audio](workingwithaudio.md) et [utilisation de la vidéo](workingwithvideo.md).

Après avoir configuré les types de médias pour les flux d’entrée et de sortie, définissez-les en appelant [**IMediaObject :: SetInputType**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-setinputtype) et [**IMediaObject :: SetOutputType**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-setoutputtype) respectivement. ces deux méthodes retournent **DMO \_ \_ type E \_ non \_ accepté** si le type spécifié n’est pas valide.

## <a name="configuring-the-codec-dmos-for-encoding"></a>Configuration du codec DMOs pour l’encodage

tous les codecs vidéo et Windows Media Audio prennent en charge un large éventail de fonctionnalités d’encodage. ces fonctionnalités sont généralement configurées en définissant des propriétés sur le DMO à l’aide des méthodes de l’interface **IPropertyBag** . Certaines propriétés sont configurées à l’aide d’interfaces de codec spécialisées. Ces interfaces sont répertoriées pour chaque codec dans la section [objets codec](codecobjects.md).

l’ordre général des opérations de configuration d’un encodage DMO est le suivant :

1.  Configurez les fonctionnalités du codec comme vous le souhaitez à l’aide des méthodes de **IPropertyBag**.
2.  utilisez les interfaces du DMO du codec pour configurer des fonctionnalités supplémentaires, si nécessaire.
3.  Configurez les types d’entrée et de sortie. L’ordre dans lequel les types doivent être configurés varie en fonction des codecs individuels. Pour plus d’informations, consultez [utilisation de l’audio](workingwithaudio.md) et [utilisation de la vidéo](workingwithvideo.md).

## <a name="configuring-the-codec-dmos-for-decoding"></a>Configuration du codec DMOs pour le décodage

Le décodage est plus simple que l’encodage, car un nombre inférieur de fonctionnalités de décodeur est pris en charge.

l’ordre général des opérations de configuration d’une DMO de décodage est le suivant :

1.  Configurez les fonctionnalités du décodeur comme vous le souhaitez à l’aide des méthodes de **IPropertyBag**.
2.  Définissez le type d’entrée sur le type utilisé pour la sortie de l’encodeur.
3.  Configurez le type de sortie. Les types de sortie pris en charge sont différents pour les différentes entrées.

> [!Note]  
> Il est important d’utiliser le même type de média pour l’entrée du décodeur que celui utilisé pour la sortie de l’encodeur. cela est dû au fait que les codecs Windows Media Audio et vidéo utilisent des formats multimédias avec des données supplémentaires. ces données sont ajoutées à la structure vers laquelle pointe le membre **pbFormat** de la structure [**de \_ \_ TYPE de média DMO**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type) (généralement [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) ou [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85))). Pour certains types, les données supplémentaires font partie du type de sortie de l’encodeur énuméré. D’autres types nécessitent que vous ajoutiez ces données manuellement. Sans les données de format étendu, vous ne pouvez pas décoder le contenu compressé.

 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Utilisation du codec DMOs](workingwithcodecdmos.md)
</dt> </dl>

 

 
