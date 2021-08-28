---
description: Définit les codes d’erreur de clé de média pour le moteur multimédia.
ms.assetid: F6E13260-74A2-40D0-A704-4E1CDB16B8D8
title: Énumération MF_MEDIA_ENGINE_KEYERR
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MF_MEDIA_ENGINE_KEYERR
api_type:
- HeaderDef
api_location:
- mfmediaengine.h
ms.openlocfilehash: 5a3573f721f31ffbe3858c7d6fb3c713468bc347f04a1b5d85c5839a1e18511b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120113929"
---
# <a name="mf_media_engine_keyerr-enumeration"></a>\_ \_ Énumération KEYERR du moteur multimédia MF \_

Définit les codes d’erreur de clé de média pour le moteur multimédia.

## <a name="syntax"></a>Syntaxe


```C++
typedef enum _MF_MEDIA_ENGINE_KEYERR { 
  MF_MEDIAENGINE_KEYERR_UNKNOWN          = 1,
  MF_MEDIAENGINE_KEYERR_CLIENT           = 2,
  MF_MEDIAENGINE_KEYERR_SERVICE          = 3,
  MF_MEDIAENGINE_KEYERR_OUTPUT           = 4,
  MF_MEDIAENGINE_KEYERR_HARDWARECHANGE   = 5,
  MF_MEDIAENGINE_KEYERR_DOMAIN           = 6
} MF_MEDIA_ENGINE_KEYERR;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="MF_MEDIAENGINE_KEYERR_UNKNOWN"></span><span id="mf_mediaengine_keyerr_unknown"></span>**MF \_ MEDIAENGINE \_ KEYERR \_ inconnu**
</dt> <dd>

Une erreur inconnue s’est produite.

</dd> <dt>

<span id="MF_MEDIAENGINE_KEYERR_CLIENT"></span><span id="mf_mediaengine_keyerr_client"></span>**\_ \_ client KEYERR MEDIAENGINE \_ MF**
</dt> <dd>

Une erreur s’est produite avec le client.

</dd> <dt>

<span id="MF_MEDIAENGINE_KEYERR_SERVICE"></span><span id="mf_mediaengine_keyerr_service"></span>**\_ \_ service KEYERR MEDIAENGINE \_ MF**
</dt> <dd>

Une erreur s’est produite avec le service.

</dd> <dt>

<span id="MF_MEDIAENGINE_KEYERR_OUTPUT"></span><span id="mf_mediaengine_keyerr_output"></span>**\_sortie MEDIAENGINE \_ KEYERR \_ MF**
</dt> <dd>

Une erreur avec la sortie s’est produite.

</dd> <dt>

<span id="MF_MEDIAENGINE_KEYERR_HARDWARECHANGE_"></span><span id="mf_mediaengine_keyerr_hardwarechange_"></span>**MF \_ MEDIAENGINE \_ KEYERR \_ HARDWARECHANGE** 
</dt> <dd>

Une erreur s’est produite en rapport avec une modification matérielle.

</dd> <dt>

<span id="MF_MEDIAENGINE_KEYERR_DOMAIN"></span><span id="mf_mediaengine_keyerr_domain"></span>**\_domaine MEDIAENGINE \_ KEYERR \_ MF**
</dt> <dd>

Une erreur s’est produite avec le domaine.

</dd> </dl>

## <a name="remarks"></a>Remarques

**MF \_ Le \_ \_ KEYERR du moteur multimédia** est utilisé avec le paramètre de *code* de [**IMFMediaKeySessionNotify :: keyerror**](/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediakeysessionnotify-keyerror) et la valeur de *code* retournée par [**IMFMediaKeySession :: GetError**](imfmediakeysession-geterror.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8.1 les \[ applications de bureau uniquement\]<br/>                                                 |
| Serveur minimal pris en charge<br/> | Windows Server 2012 \[Applications de bureau R2 uniquement\]<br/>                                      |
| MIDL<br/>                      | <dl> <dt>Mfmediaengine. idl</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Énumérations de Media Foundation](media-foundation-enumerations.md)
</dt> </dl>

 

 




