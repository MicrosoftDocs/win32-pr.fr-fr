---
title: Énumération DRM_INDIVIDUALIZATION_STATUS (Drmexternals. h)
description: Le \_ \_ type d’énumération de l’état de l’individualisation DRM définit les États valides pour l’individualisation DRM. | Énumération DRM_INDIVIDUALIZATION_STATUS (Drmexternals. h)
ms.assetid: 76748fb3-340e-47e2-969d-5e857bb4e4d8
keywords:
- Format Windows Media d’énumération DRM_INDIVIDUALIZATION_STATUS
- Format Windows Media d’énumération
topic_type:
- apiref
api_name:
- DRM_INDIVIDUALIZATION_STATUS
api_location:
- Drmexternals.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 081a8714d29cb48236bdb9191c15e92db96b18a9f8c1d9c2388c5baee7783296
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119705649"
---
# <a name="drm_individualization_status-enumeration-drmexternalsh"></a>Énumération DRM_INDIVIDUALIZATION_STATUS (Drmexternals. h)

Le type d’énumération de l’état de l' **\_ individualisation \_ DRM** définit les États valides pour l' [*individualisation*](wmformat-glossary.md)DRM. Quand une application lance l’individualisation à l’aide d’un appel à [**IWMDRMReader :: Individual**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-individualize), la progression de la demande d’individualisation est transporte à l’application via des appels à la méthode [**IWMStatusCallback :: OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) . Les messages d’état de l’individualisation utilisent tous le \_ membre de l’élément Individual de WMT du type d’énumération d' [**\_ État WMT**](/previous-versions/windows/desktop/api/Wmsdkidl/ne-wmsdkidl-wmt_status) comme paramètre d' *État* . L’état de l’individualisation est passé à **OnStatus** dans le paramètre *pValue* .

## <a name="syntax"></a>Syntaxe


```C++
typedef enum DRM_INDIVIDUALIZATION_STATUS { 
  INDI_UNDEFINED  = 0x0000,
  INDI_BEGIN      = 0x0001,
  INDI_SUCCEED    = 0x0002,
  INDI_FAIL       = 0x0004,
  INDI_CANCEL     = 0x0008,
  INDI_DOWNLOAD   = 0x0010,
  INDI_INSTALL    = 0x0020
} ;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="INDI_UNDEFINED"></span><span id="indi_undefined"></span>**INDI \_ non défini**
</dt> <dd>

Cette valeur est réservée à une utilisation ultérieure.

</dd> <dt>

<span id="INDI_BEGIN"></span><span id="indi_begin"></span>**INDI \_ Begin**
</dt> <dd>

Indique le début du processus d’individualisation.

</dd> <dt>

<span id="INDI_SUCCEED"></span><span id="indi_succeed"></span>**INDI \_ réussie**
</dt> <dd>

Indique que le processus d’individualisation est terminé.

</dd> <dt>

<span id="INDI_FAIL"></span><span id="indi_fail"></span>**échec de INDI \_**
</dt> <dd>

Indique que le processus d’individualisation a échoué.

</dd> <dt>

<span id="INDI_CANCEL"></span><span id="indi_cancel"></span>**INDI \_ Annuler**
</dt> <dd>

Indique que le processus d’individualisation a été annulé à la suite d’un appel à [**IWMDRMReader :: CancelIndividualization**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-cancelindividualization).

</dd> <dt>

<span id="INDI_DOWNLOAD"></span><span id="indi_download"></span>**Téléchargement de INDI \_**
</dt> <dd>

Indique que la mise à niveau de sécurité est en cours de téléchargement.

</dd> <dt>

<span id="INDI_INSTALL"></span><span id="indi_install"></span>**installation de INDI \_**
</dt> <dd>

Indique que la mise à niveau de sécurité est en cours d’installation.

</dd> </dl>

## <a name="remarks"></a>Remarques

Cette énumération est utilisée par la structure d' [**\_ \_ État**](wm-individualize-status.md) de l’énumération WM.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                                |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                      |
| Version<br/>                  | Windows Media Format 7 SDK ou les versions ultérieures du kit de développement logiciel (SDK)<br/>                       |
| En-tête<br/>                   | <dl> <dt>Drmexternals. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_État http \_ DRM**](drm-http-status.md)
</dt> <dt>

[**Types énumération**](enumeration-types.md)
</dt> </dl>

 

 





