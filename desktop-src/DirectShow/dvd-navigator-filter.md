---
description: Filtre de navigateur DVD
ms.assetid: 3b2c01a2-d52c-4497-8fc9-d1113e8507e8
title: Filtre de navigateur DVD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a48d4978b31683d99035f6e44ae042f3e982bcde
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122983212"
---
# <a name="dvd-navigator-filter"></a>Filtre de navigateur DVD

Le filtre de navigateur DVD est le filtre source pour un graphique de filtre de lecture DVD-Video. Il ouvre tous les fichiers nécessaires dans un volume DVD-Video, parcourt les fichiers linéaires DVD-Video. VOB et analyse le flux de programme MPEG-2 résultant, en fractionnant le flux en trois broches de sortie (vidéo, audio, sous-image).

Le filtre de navigateur DVD implémente également les interfaces [**IDvdControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2) et [**IDvdInfo2**](/windows/desktop/api/Strmif/nn-strmif-idvdinfo2) qui permettent à une application de lecture de DVD de contrôler DVD-Video la lecture.




| Étiquette | Valeur |
|--------|-------|
| Interfaces de filtre | <a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2"><strong>IDvdControl2</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-idvdinfo2"><strong>IDvdInfo2</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ifilesourcefilter"><strong>IFileSourceFilter</strong></a>, <strong>ISpecifyPropertyPages</strong> | 
| Types de média de broche d’entrée | MEDIATYPE_Stream, MEDIASUBTYPE_MPEG2_PROGRAM | 
| Interfaces pin d’entrée | Non applicable. | 
| Types de média de broche de sortie | Types de base :<br /><ul><li>Vidéo : <strong>MEDIATYPE_DVD_ENCRYPTED_PACK</strong>, <strong>MEDIASUBTYPE_MPEG2_VIDEO</strong></li><li>Audio : <strong>MEDIATYPE_DVD_ENCRYPTED_PACK</strong>, <strong>MEDIASUBTYPE_DOLBY_AC3</strong></li><li>Sous-image : <strong>MEDIATYPE_DVD_ENCRYPTED_PACK</strong>, <strong>MEDIASUBTYPE_DVD_SUBPICTURE</strong></li></ul>Types étendus :<br /> Vidéo :<br /><ul><li><strong>MEDIATYPE_DVD_ENCRYPTED_PACK</strong>, <strong>MEDIASUBTYPE_MPEG2_VIDEO</strong></li><li><strong>MEDIATYPE_Video</strong>, <strong>MEDIASUBTYPE_MPEG2_VIDEO</strong></li><li><strong>MEDIATYPE_MPEG2_PES</strong>, <strong>MEDIASUBTYPE_MPEG2_VIDEO</strong></li></ul>Audio :<br /><ul><li><strong>MEDIATYPE_DVD_ENCRYPTED_PACK</strong>, <strong>MEDIASUBTYPE_DOLBY_AC3</strong></li><li><strong>MEDIATYPE_Audio</strong>, <strong>MEDIASUBTYPE_DOLBY_AC3</strong></li><li><strong>MEDIATYPE_MPEG2_PES</strong>, <strong>MEDIASUBTYPE_DOLBY_AC3</strong></li></ul>Sous-titres<br /><ul><li><strong>MEDIATYPE_DVD_ENCRYPTED_PACK</strong>, <strong>MEDIASUBTYPE_DVD_SUBPICTURE</strong></li><li><strong>MEDIATYPE_Video</strong>, <strong>MEDIASUBTYPE_DVD_SUBPICTURE</strong></li><li><strong>MEDIATYPE_MPEG2_PES</strong>, <strong>MEDIASUBTYPE_DVD_SUBPICTURE</strong></li></ul>Pour activer les types étendus, appelez <a href="/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-setoption"><strong>IDvdControl2 :: SetOption</strong></a> et définissez le <br /> | 
| Interfaces de broche de sortie | <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPIN</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"> <strong>IQualityControl</strong></a> | 
| CLSID du filtre | CLSID_DVDNavigator | 
| CLSID de page de propriétés | Aucune page de propriétés. | 
| Exécutable | qdvd.dll | 
| <a href="merit.md">Mérite</a> | MERIT_DO_NOT_USE | 
| <a href="filter-categories.md">Catégorie de filtre</a> | CLSID_LegacyAmFilterCategory | 




 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[DirectShow Filtres](directshow-filters.md)
</dt> <dt>

[Applications DVD](dvd-applications.md)
</dt> </dl>

 

 




