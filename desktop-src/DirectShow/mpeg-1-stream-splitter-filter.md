---
description: Filtre de fractionnement de flux MPEG-1
ms.assetid: abadf37f-2876-496d-90e7-77c3475a0064
title: Filtre de fractionnement de flux MPEG-1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3241e966eb7d47431d9dd5f5818b2cff641bf9d
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122472313"
---
# <a name="mpeg-1-stream-splitter-filter"></a>Filtre de fractionnement de flux MPEG-1

Ce filtre fractionne un flux système MPEG-1 en flux audio et vidéo de composant.




| | | Filtrer les interfaces | <a href="/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iammediacontent"><strong>IAMMediaContent</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iamstreamselect"><strong>IAMStreamSelect</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a> | | Types de média de broche d’entrée | Type majeur : MEDIATYPE_Stream<br /> Sous-types<br /><ul><li>MEDIASUBTYPE_MPEG1System</li><li>MEDIASUBTYPE_MPEG1VideoCD</li><li>MEDIASUBTYPE_Audio</li><li>MEDIASUBTYPE_Video</li></ul>Voir <a href="mpeg-1-media-types.md"> <strong>types de média MPEG-1</strong></a><br /> | | Interfaces pin d’entrée | <a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPIN</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a> | | Types de média de broche de sortie | Type principal : MEDIATYPE_Audio ou MEDIATYPE_Video<br /> Sous-type : MEDIASUBTYPE_MPEG1Payload ou MEDIASUBTYPE_MPEG1Packet<br /> Voir <a href="mpeg-1-media-types.md"> <strong>types de média MPEG-1</strong></a><br /> | | Interfaces de broche de sortie | <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPIN</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a> | | CLSID du filtre | CLSID_MPEG1Splitter | | CLSID de page de propriétés | Aucune page de propriétés | | Fichier exécutable | quartz.dll | | <a href="merit.md">Mérite</a> | MERIT_NORMAL | | <a href="filter-categories.md">Catégorie de filtre</a> | CLSID_LegacyAmFilterCategory | 




 

## <a name="remarks"></a>Remarques

Ce fichier prend en charge le mode par extraction via [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) uniquement. elle ne prend pas en charge le mode push.

Étant donné que le contenu MPEG-1 n’est pas indexé, la recherche peut être très approximative. Il est généralement bon pour un flux de système MPEG-1 à débit binaire fixe (généralement généré par le matériel pour CD vidéo).

Le filtre prend en charge l’interface [**IAMMediaContent**](/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iammediacontent) pour la récupération des métadonnées ID3.

Tous les exemples MPEG n’ont pas de datage. L’absence d’horodatage sur un échantillon MPEG n’est pas une erreur. Pour les développeurs de filtre, cela signifie que vous ne devez pas retourner de code d’erreur à partir de la méthode **Receive** de votre code confidentiel d’entrée si [**IMediaSample :: getTime**](/windows/desktop/api/Strmif/nf-strmif-imediasample-gettime) échoue. Si **Receive** retourne une valeur autre que S \_ OK, le séparateur va arrêter l’envoi d’exemples.

Si le fichier contient un flux vidéo, le séparateur de flux MPEG-1 prend en charge la recherche par numéro de frame. pour activer la recherche basée sur des frames, appelez [**IMediaSeeking :: SetTimeFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-settimeformat) sur le [gestionnaire de Graph de filtre](filter-graph-manager.md) avec le **FORMAT de date \_ \_** et d’heure de valeur.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[DirectShow Filtres](directshow-filters.md)
</dt> </dl>

 

 




