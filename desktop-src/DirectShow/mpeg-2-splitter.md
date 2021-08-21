---
description: Séparateur MPEG-2
ms.assetid: 06704a5a-e7ae-4187-ae36-32512d951aaf
title: Séparateur MPEG-2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 417fcca0bfc7a5c24416cfc2cb915f968c12105d
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122465253"
---
# <a name="mpeg-2-splitter"></a>Séparateur MPEG-2

à partir de Microsoft® Windows® XP, le filtre de séparateur MPEG-2 est déconseillé. Utilisez plutôt le [démultiplexeur MPEG-2](mpeg-2-demultiplexer.md) .

Sur les plateformes antérieures, utilisez le séparateur MPEG-2 pour les flux de programme MPEG-2 fournis en mode par extraction qui contiennent au moins l’un des types de flux suivants : MPEG-2 Video ; Audio MPEG-2 ; AC3 audio codé comme défini pour la vidéo sur DVD ; ou le fichier audio PCM encodé comme défini pour la vidéo DVD. Ce filtre analyse les flux, crée une broche de sortie pour chaque flux et génère les paquets audio ou vidéo MPEG compressés dans un filtre de décodeur MPEG-2.

Pour les flux de programme et de transport remis en mode push, utilisez le [démultiplexeur MPEG-2](mpeg-2-demultiplexer.md), sur toutes les plateformes.

> [!Note]  
> Le séparateur MPEG-2 ne prend pas en charge la recherche avec une précision de trame.

 




| | | Filtrer les interfaces | <a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a>, <strong>ISpecifyPropertyPages</strong>, <a href="/previous-versions/windows/desktop/api/Amparse/nn-amparse-iamparse"><strong>IAMParse</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iamstreamselect"><strong>IAMStreamSelect</strong></a> | | Types de média de broche d’entrée | <ul><li>MEDIATYPE_Stream, MEDIASUBTYPE_MPEG2_PROGRAM</li><li>MEDIATYPE_Stream, MEDIASUBTYPE_MPEG1_Video</li><li>MEDIATYPE_Stream, MEDIASUBTYPE_NULL</li></ul> | | Interfaces pin d’entrée | <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPIN</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a> | | Types de média de broche de sortie | Dépend du type de flux. Voir <a href="mpeg-2-splitter-media-types.md">types de média MPEG-2 Splitter</a> | | Interfaces de broche de sortie | <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPIN</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a> | | CLSID du filtre | CLSID_MMSPLITTER | | CLSID de page de propriétés | Non applicable | | Fichier exécutable | mpg2splt.ax | | <a href="merit.md">Mérite</a> | MERIT_NORMAL + 1 | | <a href="filter-categories.md">Catégorie de filtre</a> | CLSID_AudioInputDeviceCategory | 




 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[DirectShow Filtres](directshow-filters.md)
</dt> <dt>

[Utilisation du séparateur MPEG-2](using-the-mpeg-2-splitter.md)
</dt> </dl>

 

 



