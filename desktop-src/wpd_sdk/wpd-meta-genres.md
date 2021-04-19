---
description: Le \_ \_ type énumération des métadonnées wpd décrit un type de genre large d’un fichier multimédia.
ms.assetid: a69cab70-5a45-4e75-abbd-230396c2b5ec
title: Énumération WPD_META_GENRES (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_META_GENRES
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 1f6ff4875474776df1e2436e0209e6d863f5b3e1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106523515"
---
# <a name="wpd_meta_genres-enumeration"></a>\_Énumération des méta- \_ genres wpd

Le type énumération des **\_ métadonnées \_ wpd** décrit un type de genre large d’un fichier multimédia.

## <a name="syntax"></a>Syntaxe


```C++
typedef enum WPD_META_GENRES { 
  WPD_META_GENRE_UNUSED                            = 0x0,
  WPD_META_GENRE_GENERIC_MUSIC_AUDIO_FILE          = 0x1,
  WPD_META_GENRE_GENERIC_NON_MUSIC_AUDIO_FILE      = 0x11,
  WPD_META_GENRE_SPOKEN_WORD_AUDIO_BOOK_FILES      = 0x12,
  WPD_META_GENRE_SPOKEN_WORD_FILES_NON_AUDIO_BOOK  = 0x13,
  WPD_META_GENRE_SPOKEN_WORD_NEWS                  = 0x14,
  WPD_META_GENRE_SPOKEN_WORD_TALK_SHOWS            = 0x15,
  WPD_META_GENRE_GENERIC_VIDEO_FILE                = 0x21,
  WPD_META_GENRE_NEWS_VIDEO_FILE                   = 0x22,
  WPD_META_GENRE_MUSIC_VIDEO_FILE                  = 0x23,
  WPD_META_GENRE_HOME_VIDEO_FILE                   = 0x24,
  WPD_META_GENRE_FEATURE_FILM_VIDEO_FILE           = 0x25,
  WPD_META_GENRE_TELEVISION_VIDEO_FILE             = 0x26,
  WPD_META_GENRE_TRAINING_EDUCATIONAL_VIDEO_FILE   = 0x27,
  WPD_META_GENRE_PHOTO_MONTAGE_VIDEO_FILE          = 0x28,
  WPD_META_GENRE_GENERIC_NON_AUDIO_NON_VIDEO       = 0x30,
  WPD_META_GENRE_AUDIO_PODCAST                     = 0x40,
  WPD_META_GENRE_VIDEO_PODCAST                     = 0x41,
  WPD_META_GENRE_MIXED_PODCAST                     = 0x42
} ;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="WPD_META_GENRE_UNUSED"></span><span id="wpd_meta_genre_unused"></span>**\_méta- \_ genre wpd \_ non utilisé**
</dt> <dd>

Le genre n’a pas été défini ou n’est pas applicable.

</dd> <dt>

<span id="WPD_META_GENRE_GENERIC_MUSIC_AUDIO_FILE"></span><span id="wpd_meta_genre_generic_music_audio_file"></span>**\_ \_ \_ \_ \_ fichier audio musical générique Meta genre \_ wpd**
</dt> <dd>

Il s’agit d’un fichier de musique générique (audio uniquement).

</dd> <dt>

<span id="WPD_META_GENRE_GENERIC_NON_MUSIC_AUDIO_FILE"></span><span id="wpd_meta_genre_generic_non_music_audio_file"></span>**\_ \_ \_ \_ \_ \_ fichier audio non musical générique \_ méta genre wpd**
</dt> <dd>

Il s’agit d’un fichier audio non musical générique, par exemple un livre vocal ou audio.

</dd> <dt>

<span id="WPD_META_GENRE_SPOKEN_WORD_AUDIO_BOOK_FILES"></span><span id="wpd_meta_genre_spoken_word_audio_book_files"></span>**\_fichiers de méta-genres de métadonnées wpd \_ \_ \_ Word \_ \_ \_**
</dt> <dd>

Il s’agit d’un fichier de livre audio.

</dd> <dt>

<span id="WPD_META_GENRE_SPOKEN_WORD_FILES_NON_AUDIO_BOOK"></span><span id="wpd_meta_genre_spoken_word_files_non_audio_book"></span>**\_méta-genres de métadonnées wpd \_ \_ \_ \_ fichiers Word \_ non \_ audio \_**
</dt> <dd>

Il s’agit d’un fichier audio de texte parlé qui n’est pas un livre audio, par exemple un entretien ou une parole.

</dd> <dt>

<span id="WPD_META_GENRE_SPOKEN_WORD_NEWS"></span><span id="wpd_meta_genre_spoken_word_news"></span>**\_actualité des méta- \_ genres wpd \_ \_ \_**
</dt> <dd>

Il s’agit d’un fichier audio ou vidéo de News.

</dd> <dt>

<span id="WPD_META_GENRE_SPOKEN_WORD_TALK_SHOWS"></span><span id="wpd_meta_genre_spoken_word_talk_shows"></span>**\_meta genre de métadonnées wpd \_ \_ parlé \_ \_ \_ de discours**
</dt> <dd>

Il s’agit d’un enregistrement audio d’un diaporama.

</dd> <dt>

<span id="WPD_META_GENRE_GENERIC_VIDEO_FILE"></span><span id="wpd_meta_genre_generic_video_file"></span>**\_ \_ \_ \_ fichier vidéo générique méta-genre wpd \_**
</dt> <dd>

Il s’agit d’un fichier vidéo générique.

</dd> <dt>

<span id="WPD_META_GENRE_NEWS_VIDEO_FILE"></span><span id="wpd_meta_genre_news_video_file"></span>**\_ \_ \_ \_ fichier vidéo Actualités méta-genres wpd \_**
</dt> <dd>

Il s’agit d’un fichier vidéo d’actualité.

</dd> <dt>

<span id="WPD_META_GENRE_MUSIC_VIDEO_FILE"></span><span id="wpd_meta_genre_music_video_file"></span>**\_ \_ \_ fichier vidéo de musique \_ méta-genres wpd \_**
</dt> <dd>

Il s’agit d’un fichier vidéo musical.

</dd> <dt>

<span id="WPD_META_GENRE_HOME_VIDEO_FILE"></span><span id="wpd_meta_genre_home_video_file"></span>**\_ \_ \_ fichier vidéo de démarrage \_ du méta wpd \_**
</dt> <dd>

Il s’agit d’un fichier vidéo d’hébergement.

</dd> <dt>

<span id="WPD_META_GENRE_FEATURE_FILM_VIDEO_FILE"></span><span id="wpd_meta_genre_feature_film_video_file"></span>**\_ \_ \_ \_ \_ \_ fichier vidéo de la fonctionnalité de méta-genres wpd**
</dt> <dd>

Il s’agit d’un fichier vidéo de film de fonctionnalité.

</dd> <dt>

<span id="WPD_META_GENRE_TELEVISION_VIDEO_FILE"></span><span id="wpd_meta_genre_television_video_file"></span>**\_ \_ \_ fichier vidéo de télévision \_ de méta-genres wpd \_**
</dt> <dd>

Il s’agit d’un fichier vidéo de programme de télévision.

</dd> <dt>

<span id="WPD_META_GENRE_TRAINING_EDUCATIONAL_VIDEO_FILE"></span><span id="wpd_meta_genre_training_educational_video_file"></span>**\_ \_ \_ \_ \_ fichier vidéo éducatif de formation Meta genre wpd \_**
</dt> <dd>

Il s’agit d’un fichier vidéo éducatif.

</dd> <dt>

<span id="WPD_META_GENRE_PHOTO_MONTAGE_VIDEO_FILE"></span><span id="wpd_meta_genre_photo_montage_video_file"></span>**\_ \_ \_ \_ \_ fichier vidéo de photomontage \_ méta-genres de photos wpd**
</dt> <dd>

Il s’agit d’un fichier vidéo présentant un photomontage.

</dd> <dt>

<span id="WPD_META_GENRE_GENERIC_NON_AUDIO_NON_VIDEO"></span><span id="wpd_meta_genre_generic_non_audio_non_video"></span>**\_méta- \_ vidéo non \_ \_ \_ audio \_ \_ générique méta-genre wpd**
</dt> <dd>

Il s’agit d’un fichier sans audio ou vidéo.

</dd> <dt>

<span id="WPD_META_GENRE_AUDIO_PODCAST"></span><span id="wpd_meta_genre_audio_podcast"></span>**\_Podcast d' \_ audio Meta genre \_ \_ wpd**
</dt> <dd>

Il s’agit d’un podcast audio.

</dd> <dt>

<span id="WPD_META_GENRE_VIDEO_PODCAST"></span><span id="wpd_meta_genre_video_podcast"></span>**\_podcast vidéo de méta- \_ genres wpd \_ \_**
</dt> <dd>

Il s’agit d’un podcast vidéo.

</dd> <dt>

<span id="WPD_META_GENRE_MIXED_PODCAST"></span><span id="wpd_meta_genre_mixed_podcast"></span>**\_podcast meta \_ genres \_ mixtes wpd \_**
</dt> <dd>

Il s’agit d’un podcast contenant à la fois des données audio et vidéo.

</dd> </dl>

## <a name="remarks"></a>Notes

Cette énumération est utilisée par la propriété [ \_ \_ meta \_ du média wpd](media-properties.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|---------------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>PortableDevice. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Structures et types énumération**](structures-and-enumeration-types.md)
</dt> </dl>

 

 




