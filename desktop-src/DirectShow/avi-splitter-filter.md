---
description: Filtre de séparateur AVI
ms.assetid: df3c7d11-7ecc-499a-af36-b74437e21999
title: Filtre de séparateur AVI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e61b9a60c4c42aafa875c166ae08ccdf337793c
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104109714"
---
# <a name="avi-splitter-filter"></a>Filtre de séparateur AVI

Le filtre de séparateur AVI est utilisé pour la lecture des fichiers AVI. Il accepte les données au format AVI et les divise en flux constitutifs pour un traitement et/ou un rendu plus poussés.



|                                          |                                                                                                                                                                     |
|------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Interfaces de filtre                        | [**IAMMediaContent**](/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iammediacontent), [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [**IPersistMediaPropertyBag**](/windows/desktop/api/Strmif/nn-strmif-ipersistmediapropertybag)                        |
| Types de média de broche d’entrée                    | \_Flux de MediaType, MEDIASUBTYPE \_ AVI                                                                                                                                |
| Interfaces pin d’entrée                     | [**IPIN**](/windows/desktop/api/Strmif/nn-strmif-ipin), [ **IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)                                                                                                    |
| Types de média de broche de sortie                   | En général, le **\_ son** de la **\_ vidéo** ou du MediaType. Le type exact dépend du contenu du fichier, du fait que le fichier est compressé et du codec utilisé. |
| Interfaces de broche de sortie                    | [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition), [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**IPIN**](/windows/desktop/api/Strmif/nn-strmif-ipin), IPropertyBag, [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)    |
| CLSID du filtre                             | CLSID \_ AviSplitter                                                                                                                                                  |
| CLSID de page de propriétés                      | Aucune page de propriétés.                                                                                                                                                   |
| Exécutable                               | quartz.dll                                                                                                                                                          |
| [Mérite](merit.md)                       | MÉRITE \_ normal                                                                                                                                                       |
| [Catégorie de filtre](filter-categories.md) | CLSID \_ LegacyAmFilterCategory                                                                                                                                       |



 

## <a name="remarks"></a>Notes

Ce filtre est généralement connecté au filtre de [source de fichier Async](file-source--async--filter.md) sur sa broche d’entrée. Il peut se connecter à n’importe quel filtre dont la broche de sortie prend en charge [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) et offre le type de média correct à la broche d’entrée du filtre de séparateur avi.

Les broches de sortie sur le séparateur AVI prennent en charge la méthode IPropertyBag :: Read pour la lecture des propriétés à partir de flux individuels. Actuellement, la propriété suivante est définie.



| Propriété | Description                                                                                                                                    |
|----------|------------------------------------------------------------------------------------------------------------------------------------------------|
| name     | Retourne le nom du flux, issu du `'strn'` segment dans le fichier avi. Si ce segment est absent, la méthode de lecture retourne E \_ INVALIDARG. |



 

La méthode IPropertyBag :: Write retourne E \_ Fail. Le filtre [multiplex MUX](avi-mux-filter.md) prend en charge IPropertyBag :: Write pour l’enregistrement des propriétés de flux dans un fichier avi.

Le séparateur AVI n’autorise pas les filtres en aval à utiliser leur propre allocateur.

La durée d’entrelacement dans le fichier détermine la quantité de mémoire allouée par le séparateur AVI pour le traiter. Un fichier entrelacé dans un deuxième segment nécessitera une quantité de mémoire supérieure à celle d’un fichier dont la durée d’entrelacement est définie sur un ou deux frames. Sur les ordinateurs modernes, ce n’est généralement pas un problème, sauf si vous exécutez plusieurs instances du séparateur AVI simultanément.

### <a name="seeking"></a>Cherche

Si le fichier contient un flux vidéo, le séparateur AVI prend en charge la recherche par numéro de frame. Pour activer la recherche basée sur des frames, appelez [**IMediaSeeking :: SetTimeFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-settimeformat) sur le [Gestionnaire de graphique de filtre](filter-graph-manager.md) avec le **\_ \_ cadre de format d’heure** de valeur.

Si le fichier contient un flux audio, le séparateur AVI prend en charge la recherche par échantillon de nombre. Pour activer la recherche basée sur les exemples, appelez [**SetTimeFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-settimeformat) sur le gestionnaire de graphique de filtre avec l’exemple de format de date et d' **heure \_ \_**.

Dans les deux cas, la broche de sortie pour ce flux doit être connectée à un filtre de convertisseur.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Filtres DirectShow](directshow-filters.md)
</dt> </dl>

 

 



