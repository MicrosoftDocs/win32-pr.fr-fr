---
description: Filtre de l’analyseur WAVE
ms.assetid: 53a9538d-7a79-40bb-9468-d710eb238925
title: Filtre de l’analyseur WAVE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d91508500b02743f7cac8b4ed5cff718d12e3b03
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122987852"
---
# <a name="wave-parser-filter"></a>Filtre de l’analyseur WAVE

Le filtre de l’analyseur WAVE analyse les données audio au format WAV à partir des fichiers. wav,... ou. AIF. Le filtre amont doit être le filtre de [source de fichier Async](file-source--async--filter.md) , le filtre de [source du fichier d’URL](file-source--url--filter.md) ou un filtre de source asynchrone tiers compatible qui contient les données audio WAV. Le flux de sortie est données audio, que vous pouvez connecter directement à un filtre de rendu audio ou à un filtre de transformation audio intermédiaire.




| Étiquette | Valeur |
|--------|-------|
| Interfaces de filtre | <a href="/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iammediacontent"><strong>IAMMediaContent</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipersistmediapropertybag"><strong>IPersistMediaPropertyBag</strong></a> | 
| Types de média de broche d’entrée | Type majeur : MEDIATYPE_StreamThe sous-types suivants sont valides :<br /><ul><li>MEDIASUBTYPE_AIFF</li><li>MEDIASUBTYPE_AU</li><li>MEDIASUBTYPE_WAVE</li></ul> | 
| Interfaces pin d’entrée | <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPIN</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"> <strong>IQualityControl</strong></a> | 
| Types de média de broche de sortie | Type majeur : MEDIATYPE_AudioSubtype : MEDIASUBTYPE_PCM ou un autre type de compression. (Voir <a href="audio-subtypes.md"><strong>sous-types audio</strong></a>.)<br /> Type de format : FORMAT_WaveFormatEx<br /> | 
| Interfaces de broche de sortie | <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPIN</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"> <strong>IMediaSeeking</strong></a> | 
| CLSID du filtre | {D51BD5A1-7548-11cf-A520-0080C77EF58A} | 
| CLSID de page de propriétés | Aucune page de propriétés. | 
| Exécutable | quartz.dll | 
| <a href="merit.md">Mérite</a> | MERIT_UNLIKELY | 
| <a href="filter-categories.md">Catégorie de filtre</a> | CLSID_LegacyAmFilterCategory | 




 

## <a name="remarks"></a>Remarques

Ce filtre prend en charge les types de fichiers suivants :

-   VAGUE (. wav)
-   AIFF et AIFF-C (. AIF)
-   Au (. au)

Toutefois, il présente les limitations suivantes au format audio :

-   L’audio doit être un PCM linéaire 8 bits ou 16 bits.
-   Pour les fichiers AIFF-C, l’audio doit être décompressé, dans l’ordre de primauté des octets de poids fort (type de compression « aucun »).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[DirectShow Filtres](directshow-filters.md)
</dt> </dl>

 

 




