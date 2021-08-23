---
description: Présentation des classes de base de filtre
ms.assetid: db6324d7-1914-44a8-a202-dff752b61c1a
title: Présentation des classes de base de filtre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f52c0682a5ba9f6a051506911cf143474d9958f1caa926464d9a4c236366e99
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118952558"
---
# <a name="introduction-to-the-filter-base-classes"></a>Présentation des classes de base de filtre

cet article décrit la bibliothèque de classes de base Microsoft DirectShow. Cette bibliothèque est destinée aux développeurs de filtres, mais les créateurs d’applications peuvent trouver des classes d’assistance et des utilitaires de débogage utiles. toutefois, la bibliothèque de classes de base n’est pas requise pour la programmation de DirectShow.

Les sections suivantes résument les classes de base les plus importantes dans la bibliothèque.

**Classes d’objets COM**

Les classes suivantes prennent en charge la création d’objets COM :



| Classe                              | Description                            |
|------------------------------------|----------------------------------------|
| [**CBaseObject**](cbaseobject.md) | Classe d’objet de base.                     |
| [**CUnknown**](cunknown.md)       | Implémente l’interface **IUnknown** . |



 

la plupart des classes DirectShow dérivent de **CBaseObject**. Cette classe fournit une assistance de débogage en conservant le décompte de tous les objets actifs dans la DLL au moment de l’exécution. Dans les versions Debug, la DLL déclare si elle est déchargée alors que le nombre d’objets est supérieur à zéro. Cela facilite le suivi des fuites provoquées par des problèmes de comptage des références.

Toutes les classes de base qui prennent en charge les interfaces COM dérivent de **CUnknown**, qui hérite de **CBaseObject**. La classe **CUnknown** prend en charge le décompte de références, **QueryInterface** et agrégation. Pour plus d’informations, consultez [comment implémenter IUnknown](how-to-implement-iunknown.md).

**Filtrer et épingler des classes**

les classes suivantes prennent en charge la création de DirectShow filtrer et épingler des objets :



| Classe                                    | Description                                                                                                                                                     |
|------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CBaseFilter**](cbasefilter.md)       | Classe de base pour les filtres. Implémente l’interface [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) .                                                                            |
| [**CBasePin**](cbasepin.md)             | Classe de base pour les codes confidentiels. Implémente les interfaces [**IPIN**](/windows/desktop/api/Strmif/nn-strmif-ipin) et [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol) .                                             |
| [**CBaseInputPin**](cbaseinputpin.md)   | Classe de base pour les broches d’entrée qui utilisent le transport de mémoire locale. Implémente l’interface [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) . Cette classe dérive de **CBasePin**. |
| [**CBaseOutputPin**](cbaseoutputpin.md) | Classe de base pour les broches de sortie qui utilisent des connexions **IMemInputPin** . Cette classe dérive de **CBasePin**.                                                         |



 

Les classes suivantes sont utiles pour créer des types de filtres plus spécialisés :



| Classe                                                  | Description                                                                                                                                                                                                                                                                                               |
|--------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CSource**](csource.md)                             | Classe de base pour les filtres sources. Cette classe est conçue pour la création de sources push. Elle n’est pas adaptée aux sources d’extraction, telles que les lecteurs de fichiers. Pour créer des broches de sortie pour cette classe, utilisez la classe [**CSourceStream**](csourcestream.md) .                                                                   |
| [**CTransformFilter**](ctransformfilter.md)           | Classe de base pour les filtres de transformation. Cette classe effectue une copie sur les données. Les codes confidentiels pour cette classe sont [**CTransformInputPin**](ctransforminputpin.md) et [**CTransformOutputPin**](ctransformoutputpin.md).                                                                                            |
| [**CTransInPlaceFilter**](ctransinplacefilter.md)     | Classe de base pour les filtres de transformation qui ne copient pas de données. Cette classe effectue le traitement des données directement sur les données d’entrée avant de la passer en aval. Les codes confidentiels pour cette classe sont [**CTransInPlaceInputPin**](ctransinplaceinputpin.md) et [**CTransInPlaceOutputPin**](ctransinplaceoutputpin.md). |
| [**CVideoTransformFilter**](cvideotransformfilter.md) | Classe de base pour les filtres de transformation vidéo. Cette classe dérive de **CTransformFilter** et ajoute la prise en charge du contrôle de qualité.                                                                                                                                                                                |
| [**CBaseRenderer**](cbaserenderer.md)                 | Classe de base pour les filtres de convertisseur. La broche d’entrée pour cette classe est [**CRendererInputPin**](crendererinputpin.md).                                                                                                                                                                                          |
| [**CBaseVideoRenderer**](cbasevideorenderer.md)       | Classe de base pour les convertisseurs vidéo. Cette classe dérive de **CBaseRenderer**.                                                                                                                                                                                                                                |



 

Pour utiliser ces classes, vous devez dériver votre propre classe et écrire du code pour prendre en charge les fonctionnalités spécifiques à votre filtre. Plus la classe de base est spécialisée, moins vous aurez besoin d’écrire du code dans votre classe dérivée.

**Objets d’assistance**

Les classes suivantes implémentent des objets d’assistance utilisés par les filtres et les codes confidentiels. La plupart de ces classes peuvent être utilisées sans dériver de nouvelles classes à partir de celles-ci :



| Classe                                              | Description                                                                                                                                                        |
|----------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CPullPin**](cpullpin.md)                       | Objet d’assistance pour les broches d’entrée sur les filtres de l’analyseur. Prend en charge les connexions [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) avec des sources d’extraction.                                       |
| [**COutputQueue**](coutputqueue.md)               | Objet d’assistance pour les codes confidentiels de sortie qui met en file d’attente des exemples à remettre sur un thread de travail.                                                                                  |
| [**CSourceSeeking**](csourceseeking.md)           | Objet d’aide pour l’implémentation de la recherche sur un filtre source avec exactement une broche de sortie. (Cette classe n’est pas conçue pour les filtres avec plusieurs codes confidentiels, tels que les analyseurs.) |
| [**CEnumPins**](cenumpins.md)                     | Objet énumérateur pour l’énumération des broches sur un filtre. Implémente l’interface [**IEnumPins**](/windows/desktop/api/Strmif/nn-strmif-ienumpins) .                                                       |
| [**CEnumMediaTypes**](cenummediatypes.md)         | Objet énumérateur pour l’énumération des types de média préférés sur un code confidentiel. Implémente l’interface [**IEnumMediaTypes**](/windows/desktop/api/Strmif/nn-strmif-ienummediatypes) .                             |
| [**CMemAllocator**](cmemallocator.md)             | Objet allocateur de mémoire. Implémente l’interface [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) .                                                                          |
| [**CMediaSample**](cmediasample.md)               | Exemple d’objet de média. Implémente l’interface [**IMediaSample2**](/windows/desktop/api/Strmif/nn-strmif-imediasample2) .                                                                              |
| [**CBaseReferenceClock**](cbasereferenceclock.md) | Classe de base pour les horloges de référence. Implémente l’interface [**IReferenceClock**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclock) .                                                              |
| [**CMediaType**](cmediatype.md)                   | Objet d’assistance pour la manipulation des structures de [**\_ \_ type de média am**](/windows/win32/api/strmif/ns-strmif-am_media_type) .                                                                                |



 

 

 



