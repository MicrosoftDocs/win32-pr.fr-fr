---
title: Énumération WMT_RIGHTS (wmdrmsdk. h)
description: Définit les droits qui peuvent être spécifiés dans une licence DRM.
ms.assetid: 9c034ca0-83e9-4a4c-8e98-96e2a95fd97c
keywords:
- Format Windows Media d’énumération WMT_RIGHTS
- Format Windows Media d’énumération
topic_type:
- apiref
api_name:
- WMT_RIGHTS
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 644cff9c94876fab11bc9fbe181ac0375d9444fb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106536256"
---
# <a name="wmt_rights-enumeration"></a>\_Énumération des droits WMT

Le type d’énumération des **\_ droits WMT** définit les droits qui peuvent être spécifiés dans une licence DRM.

## <a name="syntax"></a>Syntaxe


```C++
typedef enum WMT_RIGHTS { 
  WMT_RIGHT_PLAYBACK                 = 0x00000001,
  WMT_RIGHT_COPY_TO_NON_SDMI_DEVICE  = 0x00000002,
  WMT_RIGHT_COPY_TO_CD               = 0x00000008,
  WMT_RIGHT_COPY_TO_SDMI_DEVICE      = 0x00000010,
  WMT_RIGHT_ONE_TIME                 = 0x00000020,
  WMT_RIGHT_SAVE_STREAM_PROTECTED    = 0x00000040,
  WMT_RIGHT_COPY                     = 0x00000080,
  WMT_RIGHT_COLLABORATIVE_PLAY       = 0x00000100,
  WMT_RIGHT_SDMI_TRIGGER             = 0x00010000,
  WMT_RIGHT_SDMI_NOMORECOPIES        = 0x00020000
} ;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="WMT_RIGHT_PLAYBACK"></span><span id="wmt_right_playback"></span>**lecture d’un \_ droit WMT \_**
</dt> <dd>

Spécifie le droit de lire le contenu sans restriction.

</dd> <dt>

<span id="WMT_RIGHT_COPY_TO_NON_SDMI_DEVICE"></span><span id="wmt_right_copy_to_non_sdmi_device"></span>**\_copie appropriée \_ \_ de WMT vers un \_ \_ appareil non SDMI \_**
</dt> <dd>

Spécifie le droit de copier le contenu sur un appareil non conforme à l’initiative de Secure Digital Music (SDMI).

</dd> <dt>

<span id="WMT_RIGHT_COPY_TO_CD"></span><span id="wmt_right_copy_to_cd"></span>**\_copie d’un droit WMT \_ \_ sur \_ CD**
</dt> <dd>

Spécifie le droit de copier le contenu sur un CD.

</dd> <dt>

<span id="WMT_RIGHT_COPY_TO_SDMI_DEVICE"></span><span id="wmt_right_copy_to_sdmi_device"></span>**\_copie d’un droit WMT \_ vers un \_ \_ \_ appareil SDMI**
</dt> <dd>

Spécifie le droit de copier le contenu sur un appareil compatible avec SDMI.

</dd> <dt>

<span id="WMT_RIGHT_ONE_TIME"></span><span id="wmt_right_one_time"></span>**WMT \_ juste \_ une \_ fois**
</dt> <dd>

Spécifie le droit de lire le contenu une seule fois.

</dd> <dt>

<span id="WMT_RIGHT_SAVE_STREAM_PROTECTED"></span><span id="wmt_right_save_stream_protected"></span>**\_flux d’enregistrement approprié de WMT \_ \_ \_ protégé**
</dt> <dd>

Spécifie le droit d’enregistrer le contenu à partir d’un serveur.

</dd> <dt>

<span id="WMT_RIGHT_COPY"></span><span id="wmt_right_copy"></span>**\_copie à droite WMT \_**
</dt> <dd>

Spécifie le droit de copier le contenu. Windows Media DRM 10 régule les appareils sur lesquels le contenu peut être copié à l’aide des niveaux de protection de sortie (OPLs).

</dd> <dt>

<span id="WMT_RIGHT_COLLABORATIVE_PLAY"></span><span id="wmt_right_collaborative_play"></span>**la \_ bonne \_ lecture collaborative de WMT \_**
</dt> <dd>

Spécifie le droit de lire le contenu dans le cadre d’un scénario en ligne dans lequel plusieurs participants peuvent transmettre des chansons de leur collection vers une playlist partagée.

</dd> <dt>

<span id="WMT_RIGHT_SDMI_TRIGGER"></span><span id="wmt_right_sdmi_trigger"></span>**\_ \_ déclencheur SDMI à droite WMT \_**
</dt> <dd>

Réservé pour un usage futur. Ne pas utiliser.

</dd> <dt>

<span id="WMT_RIGHT_SDMI_NOMORECOPIES"></span><span id="wmt_right_sdmi_nomorecopies"></span>**\_ \_ NOMORECOPIES SDMI à droite WMT \_**
</dt> <dd>

Réservé pour un usage futur. Ne pas utiliser.

</dd> </dl>

## <a name="remarks"></a>Notes

Ces valeurs sont des indicateurs binaires, donc un ou plusieurs peuvent être définis en les associant à **l’opérateur de bits or.**

Si vous utilisez Windows Media DRM 10 **, \_ le \_ droit \_ de copie WMT sur un \_ \_ \_ appareil non-SDMI**, **\_ le droit \_ d’effectuer une copie de l’appareil WMT vers le \_ \_ \_ périphérique SDMI** et **le remplacement \_ d’WMT dans le \_ \_ \_ CD** sont remplacés par le droit de **\_ \_ copie de WMT**. Les limitations sur les appareils sur lesquels le contenu peut être copié sont spécifiées à l’aide de niveaux de protection de sortie (OPLs).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|---------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>Wmdrmsdk. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Types énumération**](drm-enumeration-types.md)
</dt> </dl>

 

 





