---
description: DMO Fondamentaux
ms.assetid: eaf453d2-69f8-432a-8a58-1ed70778f182
title: DMO Concepts de base (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f24c7fb988d5e5225f292585a5562cce22e67c007175fa7ddc4cd86e40ec1d18
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118742358"
---
# <a name="dmo-basics-microsoft-media-foundation"></a>DMO Concepts de base (Microsoft Media Foundation)

cette rubrique fournit une brève présentation de DMOs, car elles se rapportent à Windows codecs multimédias. Pour plus d’informations sur DMOs, consultez [objets multimédia DirectX](../directshow/directx-media-objects.md).

un DMO est un objet COM qui transforme des données. Vous lui transmettez des données et retourne les données transformées. dans le cas d’un encodeur de codec DMO, vous entrez des données multimédias non compressées et le DMO fournit des données multimédias compressées. Le principal avantage de l’utilisation de DMOs est qu’ils implémentent tous la même interface de base, [**IMediaObject**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject), qui simplifie leur utilisation, car vous pouvez utiliser le même objet, quel que soit le type de transformation effectué.

Étant donné que des variables sont impliquées dans une transformation de données, la transformation audio et vidéo doit prendre en compte la large gamme de configurations de médias possibles. les codecs Windows Media Audio et vidéo prennent également en charge un certain nombre de fonctionnalités spéciales que vous devez être en mesure de configurer à l’aide du DMO.

En général, les informations sur les variables requises par le codec DMOs pour compresser et décompresser les supports numériques sont transmises de trois manières :

-   définissez le type d’entrée sur la DMO pour transmettre les caractéristiques du média non compressé que vous transmettez à un encodeur DMO, ainsi que les caractéristiques du média compressé que vous transmettez à un décodeur DMO.
-   définissez le type de sortie sur le DMO pour transmettre les caractéristiques du média compressé qui sont fournies par un encodeur DMO, ainsi que les caractéristiques du support non compressé qui sont fournies par un décodeur DMO.
-   À l’aide des méthodes de l’interface **IPropertyBag** , configurez d’autres paramètres prenant en charge les diverses fonctionnalités du codec DMOs en tant que propriétés. **IPropertyBag** est une interface COM standard qui est prise en charge par tous les DMOs de codec.

En outre, certaines fonctionnalités du codec sont gérées à l’aide d’autres interfaces spécifiques au codec DMOs. Ces interfaces sont répertoriées pour chaque codec dans la section [objets codec](codecobjects.md).

Les types d’entrée et de sortie sont spécifiques aux flux d’entrée et de sortie. Chaque flux représente une représentation discrète du contenu. par exemple, l’encodeur Windows Media Video DMO possède un flux d’entrée unique et deux flux de sortie. Le flux d’entrée accepte les exemples vidéo non compressés. Le premier des deux flux de sortie fournit des exemples compressés. l’autre fournit des exemples non compressés. Les exemples individuels dans un flux de sortie représentent le même contenu que les échantillons correspondants dans l’autre flux, mais chaque flux remet ces exemples dans un format différent.

Chaque flux (entrée ou sortie) prend en charge un ou plusieurs types de médias. un type de média, ou format, est décrit par une structure de [**\_ \_ type de média DMO**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type) . vous pouvez interroger le DMO pour les types pris en charge par un flux de sortie en appelant [**IMediaObject :: GetOutputType**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-getoutputtype). Cette méthode retourne un type de sortie valide (bien que dans certains cas partiellement incomplet) pour ce flux. Vous pouvez énumérer les types de média pris en charge pour un flux de sortie en effectuant des appels répétés à **GetOutputType**, en incrémentant le paramètre de type à chaque appel. lorsque l’index de type que vous transmettez est hors limites, la méthode retourne **DMO \_ E \_ pas d' \_ autres \_ éléments**. Les formats d’entrée peuvent être énumérés de la même manière à l’aide de la méthode [**IMediaObject :: GetInputType**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-getinputtype) .

les types qui sont énumérés par le DMO sont uniquement les types « préférés », toutefois, d’autres types peuvent être pris en charge. Vous pouvez valider un type de sortie en appelant [**IMediaObject :: SetOutputType**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-setoutputtype). Utilisez [**IMediaObject :: SetInputType**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-setinputtype) pour valider un type d’entrée. les deux méthodes retournent **DMO \_ \_ TYPE E \_ non \_ accepté** si la structure du [**\_ \_ TYPE de média DMO**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type) que vous avez transmise n’est pas valide. Certains DMOs vous obligent à définir un type de sortie avant d’énumérer les types d’entrée. Windows Media Audio les DMOs et codecs vidéo possèdent tous des entrées et des sorties qui ont une validation interdépendante. Autrement dit, le type de sortie que vous définissez définit les critères de validation pour le type d’entrée. Il existe également certaines propriétés qui, lorsqu’elles sont définies, modifient les types d’entrée et de sortie valides. pour cette raison, vous devez définir toutes les propriétés souhaitées sur le DMO avant d’énumérer les types.

lorsque vous avez défini les types de sortie et d’entrée pour le DMO, vous pouvez commencer à traiter des exemples. Chaque exemple d’entrée est passé au codec à l’aide d’un appel à [**IMediaObject ::P rocessinput**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-processinput), et chaque exemple de sortie est remis par le codec lorsque vous effectuez un appel à [**IMediaObject ::P rocessoutput**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-processoutput).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Utilisation du codec DMOs](workingwithcodecdmos.md)
</dt> </dl>

 

 
