---
title: Énumération WMDM_FORMATCODE
description: Le \_ type d’énumération WMDM FORMATCODE définit une liste de codes de format qui décrivent les types de contenu transférés vers et à partir d’un appareil.
ms.assetid: 203d9bdf-cbbd-4d06-8292-26c8a472e2aa
keywords:
- WMDM_FORMATCODE l’énumération des Gestionnaire de périphériques Windows Media
topic_type:
- apiref
api_name:
- WMDM_FORMATCODE
api_location:
- wmdm.idl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5b09a388926a0f5fc11e24fc17fe4693b710e04aa321202e9cf31890d60d6642
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119862909"
---
# <a name="wmdm_formatcode-enumeration"></a>WMDM \_ FORMATCODE, énumération

Le type d’énumération **WMDM \_ FORMATCODE** définit une liste de codes de format qui décrivent les types de contenu transférés vers et à partir d’un appareil.

## <a name="syntax"></a>Syntaxe


```C++
typedef enum tagWMDM_FORMATCODE { 
  WMDM_FORMATCODE_NOTUSED,
  WMDM_FORMATCODE_ALLIMAGES,
  WMDM_FORMATCODE_UNDEFINED,
  WMDM_FORMATCODE_ASSOCIATION,
  WMDM_FORMATCODE_SCRIPT,
  WMDM_FORMATCODE_EXECUTABLE,
  WMDM_FORMATCODE_TEXT,
  WMDM_FORMATCODE_HTML,
  WMDM_FORMATCODE_DPOF,
  WMDM_FORMATCODE_AIFF,
  WMDM_FORMATCODE_WAVE,
  WMDM_FORMATCODE_MP3,
  WMDM_FORMATCODE_AVI,
  WMDM_FORMATCODE_MPEG,
  WMDM_FORMATCODE_ASF,
  WMDM_FORMATCODE_RESERVED_FIRST,
  WMDM_FORMATCODE_RESERVED_LAST,
  WMDM_FORMATCODE_IMAGE_UNDEFINED,
  WMDM_FORMATCODE_IMAGE_EXIF,
  WMDM_FORMATCODE_IMAGE_TIFFEP,
  WMDM_FORMATCODE_IMAGE_FLASHPIX,
  WMDM_FORMATCODE_IMAGE_BMP,
  WMDM_FORMATCODE_IMAGE_CIFF,
  WMDM_FORMATCODE_IMAGE_GIF,
  WMDM_FORMATCODE_IMAGE_JFIF,
  WMDM_FORMATCODE_IMAGE_PCD,
  WMDM_FORMATCODE_IMAGE_PICT,
  WMDM_FORMATCODE_IMAGE_PNG,
  WMDM_FORMATCODE_IMAGE_TIFF,
  WMDM_FORMATCODE_IMAGE_TIFFIT,
  WMDM_FORMATCODE_IMAGE_JP2,
  WMDM_FORMATCODE_IMAGE_JPX,
  WMDM_FORMATCODE_IMAGE_RESERVED_FIRST,
  WMDM_FORMATCODE_IMAGE_RESERVED_LAST,
  WMDM_FORMATCODE_UNDEFINEDFIRMWARE,
          WMDM_FORMATCODE_WBMP
,
                  WMDM_FORMATCODE_JPEGXR
,
  WMDM_FORMATCODE_WINDOWSIMAGEFORMAT,
  WMDM_FORMATCODE_UNDEFINEDAUDIO,
  WMDM_FORMATCODE_WMA,
  WMDM_FORMATCODE_OGG,
  WMDM_FORMATCODE_AAC,
  WMDM_FORMATCODE_AUDIBLE,
  WMDM_FORMATCODE_FLAC,
          WMDM_FORMATCODE_QCELP
,
          WMDM_FORMATCODE_AMR
,
  WMDM_FORMATCODE_UNDEFINEDVIDEO,
  WMDM_FORMATCODE_WMV,
  WMDM_FORMATCODE_MP4,
  WMDM_FORMATCODE_MP2,
          WMDM_FORMATCODE_3G2
,
                  WMDM_FORMATCODE_AVCHD
,
                  WMDM_FORMATCODE_ATSCTS
,
                          WMDM_FORMATCODE_DVBTS
,
  WMDM_FORMATCODE_UNDEFINEDCOLLECTION,
  WMDM_FORMATCODE_ABSTRACTMULTIMEDIAALBUM,
  WMDM_FORMATCODE_ABSTRACTIMAGEALBUM,
  WMDM_FORMATCODE_ABSTRACTAUDIOALBUM,
  WMDM_FORMATCODE_ABSTRACTVIDEOALBUM,
  WMDM_FORMATCODE_ABSTRACTAUDIOVIDEOPLAYLIST,
  WMDM_FORMATCODE_ABSTRACTCONTACTGROUP,
  WMDM_FORMATCODE_ABSTRACTMESSAGEFOLDER,
  WMDM_FORMATCODE_ABSTRACTCHAPTEREDPRODUCTION,
  WMDM_FORMATCODE_WPLPLAYLIST,
  WMDM_FORMATCODE_M3UPLAYLIST,
  WMDM_FORMATCODE_MPLPLAYLIST,
  WMDM_FORMATCODE_ASXPLAYLIST,
  WMDM_FORMATCODE_PLSPLAYLIST,
  WMDM_FORMATCODE_UNDEFINEDDOCUMENT,
  WMDM_FORMATCODE_ABSTRACTDOCUMENT,
  WMDM_FORMATCODE_XMLDOCUMENT,
  WMDM_FORMATCODE_MICROSOFTWORDDOCUMENT,
  WMDM_FORMATCODE_MHTCOMPILEDHTMLDOCUMENT,
  WMDM_FORMATCODE_MICROSOFTEXCELSPREADSHEET,
  WMDM_FORMATCODE_MICROSOFTPOWERPOINTDOCUMENT,
  WMDM_FORMATCODE_UNDEFINEDMESSAGE,
  WMDM_FORMATCODE_ABSTRACTMESSAGE,
  WMDM_FORMATCODE_UNDEFINEDCONTACT,
  WMDM_FORMATCODE_ABSTRACTCONTACT,
  WMDM_FORMATCODE_VCARD2,
  WMDM_FORMATCODE_VCARD3,
  WMDM_FORMATCODE_UNDEFINEDCALENDARITEM,
  WMDM_FORMATCODE_ABSTRACTCALENDARITEM,
  WMDM_FORMATCODE_VCALENDAR1,
  WMDM_FORMATCODE_VCALENDAR2,
  WMDM_FORMATCODE_UNDEFINEDWINDOWSEXECUTABLE,
  WMDM_FORMATCODE_MEDIA_CAST,
  WMDM_FORMATCODE_SECTION,
                                  WMDM_FORMATCODE_3G2A

} WMDM_FORMATCODE;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="WMDM_FORMATCODE_NOTUSED"></span><span id="wmdm_formatcode_notused"></span>**WMDM \_ FORMATCODE \_ NOTUSED**
</dt> <dd>

Aucun code de format n’est utilisé.

</dd> <dt>

<span id="WMDM_FORMATCODE_ALLIMAGES"></span><span id="wmdm_formatcode_allimages"></span>**WMDM \_ FORMATCODE \_ ALLIMAGES**
</dt> <dd>

Mettre en forme le code qui peut être utilisé pour interroger toutes les images.

</dd> <dt>

<span id="WMDM_FORMATCODE_UNDEFINED"></span><span id="wmdm_formatcode_undefined"></span>**WMDM \_ FORMATCODE \_ non défini**
</dt> <dd>

Code de format utilisé pour rechercher tous les objets non définis.

</dd> <dt>

<span id="WMDM_FORMATCODE_ASSOCIATION"></span><span id="wmdm_formatcode_association"></span>**WMDM \_ FORMATCODE \_ Association**
</dt> <dd>

Code de format utilisé pour définir un lien entre deux objets.

</dd> <dt>

<span id="WMDM_FORMATCODE_SCRIPT"></span><span id="wmdm_formatcode_script"></span>**\_script WMDM FORMATCODE \_**
</dt> <dd>

Mettre en forme le code d’un fichier de script.

</dd> <dt>

<span id="WMDM_FORMATCODE_EXECUTABLE"></span><span id="wmdm_formatcode_executable"></span>**\_exécutable FORMATCODE \_ WMDM**
</dt> <dd>

Mettre en forme le code d’un fichier exécutable.

</dd> <dt>

<span id="WMDM_FORMATCODE_TEXT"></span><span id="wmdm_formatcode_text"></span>**\_texte WMDM FORMATCODE \_**
</dt> <dd>

Mettre en forme le code d’un fichier texte.

</dd> <dt>

<span id="WMDM_FORMATCODE_HTML"></span><span id="wmdm_formatcode_html"></span>**\_HTML WMDM FORMATCODE \_**
</dt> <dd>

Mettre en forme le code d’un fichier HTML.

</dd> <dt>

<span id="WMDM_FORMATCODE_DPOF"></span><span id="wmdm_formatcode_dpof"></span>**WMDM \_ FORMATCODE \_ DPOF**
</dt> <dd>

Code de format utilisé pour représenter le format de la commande Digital Print.

</dd> <dt>

<span id="WMDM_FORMATCODE_AIFF"></span><span id="wmdm_formatcode_aiff"></span>**WMDM \_ FORMATCODE \_ AIFF**
</dt> <dd>

Code de format utilisé pour représenter le format de fichier d’échange audio.

</dd> <dt>

<span id="WMDM_FORMATCODE_WAVE"></span><span id="wmdm_formatcode_wave"></span>**WMDM \_ FORMATCODE \_ Wave**
</dt> <dd>

Code de format utilisé pour un fichier WAV.

</dd> <dt>

<span id="WMDM_FORMATCODE_MP3"></span><span id="wmdm_formatcode_mp3"></span>**\_Mp3 WMDM FORMATCODE \_**
</dt> <dd>

Code de format utilisé pour un fichier MP3.

</dd> <dt>

<span id="WMDM_FORMATCODE_AVI"></span><span id="wmdm_formatcode_avi"></span>**\_AVI WMDM FORMATCODE \_**
</dt> <dd>

Code de format utilisé pour un fichier AVI.

</dd> <dt>

<span id="WMDM_FORMATCODE_MPEG"></span><span id="wmdm_formatcode_mpeg"></span>**\_MPEG WMDM FORMATCODE \_**
</dt> <dd>

Code de format utilisé pour un fichier MPEG.

</dd> <dt>

<span id="WMDM_FORMATCODE_ASF"></span><span id="wmdm_formatcode_asf"></span>**WMDM \_ FORMATCODE \_ ASF**
</dt> <dd>

Code de format utilisé pour représenter un fichier ASF (Advanced Systems Format).

</dd> <dt>

<span id="WMDM_FORMATCODE_RESERVED_FIRST"></span><span id="wmdm_formatcode_reserved_first"></span>**WMDM \_ FORMATCODE \_ réservé en \_ premier**
</dt> <dd>

Mettre en forme le code qui est le premier d’une plage réservée au protocole PTP (Image Transfer Protocol).

</dd> <dt>

<span id="WMDM_FORMATCODE_RESERVED_LAST"></span><span id="wmdm_formatcode_reserved_last"></span>**WMDM \_ FORMATCODE \_ réservé en \_ dernier**
</dt> <dd>

Mettre en forme le code qui est le dernier dans une plage réservée pour PTP.

</dd> <dt>

<span id="WMDM_FORMATCODE_IMAGE_UNDEFINED"></span><span id="wmdm_formatcode_image_undefined"></span>**\_image FORMATCODE \_ WMDM \_ non définie**
</dt> <dd>

Code de format utilisé pour représenter l’image d’un type non défini.

</dd> <dt>

<span id="WMDM_FORMATCODE_IMAGE_EXIF"></span><span id="wmdm_formatcode_image_exif"></span>**\_image WMDM \_ FORMATCODE \_ EXIF**
</dt> <dd>

Mettre en forme le code d’un fichier EXIF. Également utilisé pour les images JPEG non couvertes par WMDM \_ FORMATCODE \_ image \_ JP2 ou WMDM \_ FORMATCODE image JPX \_ \_ .

</dd> <dt>

<span id="WMDM_FORMATCODE_IMAGE_TIFFEP"></span><span id="wmdm_formatcode_image_tiffep"></span>**\_image WMDM \_ FORMATCODE \_ TIFFEP**
</dt> <dd>

Code de format utilisé pour les images de type format de fichier image balisé pour la photographie électronique (TIFF/EP)

</dd> <dt>

<span id="WMDM_FORMATCODE_IMAGE_FLASHPIX"></span><span id="wmdm_formatcode_image_flashpix"></span>**WMDM \_ FORMATCODE \_ image \_ FLASHPIX**
</dt> <dd>

Mettre en forme le code d’un fichier de type FPX.

</dd> <dt>

<span id="WMDM_FORMATCODE_IMAGE_BMP"></span><span id="wmdm_formatcode_image_bmp"></span>**\_ \_ image BMP WMDM \_ FORMATCODE**
</dt> <dd>

Mettre en forme le code d’un fichier de type BMP.

</dd> <dt>

<span id="WMDM_FORMATCODE_IMAGE_CIFF"></span><span id="wmdm_formatcode_image_ciff"></span>**\_image WMDM \_ FORMATCODE \_ CIFF**
</dt> <dd>

Mettre en forme le code d’une image dans le format de fichier image de l’appareil photo.

</dd> <dt>

<span id="WMDM_FORMATCODE_IMAGE_GIF"></span><span id="wmdm_formatcode_image_gif"></span>**\_ \_ image gif WMDM \_ FORMATCODE**
</dt> <dd>

Mettre en forme le code d’un fichier GIF.

</dd> <dt>

<span id="WMDM_FORMATCODE_IMAGE_JFIF"></span><span id="wmdm_formatcode_image_jfif"></span>**WMDM \_ FORMATCODE \_ image \_ JFIF**
</dt> <dd>

Mettre en forme le code d’un fichier de type JFIF.

</dd> <dt>

<span id="WMDM_FORMATCODE_IMAGE_PCD"></span><span id="wmdm_formatcode_image_pcd"></span>**\_image WMDM \_ FORMATCODE \_ PCD**
</dt> <dd>

Mettez en forme le code d’une image de type Photo CD.

</dd> <dt>

<span id="WMDM_FORMATCODE_IMAGE_PICT"></span><span id="wmdm_formatcode_image_pict"></span>**\_ \_ image PICT WMDM \_ FORMATCODE**
</dt> <dd>

Mettez en forme le code d’une image de type PICT.

</dd> <dt>

<span id="WMDM_FORMATCODE_IMAGE_PNG"></span><span id="wmdm_formatcode_image_png"></span>**\_ \_ image png WMDM \_ FORMATCODE**
</dt> <dd>

Mettre en forme le code d’une image de type PNG.

</dd> <dt>

<span id="WMDM_FORMATCODE_IMAGE_TIFF"></span><span id="wmdm_formatcode_image_tiff"></span>**\_ \_ image TIFF WMDM \_ FORMATCODE**
</dt> <dd>

Mettre en forme le code d’un fichier de type TIFF.

</dd> <dt>

<span id="WMDM_FORMATCODE_IMAGE_TIFFIT"></span><span id="wmdm_formatcode_image_tiffit"></span>**\_image WMDM \_ FORMATCODE \_ TIFFIT**
</dt> <dd>

Mettez en forme le code d’une image de type format de fichier image balisé avec la technologie image.

</dd> <dt>

<span id="WMDM_FORMATCODE_IMAGE_JP2"></span><span id="wmdm_formatcode_image_jp2"></span>**\_Image WMDM \_ FORMATCODE \_ JP2**
</dt> <dd>

Mettre en forme le code pour une image JPEG200.

</dd> <dt>

<span id="WMDM_FORMATCODE_IMAGE_JPX"></span><span id="wmdm_formatcode_image_jpx"></span>**\_image WMDM \_ FORMATCODE \_ JPX**
</dt> <dd>

Mettez en forme le code pour une image générée sur JPEG200, à l’aide de l’inscription d’image continue étendue. L’extension de nom de fichier est généralement. JPF ou. JPX.

</dd> <dt>

<span id="WMDM_FORMATCODE_IMAGE_RESERVED_FIRST"></span><span id="wmdm_formatcode_image_reserved_first"></span>**\_image WMDM \_ FORMATCODE \_ réservée en \_ premier**
</dt> <dd>

Mettre en forme le code qui est le premier d’une plage réservée pour une référence d’image dans PTP.

</dd> <dt>

<span id="WMDM_FORMATCODE_IMAGE_RESERVED_LAST"></span><span id="wmdm_formatcode_image_reserved_last"></span>**\_image WMDM \_ FORMATCODE \_ réservée en \_ dernier**
</dt> <dd>

Mettre en forme le code qui est le dernier d’une plage réservée à une référence d’image dans PTP.

</dd> <dt>

<span id="WMDM_FORMATCODE_UNDEFINEDFIRMWARE"></span><span id="wmdm_formatcode_undefinedfirmware"></span>**WMDM \_ FORMATCODE \_ UNDEFINEDFIRMWARE**
</dt> <dd>

Mettre en forme le code lorsque le microprogramme n’est pas défini.

</dd> <dt>

<span id="________WMDM_FORMATCODE_WBMP_"></span><span id="________wmdm_formatcode_wbmp_"></span>**WMDM \_ FORMATCODE \_ WBMP** 
</dt> <dd>

Code de format pour une image bitmap de protocole d’application sans fil (. WBMP).

</dd> <dt>

<span id="________________WMDM_FORMATCODE_JPEGXR_"></span><span id="________________wmdm_formatcode_jpegxr_"></span>**WMDM \_ FORMATCODE \_ JPEGXR** 
</dt> <dd>

Mettre en forme le code d’une image de photo HD

</dd> <dt>

<span id="WMDM_FORMATCODE_WINDOWSIMAGEFORMAT"></span><span id="wmdm_formatcode_windowsimageformat"></span>**WMDM \_ FORMATCODE \_ WINDOWSIMAGEFORMAT**
</dt> <dd>

mettre en forme le code pour Windows format d’image.

</dd> <dt>

<span id="WMDM_FORMATCODE_UNDEFINEDAUDIO"></span><span id="wmdm_formatcode_undefinedaudio"></span>**WMDM \_ FORMATCODE \_ UNDEFINEDAUDIO**
</dt> <dd>

Mettre en forme le code pour un fichier audio de type non défini.

</dd> <dt>

<span id="WMDM_FORMATCODE_WMA"></span><span id="wmdm_formatcode_wma"></span>**WMDM \_ FORMATCODE \_ WMA**
</dt> <dd>

mettre en forme le code d’un fichier Windows Media Audio (WMA).

</dd> <dt>

<span id="WMDM_FORMATCODE_OGG"></span><span id="wmdm_formatcode_ogg"></span>**WMDM \_ FORMATCODE \_ OGG**
</dt> <dd>

Mettre en forme le code d’un fichier audio encodé en Vorbis dans un conteneur Ogg.

</dd> <dt>

<span id="WMDM_FORMATCODE_AAC"></span><span id="wmdm_formatcode_aac"></span>**WMDM \_ FORMATCODE \_ AAC**
</dt> <dd>

Mettre en forme le code d’un fichier d’encodage audio avancé (AAC).

</dd> <dt>

<span id="WMDM_FORMATCODE_AUDIBLE"></span><span id="wmdm_formatcode_audible"></span>**WMDM \_ FORMATCODE \_ audible**
</dt> <dd>

Mettre en forme le code d’un fichier audible.

</dd> <dt>

<span id="WMDM_FORMATCODE_FLAC"></span><span id="wmdm_formatcode_flac"></span>**WMDM \_ FORMATCODE \_ FLAC**
</dt> <dd>

Mettez en forme le code d’un fichier de codec audio sans perte (FLAC) gratuit.

</dd> <dt>

<span id="________WMDM_FORMATCODE_QCELP_"></span><span id="________wmdm_formatcode_qcelp_"></span>**WMDM \_ FORMATCODE \_ QCELP** 
</dt> <dd>

Code de format pour un fichier de codec QCELP (code de prédiction linéaire) Qualcomm.

</dd> <dt>

<span id="________WMDM_FORMATCODE_AMR_"></span><span id="________wmdm_formatcode_amr_"></span>**WMDM \_ FORMATCODE \_ Amr** 
</dt> <dd>

Code de format pour un fichier de Codec AMR (multi-rate audio) adaptatif.

</dd> <dt>

<span id="WMDM_FORMATCODE_UNDEFINEDVIDEO"></span><span id="wmdm_formatcode_undefinedvideo"></span>**WMDM \_ FORMATCODE \_ UNDEFINEDVIDEO**
</dt> <dd>

Mettre en forme le code d’un fichier vidéo avec un type non défini.

</dd> <dt>

<span id="WMDM_FORMATCODE_WMV"></span><span id="wmdm_formatcode_wmv"></span>**\_WMV FORMATCODE \_ WMDM**
</dt> <dd>

mettez en forme le code d’un fichier Windows Media Video (WMV).

</dd> <dt>

<span id="WMDM_FORMATCODE_MP4"></span><span id="wmdm_formatcode_mp4"></span>**WMDM \_ FORMATCODE \_ MP4**
</dt> <dd>

Mettre en forme le code d’un fichier MP4.

</dd> <dt>

<span id="WMDM_FORMATCODE_MP2"></span><span id="wmdm_formatcode_mp2"></span>**WMDM \_ FORMATCODE \_ MP2**
</dt> <dd>

Mettre en forme le code d’un fichier MP2.

</dd> <dt>

<span id="________WMDM_FORMATCODE_3G2_"></span><span id="________wmdm_formatcode_3g2_"></span>**WMDM \_ FORMATCODE \_ 3g2** 
</dt> <dd>

Mettre en forme le code pour un format de conteneur multimédia 3G2 (3GPP2). Un fichier de ce type peut contenir des données audio, vidéo ou texte.

</dd> <dt>

<span id="________________WMDM_FORMATCODE_AVCHD_"></span><span id="________________wmdm_formatcode_avchd_"></span>**WMDM \_ FORMATCODE \_ AVCHD** 
</dt> <dd>

Mettez en forme le code d’un fichier vidéo AVCHD (Advanced Video encodage High Definition).

</dd> <dt>

<span id="________________WMDM_FORMATCODE_ATSCTS_"></span><span id="________________wmdm_formatcode_atscts_"></span>**WMDM \_ FORMATCODE \_ ATSCTS** 
</dt> <dd>

Mettez en forme le code pour le format standard ATSCTS (Advanced TV Systems Committee).

</dd> <dt>

<span id="________________________WMDM_FORMATCODE_DVBTS_"></span><span id="________________________wmdm_formatcode_dvbts_"></span>**WMDM \_ FORMATCODE \_ DVBTS** 
</dt> <dd>

Code de format pour une vidéo MPEG-2 et MPEG-1 Layer II, ou AC-3, audio dans un flux de transport MPEG-2 compatible DVB.

</dd> <dt>

<span id="WMDM_FORMATCODE_UNDEFINEDCOLLECTION"></span><span id="wmdm_formatcode_undefinedcollection"></span>**WMDM \_ FORMATCODE \_ UNDEFINEDCOLLECTION**
</dt> <dd>

Mettre en forme le code pour une collection d’un type non défini.

</dd> <dt>

<span id="WMDM_FORMATCODE_ABSTRACTMULTIMEDIAALBUM"></span><span id="wmdm_formatcode_abstractmultimediaalbum"></span>**WMDM \_ FORMATCODE \_ ABSTRACTMULTIMEDIAALBUM**
</dt> <dd>

Mettez en forme le code d’un album multimédia où l’objet contient les propriétés d’un album multimédia et, éventuellement, les données. Le format des données contenues n’est pas défini par rapport à la spécification MTP.

</dd> <dt>

<span id="WMDM_FORMATCODE_ABSTRACTIMAGEALBUM"></span><span id="wmdm_formatcode_abstractimagealbum"></span>**WMDM \_ FORMATCODE \_ ABSTRACTIMAGEALBUM**
</dt> <dd>

Mettez en forme le code d’un album d’images où l’objet contient les propriétés d’un album d’images et, éventuellement, les données. Le format des données contenues n’est pas défini par rapport à la spécification MTP.

</dd> <dt>

<span id="WMDM_FORMATCODE_ABSTRACTAUDIOALBUM"></span><span id="wmdm_formatcode_abstractaudioalbum"></span>**WMDM \_ FORMATCODE \_ ABSTRACTAUDIOALBUM**
</dt> <dd>

Mettez en forme le code d’un album audio dans lequel l’objet contient les propriétés d’un album audio et, éventuellement, les données. Le format des données contenues n’est pas défini par rapport à la spécification MTP.

</dd> <dt>

<span id="WMDM_FORMATCODE_ABSTRACTVIDEOALBUM"></span><span id="wmdm_formatcode_abstractvideoalbum"></span>**WMDM \_ FORMATCODE \_ ABSTRACTVIDEOALBUM**
</dt> <dd>

Mettez en forme le code d’un album vidéo dans lequel l’objet contient les propriétés d’un album vidéo et, éventuellement, les données. Le format des données contenues n’est pas défini par rapport à la spécification MTP.

</dd> <dt>

<span id="WMDM_FORMATCODE_ABSTRACTAUDIOVIDEOPLAYLIST"></span><span id="wmdm_formatcode_abstractaudiovideoplaylist"></span>**WMDM \_ FORMATCODE \_ ABSTRACTAUDIOVIDEOPLAYLIST**
</dt> <dd>

Mettre en forme le code pour une sélection audio/vidéo où l’objet contient les propriétés d’une sélection audio/vidéo et, éventuellement, les données. Le format des données contenues n’est pas défini par rapport à la spécification MTP.

</dd> <dt>

<span id="WMDM_FORMATCODE_ABSTRACTCONTACTGROUP"></span><span id="wmdm_formatcode_abstractcontactgroup"></span>**WMDM \_ FORMATCODE \_ ABSTRACTCONTACTGROUP**
</dt> <dd>

Mettre en forme le code pour un groupe de contacts dans lequel l’objet contient les propriétés d’un groupe de contacts et, éventuellement, les données. Le format des données contenues n’est pas défini par rapport à la spécification MTP.

</dd> <dt>

<span id="WMDM_FORMATCODE_ABSTRACTMESSAGEFOLDER"></span><span id="wmdm_formatcode_abstractmessagefolder"></span>**WMDM \_ FORMATCODE \_ ABSTRACTMESSAGEFOLDER**
</dt> <dd>

Mettez en forme le code d’un dossier de message où l’objet contient les propriétés d’un dossier de message et, éventuellement, les données. Le format des données contenues n’est pas défini par rapport à la spécification MTP.

</dd> <dt>

<span id="WMDM_FORMATCODE_ABSTRACTCHAPTEREDPRODUCTION"></span><span id="wmdm_formatcode_abstractchapteredproduction"></span>**WMDM \_ FORMATCODE \_ ABSTRACTCHAPTEREDPRODUCTION**
</dt> <dd>

Mettez en forme le code pour une production par chapitre dans laquelle l’objet contient les propriétés d’une production par chapitre et, éventuellement, des données. Le format des données contenues n’est pas défini par rapport à la spécification MTP.

</dd> <dt>

<span id="WMDM_FORMATCODE_WPLPLAYLIST"></span><span id="wmdm_formatcode_wplplaylist"></span>**WMDM \_ FORMATCODE \_ WPLPLAYLIST**
</dt> <dd>

mettre en forme le code pour une sélection mise en forme avec Windows la mise en forme de la sélection de média.

</dd> <dt>

<span id="WMDM_FORMATCODE_M3UPLAYLIST"></span><span id="wmdm_formatcode_m3uplaylist"></span>**WMDM \_ FORMATCODE \_ M3UPLAYLIST**
</dt> <dd>

Mettre en forme le code pour une sélection avec une mise en forme M3U.

</dd> <dt>

<span id="WMDM_FORMATCODE_MPLPLAYLIST"></span><span id="wmdm_formatcode_mplplaylist"></span>**WMDM \_ FORMATCODE \_ MPLPLAYLIST**
</dt> <dd>

Mettre en forme le code d’une sélection avec une mise en forme MPL.

</dd> <dt>

<span id="WMDM_FORMATCODE_ASXPLAYLIST"></span><span id="wmdm_formatcode_asxplaylist"></span>**WMDM \_ FORMATCODE \_ ASXPLAYLIST**
</dt> <dd>

Formater le code pour une sélection avec une mise en forme ASX.

</dd> <dt>

<span id="WMDM_FORMATCODE_PLSPLAYLIST"></span><span id="wmdm_formatcode_plsplaylist"></span>**WMDM \_ FORMATCODE \_ PLSPLAYLIST**
</dt> <dd>

Mettre en forme le code d’une sélection avec une mise en forme patientez.

</dd> <dt>

<span id="WMDM_FORMATCODE_UNDEFINEDDOCUMENT"></span><span id="wmdm_formatcode_undefineddocument"></span>**WMDM \_ FORMATCODE \_ UNDEFINEDDOCUMENT**
</dt> <dd>

Mettre en forme le code d’un document de type non défini.

</dd> <dt>

<span id="WMDM_FORMATCODE_ABSTRACTDOCUMENT"></span><span id="wmdm_formatcode_abstractdocument"></span>**WMDM \_ FORMATCODE \_ ABSTRACTDOCUMENT**
</dt> <dd>

Mettre en forme le code d’un document dans lequel l’objet contient les propriétés d’un document et, éventuellement, les données. Le format des données contenues n’est pas défini par rapport à la spécification MTP.

</dd> <dt>

<span id="WMDM_FORMATCODE_XMLDOCUMENT"></span><span id="wmdm_formatcode_xmldocument"></span>**WMDM \_ FORMATCODE \_ XMLDOCUMENT**
</dt> <dd>

Mettre en forme le code d’un document XML.

</dd> <dt>

<span id="WMDM_FORMATCODE_MICROSOFTWORDDOCUMENT"></span><span id="wmdm_formatcode_microsoftworddocument"></span>**WMDM \_ FORMATCODE \_ MICROSOFTWORDDOCUMENT**
</dt> <dd>

mettre en forme le code d’un document Microsoft Word.

</dd> <dt>

<span id="WMDM_FORMATCODE_MHTCOMPILEDHTMLDOCUMENT"></span><span id="wmdm_formatcode_mhtcompiledhtmldocument"></span>**WMDM \_ FORMATCODE \_ MHTCOMPILEDHTMLDOCUMENT**
</dt> <dd>

Mettre en forme le code d’un document HTML compilé.

</dd> <dt>

<span id="WMDM_FORMATCODE_MICROSOFTEXCELSPREADSHEET"></span><span id="wmdm_formatcode_microsoftexcelspreadsheet"></span>**WMDM \_ FORMATCODE \_ MICROSOFTEXCELSPREADSHEET**
</dt> <dd>

mettre en forme le code d’une feuille de calcul Microsoft Excel.

</dd> <dt>

<span id="WMDM_FORMATCODE_MICROSOFTPOWERPOINTDOCUMENT"></span><span id="wmdm_formatcode_microsoftpowerpointdocument"></span>**WMDM \_ FORMATCODE \_ MICROSOFTPOWERPOINTDOCUMENT**
</dt> <dd>

mettez en forme le code d’un document Microsoft PowerPoint.

</dd> <dt>

<span id="WMDM_FORMATCODE_UNDEFINEDMESSAGE"></span><span id="wmdm_formatcode_undefinedmessage"></span>**WMDM \_ FORMATCODE \_ UNDEFINEDMESSAGE**
</dt> <dd>

Mettre en forme le code pour un message de type non défini.

</dd> <dt>

<span id="WMDM_FORMATCODE_ABSTRACTMESSAGE"></span><span id="wmdm_formatcode_abstractmessage"></span>**WMDM \_ FORMATCODE \_ ABSTRACTMESSAGE**
</dt> <dd>

Mettre en forme le code pour un message dans lequel l’objet contient les propriétés d’un message et, éventuellement, les données. Le format des données contenues n’est pas défini par rapport à la spécification MTP.

</dd> <dt>

<span id="WMDM_FORMATCODE_UNDEFINEDCONTACT"></span><span id="wmdm_formatcode_undefinedcontact"></span>**WMDM \_ FORMATCODE \_ UNDEFINEDCONTACT**
</dt> <dd>

Mettre en forme le code d’un contact de type non défini.

</dd> <dt>

<span id="WMDM_FORMATCODE_ABSTRACTCONTACT"></span><span id="wmdm_formatcode_abstractcontact"></span>**WMDM \_ FORMATCODE \_ ABSTRACTCONTACT**
</dt> <dd>

Mettre en forme le code d’un contact dans lequel l’objet contient les propriétés d’un contact et, éventuellement, les données. Le format des données contenues n’est pas défini par rapport à la spécification MTP.

</dd> <dt>

<span id="WMDM_FORMATCODE_VCARD2"></span><span id="wmdm_formatcode_vcard2"></span>**WMDM \_ FORMATCODE \_ VCARD2**
</dt> <dd>

Formater le code pour une carte électronique avec la mise en forme vCard version 2.

</dd> <dt>

<span id="WMDM_FORMATCODE_VCARD3"></span><span id="wmdm_formatcode_vcard3"></span>**WMDM \_ FORMATCODE \_ VCARD3**
</dt> <dd>

Formater le code pour une carte électronique avec la mise en forme vCard version 3.

</dd> <dt>

<span id="WMDM_FORMATCODE_UNDEFINEDCALENDARITEM"></span><span id="wmdm_formatcode_undefinedcalendaritem"></span>**WMDM \_ FORMATCODE \_ UNDEFINEDCALENDARITEM**
</dt> <dd>

Mettre en forme le code pour un élément de calendrier électronique d’un type non défini.

</dd> <dt>

<span id="WMDM_FORMATCODE_ABSTRACTCALENDARITEM"></span><span id="wmdm_formatcode_abstractcalendaritem"></span>**WMDM \_ FORMATCODE \_ ABSTRACTCALENDARITEM**
</dt> <dd>

Mettez en forme le code d’un élément de calendrier dans lequel l’objet contient les propriétés d’un élément de calendrier et, éventuellement, les données. Le format des données contenues n’est pas défini par rapport à la spécification MTP.

</dd> <dt>

<span id="WMDM_FORMATCODE_VCALENDAR1"></span><span id="wmdm_formatcode_vcalendar1"></span>**WMDM \_ FORMATCODE \_ VCALENDAR1**
</dt> <dd>

Mettez en forme le code d’un élément de calendrier électronique avec la mise en forme vCalendar version 1.

</dd> <dt>

<span id="WMDM_FORMATCODE_VCALENDAR2"></span><span id="wmdm_formatcode_vcalendar2"></span>**WMDM \_ FORMATCODE \_ VCALENDAR2**
</dt> <dd>

Mettre en forme le code d’un élément de calendrier électronique avec la mise en forme vCalendar version 2.

</dd> <dt>

<span id="WMDM_FORMATCODE_UNDEFINEDWINDOWSEXECUTABLE"></span><span id="wmdm_formatcode_undefinedwindowsexecutable"></span>**WMDM \_ FORMATCODE \_ UNDEFINEDWINDOWSEXECUTABLE**
</dt> <dd>

mettre en forme le code pour un exécutable basé sur le Windows de type non défini.

</dd> <dt>

<span id="WMDM_FORMATCODE_MEDIA_CAST"></span><span id="wmdm_formatcode_media_cast"></span>**WMDM \_ FORMATCODE \_ Media \_ cast**
</dt> <dd>

Mettre en forme le code d’un objet de transtypage multimédia.

</dd> <dt>

<span id="WMDM_FORMATCODE_SECTION"></span><span id="wmdm_formatcode_section"></span>**\_section WMDM FORMATCODE \_**
</dt> <dd>

Mettre en forme le code d’une section de données contenue dans un autre objet.

</dd> <dt>

<span id="________________________________WMDM_FORMATCODE_3G2A_"></span><span id="________________________________wmdm_formatcode_3g2a_"></span>**WMDM \_ FORMATCODE \_ 3G2A** 
</dt> <dd>

Mettre en forme le code pour un format de conteneur multimédia 3G2A (3GPP2A).

</dd> </dl>

## <a name="remarks"></a>Remarques

Pour découvrir les formats pris en charge par un appareil, une application peut utiliser [**IWMDMDevice3 :: GetProperty**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getproperty) pour interroger la propriété de l’appareil **g \_ wszWMDMFormatsSupported** .

Pour découvrir les fonctionnalités de l’appareil pour un format particulier, une application peut appeler [**IWMDMDevice3 :: GetFormatCapability**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getformatcapability).

Une application peut définir le code de format lors de la création d’un stockage sur l’appareil en incluant la propriété **g \_ wszWMDMFormatCode** dans les métadonnées passées dans le paramètre *pMetaData* d’un appel à [**IWMDMStorageControl3 :: Insert3**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol3-insert3).

Une application peut interroger le code de format d’un stockage en appelant [**IWMDMStorage3 :: GetMetadata**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage3-getmetadata) ou [**IWMDMStorage4 :: GetSpecifiedMetadata**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage4-getspecifiedmetadata) et en extrayant la propriété **g \_ wszWMDMFormatCode** .

Si l’appareil prend en charge la définition du code de format après la création du stockage, une application peut utiliser [**IWMDMStorage3 :: SetMetadata**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage3-setmetadata) pour définir la propriété **g \_ wszWMDMFormatCode** . Certains appareils peuvent ne pas autoriser la modification du code de format une fois le stockage créé sur l’appareil. Par conséquent, la définition de cette propriété avec les métadonnées passées dans [**IWMDMStorageControl3 :: Insert3**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol3-insert3) est fortement recommandée.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|-------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>WMDM. idl</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Types énumération**](enumeration-types.md)
</dt> <dt>

[**IWMDMDevice3::GetFormatCapability**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getformatcapability)
</dt> <dt>

[**IWMDMDevice3 :: GetProperty**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getproperty)
</dt> <dt>

[**IWMDMStorage3 :: GetMetadata**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage3-getmetadata)
</dt> <dt>

[**IWMDMStorage3::SetMetadata**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage3-setmetadata)
</dt> <dt>

[**IWMDMStorage4::GetSpecifiedMetadata**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage4-getspecifiedmetadata)
</dt> <dt>

[**IWMDMStorageControl3::Insert3**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol3-insert3)
</dt> <dt>

[**Constantes de métadonnées**](metadata-constants.md)
</dt> </dl>

 

 





