---
description: L’exemple de filtre d’accrochage permet de récupérer des exemples au fur et à mesure qu’ils passent par le graphique de filtre.
ms.assetid: 3c2fb52f-2b44-449a-ae96-3cf35a0a401d
title: Exemple de filtre d’accrochage (qedit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Sample
api_type:
- HeaderDef
api_location:
- Qedit.h
ms.openlocfilehash: 18cedd24b0ddcb8f71373641905228f8252ae4ef
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106532744"
---
# <a name="sample-grabber-filter"></a>Exemple de filtre d’accrochage

> [!Note]  
> \[Action déconseillée. Cette API peut être supprimée dans les versions futures de Windows.\]

 

L’exemple de filtre d’accrochage permet de récupérer des exemples au fur et à mesure qu’ils passent par le graphique de filtre. Il s’agit d’un filtre de transformation avec une broche d’entrée et une broche de sortie. Il passe tous les exemples en aval inchangés, de sorte que vous pouvez l’insérer dans un graphique de filtre sans modifier le flux de données. Votre application peut ensuite récupérer des échantillons individuels à partir du filtre en appelant des méthodes sur l’interface [**ISampleGrabber**](isamplegrabber.md) .

Si vous souhaitez récupérer des exemples sans restituer les données, connectez le filtre d’accroche d’échantillon au filtre de [**convertisseur null**](null-renderer-filter.md) .



|                                          |                                                                                                                                                    |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| Interfaces de filtre                        | [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [ **ISampleGrabber**](isamplegrabber.md)                                                                       |
| Types de média de broche d’entrée                    | Tout type de média.                                                                                                                                    |
| Interfaces pin d’entrée                     | [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPIN**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)                                             |
| Types de média de broche de sortie                   | Tout type de média. Correspond au type de média d’entrée.                                                                                                          |
| Interfaces de broche de sortie                    | [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition), [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**IPIN**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol) |
| CLSID du filtre                             | CLSID \_ SampleGrabber                                                                                                                               |
| CLSID de page de propriétés                      | Aucune page de propriétés.                                                                                                                                  |
| Exécutable                               | Qedit.dll                                                                                                                                          |
| [Mérite](merit.md)                       | MÉRITE \_ n' \_ \_ utilise pas                                                                                                                                |
| [Catégorie de filtre](filter-categories.md) | CLSID \_ LegacyAmFilterCategory                                                                                                                      |



 

## <a name="remarks"></a>Notes

Pour utiliser ce filtre, ajoutez-le au graphique de filtre et appelez [**ISampleGrabber :: SetMediaType**](isamplegrabber-setmediatype.md) avec le type de média souhaité. Cette méthode spécifie le type de média pour les connexions de broche d’entrée et de sortie du filtre. Connectez ensuite le filtre à d’autres filtres dans le graphique.

Si vous appelez [**ISampleGrabber :: SetBufferSamples**](isamplegrabber-setbuffersamples.md) avec la valeur **true**, le filtre met en mémoire tampon chaque échantillon qu’il reçoit avant de le passer en aval. Appelez la méthode [**ISampleGrabber :: GetCurrentBuffer**](isamplegrabber-getcurrentbuffer.md) pour récupérer le contenu actuel de la mémoire tampon. Vous pouvez également appeler [**ISampleGrabber :: SetCallback**](isamplegrabber-setcallback.md) pour que le filtre appelle une fonction de rappel chaque fois qu’il reçoit un exemple.

Le filtre présente les limitations suivantes pour les formats vidéo :

-   Il ne prend pas en charge les types vidéo avec une orientation verticale ( **bihauteur** négative).
-   Elle ne prend pas en charge la structure de format [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) (type de format égal au **format \_ VideoInfo2**).
-   Elle rejette tout type de vidéo dans lequel le Stride de la surface ne correspond pas à la largeur de la vidéo.

Par conséquent, la accroche d’échantillon ne se connecte pas au convertisseur de mixage vidéo (VMR) pour certains types de vidéo.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>Qedit. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Objets des services de modification DirectShow](directshow-editing-services-objects.md)
</dt> <dt>

[Utilisation de l’exemple d’accrochage](using-the-sample-grabber.md)
</dt> </dl>

 

 




