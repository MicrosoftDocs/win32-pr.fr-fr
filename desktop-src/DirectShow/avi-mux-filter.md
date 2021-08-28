---
description: Filtre multiplex MUX
ms.assetid: 31d30c91-fc6a-45ec-a2e0-34e6a1e902a4
title: Filtre multiplex MUX
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f923ed944781bbaa36179b02db9022f38fc98ff6
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122478635"
---
# <a name="avi-mux-filter"></a>Filtre multiplex MUX

Le filtre MUX AVI accepte plusieurs flux d’entrée et les entrelace au format AVI. Le filtre utilise des codes confidentiels d’entrée distincts pour chaque flux d’entrée, et une broche de sortie pour le flux AVI.

Les applications de capture vidéo ou de création peuvent utiliser ce filtre pour enregistrer des fichiers sur disque au format AVI. Le filtre est généralement connecté au filtre du [writer de fichier](file-writer-filter.md) , mais il peut se connecter à n’importe quel filtre dont la broche d’entrée prend en charge les interfaces IStream et [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) .




| | | Filtrer les interfaces | <a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iconfigavimux"><strong>IConfigAviMux</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iconfiginterleaving"><strong>IConfigInterleaving</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipersistmediapropertybag"><strong>IPersistMediaPropertyBag</strong></a>, ISpecifyPropertyPages | | Types de média de broche d’entrée | Tout type principal qui correspond à un FOURCC de style ancien ou MEDIATYPE_AUXLine21Data. (Pour plus d’informations, consultez <a href="fourccmap.md"><strong>FOURCCMap, classe</strong></a>.)<ul><li>Si le type principal est MEDIATYPE_Audio, le format doit être FORMAT_WaveFormatEx.</li><li>Si le type principal est MEDIATYPE_Video, le format doit être FORMAT_VideoInfo ou FORMAT_DvInfo.</li><li>Si le type principal est MEDIATYPE_Interleaved, le format doit être FORMAT_DvInfo.</li></ul> | | Interfaces pin d’entrée | <a href="/windows/desktop/api/Strmif/nn-strmif-iamstreamcontrol"><strong>IAMStreamControl</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPIN</strong></a>, IPropertyBag, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a> | | Types de média de broche de sortie | MEDIATYPE_Stream, MEDIASUBTYPE_Avi | | Interfaces de broche de sortie | <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPIN</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a> | | CLSID du filtre | CLSID_AviDest | | CLSID de page de propriétés | CLSID_AviMuxProptyPage, CLSID_AviMuxProptyPage1 | | Fichier exécutable | qcap.dll | | <a href="merit.md">Mérite</a> | MERIT_DO_NOT_USE | | <a href="filter-categories.md">Catégorie de filtre</a> | CLSID_LegacyAmFilterCategory | 




 

### <a name="remarks"></a>Remarques

Les notes suivantes décrivent les différents aspects de la fonctionnalité du filtre multiplex Mux.

Épingles

Une fois le filtre multiplex MUX créé, il dispose d’une seule broche d’entrée. À mesure que chaque broche d’entrée est connectée, le filtre crée une nouvelle broche d’entrée.

Propriétés du flux

Les broches d’entrée prennent en charge l’interface IPropertyBag pour définir des propriétés sur des flux individuels. Actuellement, la propriété suivante est définie :



| Propriété | Description                                                           |
|----------|-----------------------------------------------------------------------|
| name     | Nom du flux de données. Cette propriété est écrite sous la forme d’un `'strn'` bloc. |



 

Si le filtre est en cours d’exécution ou en pause, la méthode IPropertyBag :: Write retourne VFW \_ E \_ mauvais \_ État.

Fréquences d’images

Si le filtre amont ne spécifie pas de fréquence d’images dans le membre **AvgTimePerFrame** de la structure [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) , le multiplexeur de flux de contenu (AVI) utilise les horodatages sur la première image vidéo. Le format de fichier AVI ne prend pas en charge les fréquences d’images variables.

Frames supprimés

Le filtre multiplex MUX calcule les images supprimées en fonction des durées de support de chaque échantillon, le cas échéant, ou des horodatages de l’exemple. Il écrit une entrée d’index de longueur nulle pour chaque frame supprimé.

IMediaSeeking

Le filtre multiplex MUX implémente l’interface [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) comme suit :

-   La méthode [**getCurrentPosition**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getcurrentposition) retourne la progression actuelle du multiplexage. si vous transcodez un fichier (plus lentement que le temps réel), cette valeur est plus précise que la valeur renvoyée par le gestionnaire de Graph de filtre. Pour plus d’informations, consultez la section Notes de la page de référence GetCurrentPosition.
-   La méthode [**GetDuration**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getduration) interroge chaque filtre en amont et retourne la durée du flux le plus long. Si l’un de ces filtres échoue à l’appel GetDuration (ou ne prend pas en charge IMediaSeeking), le multiplexeur de contenu AVI retourne un code d’échec et remplit le paramètre *pDuration* avec la durée la plus longue trouvée. Toutefois, dans ce cas, la valeur de *pDuration* n’est pas nécessairement la longueur du flux d’entrée le plus long.
-   La méthode AVI MUX n’implémente pas les méthodes GetStopPosition, GetPositions, GetAvailable, GetRate ou GetPreroll ; elle n’implémente pas non plus \* de méthodes Set pour la recherche.

Extensions de format de fichier AVI 2,0

DirectShow prend actuellement en charge les extensions de format de fichier AVI 2,0 suivantes :

-   Augmentation de la taille du fichier AVI (supérieure à 1 Go)
-   Indexation hiérarchique

Pour plus d’informations, consultez la version 1,02 des « extensions de format de fichier AVI OpenDML » publiées par le sous-comité du format de fichier AVI M-JPEG OpenDML.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[DirectShow Filtres](directshow-filters.md)
</dt> </dl>

 

 



