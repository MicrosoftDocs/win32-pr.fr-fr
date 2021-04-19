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
# <a name="wpd_meta_genres-enumeration"></a><span data-ttu-id="1e654-103">\_Énumération des méta- \_ genres wpd</span><span class="sxs-lookup"><span data-stu-id="1e654-103">WPD\_META\_GENRES enumeration</span></span>

<span data-ttu-id="1e654-104">Le type énumération des **\_ métadonnées \_ wpd** décrit un type de genre large d’un fichier multimédia.</span><span class="sxs-lookup"><span data-stu-id="1e654-104">The **WPD\_META\_GENRES** enumeration type describes a broad genre type of a media file.</span></span>

## <a name="syntax"></a><span data-ttu-id="1e654-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1e654-105">Syntax</span></span>


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



## <a name="constants"></a><span data-ttu-id="1e654-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="1e654-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="1e654-107"><span id="WPD_META_GENRE_UNUSED"></span><span id="wpd_meta_genre_unused"></span>**\_méta- \_ genre wpd \_ non utilisé**</span><span class="sxs-lookup"><span data-stu-id="1e654-107"><span id="WPD_META_GENRE_UNUSED"></span><span id="wpd_meta_genre_unused"></span>**WPD\_META\_GENRE\_UNUSED**</span></span>
</dt> <dd>

<span data-ttu-id="1e654-108">Le genre n’a pas été défini ou n’est pas applicable.</span><span class="sxs-lookup"><span data-stu-id="1e654-108">The genre has not been set, or is not applicable.</span></span>

</dd> <dt>

<span data-ttu-id="1e654-109"><span id="WPD_META_GENRE_GENERIC_MUSIC_AUDIO_FILE"></span><span id="wpd_meta_genre_generic_music_audio_file"></span>**\_ \_ \_ \_ \_ fichier audio musical générique Meta genre \_ wpd**</span><span class="sxs-lookup"><span data-stu-id="1e654-109"><span id="WPD_META_GENRE_GENERIC_MUSIC_AUDIO_FILE"></span><span id="wpd_meta_genre_generic_music_audio_file"></span>**WPD\_META\_GENRE\_GENERIC\_MUSIC\_AUDIO\_FILE**</span></span>
</dt> <dd>

<span data-ttu-id="1e654-110">Il s’agit d’un fichier de musique générique (audio uniquement).</span><span class="sxs-lookup"><span data-stu-id="1e654-110">This is a generic music file (audio only).</span></span>

</dd> <dt>

<span data-ttu-id="1e654-111"><span id="WPD_META_GENRE_GENERIC_NON_MUSIC_AUDIO_FILE"></span><span id="wpd_meta_genre_generic_non_music_audio_file"></span>**\_ \_ \_ \_ \_ \_ fichier audio non musical générique \_ méta genre wpd**</span><span class="sxs-lookup"><span data-stu-id="1e654-111"><span id="WPD_META_GENRE_GENERIC_NON_MUSIC_AUDIO_FILE"></span><span id="wpd_meta_genre_generic_non_music_audio_file"></span>**WPD\_META\_GENRE\_GENERIC\_NON\_MUSIC\_AUDIO\_FILE**</span></span>
</dt> <dd>

<span data-ttu-id="1e654-112">Il s’agit d’un fichier audio non musical générique, par exemple un livre vocal ou audio.</span><span class="sxs-lookup"><span data-stu-id="1e654-112">This is a generic non-music audio file, for example, a speech or audio book.</span></span>

</dd> <dt>

<span data-ttu-id="1e654-113"><span id="WPD_META_GENRE_SPOKEN_WORD_AUDIO_BOOK_FILES"></span><span id="wpd_meta_genre_spoken_word_audio_book_files"></span>**\_fichiers de méta-genres de métadonnées wpd \_ \_ \_ Word \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="1e654-113"><span id="WPD_META_GENRE_SPOKEN_WORD_AUDIO_BOOK_FILES"></span><span id="wpd_meta_genre_spoken_word_audio_book_files"></span>**WPD\_META\_GENRE\_SPOKEN\_WORD\_AUDIO\_BOOK\_FILES**</span></span>
</dt> <dd>

<span data-ttu-id="1e654-114">Il s’agit d’un fichier de livre audio.</span><span class="sxs-lookup"><span data-stu-id="1e654-114">This is an audio book file.</span></span>

</dd> <dt>

<span data-ttu-id="1e654-115"><span id="WPD_META_GENRE_SPOKEN_WORD_FILES_NON_AUDIO_BOOK"></span><span id="wpd_meta_genre_spoken_word_files_non_audio_book"></span>**\_méta-genres de métadonnées wpd \_ \_ \_ \_ fichiers Word \_ non \_ audio \_**</span><span class="sxs-lookup"><span data-stu-id="1e654-115"><span id="WPD_META_GENRE_SPOKEN_WORD_FILES_NON_AUDIO_BOOK"></span><span id="wpd_meta_genre_spoken_word_files_non_audio_book"></span>**WPD\_META\_GENRE\_SPOKEN\_WORD\_FILES\_NON\_AUDIO\_BOOK**</span></span>
</dt> <dd>

<span data-ttu-id="1e654-116">Il s’agit d’un fichier audio de texte parlé qui n’est pas un livre audio, par exemple un entretien ou une parole.</span><span class="sxs-lookup"><span data-stu-id="1e654-116">This is a spoken-word audio file that is not an audio book, for example, an interview or speech.</span></span>

</dd> <dt>

<span data-ttu-id="1e654-117"><span id="WPD_META_GENRE_SPOKEN_WORD_NEWS"></span><span id="wpd_meta_genre_spoken_word_news"></span>**\_actualité des méta- \_ genres wpd \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="1e654-117"><span id="WPD_META_GENRE_SPOKEN_WORD_NEWS"></span><span id="wpd_meta_genre_spoken_word_news"></span>**WPD\_META\_GENRE\_SPOKEN\_WORD\_NEWS**</span></span>
</dt> <dd>

<span data-ttu-id="1e654-118">Il s’agit d’un fichier audio ou vidéo de News.</span><span class="sxs-lookup"><span data-stu-id="1e654-118">This is a news audio or video file.</span></span>

</dd> <dt>

<span data-ttu-id="1e654-119"><span id="WPD_META_GENRE_SPOKEN_WORD_TALK_SHOWS"></span><span id="wpd_meta_genre_spoken_word_talk_shows"></span>**\_meta genre de métadonnées wpd \_ \_ parlé \_ \_ \_ de discours**</span><span class="sxs-lookup"><span data-stu-id="1e654-119"><span id="WPD_META_GENRE_SPOKEN_WORD_TALK_SHOWS"></span><span id="wpd_meta_genre_spoken_word_talk_shows"></span>**WPD\_META\_GENRE\_SPOKEN\_WORD\_TALK\_SHOWS**</span></span>
</dt> <dd>

<span data-ttu-id="1e654-120">Il s’agit d’un enregistrement audio d’un diaporama.</span><span class="sxs-lookup"><span data-stu-id="1e654-120">This is an audio recording of a talk show.</span></span>

</dd> <dt>

<span data-ttu-id="1e654-121"><span id="WPD_META_GENRE_GENERIC_VIDEO_FILE"></span><span id="wpd_meta_genre_generic_video_file"></span>**\_ \_ \_ \_ fichier vidéo générique méta-genre wpd \_**</span><span class="sxs-lookup"><span data-stu-id="1e654-121"><span id="WPD_META_GENRE_GENERIC_VIDEO_FILE"></span><span id="wpd_meta_genre_generic_video_file"></span>**WPD\_META\_GENRE\_GENERIC\_VIDEO\_FILE**</span></span>
</dt> <dd>

<span data-ttu-id="1e654-122">Il s’agit d’un fichier vidéo générique.</span><span class="sxs-lookup"><span data-stu-id="1e654-122">This is a generic video file.</span></span>

</dd> <dt>

<span data-ttu-id="1e654-123"><span id="WPD_META_GENRE_NEWS_VIDEO_FILE"></span><span id="wpd_meta_genre_news_video_file"></span>**\_ \_ \_ \_ fichier vidéo Actualités méta-genres wpd \_**</span><span class="sxs-lookup"><span data-stu-id="1e654-123"><span id="WPD_META_GENRE_NEWS_VIDEO_FILE"></span><span id="wpd_meta_genre_news_video_file"></span>**WPD\_META\_GENRE\_NEWS\_VIDEO\_FILE**</span></span>
</dt> <dd>

<span data-ttu-id="1e654-124">Il s’agit d’un fichier vidéo d’actualité.</span><span class="sxs-lookup"><span data-stu-id="1e654-124">This is a news video file.</span></span>

</dd> <dt>

<span data-ttu-id="1e654-125"><span id="WPD_META_GENRE_MUSIC_VIDEO_FILE"></span><span id="wpd_meta_genre_music_video_file"></span>**\_ \_ \_ fichier vidéo de musique \_ méta-genres wpd \_**</span><span class="sxs-lookup"><span data-stu-id="1e654-125"><span id="WPD_META_GENRE_MUSIC_VIDEO_FILE"></span><span id="wpd_meta_genre_music_video_file"></span>**WPD\_META\_GENRE\_MUSIC\_VIDEO\_FILE**</span></span>
</dt> <dd>

<span data-ttu-id="1e654-126">Il s’agit d’un fichier vidéo musical.</span><span class="sxs-lookup"><span data-stu-id="1e654-126">This is a music video file.</span></span>

</dd> <dt>

<span data-ttu-id="1e654-127"><span id="WPD_META_GENRE_HOME_VIDEO_FILE"></span><span id="wpd_meta_genre_home_video_file"></span>**\_ \_ \_ fichier vidéo de démarrage \_ du méta wpd \_**</span><span class="sxs-lookup"><span data-stu-id="1e654-127"><span id="WPD_META_GENRE_HOME_VIDEO_FILE"></span><span id="wpd_meta_genre_home_video_file"></span>**WPD\_META\_GENRE\_HOME\_VIDEO\_FILE**</span></span>
</dt> <dd>

<span data-ttu-id="1e654-128">Il s’agit d’un fichier vidéo d’hébergement.</span><span class="sxs-lookup"><span data-stu-id="1e654-128">This is a home video file.</span></span>

</dd> <dt>

<span data-ttu-id="1e654-129"><span id="WPD_META_GENRE_FEATURE_FILM_VIDEO_FILE"></span><span id="wpd_meta_genre_feature_film_video_file"></span>**\_ \_ \_ \_ \_ \_ fichier vidéo de la fonctionnalité de méta-genres wpd**</span><span class="sxs-lookup"><span data-stu-id="1e654-129"><span id="WPD_META_GENRE_FEATURE_FILM_VIDEO_FILE"></span><span id="wpd_meta_genre_feature_film_video_file"></span>**WPD\_META\_GENRE\_FEATURE\_FILM\_VIDEO\_FILE**</span></span>
</dt> <dd>

<span data-ttu-id="1e654-130">Il s’agit d’un fichier vidéo de film de fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="1e654-130">This is a feature film video file.</span></span>

</dd> <dt>

<span data-ttu-id="1e654-131"><span id="WPD_META_GENRE_TELEVISION_VIDEO_FILE"></span><span id="wpd_meta_genre_television_video_file"></span>**\_ \_ \_ fichier vidéo de télévision \_ de méta-genres wpd \_**</span><span class="sxs-lookup"><span data-stu-id="1e654-131"><span id="WPD_META_GENRE_TELEVISION_VIDEO_FILE"></span><span id="wpd_meta_genre_television_video_file"></span>**WPD\_META\_GENRE\_TELEVISION\_VIDEO\_FILE**</span></span>
</dt> <dd>

<span data-ttu-id="1e654-132">Il s’agit d’un fichier vidéo de programme de télévision.</span><span class="sxs-lookup"><span data-stu-id="1e654-132">This is a television program video file.</span></span>

</dd> <dt>

<span data-ttu-id="1e654-133"><span id="WPD_META_GENRE_TRAINING_EDUCATIONAL_VIDEO_FILE"></span><span id="wpd_meta_genre_training_educational_video_file"></span>**\_ \_ \_ \_ \_ fichier vidéo éducatif de formation Meta genre wpd \_**</span><span class="sxs-lookup"><span data-stu-id="1e654-133"><span id="WPD_META_GENRE_TRAINING_EDUCATIONAL_VIDEO_FILE"></span><span id="wpd_meta_genre_training_educational_video_file"></span>**WPD\_META\_GENRE\_TRAINING\_EDUCATIONAL\_VIDEO\_FILE**</span></span>
</dt> <dd>

<span data-ttu-id="1e654-134">Il s’agit d’un fichier vidéo éducatif.</span><span class="sxs-lookup"><span data-stu-id="1e654-134">This is an educational video file.</span></span>

</dd> <dt>

<span data-ttu-id="1e654-135"><span id="WPD_META_GENRE_PHOTO_MONTAGE_VIDEO_FILE"></span><span id="wpd_meta_genre_photo_montage_video_file"></span>**\_ \_ \_ \_ \_ fichier vidéo de photomontage \_ méta-genres de photos wpd**</span><span class="sxs-lookup"><span data-stu-id="1e654-135"><span id="WPD_META_GENRE_PHOTO_MONTAGE_VIDEO_FILE"></span><span id="wpd_meta_genre_photo_montage_video_file"></span>**WPD\_META\_GENRE\_PHOTO\_MONTAGE\_VIDEO\_FILE**</span></span>
</dt> <dd>

<span data-ttu-id="1e654-136">Il s’agit d’un fichier vidéo présentant un photomontage.</span><span class="sxs-lookup"><span data-stu-id="1e654-136">This is a video file featuring a photo montage.</span></span>

</dd> <dt>

<span data-ttu-id="1e654-137"><span id="WPD_META_GENRE_GENERIC_NON_AUDIO_NON_VIDEO"></span><span id="wpd_meta_genre_generic_non_audio_non_video"></span>**\_méta- \_ vidéo non \_ \_ \_ audio \_ \_ générique méta-genre wpd**</span><span class="sxs-lookup"><span data-stu-id="1e654-137"><span id="WPD_META_GENRE_GENERIC_NON_AUDIO_NON_VIDEO"></span><span id="wpd_meta_genre_generic_non_audio_non_video"></span>**WPD\_META\_GENRE\_GENERIC\_NON\_AUDIO\_NON\_VIDEO**</span></span>
</dt> <dd>

<span data-ttu-id="1e654-138">Il s’agit d’un fichier sans audio ou vidéo.</span><span class="sxs-lookup"><span data-stu-id="1e654-138">This is a file without audio or video.</span></span>

</dd> <dt>

<span data-ttu-id="1e654-139"><span id="WPD_META_GENRE_AUDIO_PODCAST"></span><span id="wpd_meta_genre_audio_podcast"></span>**\_Podcast d' \_ audio Meta genre \_ \_ wpd**</span><span class="sxs-lookup"><span data-stu-id="1e654-139"><span id="WPD_META_GENRE_AUDIO_PODCAST"></span><span id="wpd_meta_genre_audio_podcast"></span>**WPD\_META\_GENRE\_AUDIO\_PODCAST**</span></span>
</dt> <dd>

<span data-ttu-id="1e654-140">Il s’agit d’un podcast audio.</span><span class="sxs-lookup"><span data-stu-id="1e654-140">This is an audio podcast.</span></span>

</dd> <dt>

<span data-ttu-id="1e654-141"><span id="WPD_META_GENRE_VIDEO_PODCAST"></span><span id="wpd_meta_genre_video_podcast"></span>**\_podcast vidéo de méta- \_ genres wpd \_ \_**</span><span class="sxs-lookup"><span data-stu-id="1e654-141"><span id="WPD_META_GENRE_VIDEO_PODCAST"></span><span id="wpd_meta_genre_video_podcast"></span>**WPD\_META\_GENRE\_VIDEO\_PODCAST**</span></span>
</dt> <dd>

<span data-ttu-id="1e654-142">Il s’agit d’un podcast vidéo.</span><span class="sxs-lookup"><span data-stu-id="1e654-142">This is a video podcast.</span></span>

</dd> <dt>

<span data-ttu-id="1e654-143"><span id="WPD_META_GENRE_MIXED_PODCAST"></span><span id="wpd_meta_genre_mixed_podcast"></span>**\_podcast meta \_ genres \_ mixtes wpd \_**</span><span class="sxs-lookup"><span data-stu-id="1e654-143"><span id="WPD_META_GENRE_MIXED_PODCAST"></span><span id="wpd_meta_genre_mixed_podcast"></span>**WPD\_META\_GENRE\_MIXED\_PODCAST**</span></span>
</dt> <dd>

<span data-ttu-id="1e654-144">Il s’agit d’un podcast contenant à la fois des données audio et vidéo.</span><span class="sxs-lookup"><span data-stu-id="1e654-144">This is a podcast containing both audio and video.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1e654-145">Notes</span><span class="sxs-lookup"><span data-stu-id="1e654-145">Remarks</span></span>

<span data-ttu-id="1e654-146">Cette énumération est utilisée par la propriété [ \_ \_ meta \_ du média wpd](media-properties.md) .</span><span class="sxs-lookup"><span data-stu-id="1e654-146">This enumeration is used by the [WPD\_MEDIA\_META\_GENRE](media-properties.md) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="1e654-147">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1e654-147">Requirements</span></span>



| <span data-ttu-id="1e654-148">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1e654-148">Requirement</span></span> | <span data-ttu-id="1e654-149">Valeur</span><span class="sxs-lookup"><span data-stu-id="1e654-149">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="1e654-150">En-tête</span><span class="sxs-lookup"><span data-stu-id="1e654-150">Header</span></span><br/> | <dl> <span data-ttu-id="1e654-151"><dt>PortableDevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="1e654-151"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1e654-152">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1e654-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1e654-153">**Structures et types énumération**</span><span class="sxs-lookup"><span data-stu-id="1e654-153">**Structures and Enumeration Types**</span></span>](structures-and-enumeration-types.md)
</dt> </dl>

 

 




