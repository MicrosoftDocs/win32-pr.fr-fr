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
ms.openlocfilehash: d04db31578f36455fdf77bb4044ad45e5ca9f9a6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106545897"
---
# <a name="wmdm_formatcode-enumeration"></a><span data-ttu-id="5c8cd-104">WMDM \_ FORMATCODE, énumération</span><span class="sxs-lookup"><span data-stu-id="5c8cd-104">WMDM\_FORMATCODE enumeration</span></span>

<span data-ttu-id="5c8cd-105">Le type d’énumération **WMDM \_ FORMATCODE** définit une liste de codes de format qui décrivent les types de contenu transférés vers et à partir d’un appareil.</span><span class="sxs-lookup"><span data-stu-id="5c8cd-105">The **WMDM\_FORMATCODE** enumeration type defines a list of format codes that describe types of content transferred to and from a device.</span></span>

## <a name="syntax"></a><span data-ttu-id="5c8cd-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5c8cd-106">Syntax</span></span>


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



## <a name="constants"></a><span data-ttu-id="5c8cd-107">Constantes</span><span class="sxs-lookup"><span data-stu-id="5c8cd-107">Constants</span></span>

<dl> <dt>

<span data-ttu-id="5c8cd-108"><span id="WMDM_FORMATCODE_NOTUSED"></span><span id="wmdm_formatcode_notused"></span>**WMDM \_ FORMATCODE \_ NOTUSED**</span><span class="sxs-lookup"><span data-stu-id="5c8cd-108"><span id="WMDM_FORMATCODE_NOTUSED"></span><span id="wmdm_formatcode_notused"></span>**WMDM\_FORMATCODE\_NOTUSED**</span></span>
</dt> <dd>

<span data-ttu-id="5c8cd-109">Aucun code de format n’est utilisé.</span><span class="sxs-lookup"><span data-stu-id="5c8cd-109">No format code is used.</span></span>

</dd> <dt>

<span data-ttu-id="5c8cd-110"><span id="WMDM_FORMATCODE_ALLIMAGES"></span><span id="wmdm_formatcode_allimages"></span>**WMDM \_ FORMATCODE \_ ALLIMAGES**</span><span class="sxs-lookup"><span data-stu-id="5c8cd-110"><span id="WMDM_FORMATCODE_ALLIMAGES"></span><span id="wmdm_formatcode_allimages"></span>**WMDM\_FORMATCODE\_ALLIMAGES**</span></span>
</dt> <dd>

<span data-ttu-id="5c8cd-111">Mettre en forme le code qui peut être utilisé pour interroger toutes les images.</span><span class="sxs-lookup"><span data-stu-id="5c8cd-111">Format code that can be used to query for all images.</span></span>

</dd> <dt>

<span data-ttu-id="5c8cd-112"><span id="WMDM_FORMATCODE_UNDEFINED"></span><span id="wmdm_formatcode_undefined"></span>**WMDM \_ FORMATCODE \_ non défini**</span><span class="sxs-lookup"><span data-stu-id="5c8cd-112"><span id="WMDM_FORMATCODE_UNDEFINED"></span><span id="wmdm_formatcode_undefined"></span>**WMDM\_FORMATCODE\_UNDEFINED**</span></span>
</dt> <dd>

<span data-ttu-id="5c8cd-113">Code de format utilisé pour rechercher tous les objets non définis.</span><span class="sxs-lookup"><span data-stu-id="5c8cd-113">Format code used to query for all undefined objects.</span></span>

</dd> <dt>

<span data-ttu-id="5c8cd-114"><span id="WMDM_FORMATCODE_ASSOCIATION"></span><span id="wmdm_formatcode_association"></span>**WMDM \_ FORMATCODE \_ Association**</span><span class="sxs-lookup"><span data-stu-id="5c8cd-114"><span id="WMDM_FORMATCODE_ASSOCIATION"></span><span id="wmdm_formatcode_association"></span>**WMDM\_FORMATCODE\_ASSOCIATION**</span></span>
</dt> <dd>

<span data-ttu-id="5c8cd-115">Code de format utilisé pour définir un lien entre deux objets.</span><span class="sxs-lookup"><span data-stu-id="5c8cd-115">Format code used to define a link between two objects.</span></span>

</dd> <dt>

<span data-ttu-id="5c8cd-116"><span id="WMDM_FORMATCODE_SCRIPT"></span><span id="wmdm_formatcode_script"></span>**\_script WMDM FORMATCODE \_**</span><span class="sxs-lookup"><span data-stu-id="5c8cd-116"><span id="WMDM_FORMATCODE_SCRIPT"></span><span id="wmdm_formatcode_script"></span>**WMDM\_FORMATCODE\_SCRIPT**</span></span>
</dt> <dd>

<span data-ttu-id="5c8cd-117">Mettre en forme le code d’un fichier de script.</span><span class="sxs-lookup"><span data-stu-id="5c8cd-117">Format code for a script file.</span></span>

</dd> <dt>

<span data-ttu-id="5c8cd-118"><span id="WMDM_FORMATCODE_EXECUTABLE"></span><span id="wmdm_formatcode_executable"></span>**\_exécutable FORMATCODE \_ WMDM**</span><span class="sxs-lookup"><span data-stu-id="5c8cd-118"><span id="WMDM_FORMATCODE_EXECUTABLE"></span><span id="wmdm_formatcode_executable"></span>**WMDM\_FORMATCODE\_EXECUTABLE**</span></span>
</dt> <dd>

<span data-ttu-id="5c8cd-119">Mettre en forme le code d’un fichier exécutable.</span><span class="sxs-lookup"><span data-stu-id="5c8cd-119">Format code for an executable file.</span></span>

</dd> <dt>

<span data-ttu-id="5c8cd-120"><span id="WMDM_FORMATCODE_TEXT"></span><span id="wmdm_formatcode_text"></span>**\_texte WMDM FORMATCODE \_**</span><span class="sxs-lookup"><span data-stu-id="5c8cd-120"><span id="WMDM_FORMATCODE_TEXT"></span><span id="wmdm_formatcode_text"></span>**WMDM\_FORMATCODE\_TEXT**</span></span>
</dt> <dd>

<span data-ttu-id="5c8cd-121">Mettre en forme le code d’un fichier texte.</span><span class="sxs-lookup"><span data-stu-id="5c8cd-121">Format code for a text file.</span></span>

</dd> <dt>

<span data-ttu-id="5c8cd-122"><span id="WMDM_FORMATCODE_HTML"></span><span id="wmdm_formatcode_html"></span>**\_HTML WMDM FORMATCODE \_**</span><span class="sxs-lookup"><span data-stu-id="5c8cd-122"><span id="WMDM_FORMATCODE_HTML"></span><span id="wmdm_formatcode_html"></span>**WMDM\_FORMATCODE\_HTML**</span></span>
</dt> <dd>

<span data-ttu-id="5c8cd-123">Mettre en forme le code d’un fichier HTML.</span><span class="sxs-lookup"><span data-stu-id="5c8cd-123">Format code for an HTML file.</span></span>

</dd> <dt>

<span data-ttu-id="5c8cd-124"><span id="WMDM_FORMATCODE_DPOF"></span><span id="wmdm_formatcode_dpof"></span>**WMDM \_ FORMATCODE \_ DPOF**</span><span class="sxs-lookup"><span data-stu-id="5c8cd-124"><span id="WMDM_FORMATCODE_DPOF"></span><span id="wmdm_formatcode_dpof"></span>**WMDM\_FORMATCODE\_DPOF**</span></span>
</dt> <dd>

<span data-ttu-id="5c8cd-125">Code de format utilisé pour représenter le format de la commande Digital Print.</span><span class="sxs-lookup"><span data-stu-id="5c8cd-125">Format code used to represent the digital print order format.</span></span>

</dd> <dt>

<span data-ttu-id="5c8cd-126"><span id="WMDM_FORMATCODE_AIFF"></span><span id="wmdm_formatcode_aiff"></span>**WMDM \_ FORMATCODE \_ AIFF**</span><span class="sxs-lookup"><span data-stu-id="5c8cd-126"><span id="WMDM_FORMATCODE_AIFF"></span><span id="wmdm_formatcode_aiff"></span>**WMDM\_FORMATCODE\_AIFF**</span></span>
</dt> <dd>

<span data-ttu-id="5c8cd-127">Code de format utilisé pour représenter le format de fichier d’échange audio.</span><span class="sxs-lookup"><span data-stu-id="5c8cd-127">Format code used to represent the audio interchange file format.</span></span>

</dd> <dt>

<span data-ttu-id="5c8cd-128"><span id="WMDM_FORMATCODE_WAVE"></span><span id="wmdm_formatcode_wave"></span>**WMDM \_ FORMATCODE \_ Wave**</span><span class="sxs-lookup"><span data-stu-id="5c8cd-128"><span id="WMDM_FORMATCODE_WAVE"></span><span id="wmdm_formatcode_wave"></span>**WMDM\_FORMATCODE\_WAVE**</span></span>
</dt> <dd>

<span data-ttu-id="5c8cd-129">Code de format utilisé pour un fichier WAV.</span><span class="sxs-lookup"><span data-stu-id="5c8cd-129">Format code used for a WAV file.</span></span>

</dd> <dt>

<span data-ttu-id="5c8cd-130"><span id="WMDM_FORMATCODE_MP3"></span><span id="wmdm_formatcode_mp3"></span>**\_Mp3 WMDM FORMATCODE \_**</span><span class="sxs-lookup"><span data-stu-id="5c8cd-130"><span id="WMDM_FORMATCODE_MP3"></span><span id="wmdm_formatcode_mp3"></span>**WMDM\_FORMATCODE\_MP3**</span></span>
</dt> <dd>

<span data-ttu-id="5c8cd-131">Code de format utilisé pour un fichier MP3.</span><span class="sxs-lookup"><span data-stu-id="5c8cd-131">Format code used for an MP3 file.</span></span>

</dd> <dt>

<span data-ttu-id="5c8cd-132"><span id="WMDM_FORMATCODE_AVI"></span><span id="wmdm_formatcode_avi"></span>**\_AVI WMDM FORMATCODE \_**</span><span class="sxs-lookup"><span data-stu-id="5c8cd-132"><span id="WMDM_FORMATCODE_AVI"></span><span id="wmdm_formatcode_avi"></span>**WMDM\_FORMATCODE\_AVI**</span></span>
</dt> <dd>

<span data-ttu-id="5c8cd-133">Code de format utilisé pour un fichier AVI.</span><span class="sxs-lookup"><span data-stu-id="5c8cd-133">Format code used for an AVI file.</span></span>

</dd> <dt>

<span data-ttu-id="5c8cd-134"><span id="WMDM_FORMATCODE_MPEG"></span><span id="wmdm_formatcode_mpeg"></span>**\_MPEG WMDM FORMATCODE \_**</span><span class="sxs-lookup"><span data-stu-id="5c8cd-134"><span id="WMDM_FORMATCODE_MPEG"></span><span id="wmdm_formatcode_mpeg"></span>**WMDM\_FORMATCODE\_MPEG**</span></span>
</dt> <dd>

<span data-ttu-id="5c8cd-135">Code de format utilisé pour un fichier MPEG.</span><span class="sxs-lookup"><span data-stu-id="5c8cd-135">Format code used for an MPEG file.</span></span>

</dd> <dt>

<span data-ttu-id="5c8cd-136"><span id="WMDM_FORMATCODE_ASF"></span><span id="wmdm_formatcode_asf"></span>**WMDM \_ FORMATCODE \_ ASF**</span><span class="sxs-lookup"><span data-stu-id="5c8cd-136"><span id="WMDM_FORMATCODE_ASF"></span><span id="wmdm_formatcode_asf"></span>**WMDM\_FORMATCODE\_ASF**</span></span>
</dt> <dd>

<span data-ttu-id="5c8cd-137">Code de format utilisé pour représenter un fichier ASF (Advanced Systems Format).</span><span class="sxs-lookup"><span data-stu-id="5c8cd-137">Format code used to represent an Advanced Systems Format (ASF) file.</span></span>

</dd> <dt>

<span data-ttu-id="5c8cd-138"><span id="WMDM_FORMATCODE_RESERVED_FIRST"></span><span id="wmdm_formatcode_reserved_first"></span>**WMDM \_ FORMATCODE \_ réservé en \_ premier**</span><span class="sxs-lookup"><span data-stu-id="5c8cd-138"><span id="WMDM_FORMATCODE_RESERVED_FIRST"></span><span id="wmdm_formatcode_reserved_first"></span>**WMDM\_FORMATCODE\_RESERVED\_FIRST**</span></span>
</dt> <dd>

<span data-ttu-id="5c8cd-139">Mettre en forme le code qui est le premier d’une plage réservée au protocole PTP (Image Transfer Protocol).</span><span class="sxs-lookup"><span data-stu-id="5c8cd-139">Format code that is the first in a range reserved for Picture Transfer Protocol (PTP).</span></span>

</dd> <dt>

<span data-ttu-id="5c8cd-140"><span id="WMDM_FORMATCODE_RESERVED_LAST"></span><span id="wmdm_formatcode_reserved_last"></span>**WMDM \_ FORMATCODE \_ réservé en \_ dernier**</span><span class="sxs-lookup"><span data-stu-id="5c8cd-140"><span id="WMDM_FORMATCODE_RESERVED_LAST"></span><span id="wmdm_formatcode_reserved_last"></span>**WMDM\_FORMATCODE\_RESERVED\_LAST**</span></span>
</dt> <dd>

<span data-ttu-id="5c8cd-141">Mettre en forme le code qui est le dernier dans une plage réservée pour PTP.</span><span class="sxs-lookup"><span data-stu-id="5c8cd-141">Format code that is last in a range reserved for PTP.</span></span>

</dd> <dt>

<span data-ttu-id="5c8cd-142"><span id="WMDM_FORMATCODE_IMAGE_UNDEFINED"></span><span id="wmdm_formatcode_image_undefined"></span>**\_image FORMATCODE \_ WMDM \_ non définie**</span><span class="sxs-lookup"><span data-stu-id="5c8cd-142"><span id="WMDM_FORMATCODE_IMAGE_UNDEFINED"></span><span id="wmdm_formatcode_image_undefined"></span>**WMDM\_FORMATCODE\_IMAGE\_UNDEFINED**</span></span>
</dt> <dd>

<span data-ttu-id="5c8cd-143">Code de format utilisé pour représenter l’image d’un type non défini.</span><span class="sxs-lookup"><span data-stu-id="5c8cd-143">Format code used to represent and image of an undefined type.</span></span>

</dd> <dt>

<span data-ttu-id="5c8cd-144"><span id="WMDM_FORMATCODE_IMAGE_EXIF"></span><span id="wmdm_formatcode_image_exif"></span>**\_image WMDM \_ FORMATCODE \_ EXIF**</span><span class="sxs-lookup"><span data-stu-id="5c8cd-144"><span id="WMDM_FORMATCODE_IMAGE_EXIF"></span><span id="wmdm_formatcode_image_exif"></span>**WMDM\_FORMATCODE\_IMAGE\_EXIF**</span></span>
</dt> <dd>

<span data-ttu-id="5c8cd-145">Mettre en forme le code d’un fichier EXIF.</span><span class="sxs-lookup"><span data-stu-id="5c8cd-145">Format code for an EXIF file.</span></span> <span data-ttu-id="5c8cd-146">Également utilisé pour les images JPEG non couvertes par WMDM \_ FORMATCODE \_ image \_ JP2 ou WMDM \_ FORMATCODE image JPX \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="5c8cd-146">Also used for JPEG images not covered by WMDM\_FORMATCODE\_IMAGE\_JP2 or WMDM\_FORMATCODE\_IMAGE\_JPX.</span></span>

</dd> <dt>

<span data-ttu-id="5c8cd-147"><span id="WMDM_FORMATCODE_IMAGE_TIFFEP"></span><span id="wmdm_formatcode_image_tiffep"></span>**\_image WMDM \_ FORMATCODE \_ TIFFEP**</span><span class="sxs-lookup"><span data-stu-id="5c8cd-147"><span id="WMDM_FORMATCODE_IMAGE_TIFFEP"></span><span id="wmdm_formatcode_image_tiffep"></span>**WMDM\_FORMATCODE\_IMAGE\_TIFFEP**</span></span>
</dt> <dd>

<span data-ttu-id="5c8cd-148">Code de format utilisé pour les images de type format de fichier image balisé pour la photographie électronique (TIFF/EP)</span><span class="sxs-lookup"><span data-stu-id="5c8cd-148">Format code used for images that are of type Tagged Image File Format for Electronic Photography (TIFF/EP)</span></span>

</dd> <dt>

<span data-ttu-id="5c8cd-149"><span id="WMDM_FORMATCODE_IMAGE_FLASHPIX"></span><span id="wmdm_formatcode_image_flashpix"></span>**WMDM \_ FORMATCODE \_ image \_ FLASHPIX**</span><span class="sxs-lookup"><span data-stu-id="5c8cd-149"><span id="WMDM_FORMATCODE_IMAGE_FLASHPIX"></span><span id="wmdm_formatcode_image_flashpix"></span>**WMDM\_FORMATCODE\_IMAGE\_FLASHPIX**</span></span>
</dt> <dd>

<span data-ttu-id="5c8cd-150">Mettre en forme le code d’un fichier de type FPX.</span><span class="sxs-lookup"><span data-stu-id="5c8cd-150">Format code for a file of type FPX.</span></span>

</dd> <dt>

<span data-ttu-id="5c8cd-151"><span id="WMDM_FORMATCODE_IMAGE_BMP"></span><span id="wmdm_formatcode_image_bmp"></span>**\_ \_ image BMP WMDM \_ FORMATCODE**</span><span class="sxs-lookup"><span data-stu-id="5c8cd-151"><span id="WMDM_FORMATCODE_IMAGE_BMP"></span><span id="wmdm_formatcode_image_bmp"></span>**WMDM\_FORMATCODE\_IMAGE\_BMP**</span></span>
</dt> <dd>

<span data-ttu-id="5c8cd-152">Mettre en forme le code d’un fichier de type BMP.</span><span class="sxs-lookup"><span data-stu-id="5c8cd-152">Format code for a file of type BMP.</span></span>

</dd> <dt>

<span data-ttu-id="5c8cd-153"><span id="WMDM_FORMATCODE_IMAGE_CIFF"></span><span id="wmdm_formatcode_image_ciff"></span>**\_image WMDM \_ FORMATCODE \_ CIFF**</span><span class="sxs-lookup"><span data-stu-id="5c8cd-153"><span id="WMDM_FORMATCODE_IMAGE_CIFF"></span><span id="wmdm_formatcode_image_ciff"></span>**WMDM\_FORMATCODE\_IMAGE\_CIFF**</span></span>
</dt> <dd>

<span data-ttu-id="5c8cd-154">Mettre en forme le code d’une image dans le format de fichier image de l’appareil photo.</span><span class="sxs-lookup"><span data-stu-id="5c8cd-154">Format code for an image in the camera image file format.</span></span>

</dd> <dt>

<span data-ttu-id="5c8cd-155"><span id="WMDM_FORMATCODE_IMAGE_GIF"></span><span id="wmdm_formatcode_image_gif"></span>**\_ \_ image gif WMDM \_ FORMATCODE**</span><span class="sxs-lookup"><span data-stu-id="5c8cd-155"><span id="WMDM_FORMATCODE_IMAGE_GIF"></span><span id="wmdm_formatcode_image_gif"></span>**WMDM\_FORMATCODE\_IMAGE\_GIF**</span></span>
</dt> <dd>

<span data-ttu-id="5c8cd-156">Mettre en forme le code d’un fichier GIF.</span><span class="sxs-lookup"><span data-stu-id="5c8cd-156">Format code for a GIF file.</span></span>

</dd> <dt>

<span data-ttu-id="5c8cd-157"><span id="WMDM_FORMATCODE_IMAGE_JFIF"></span><span id="wmdm_formatcode_image_jfif"></span>**WMDM \_ FORMATCODE \_ image \_ JFIF**</span><span class="sxs-lookup"><span data-stu-id="5c8cd-157"><span id="WMDM_FORMATCODE_IMAGE_JFIF"></span><span id="wmdm_formatcode_image_jfif"></span>**WMDM\_FORMATCODE\_IMAGE\_JFIF**</span></span>
</dt> <dd>

<span data-ttu-id="5c8cd-158">Mettre en forme le code d’un fichier de type JFIF.</span><span class="sxs-lookup"><span data-stu-id="5c8cd-158">Format code for a file of type JFIF.</span></span>

</dd> <dt>

<span data-ttu-id="5c8cd-159"><span id="WMDM_FORMATCODE_IMAGE_PCD"></span><span id="wmdm_formatcode_image_pcd"></span>**\_image WMDM \_ FORMATCODE \_ PCD**</span><span class="sxs-lookup"><span data-stu-id="5c8cd-159"><span id="WMDM_FORMATCODE_IMAGE_PCD"></span><span id="wmdm_formatcode_image_pcd"></span>**WMDM\_FORMATCODE\_IMAGE\_PCD**</span></span>
</dt> <dd>

<span data-ttu-id="5c8cd-160">Mettez en forme le code d’une image de type Photo CD.</span><span class="sxs-lookup"><span data-stu-id="5c8cd-160">Format code for an image of type photo cd.</span></span>

</dd> <dt>

<span data-ttu-id="5c8cd-161"><span id="WMDM_FORMATCODE_IMAGE_PICT"></span><span id="wmdm_formatcode_image_pict"></span>**\_ \_ image PICT WMDM \_ FORMATCODE**</span><span class="sxs-lookup"><span data-stu-id="5c8cd-161"><span id="WMDM_FORMATCODE_IMAGE_PICT"></span><span id="wmdm_formatcode_image_pict"></span>**WMDM\_FORMATCODE\_IMAGE\_PICT**</span></span>
</dt> <dd>

<span data-ttu-id="5c8cd-162">Mettez en forme le code d’une image de type PICT.</span><span class="sxs-lookup"><span data-stu-id="5c8cd-162">Format code for an image of type PICT.</span></span>

</dd> <dt>

<span data-ttu-id="5c8cd-163"><span id="WMDM_FORMATCODE_IMAGE_PNG"></span><span id="wmdm_formatcode_image_png"></span>**\_ \_ image png WMDM \_ FORMATCODE**</span><span class="sxs-lookup"><span data-stu-id="5c8cd-163"><span id="WMDM_FORMATCODE_IMAGE_PNG"></span><span id="wmdm_formatcode_image_png"></span>**WMDM\_FORMATCODE\_IMAGE\_PNG**</span></span>
</dt> <dd>

<span data-ttu-id="5c8cd-164">Mettre en forme le code d’une image de type PNG.</span><span class="sxs-lookup"><span data-stu-id="5c8cd-164">Format code for an image of type PNG.</span></span>

</dd> <dt>

<span data-ttu-id="5c8cd-165"><span id="WMDM_FORMATCODE_IMAGE_TIFF"></span><span id="wmdm_formatcode_image_tiff"></span>**\_ \_ image TIFF WMDM \_ FORMATCODE**</span><span class="sxs-lookup"><span data-stu-id="5c8cd-165"><span id="WMDM_FORMATCODE_IMAGE_TIFF"></span><span id="wmdm_formatcode_image_tiff"></span>**WMDM\_FORMATCODE\_IMAGE\_TIFF**</span></span>
</dt> <dd>

<span data-ttu-id="5c8cd-166">Mettre en forme le code d’un fichier de type TIFF.</span><span class="sxs-lookup"><span data-stu-id="5c8cd-166">Format code for a file of type TIFF.</span></span>

</dd> <dt>

<span data-ttu-id="5c8cd-167"><span id="WMDM_FORMATCODE_IMAGE_TIFFIT"></span><span id="wmdm_formatcode_image_tiffit"></span>**\_image WMDM \_ FORMATCODE \_ TIFFIT**</span><span class="sxs-lookup"><span data-stu-id="5c8cd-167"><span id="WMDM_FORMATCODE_IMAGE_TIFFIT"></span><span id="wmdm_formatcode_image_tiffit"></span>**WMDM\_FORMATCODE\_IMAGE\_TIFFIT**</span></span>
</dt> <dd>

<span data-ttu-id="5c8cd-168">Mettez en forme le code d’une image de type format de fichier image balisé avec la technologie image.</span><span class="sxs-lookup"><span data-stu-id="5c8cd-168">Format code for an image of type Tagged Image File Format with image technology.</span></span>

</dd> <dt>

<span data-ttu-id="5c8cd-169"><span id="WMDM_FORMATCODE_IMAGE_JP2"></span><span id="wmdm_formatcode_image_jp2"></span>**\_Image WMDM \_ FORMATCODE \_ JP2**</span><span class="sxs-lookup"><span data-stu-id="5c8cd-169"><span id="WMDM_FORMATCODE_IMAGE_JP2"></span><span id="wmdm_formatcode_image_jp2"></span>**WMDM\_FORMATCODE\_IMAGE\_JP2**</span></span>
</dt> <dd>

<span data-ttu-id="5c8cd-170">Mettre en forme le code pour une image JPEG200.</span><span class="sxs-lookup"><span data-stu-id="5c8cd-170">Format code for a jpeg200 image.</span></span>

</dd> <dt>

<span data-ttu-id="5c8cd-171"><span id="WMDM_FORMATCODE_IMAGE_JPX"></span><span id="wmdm_formatcode_image_jpx"></span>**\_image WMDM \_ FORMATCODE \_ JPX**</span><span class="sxs-lookup"><span data-stu-id="5c8cd-171"><span id="WMDM_FORMATCODE_IMAGE_JPX"></span><span id="wmdm_formatcode_image_jpx"></span>**WMDM\_FORMATCODE\_IMAGE\_JPX**</span></span>
</dt> <dd>

<span data-ttu-id="5c8cd-172">Mettez en forme le code pour une image générée sur JPEG200, à l’aide de l’inscription d’image continue étendue.</span><span class="sxs-lookup"><span data-stu-id="5c8cd-172">Format code for an image built on JPEG200, using extended still image registration.</span></span> <span data-ttu-id="5c8cd-173">L’extension de nom de fichier est généralement. JPF ou. JPX.</span><span class="sxs-lookup"><span data-stu-id="5c8cd-173">The file name extension is usually .jpf or .jpx.</span></span>

</dd> <dt>

<span data-ttu-id="5c8cd-174"><span id="WMDM_FORMATCODE_IMAGE_RESERVED_FIRST"></span><span id="wmdm_formatcode_image_reserved_first"></span>**\_image WMDM \_ FORMATCODE \_ réservée en \_ premier**</span><span class="sxs-lookup"><span data-stu-id="5c8cd-174"><span id="WMDM_FORMATCODE_IMAGE_RESERVED_FIRST"></span><span id="wmdm_formatcode_image_reserved_first"></span>**WMDM\_FORMATCODE\_IMAGE\_RESERVED\_FIRST**</span></span>
</dt> <dd>

<span data-ttu-id="5c8cd-175">Mettre en forme le code qui est le premier d’une plage réservée pour une référence d’image dans PTP.</span><span class="sxs-lookup"><span data-stu-id="5c8cd-175">Format code that is the first in a range reserved for an image reference in PTP.</span></span>

</dd> <dt>

<span data-ttu-id="5c8cd-176"><span id="WMDM_FORMATCODE_IMAGE_RESERVED_LAST"></span><span id="wmdm_formatcode_image_reserved_last"></span>**\_image WMDM \_ FORMATCODE \_ réservée en \_ dernier**</span><span class="sxs-lookup"><span data-stu-id="5c8cd-176"><span id="WMDM_FORMATCODE_IMAGE_RESERVED_LAST"></span><span id="wmdm_formatcode_image_reserved_last"></span>**WMDM\_FORMATCODE\_IMAGE\_RESERVED\_LAST**</span></span>
</dt> <dd>

<span data-ttu-id="5c8cd-177">Mettre en forme le code qui est le dernier d’une plage réservée à une référence d’image dans PTP.</span><span class="sxs-lookup"><span data-stu-id="5c8cd-177">Format code that is the last in a range reserved for an image reference in PTP.</span></span>

</dd> <dt>

<span data-ttu-id="5c8cd-178"><span id="WMDM_FORMATCODE_UNDEFINEDFIRMWARE"></span><span id="wmdm_formatcode_undefinedfirmware"></span>**WMDM \_ FORMATCODE \_ UNDEFINEDFIRMWARE**</span><span class="sxs-lookup"><span data-stu-id="5c8cd-178"><span id="WMDM_FORMATCODE_UNDEFINEDFIRMWARE"></span><span id="wmdm_formatcode_undefinedfirmware"></span>**WMDM\_FORMATCODE\_UNDEFINEDFIRMWARE**</span></span>
</dt> <dd>

<span data-ttu-id="5c8cd-179">Mettre en forme le code lorsque le microprogramme n’est pas défini.</span><span class="sxs-lookup"><span data-stu-id="5c8cd-179">Format code when firmware is undefined.</span></span>

</dd> <dt>

<span data-ttu-id="5c8cd-180"><span id="________WMDM_FORMATCODE_WBMP_"></span><span id="________wmdm_formatcode_wbmp_"></span>**WMDM \_ FORMATCODE \_ WBMP**</span><span class="sxs-lookup"><span data-stu-id="5c8cd-180"><span id="________WMDM_FORMATCODE_WBMP_"></span><span id="________wmdm_formatcode_wbmp_"></span> **WMDM\_FORMATCODE\_WBMP**</span></span> 
</dt> <dd>

<span data-ttu-id="5c8cd-181">Code de format pour une image bitmap de protocole d’application sans fil (. WBMP).</span><span class="sxs-lookup"><span data-stu-id="5c8cd-181">Format code for a Wireless Application Protocol Bitmap (.wbmp) image.</span></span>

</dd> <dt>

<span data-ttu-id="5c8cd-182"><span id="________________WMDM_FORMATCODE_JPEGXR_"></span><span id="________________wmdm_formatcode_jpegxr_"></span>**WMDM \_ FORMATCODE \_ JPEGXR**</span><span class="sxs-lookup"><span data-stu-id="5c8cd-182"><span id="________________WMDM_FORMATCODE_JPEGXR_"></span><span id="________________wmdm_formatcode_jpegxr_"></span> **WMDM\_FORMATCODE\_JPEGXR**</span></span> 
</dt> <dd>

<span data-ttu-id="5c8cd-183">Mettre en forme le code d’une image de photo HD</span><span class="sxs-lookup"><span data-stu-id="5c8cd-183">Format code for an HD Photo image</span></span>

</dd> <dt>

<span data-ttu-id="5c8cd-184"><span id="WMDM_FORMATCODE_WINDOWSIMAGEFORMAT"></span><span id="wmdm_formatcode_windowsimageformat"></span>**WMDM \_ FORMATCODE \_ WINDOWSIMAGEFORMAT**</span><span class="sxs-lookup"><span data-stu-id="5c8cd-184"><span id="WMDM_FORMATCODE_WINDOWSIMAGEFORMAT"></span><span id="wmdm_formatcode_windowsimageformat"></span>**WMDM\_FORMATCODE\_WINDOWSIMAGEFORMAT**</span></span>
</dt> <dd>

<span data-ttu-id="5c8cd-185">Mettre en forme le code pour le format d’image Windows.</span><span class="sxs-lookup"><span data-stu-id="5c8cd-185">Format code for Windows image format.</span></span>

</dd> <dt>

<span data-ttu-id="5c8cd-186"><span id="WMDM_FORMATCODE_UNDEFINEDAUDIO"></span><span id="wmdm_formatcode_undefinedaudio"></span>**WMDM \_ FORMATCODE \_ UNDEFINEDAUDIO**</span><span class="sxs-lookup"><span data-stu-id="5c8cd-186"><span id="WMDM_FORMATCODE_UNDEFINEDAUDIO"></span><span id="wmdm_formatcode_undefinedaudio"></span>**WMDM\_FORMATCODE\_UNDEFINEDAUDIO**</span></span>
</dt> <dd>

<span data-ttu-id="5c8cd-187">Mettre en forme le code pour un fichier audio de type non défini.</span><span class="sxs-lookup"><span data-stu-id="5c8cd-187">Format code for an audio file of undefined type.</span></span>

</dd> <dt>

<span data-ttu-id="5c8cd-188"><span id="WMDM_FORMATCODE_WMA"></span><span id="wmdm_formatcode_wma"></span>**WMDM \_ FORMATCODE \_ WMA**</span><span class="sxs-lookup"><span data-stu-id="5c8cd-188"><span id="WMDM_FORMATCODE_WMA"></span><span id="wmdm_formatcode_wma"></span>**WMDM\_FORMATCODE\_WMA**</span></span>
</dt> <dd>

<span data-ttu-id="5c8cd-189">Mettre en forme le code d’un fichier Windows Media Audio (WMA).</span><span class="sxs-lookup"><span data-stu-id="5c8cd-189">Format code for a Windows Media Audio (WMA) file.</span></span>

</dd> <dt>

<span data-ttu-id="5c8cd-190"><span id="WMDM_FORMATCODE_OGG"></span><span id="wmdm_formatcode_ogg"></span>**WMDM \_ FORMATCODE \_ OGG**</span><span class="sxs-lookup"><span data-stu-id="5c8cd-190"><span id="WMDM_FORMATCODE_OGG"></span><span id="wmdm_formatcode_ogg"></span>**WMDM\_FORMATCODE\_OGG**</span></span>
</dt> <dd>

<span data-ttu-id="5c8cd-191">Mettre en forme le code d’un fichier audio encodé en Vorbis dans un conteneur Ogg.</span><span class="sxs-lookup"><span data-stu-id="5c8cd-191">Format code for a Vorbis-encoded audio file in an Ogg container.</span></span>

</dd> <dt>

<span data-ttu-id="5c8cd-192"><span id="WMDM_FORMATCODE_AAC"></span><span id="wmdm_formatcode_aac"></span>**WMDM \_ FORMATCODE \_ AAC**</span><span class="sxs-lookup"><span data-stu-id="5c8cd-192"><span id="WMDM_FORMATCODE_AAC"></span><span id="wmdm_formatcode_aac"></span>**WMDM\_FORMATCODE\_AAC**</span></span>
</dt> <dd>

<span data-ttu-id="5c8cd-193">Mettre en forme le code d’un fichier d’encodage audio avancé (AAC).</span><span class="sxs-lookup"><span data-stu-id="5c8cd-193">Format code for an Advanced Audio Coding (AAC) file.</span></span>

</dd> <dt>

<span data-ttu-id="5c8cd-194"><span id="WMDM_FORMATCODE_AUDIBLE"></span><span id="wmdm_formatcode_audible"></span>**WMDM \_ FORMATCODE \_ audible**</span><span class="sxs-lookup"><span data-stu-id="5c8cd-194"><span id="WMDM_FORMATCODE_AUDIBLE"></span><span id="wmdm_formatcode_audible"></span>**WMDM\_FORMATCODE\_AUDIBLE**</span></span>
</dt> <dd>

<span data-ttu-id="5c8cd-195">Mettre en forme le code d’un fichier audible.</span><span class="sxs-lookup"><span data-stu-id="5c8cd-195">Format code for an Audible file.</span></span>

</dd> <dt>

<span data-ttu-id="5c8cd-196"><span id="WMDM_FORMATCODE_FLAC"></span><span id="wmdm_formatcode_flac"></span>**WMDM \_ FORMATCODE \_ FLAC**</span><span class="sxs-lookup"><span data-stu-id="5c8cd-196"><span id="WMDM_FORMATCODE_FLAC"></span><span id="wmdm_formatcode_flac"></span>**WMDM\_FORMATCODE\_FLAC**</span></span>
</dt> <dd>

<span data-ttu-id="5c8cd-197">Mettez en forme le code d’un fichier de codec audio sans perte (FLAC) gratuit.</span><span class="sxs-lookup"><span data-stu-id="5c8cd-197">Format code for a Free Lossless Audio Codec (FLAC) file.</span></span>

</dd> <dt>

<span data-ttu-id="5c8cd-198"><span id="________WMDM_FORMATCODE_QCELP_"></span><span id="________wmdm_formatcode_qcelp_"></span>**WMDM \_ FORMATCODE \_ QCELP**</span><span class="sxs-lookup"><span data-stu-id="5c8cd-198"><span id="________WMDM_FORMATCODE_QCELP_"></span><span id="________wmdm_formatcode_qcelp_"></span> **WMDM\_FORMATCODE\_QCELP**</span></span> 
</dt> <dd>

<span data-ttu-id="5c8cd-199">Code de format pour un fichier de codec QCELP (code de prédiction linéaire) Qualcomm.</span><span class="sxs-lookup"><span data-stu-id="5c8cd-199">Format code for a Qualcomm Code Excited Linear Prediction (QCELP) codec file.</span></span>

</dd> <dt>

<span data-ttu-id="5c8cd-200"><span id="________WMDM_FORMATCODE_AMR_"></span><span id="________wmdm_formatcode_amr_"></span>**WMDM \_ FORMATCODE \_ Amr**</span><span class="sxs-lookup"><span data-stu-id="5c8cd-200"><span id="________WMDM_FORMATCODE_AMR_"></span><span id="________wmdm_formatcode_amr_"></span> **WMDM\_FORMATCODE\_AMR**</span></span> 
</dt> <dd>

<span data-ttu-id="5c8cd-201">Code de format pour un fichier de Codec AMR (multi-rate audio) adaptatif.</span><span class="sxs-lookup"><span data-stu-id="5c8cd-201">Format code for an Adaptive Multi-Rate audio (AMR) codec file.</span></span>

</dd> <dt>

<span data-ttu-id="5c8cd-202"><span id="WMDM_FORMATCODE_UNDEFINEDVIDEO"></span><span id="wmdm_formatcode_undefinedvideo"></span>**WMDM \_ FORMATCODE \_ UNDEFINEDVIDEO**</span><span class="sxs-lookup"><span data-stu-id="5c8cd-202"><span id="WMDM_FORMATCODE_UNDEFINEDVIDEO"></span><span id="wmdm_formatcode_undefinedvideo"></span>**WMDM\_FORMATCODE\_UNDEFINEDVIDEO**</span></span>
</dt> <dd>

<span data-ttu-id="5c8cd-203">Mettre en forme le code d’un fichier vidéo avec un type non défini.</span><span class="sxs-lookup"><span data-stu-id="5c8cd-203">Format code for a video file with an undefined type.</span></span>

</dd> <dt>

<span data-ttu-id="5c8cd-204"><span id="WMDM_FORMATCODE_WMV"></span><span id="wmdm_formatcode_wmv"></span>**\_WMV FORMATCODE \_ WMDM**</span><span class="sxs-lookup"><span data-stu-id="5c8cd-204"><span id="WMDM_FORMATCODE_WMV"></span><span id="wmdm_formatcode_wmv"></span>**WMDM\_FORMATCODE\_WMV**</span></span>
</dt> <dd>

<span data-ttu-id="5c8cd-205">Mettez en forme le code d’un fichier Windows Media Video (WMV).</span><span class="sxs-lookup"><span data-stu-id="5c8cd-205">Format code for a Windows Media Video (WMV) file.</span></span>

</dd> <dt>

<span data-ttu-id="5c8cd-206"><span id="WMDM_FORMATCODE_MP4"></span><span id="wmdm_formatcode_mp4"></span>**WMDM \_ FORMATCODE \_ MP4**</span><span class="sxs-lookup"><span data-stu-id="5c8cd-206"><span id="WMDM_FORMATCODE_MP4"></span><span id="wmdm_formatcode_mp4"></span>**WMDM\_FORMATCODE\_MP4**</span></span>
</dt> <dd>

<span data-ttu-id="5c8cd-207">Mettre en forme le code d’un fichier MP4.</span><span class="sxs-lookup"><span data-stu-id="5c8cd-207">Format code for an MP4 file.</span></span>

</dd> <dt>

<span data-ttu-id="5c8cd-208"><span id="WMDM_FORMATCODE_MP2"></span><span id="wmdm_formatcode_mp2"></span>**WMDM \_ FORMATCODE \_ MP2**</span><span class="sxs-lookup"><span data-stu-id="5c8cd-208"><span id="WMDM_FORMATCODE_MP2"></span><span id="wmdm_formatcode_mp2"></span>**WMDM\_FORMATCODE\_MP2**</span></span>
</dt> <dd>

<span data-ttu-id="5c8cd-209">Mettre en forme le code d’un fichier MP2.</span><span class="sxs-lookup"><span data-stu-id="5c8cd-209">Format code for an MP2 file.</span></span>

</dd> <dt>

<span data-ttu-id="5c8cd-210"><span id="________WMDM_FORMATCODE_3G2_"></span><span id="________wmdm_formatcode_3g2_"></span>**WMDM \_ FORMATCODE \_ 3g2**</span><span class="sxs-lookup"><span data-stu-id="5c8cd-210"><span id="________WMDM_FORMATCODE_3G2_"></span><span id="________wmdm_formatcode_3g2_"></span> **WMDM\_FORMATCODE\_3G2**</span></span> 
</dt> <dd>

<span data-ttu-id="5c8cd-211">Mettre en forme le code pour un format de conteneur multimédia 3G2 (3GPP2).</span><span class="sxs-lookup"><span data-stu-id="5c8cd-211">Format code for a 3G2 (3GPP2) multimedia container format.</span></span> <span data-ttu-id="5c8cd-212">Un fichier de ce type peut contenir des données audio, vidéo ou texte.</span><span class="sxs-lookup"><span data-stu-id="5c8cd-212">A file of this type may contain audio, video, or text.</span></span>

</dd> <dt>

<span data-ttu-id="5c8cd-213"><span id="________________WMDM_FORMATCODE_AVCHD_"></span><span id="________________wmdm_formatcode_avchd_"></span>**WMDM \_ FORMATCODE \_ AVCHD**</span><span class="sxs-lookup"><span data-stu-id="5c8cd-213"><span id="________________WMDM_FORMATCODE_AVCHD_"></span><span id="________________wmdm_formatcode_avchd_"></span> **WMDM\_FORMATCODE\_AVCHD**</span></span> 
</dt> <dd>

<span data-ttu-id="5c8cd-214">Mettez en forme le code d’un fichier vidéo AVCHD (Advanced Video encodage High Definition).</span><span class="sxs-lookup"><span data-stu-id="5c8cd-214">Format code for an AVCHD (Advanced Video Coding High Definition) video file.</span></span>

</dd> <dt>

<span data-ttu-id="5c8cd-215"><span id="________________WMDM_FORMATCODE_ATSCTS_"></span><span id="________________wmdm_formatcode_atscts_"></span>**WMDM \_ FORMATCODE \_ ATSCTS**</span><span class="sxs-lookup"><span data-stu-id="5c8cd-215"><span id="________________WMDM_FORMATCODE_ATSCTS_"></span><span id="________________wmdm_formatcode_atscts_"></span> **WMDM\_FORMATCODE\_ATSCTS**</span></span> 
</dt> <dd>

<span data-ttu-id="5c8cd-216">Mettez en forme le code pour le format standard ATSCTS (Advanced TV Systems Committee).</span><span class="sxs-lookup"><span data-stu-id="5c8cd-216">Format code for the Advanced Television Systems Committee (ATSCTS) format standard.</span></span>

</dd> <dt>

<span data-ttu-id="5c8cd-217"><span id="________________________WMDM_FORMATCODE_DVBTS_"></span><span id="________________________wmdm_formatcode_dvbts_"></span>**WMDM \_ FORMATCODE \_ DVBTS**</span><span class="sxs-lookup"><span data-stu-id="5c8cd-217"><span id="________________________WMDM_FORMATCODE_DVBTS_"></span><span id="________________________wmdm_formatcode_dvbts_"></span> **WMDM\_FORMATCODE\_DVBTS**</span></span> 
</dt> <dd>

<span data-ttu-id="5c8cd-218">Code de format pour une vidéo MPEG-2 et MPEG-1 Layer II, ou AC-3, audio dans un flux de transport MPEG-2 compatible DVB.</span><span class="sxs-lookup"><span data-stu-id="5c8cd-218">Format code for an MPEG-2 video and MPEG-1 Layer II, or AC-3, audio within a DVB-compliant MPEG-2 Transport Stream.</span></span>

</dd> <dt>

<span data-ttu-id="5c8cd-219"><span id="WMDM_FORMATCODE_UNDEFINEDCOLLECTION"></span><span id="wmdm_formatcode_undefinedcollection"></span>**WMDM \_ FORMATCODE \_ UNDEFINEDCOLLECTION**</span><span class="sxs-lookup"><span data-stu-id="5c8cd-219"><span id="WMDM_FORMATCODE_UNDEFINEDCOLLECTION"></span><span id="wmdm_formatcode_undefinedcollection"></span>**WMDM\_FORMATCODE\_UNDEFINEDCOLLECTION**</span></span>
</dt> <dd>

<span data-ttu-id="5c8cd-220">Mettre en forme le code pour une collection d’un type non défini.</span><span class="sxs-lookup"><span data-stu-id="5c8cd-220">Format code for a collection of an undefined type.</span></span>

</dd> <dt>

<span data-ttu-id="5c8cd-221"><span id="WMDM_FORMATCODE_ABSTRACTMULTIMEDIAALBUM"></span><span id="wmdm_formatcode_abstractmultimediaalbum"></span>**WMDM \_ FORMATCODE \_ ABSTRACTMULTIMEDIAALBUM**</span><span class="sxs-lookup"><span data-stu-id="5c8cd-221"><span id="WMDM_FORMATCODE_ABSTRACTMULTIMEDIAALBUM"></span><span id="wmdm_formatcode_abstractmultimediaalbum"></span>**WMDM\_FORMATCODE\_ABSTRACTMULTIMEDIAALBUM**</span></span>
</dt> <dd>

<span data-ttu-id="5c8cd-222">Mettez en forme le code d’un album multimédia où l’objet contient les propriétés d’un album multimédia et, éventuellement, les données.</span><span class="sxs-lookup"><span data-stu-id="5c8cd-222">Format code for a multimedia album where the object contains the properties of a multimedia album and, optionally, data.</span></span> <span data-ttu-id="5c8cd-223">Le format des données contenues n’est pas défini par rapport à la spécification MTP.</span><span class="sxs-lookup"><span data-stu-id="5c8cd-223">Any contained data is of an undefined format with respect to the MTP specification.</span></span>

</dd> <dt>

<span data-ttu-id="5c8cd-224"><span id="WMDM_FORMATCODE_ABSTRACTIMAGEALBUM"></span><span id="wmdm_formatcode_abstractimagealbum"></span>**WMDM \_ FORMATCODE \_ ABSTRACTIMAGEALBUM**</span><span class="sxs-lookup"><span data-stu-id="5c8cd-224"><span id="WMDM_FORMATCODE_ABSTRACTIMAGEALBUM"></span><span id="wmdm_formatcode_abstractimagealbum"></span>**WMDM\_FORMATCODE\_ABSTRACTIMAGEALBUM**</span></span>
</dt> <dd>

<span data-ttu-id="5c8cd-225">Mettez en forme le code d’un album d’images où l’objet contient les propriétés d’un album d’images et, éventuellement, les données.</span><span class="sxs-lookup"><span data-stu-id="5c8cd-225">Format code for an image album where the object contains the properties of an image album and, optionally, data.</span></span> <span data-ttu-id="5c8cd-226">Le format des données contenues n’est pas défini par rapport à la spécification MTP.</span><span class="sxs-lookup"><span data-stu-id="5c8cd-226">Any contained data is of an undefined format with respect to the MTP specification.</span></span>

</dd> <dt>

<span data-ttu-id="5c8cd-227"><span id="WMDM_FORMATCODE_ABSTRACTAUDIOALBUM"></span><span id="wmdm_formatcode_abstractaudioalbum"></span>**WMDM \_ FORMATCODE \_ ABSTRACTAUDIOALBUM**</span><span class="sxs-lookup"><span data-stu-id="5c8cd-227"><span id="WMDM_FORMATCODE_ABSTRACTAUDIOALBUM"></span><span id="wmdm_formatcode_abstractaudioalbum"></span>**WMDM\_FORMATCODE\_ABSTRACTAUDIOALBUM**</span></span>
</dt> <dd>

<span data-ttu-id="5c8cd-228">Mettez en forme le code d’un album audio dans lequel l’objet contient les propriétés d’un album audio et, éventuellement, les données.</span><span class="sxs-lookup"><span data-stu-id="5c8cd-228">Format code for an audio album where the object contains the properties of an audio album and, optionally, data.</span></span> <span data-ttu-id="5c8cd-229">Le format des données contenues n’est pas défini par rapport à la spécification MTP.</span><span class="sxs-lookup"><span data-stu-id="5c8cd-229">Any contained data is of an undefined format with respect to the MTP specification.</span></span>

</dd> <dt>

<span data-ttu-id="5c8cd-230"><span id="WMDM_FORMATCODE_ABSTRACTVIDEOALBUM"></span><span id="wmdm_formatcode_abstractvideoalbum"></span>**WMDM \_ FORMATCODE \_ ABSTRACTVIDEOALBUM**</span><span class="sxs-lookup"><span data-stu-id="5c8cd-230"><span id="WMDM_FORMATCODE_ABSTRACTVIDEOALBUM"></span><span id="wmdm_formatcode_abstractvideoalbum"></span>**WMDM\_FORMATCODE\_ABSTRACTVIDEOALBUM**</span></span>
</dt> <dd>

<span data-ttu-id="5c8cd-231">Mettez en forme le code d’un album vidéo dans lequel l’objet contient les propriétés d’un album vidéo et, éventuellement, les données.</span><span class="sxs-lookup"><span data-stu-id="5c8cd-231">Format code for a video album where the object contains the properties of a video album and, optionally, data.</span></span> <span data-ttu-id="5c8cd-232">Le format des données contenues n’est pas défini par rapport à la spécification MTP.</span><span class="sxs-lookup"><span data-stu-id="5c8cd-232">Any contained data is of an undefined format with respect to the MTP specification.</span></span>

</dd> <dt>

<span data-ttu-id="5c8cd-233"><span id="WMDM_FORMATCODE_ABSTRACTAUDIOVIDEOPLAYLIST"></span><span id="wmdm_formatcode_abstractaudiovideoplaylist"></span>**WMDM \_ FORMATCODE \_ ABSTRACTAUDIOVIDEOPLAYLIST**</span><span class="sxs-lookup"><span data-stu-id="5c8cd-233"><span id="WMDM_FORMATCODE_ABSTRACTAUDIOVIDEOPLAYLIST"></span><span id="wmdm_formatcode_abstractaudiovideoplaylist"></span>**WMDM\_FORMATCODE\_ABSTRACTAUDIOVIDEOPLAYLIST**</span></span>
</dt> <dd>

<span data-ttu-id="5c8cd-234">Mettre en forme le code pour une sélection audio/vidéo où l’objet contient les propriétés d’une sélection audio/vidéo et, éventuellement, les données.</span><span class="sxs-lookup"><span data-stu-id="5c8cd-234">Format code for an audio/video playlist where the object contains the properties of an audio/video playlist and, optionally, data.</span></span> <span data-ttu-id="5c8cd-235">Le format des données contenues n’est pas défini par rapport à la spécification MTP.</span><span class="sxs-lookup"><span data-stu-id="5c8cd-235">Any contained data is of an undefined format with respect to the MTP specification.</span></span>

</dd> <dt>

<span data-ttu-id="5c8cd-236"><span id="WMDM_FORMATCODE_ABSTRACTCONTACTGROUP"></span><span id="wmdm_formatcode_abstractcontactgroup"></span>**WMDM \_ FORMATCODE \_ ABSTRACTCONTACTGROUP**</span><span class="sxs-lookup"><span data-stu-id="5c8cd-236"><span id="WMDM_FORMATCODE_ABSTRACTCONTACTGROUP"></span><span id="wmdm_formatcode_abstractcontactgroup"></span>**WMDM\_FORMATCODE\_ABSTRACTCONTACTGROUP**</span></span>
</dt> <dd>

<span data-ttu-id="5c8cd-237">Mettre en forme le code pour un groupe de contacts dans lequel l’objet contient les propriétés d’un groupe de contacts et, éventuellement, les données.</span><span class="sxs-lookup"><span data-stu-id="5c8cd-237">Format code for a contact group where the object contains the properties of a contact group and, optionally, data.</span></span> <span data-ttu-id="5c8cd-238">Le format des données contenues n’est pas défini par rapport à la spécification MTP.</span><span class="sxs-lookup"><span data-stu-id="5c8cd-238">Any contained data is of an undefined format with respect to the MTP specification.</span></span>

</dd> <dt>

<span data-ttu-id="5c8cd-239"><span id="WMDM_FORMATCODE_ABSTRACTMESSAGEFOLDER"></span><span id="wmdm_formatcode_abstractmessagefolder"></span>**WMDM \_ FORMATCODE \_ ABSTRACTMESSAGEFOLDER**</span><span class="sxs-lookup"><span data-stu-id="5c8cd-239"><span id="WMDM_FORMATCODE_ABSTRACTMESSAGEFOLDER"></span><span id="wmdm_formatcode_abstractmessagefolder"></span>**WMDM\_FORMATCODE\_ABSTRACTMESSAGEFOLDER**</span></span>
</dt> <dd>

<span data-ttu-id="5c8cd-240">Mettez en forme le code d’un dossier de message où l’objet contient les propriétés d’un dossier de message et, éventuellement, les données.</span><span class="sxs-lookup"><span data-stu-id="5c8cd-240">Format code for a message folder where the object contains the properties of a message folder and, optionally, data.</span></span> <span data-ttu-id="5c8cd-241">Le format des données contenues n’est pas défini par rapport à la spécification MTP.</span><span class="sxs-lookup"><span data-stu-id="5c8cd-241">Any contained data is of an undefined format with respect to the MTP specification.</span></span>

</dd> <dt>

<span data-ttu-id="5c8cd-242"><span id="WMDM_FORMATCODE_ABSTRACTCHAPTEREDPRODUCTION"></span><span id="wmdm_formatcode_abstractchapteredproduction"></span>**WMDM \_ FORMATCODE \_ ABSTRACTCHAPTEREDPRODUCTION**</span><span class="sxs-lookup"><span data-stu-id="5c8cd-242"><span id="WMDM_FORMATCODE_ABSTRACTCHAPTEREDPRODUCTION"></span><span id="wmdm_formatcode_abstractchapteredproduction"></span>**WMDM\_FORMATCODE\_ABSTRACTCHAPTEREDPRODUCTION**</span></span>
</dt> <dd>

<span data-ttu-id="5c8cd-243">Mettez en forme le code pour une production par chapitre dans laquelle l’objet contient les propriétés d’une production par chapitre et, éventuellement, des données.</span><span class="sxs-lookup"><span data-stu-id="5c8cd-243">Format code for a chaptered production where the object contains the properties of a chaptered production and, optionally, data.</span></span> <span data-ttu-id="5c8cd-244">Le format des données contenues n’est pas défini par rapport à la spécification MTP.</span><span class="sxs-lookup"><span data-stu-id="5c8cd-244">Any contained data is of an undefined format with respect to the MTP specification.</span></span>

</dd> <dt>

<span data-ttu-id="5c8cd-245"><span id="WMDM_FORMATCODE_WPLPLAYLIST"></span><span id="wmdm_formatcode_wplplaylist"></span>**WMDM \_ FORMATCODE \_ WPLPLAYLIST**</span><span class="sxs-lookup"><span data-stu-id="5c8cd-245"><span id="WMDM_FORMATCODE_WPLPLAYLIST"></span><span id="wmdm_formatcode_wplplaylist"></span>**WMDM\_FORMATCODE\_WPLPLAYLIST**</span></span>
</dt> <dd>

<span data-ttu-id="5c8cd-246">Mettre en forme le code pour une sélection mise en forme avec la mise en forme de la sélection Windows Media.</span><span class="sxs-lookup"><span data-stu-id="5c8cd-246">Format code for a playlist formatted with Windows Media playlist formatting.</span></span>

</dd> <dt>

<span data-ttu-id="5c8cd-247"><span id="WMDM_FORMATCODE_M3UPLAYLIST"></span><span id="wmdm_formatcode_m3uplaylist"></span>**WMDM \_ FORMATCODE \_ M3UPLAYLIST**</span><span class="sxs-lookup"><span data-stu-id="5c8cd-247"><span id="WMDM_FORMATCODE_M3UPLAYLIST"></span><span id="wmdm_formatcode_m3uplaylist"></span>**WMDM\_FORMATCODE\_M3UPLAYLIST**</span></span>
</dt> <dd>

<span data-ttu-id="5c8cd-248">Mettre en forme le code pour une sélection avec une mise en forme M3U.</span><span class="sxs-lookup"><span data-stu-id="5c8cd-248">Format code for a playlist with M3U formatting.</span></span>

</dd> <dt>

<span data-ttu-id="5c8cd-249"><span id="WMDM_FORMATCODE_MPLPLAYLIST"></span><span id="wmdm_formatcode_mplplaylist"></span>**WMDM \_ FORMATCODE \_ MPLPLAYLIST**</span><span class="sxs-lookup"><span data-stu-id="5c8cd-249"><span id="WMDM_FORMATCODE_MPLPLAYLIST"></span><span id="wmdm_formatcode_mplplaylist"></span>**WMDM\_FORMATCODE\_MPLPLAYLIST**</span></span>
</dt> <dd>

<span data-ttu-id="5c8cd-250">Mettre en forme le code d’une sélection avec une mise en forme MPL.</span><span class="sxs-lookup"><span data-stu-id="5c8cd-250">Format code for a playlist with MPL formatting.</span></span>

</dd> <dt>

<span data-ttu-id="5c8cd-251"><span id="WMDM_FORMATCODE_ASXPLAYLIST"></span><span id="wmdm_formatcode_asxplaylist"></span>**WMDM \_ FORMATCODE \_ ASXPLAYLIST**</span><span class="sxs-lookup"><span data-stu-id="5c8cd-251"><span id="WMDM_FORMATCODE_ASXPLAYLIST"></span><span id="wmdm_formatcode_asxplaylist"></span>**WMDM\_FORMATCODE\_ASXPLAYLIST**</span></span>
</dt> <dd>

<span data-ttu-id="5c8cd-252">Formater le code pour une sélection avec une mise en forme ASX.</span><span class="sxs-lookup"><span data-stu-id="5c8cd-252">Format code for a playlist with ASX formatting.</span></span>

</dd> <dt>

<span data-ttu-id="5c8cd-253"><span id="WMDM_FORMATCODE_PLSPLAYLIST"></span><span id="wmdm_formatcode_plsplaylist"></span>**WMDM \_ FORMATCODE \_ PLSPLAYLIST**</span><span class="sxs-lookup"><span data-stu-id="5c8cd-253"><span id="WMDM_FORMATCODE_PLSPLAYLIST"></span><span id="wmdm_formatcode_plsplaylist"></span>**WMDM\_FORMATCODE\_PLSPLAYLIST**</span></span>
</dt> <dd>

<span data-ttu-id="5c8cd-254">Mettre en forme le code d’une sélection avec une mise en forme patientez.</span><span class="sxs-lookup"><span data-stu-id="5c8cd-254">Format code for a playlist with PLS formatting.</span></span>

</dd> <dt>

<span data-ttu-id="5c8cd-255"><span id="WMDM_FORMATCODE_UNDEFINEDDOCUMENT"></span><span id="wmdm_formatcode_undefineddocument"></span>**WMDM \_ FORMATCODE \_ UNDEFINEDDOCUMENT**</span><span class="sxs-lookup"><span data-stu-id="5c8cd-255"><span id="WMDM_FORMATCODE_UNDEFINEDDOCUMENT"></span><span id="wmdm_formatcode_undefineddocument"></span>**WMDM\_FORMATCODE\_UNDEFINEDDOCUMENT**</span></span>
</dt> <dd>

<span data-ttu-id="5c8cd-256">Mettre en forme le code d’un document de type non défini.</span><span class="sxs-lookup"><span data-stu-id="5c8cd-256">Format code for a document of undefined type.</span></span>

</dd> <dt>

<span data-ttu-id="5c8cd-257"><span id="WMDM_FORMATCODE_ABSTRACTDOCUMENT"></span><span id="wmdm_formatcode_abstractdocument"></span>**WMDM \_ FORMATCODE \_ ABSTRACTDOCUMENT**</span><span class="sxs-lookup"><span data-stu-id="5c8cd-257"><span id="WMDM_FORMATCODE_ABSTRACTDOCUMENT"></span><span id="wmdm_formatcode_abstractdocument"></span>**WMDM\_FORMATCODE\_ABSTRACTDOCUMENT**</span></span>
</dt> <dd>

<span data-ttu-id="5c8cd-258">Mettre en forme le code d’un document dans lequel l’objet contient les propriétés d’un document et, éventuellement, les données.</span><span class="sxs-lookup"><span data-stu-id="5c8cd-258">Format code for a document where the object contains the properties of a document and, optionally, data.</span></span> <span data-ttu-id="5c8cd-259">Le format des données contenues n’est pas défini par rapport à la spécification MTP.</span><span class="sxs-lookup"><span data-stu-id="5c8cd-259">Any contained data is of an undefined format with respect to the MTP specification.</span></span>

</dd> <dt>

<span data-ttu-id="5c8cd-260"><span id="WMDM_FORMATCODE_XMLDOCUMENT"></span><span id="wmdm_formatcode_xmldocument"></span>**WMDM \_ FORMATCODE \_ XMLDOCUMENT**</span><span class="sxs-lookup"><span data-stu-id="5c8cd-260"><span id="WMDM_FORMATCODE_XMLDOCUMENT"></span><span id="wmdm_formatcode_xmldocument"></span>**WMDM\_FORMATCODE\_XMLDOCUMENT**</span></span>
</dt> <dd>

<span data-ttu-id="5c8cd-261">Mettre en forme le code d’un document XML.</span><span class="sxs-lookup"><span data-stu-id="5c8cd-261">Format code for an XML document.</span></span>

</dd> <dt>

<span data-ttu-id="5c8cd-262"><span id="WMDM_FORMATCODE_MICROSOFTWORDDOCUMENT"></span><span id="wmdm_formatcode_microsoftworddocument"></span>**WMDM \_ FORMATCODE \_ MICROSOFTWORDDOCUMENT**</span><span class="sxs-lookup"><span data-stu-id="5c8cd-262"><span id="WMDM_FORMATCODE_MICROSOFTWORDDOCUMENT"></span><span id="wmdm_formatcode_microsoftworddocument"></span>**WMDM\_FORMATCODE\_MICROSOFTWORDDOCUMENT**</span></span>
</dt> <dd>

<span data-ttu-id="5c8cd-263">Mettre en forme le code d’un document Microsoft Word.</span><span class="sxs-lookup"><span data-stu-id="5c8cd-263">Format code for a Microsoft Word document.</span></span>

</dd> <dt>

<span data-ttu-id="5c8cd-264"><span id="WMDM_FORMATCODE_MHTCOMPILEDHTMLDOCUMENT"></span><span id="wmdm_formatcode_mhtcompiledhtmldocument"></span>**WMDM \_ FORMATCODE \_ MHTCOMPILEDHTMLDOCUMENT**</span><span class="sxs-lookup"><span data-stu-id="5c8cd-264"><span id="WMDM_FORMATCODE_MHTCOMPILEDHTMLDOCUMENT"></span><span id="wmdm_formatcode_mhtcompiledhtmldocument"></span>**WMDM\_FORMATCODE\_MHTCOMPILEDHTMLDOCUMENT**</span></span>
</dt> <dd>

<span data-ttu-id="5c8cd-265">Mettre en forme le code d’un document HTML compilé.</span><span class="sxs-lookup"><span data-stu-id="5c8cd-265">Format code for a compiled HTML document.</span></span>

</dd> <dt>

<span data-ttu-id="5c8cd-266"><span id="WMDM_FORMATCODE_MICROSOFTEXCELSPREADSHEET"></span><span id="wmdm_formatcode_microsoftexcelspreadsheet"></span>**WMDM \_ FORMATCODE \_ MICROSOFTEXCELSPREADSHEET**</span><span class="sxs-lookup"><span data-stu-id="5c8cd-266"><span id="WMDM_FORMATCODE_MICROSOFTEXCELSPREADSHEET"></span><span id="wmdm_formatcode_microsoftexcelspreadsheet"></span>**WMDM\_FORMATCODE\_MICROSOFTEXCELSPREADSHEET**</span></span>
</dt> <dd>

<span data-ttu-id="5c8cd-267">Mettre en forme le code pour une feuille de calcul Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="5c8cd-267">Format code for a Microsoft Excel spreadsheet.</span></span>

</dd> <dt>

<span data-ttu-id="5c8cd-268"><span id="WMDM_FORMATCODE_MICROSOFTPOWERPOINTDOCUMENT"></span><span id="wmdm_formatcode_microsoftpowerpointdocument"></span>**WMDM \_ FORMATCODE \_ MICROSOFTPOWERPOINTDOCUMENT**</span><span class="sxs-lookup"><span data-stu-id="5c8cd-268"><span id="WMDM_FORMATCODE_MICROSOFTPOWERPOINTDOCUMENT"></span><span id="wmdm_formatcode_microsoftpowerpointdocument"></span>**WMDM\_FORMATCODE\_MICROSOFTPOWERPOINTDOCUMENT**</span></span>
</dt> <dd>

<span data-ttu-id="5c8cd-269">Mettre en forme le code d’un document Microsoft PowerPoint.</span><span class="sxs-lookup"><span data-stu-id="5c8cd-269">Format code for a Microsoft PowerPoint document.</span></span>

</dd> <dt>

<span data-ttu-id="5c8cd-270"><span id="WMDM_FORMATCODE_UNDEFINEDMESSAGE"></span><span id="wmdm_formatcode_undefinedmessage"></span>**WMDM \_ FORMATCODE \_ UNDEFINEDMESSAGE**</span><span class="sxs-lookup"><span data-stu-id="5c8cd-270"><span id="WMDM_FORMATCODE_UNDEFINEDMESSAGE"></span><span id="wmdm_formatcode_undefinedmessage"></span>**WMDM\_FORMATCODE\_UNDEFINEDMESSAGE**</span></span>
</dt> <dd>

<span data-ttu-id="5c8cd-271">Mettre en forme le code pour un message de type non défini.</span><span class="sxs-lookup"><span data-stu-id="5c8cd-271">Format code for a message of undefined type.</span></span>

</dd> <dt>

<span data-ttu-id="5c8cd-272"><span id="WMDM_FORMATCODE_ABSTRACTMESSAGE"></span><span id="wmdm_formatcode_abstractmessage"></span>**WMDM \_ FORMATCODE \_ ABSTRACTMESSAGE**</span><span class="sxs-lookup"><span data-stu-id="5c8cd-272"><span id="WMDM_FORMATCODE_ABSTRACTMESSAGE"></span><span id="wmdm_formatcode_abstractmessage"></span>**WMDM\_FORMATCODE\_ABSTRACTMESSAGE**</span></span>
</dt> <dd>

<span data-ttu-id="5c8cd-273">Mettre en forme le code pour un message dans lequel l’objet contient les propriétés d’un message et, éventuellement, les données.</span><span class="sxs-lookup"><span data-stu-id="5c8cd-273">Format code for a message where the object contains the properties of a message and, optionally, data.</span></span> <span data-ttu-id="5c8cd-274">Le format des données contenues n’est pas défini par rapport à la spécification MTP.</span><span class="sxs-lookup"><span data-stu-id="5c8cd-274">Any contained data is of an undefined format with respect to the MTP specification.</span></span>

</dd> <dt>

<span data-ttu-id="5c8cd-275"><span id="WMDM_FORMATCODE_UNDEFINEDCONTACT"></span><span id="wmdm_formatcode_undefinedcontact"></span>**WMDM \_ FORMATCODE \_ UNDEFINEDCONTACT**</span><span class="sxs-lookup"><span data-stu-id="5c8cd-275"><span id="WMDM_FORMATCODE_UNDEFINEDCONTACT"></span><span id="wmdm_formatcode_undefinedcontact"></span>**WMDM\_FORMATCODE\_UNDEFINEDCONTACT**</span></span>
</dt> <dd>

<span data-ttu-id="5c8cd-276">Mettre en forme le code d’un contact de type non défini.</span><span class="sxs-lookup"><span data-stu-id="5c8cd-276">Format code for a contact of undefined type.</span></span>

</dd> <dt>

<span data-ttu-id="5c8cd-277"><span id="WMDM_FORMATCODE_ABSTRACTCONTACT"></span><span id="wmdm_formatcode_abstractcontact"></span>**WMDM \_ FORMATCODE \_ ABSTRACTCONTACT**</span><span class="sxs-lookup"><span data-stu-id="5c8cd-277"><span id="WMDM_FORMATCODE_ABSTRACTCONTACT"></span><span id="wmdm_formatcode_abstractcontact"></span>**WMDM\_FORMATCODE\_ABSTRACTCONTACT**</span></span>
</dt> <dd>

<span data-ttu-id="5c8cd-278">Mettre en forme le code d’un contact dans lequel l’objet contient les propriétés d’un contact et, éventuellement, les données.</span><span class="sxs-lookup"><span data-stu-id="5c8cd-278">Format code for a contact where the object contains the properties of a contact and, optionally, data.</span></span> <span data-ttu-id="5c8cd-279">Le format des données contenues n’est pas défini par rapport à la spécification MTP.</span><span class="sxs-lookup"><span data-stu-id="5c8cd-279">Any contained data is of an undefined format with respect to the MTP specification.</span></span>

</dd> <dt>

<span data-ttu-id="5c8cd-280"><span id="WMDM_FORMATCODE_VCARD2"></span><span id="wmdm_formatcode_vcard2"></span>**WMDM \_ FORMATCODE \_ VCARD2**</span><span class="sxs-lookup"><span data-stu-id="5c8cd-280"><span id="WMDM_FORMATCODE_VCARD2"></span><span id="wmdm_formatcode_vcard2"></span>**WMDM\_FORMATCODE\_VCARD2**</span></span>
</dt> <dd>

<span data-ttu-id="5c8cd-281">Formater le code pour une carte électronique avec la mise en forme vCard version 2.</span><span class="sxs-lookup"><span data-stu-id="5c8cd-281">Format code for an electronic card with vcard version 2 formatting.</span></span>

</dd> <dt>

<span data-ttu-id="5c8cd-282"><span id="WMDM_FORMATCODE_VCARD3"></span><span id="wmdm_formatcode_vcard3"></span>**WMDM \_ FORMATCODE \_ VCARD3**</span><span class="sxs-lookup"><span data-stu-id="5c8cd-282"><span id="WMDM_FORMATCODE_VCARD3"></span><span id="wmdm_formatcode_vcard3"></span>**WMDM\_FORMATCODE\_VCARD3**</span></span>
</dt> <dd>

<span data-ttu-id="5c8cd-283">Formater le code pour une carte électronique avec la mise en forme vCard version 3.</span><span class="sxs-lookup"><span data-stu-id="5c8cd-283">Format code for an electronic card with vcard version 3 formatting.</span></span>

</dd> <dt>

<span data-ttu-id="5c8cd-284"><span id="WMDM_FORMATCODE_UNDEFINEDCALENDARITEM"></span><span id="wmdm_formatcode_undefinedcalendaritem"></span>**WMDM \_ FORMATCODE \_ UNDEFINEDCALENDARITEM**</span><span class="sxs-lookup"><span data-stu-id="5c8cd-284"><span id="WMDM_FORMATCODE_UNDEFINEDCALENDARITEM"></span><span id="wmdm_formatcode_undefinedcalendaritem"></span>**WMDM\_FORMATCODE\_UNDEFINEDCALENDARITEM**</span></span>
</dt> <dd>

<span data-ttu-id="5c8cd-285">Mettre en forme le code pour un élément de calendrier électronique d’un type non défini.</span><span class="sxs-lookup"><span data-stu-id="5c8cd-285">Format code for an electronic calendar item of undefined type.</span></span>

</dd> <dt>

<span data-ttu-id="5c8cd-286"><span id="WMDM_FORMATCODE_ABSTRACTCALENDARITEM"></span><span id="wmdm_formatcode_abstractcalendaritem"></span>**WMDM \_ FORMATCODE \_ ABSTRACTCALENDARITEM**</span><span class="sxs-lookup"><span data-stu-id="5c8cd-286"><span id="WMDM_FORMATCODE_ABSTRACTCALENDARITEM"></span><span id="wmdm_formatcode_abstractcalendaritem"></span>**WMDM\_FORMATCODE\_ABSTRACTCALENDARITEM**</span></span>
</dt> <dd>

<span data-ttu-id="5c8cd-287">Mettez en forme le code d’un élément de calendrier dans lequel l’objet contient les propriétés d’un élément de calendrier et, éventuellement, les données.</span><span class="sxs-lookup"><span data-stu-id="5c8cd-287">Format code for a calendar item where the object contains the properties of a calendar item and, optionally, data.</span></span> <span data-ttu-id="5c8cd-288">Le format des données contenues n’est pas défini par rapport à la spécification MTP.</span><span class="sxs-lookup"><span data-stu-id="5c8cd-288">Any contained data is of an undefined format with respect to the MTP specification.</span></span>

</dd> <dt>

<span data-ttu-id="5c8cd-289"><span id="WMDM_FORMATCODE_VCALENDAR1"></span><span id="wmdm_formatcode_vcalendar1"></span>**WMDM \_ FORMATCODE \_ VCALENDAR1**</span><span class="sxs-lookup"><span data-stu-id="5c8cd-289"><span id="WMDM_FORMATCODE_VCALENDAR1"></span><span id="wmdm_formatcode_vcalendar1"></span>**WMDM\_FORMATCODE\_VCALENDAR1**</span></span>
</dt> <dd>

<span data-ttu-id="5c8cd-290">Mettez en forme le code d’un élément de calendrier électronique avec la mise en forme vCalendar version 1.</span><span class="sxs-lookup"><span data-stu-id="5c8cd-290">Format code for an electronic calendar item with vcalendar version 1 formatting.</span></span>

</dd> <dt>

<span data-ttu-id="5c8cd-291"><span id="WMDM_FORMATCODE_VCALENDAR2"></span><span id="wmdm_formatcode_vcalendar2"></span>**WMDM \_ FORMATCODE \_ VCALENDAR2**</span><span class="sxs-lookup"><span data-stu-id="5c8cd-291"><span id="WMDM_FORMATCODE_VCALENDAR2"></span><span id="wmdm_formatcode_vcalendar2"></span>**WMDM\_FORMATCODE\_VCALENDAR2**</span></span>
</dt> <dd>

<span data-ttu-id="5c8cd-292">Mettre en forme le code d’un élément de calendrier électronique avec la mise en forme vCalendar version 2.</span><span class="sxs-lookup"><span data-stu-id="5c8cd-292">Format code for an electronic calendar item with vcalendar version 2 formatting.</span></span>

</dd> <dt>

<span data-ttu-id="5c8cd-293"><span id="WMDM_FORMATCODE_UNDEFINEDWINDOWSEXECUTABLE"></span><span id="wmdm_formatcode_undefinedwindowsexecutable"></span>**WMDM \_ FORMATCODE \_ UNDEFINEDWINDOWSEXECUTABLE**</span><span class="sxs-lookup"><span data-stu-id="5c8cd-293"><span id="WMDM_FORMATCODE_UNDEFINEDWINDOWSEXECUTABLE"></span><span id="wmdm_formatcode_undefinedwindowsexecutable"></span>**WMDM\_FORMATCODE\_UNDEFINEDWINDOWSEXECUTABLE**</span></span>
</dt> <dd>

<span data-ttu-id="5c8cd-294">Mettre en forme le code pour un fichier exécutable Windows de type non défini.</span><span class="sxs-lookup"><span data-stu-id="5c8cd-294">Format code for a Windows-based executable of undefined type.</span></span>

</dd> <dt>

<span data-ttu-id="5c8cd-295"><span id="WMDM_FORMATCODE_MEDIA_CAST"></span><span id="wmdm_formatcode_media_cast"></span>**WMDM \_ FORMATCODE \_ Media \_ cast**</span><span class="sxs-lookup"><span data-stu-id="5c8cd-295"><span id="WMDM_FORMATCODE_MEDIA_CAST"></span><span id="wmdm_formatcode_media_cast"></span>**WMDM\_FORMATCODE\_MEDIA\_CAST**</span></span>
</dt> <dd>

<span data-ttu-id="5c8cd-296">Mettre en forme le code d’un objet de transtypage multimédia.</span><span class="sxs-lookup"><span data-stu-id="5c8cd-296">Format code for a media cast object.</span></span>

</dd> <dt>

<span data-ttu-id="5c8cd-297"><span id="WMDM_FORMATCODE_SECTION"></span><span id="wmdm_formatcode_section"></span>**\_section WMDM FORMATCODE \_**</span><span class="sxs-lookup"><span data-stu-id="5c8cd-297"><span id="WMDM_FORMATCODE_SECTION"></span><span id="wmdm_formatcode_section"></span>**WMDM\_FORMATCODE\_SECTION**</span></span>
</dt> <dd>

<span data-ttu-id="5c8cd-298">Mettre en forme le code d’une section de données contenue dans un autre objet.</span><span class="sxs-lookup"><span data-stu-id="5c8cd-298">Format code for a section of data that is contained in another object.</span></span>

</dd> <dt>

<span data-ttu-id="5c8cd-299"><span id="________________________________WMDM_FORMATCODE_3G2A_"></span><span id="________________________________wmdm_formatcode_3g2a_"></span>**WMDM \_ FORMATCODE \_ 3G2A**</span><span class="sxs-lookup"><span data-stu-id="5c8cd-299"><span id="________________________________WMDM_FORMATCODE_3G2A_"></span><span id="________________________________wmdm_formatcode_3g2a_"></span> **WMDM\_FORMATCODE\_3G2A**</span></span> 
</dt> <dd>

<span data-ttu-id="5c8cd-300">Mettre en forme le code pour un format de conteneur multimédia 3G2A (3GPP2A).</span><span class="sxs-lookup"><span data-stu-id="5c8cd-300">Format code for a 3G2A (3GPP2A) multimedia container format.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5c8cd-301">Notes</span><span class="sxs-lookup"><span data-stu-id="5c8cd-301">Remarks</span></span>

<span data-ttu-id="5c8cd-302">Pour découvrir les formats pris en charge par un appareil, une application peut utiliser [**IWMDMDevice3 :: GetProperty**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getproperty) pour interroger la propriété de l’appareil **g \_ wszWMDMFormatsSupported** .</span><span class="sxs-lookup"><span data-stu-id="5c8cd-302">To discover the formats supported by a device, an application can use [**IWMDMDevice3::GetProperty**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getproperty) to query the **g\_wszWMDMFormatsSupported** device property.</span></span>

<span data-ttu-id="5c8cd-303">Pour découvrir les fonctionnalités de l’appareil pour un format particulier, une application peut appeler [**IWMDMDevice3 :: GetFormatCapability**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getformatcapability).</span><span class="sxs-lookup"><span data-stu-id="5c8cd-303">To discover device capabilities for a particular format, an application can call [**IWMDMDevice3::GetFormatCapability**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getformatcapability).</span></span>

<span data-ttu-id="5c8cd-304">Une application peut définir le code de format lors de la création d’un stockage sur l’appareil en incluant la propriété **g \_ wszWMDMFormatCode** dans les métadonnées passées dans le paramètre *pMetaData* d’un appel à [**IWMDMStorageControl3 :: Insert3**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol3-insert3).</span><span class="sxs-lookup"><span data-stu-id="5c8cd-304">An application can set the format code while creating a storage on device by including the **g\_wszWMDMFormatCode** property in metadata passed in the *pMetaData* parameter of a call to [**IWMDMStorageControl3::Insert3**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol3-insert3).</span></span>

<span data-ttu-id="5c8cd-305">Une application peut interroger le code de format d’un stockage en appelant [**IWMDMStorage3 :: GetMetadata**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage3-getmetadata) ou [**IWMDMStorage4 :: GetSpecifiedMetadata**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage4-getspecifiedmetadata) et en extrayant la propriété **g \_ wszWMDMFormatCode** .</span><span class="sxs-lookup"><span data-stu-id="5c8cd-305">An application can query the format code of a storage by calling [**IWMDMStorage3::GetMetadata**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage3-getmetadata) or [**IWMDMStorage4::GetSpecifiedMetadata**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage4-getspecifiedmetadata) and retrieving the **g\_wszWMDMFormatCode** property.</span></span>

<span data-ttu-id="5c8cd-306">Si l’appareil prend en charge la définition du code de format après la création du stockage, une application peut utiliser [**IWMDMStorage3 :: SetMetadata**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage3-setmetadata) pour définir la propriété **g \_ wszWMDMFormatCode** .</span><span class="sxs-lookup"><span data-stu-id="5c8cd-306">If the device supports setting the format code after the creation of storage, an application can use [**IWMDMStorage3::SetMetadata**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage3-setmetadata) to set the **g\_wszWMDMFormatCode** property.</span></span> <span data-ttu-id="5c8cd-307">Certains appareils peuvent ne pas autoriser la modification du code de format une fois le stockage créé sur l’appareil.</span><span class="sxs-lookup"><span data-stu-id="5c8cd-307">Some devices may not allow changing the format code after the storage is created on the device.</span></span> <span data-ttu-id="5c8cd-308">Par conséquent, la définition de cette propriété avec les métadonnées passées dans [**IWMDMStorageControl3 :: Insert3**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol3-insert3) est fortement recommandée.</span><span class="sxs-lookup"><span data-stu-id="5c8cd-308">Therefore, setting this property along with the metadata passed in [**IWMDMStorageControl3::Insert3**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol3-insert3) is strongly recommended.</span></span>

## <a name="requirements"></a><span data-ttu-id="5c8cd-309">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5c8cd-309">Requirements</span></span>



| <span data-ttu-id="5c8cd-310">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5c8cd-310">Requirement</span></span> | <span data-ttu-id="5c8cd-311">Valeur</span><span class="sxs-lookup"><span data-stu-id="5c8cd-311">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="5c8cd-312">En-tête</span><span class="sxs-lookup"><span data-stu-id="5c8cd-312">Header</span></span><br/> | <dl> <span data-ttu-id="5c8cd-313"><dt>WMDM. idl</dt></span><span class="sxs-lookup"><span data-stu-id="5c8cd-313"><dt>Wmdm.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5c8cd-314">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5c8cd-314">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5c8cd-315">**Types énumération**</span><span class="sxs-lookup"><span data-stu-id="5c8cd-315">**Enumeration Types**</span></span>](enumeration-types.md)
</dt> <dt>

[<span data-ttu-id="5c8cd-316">**IWMDMDevice3::GetFormatCapability**</span><span class="sxs-lookup"><span data-stu-id="5c8cd-316">**IWMDMDevice3::GetFormatCapability**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getformatcapability)
</dt> <dt>

[<span data-ttu-id="5c8cd-317">**IWMDMDevice3 :: GetProperty**</span><span class="sxs-lookup"><span data-stu-id="5c8cd-317">**IWMDMDevice3::GetProperty**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getproperty)
</dt> <dt>

[<span data-ttu-id="5c8cd-318">**IWMDMStorage3 :: GetMetadata**</span><span class="sxs-lookup"><span data-stu-id="5c8cd-318">**IWMDMStorage3::GetMetadata**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage3-getmetadata)
</dt> <dt>

[<span data-ttu-id="5c8cd-319">**IWMDMStorage3::SetMetadata**</span><span class="sxs-lookup"><span data-stu-id="5c8cd-319">**IWMDMStorage3::SetMetadata**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage3-setmetadata)
</dt> <dt>

[<span data-ttu-id="5c8cd-320">**IWMDMStorage4::GetSpecifiedMetadata**</span><span class="sxs-lookup"><span data-stu-id="5c8cd-320">**IWMDMStorage4::GetSpecifiedMetadata**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage4-getspecifiedmetadata)
</dt> <dt>

[<span data-ttu-id="5c8cd-321">**IWMDMStorageControl3::Insert3**</span><span class="sxs-lookup"><span data-stu-id="5c8cd-321">**IWMDMStorageControl3::Insert3**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol3-insert3)
</dt> <dt>

[<span data-ttu-id="5c8cd-322">**Constantes de métadonnées**</span><span class="sxs-lookup"><span data-stu-id="5c8cd-322">**Metadata Constants**</span></span>](metadata-constants.md)
</dt> </dl>

 

 





