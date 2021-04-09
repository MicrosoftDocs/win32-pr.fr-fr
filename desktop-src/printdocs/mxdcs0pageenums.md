---
description: L' \_ \_ énumération de la page S0 MXDC \_ est utilisée pour spécifier les types de ressources qui peuvent être associées à des pages dans les documents XPS et qui peuvent être traitées, ou transmises sans traitement, par Microsoft XPS Document Converter (MXDC) dans sa sortie.
ms.assetid: e111d92e-5102-4b39-b311-f9ff1d1a96f1
title: Énumération MXDC_S0_PAGE_ENUMS (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MXDC_S0_PAGE_ENUMS
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 1b4331210027f7fc23f36fb6b9d13a2c232ccbf6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864958"
---
# <a name="mxdc_s0_page_enums-enumeration"></a>Énumération des énumérations de la \_ page S0 MXDC \_ \_

L’énumération de la **\_ \_ page \_ S0 MXDC** est utilisée pour spécifier les types de ressources qui peuvent être associées à des pages dans les documents XPS et qui peuvent être traitées, ou transmises sans traitement, par Microsoft XPS Document Converter (MXDC) dans sa sortie.

## <a name="syntax"></a>Syntaxe


```C++
typedef enum tagMxdcS0PageEnums { 
  MXDC_RESOURCE_TTF,
  MXDC_RESOURCE_JPEG,
  MXDC_RESOURCE_PNG,
  MXDC_RESOURCE_TIFF,
  MXDC_RESOURCE_WDP,
  MXDC_RESOURCE_DICTIONARY,
  MXDC_RESOURCE_ICC_PROFILE,
  MXDC_RESOURCE_JPEG_THUMBNAIL,
  MXDC_RESOURCE_PNG_THUMBNAIL,
  MXDC_RESOURCE_MAX
} MXDC_S0_PAGE_ENUMS;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="MXDC_RESOURCE_TTF"></span><span id="mxdc_resource_ttf"></span>**MXDC, \_ ressource \_ ttf**
</dt> <dd>

Police TrueType ou OpenType.

</dd> <dt>

<span id="MXDC_RESOURCE_JPEG"></span><span id="mxdc_resource_jpeg"></span>**MXDC \_ ressource \_ JPEG**
</dt> <dd>

Image JPEG

</dd> <dt>

<span id="MXDC_RESOURCE_PNG"></span><span id="mxdc_resource_png"></span>**MXDC \_ ressource \_ PNG**
</dt> <dd>

Image PNG.

</dd> <dt>

<span id="MXDC_RESOURCE_TIFF"></span><span id="mxdc_resource_tiff"></span>**MXDC \_ ressource \_ TIFF**
</dt> <dd>

Image TIFF.

</dd> <dt>

<span id="MXDC_RESOURCE_WDP"></span><span id="mxdc_resource_wdp"></span>**\_ressource MXDC \_ WDP**
</dt> <dd>

Image Windows Media photo.

</dd> <dt>

<span id="MXDC_RESOURCE_DICTIONARY"></span><span id="mxdc_resource_dictionary"></span>**\_dictionnaire de ressources MXDC \_**
</dt> <dd>

Dictionnaire de ressources distant qui doit être passé à la sortie de MXDC non traité.

</dd> <dt>

<span id="MXDC_RESOURCE_ICC_PROFILE"></span><span id="mxdc_resource_icc_profile"></span>**\_ \_ profil ICC de la ressource MXDC \_**
</dt> <dd>

Profil ICC qui doit être passé à la sortie de MXDC non traité.

</dd> <dt>

<span id="MXDC_RESOURCE_JPEG_THUMBNAIL"></span><span id="mxdc_resource_jpeg_thumbnail"></span>**\_ \_ miniature JPEG de la ressource MXDC \_**
</dt> <dd>

Miniature JPEG qui doit être transmise à la sortie de MXDC non traité.

</dd> <dt>

<span id="MXDC_RESOURCE_PNG_THUMBNAIL"></span><span id="mxdc_resource_png_thumbnail"></span>**\_ \_ miniature png de ressource MXDC \_**
</dt> <dd>

Miniature PNG qui doit être transmise à la sortie de MXDC non traité.

</dd> <dt>

<span id="MXDC_RESOURCE_MAX"></span><span id="mxdc_resource_max"></span>**MXDC \_ ressource \_ Max.**
</dt> <dd>

Nombre maximal de ressources pour la validation.

</dd> </dl>

## <a name="remarks"></a>Notes

Cette énumération est principalement utilisée en tant que membre **dwResourceType** de la structure de la [**\_ ressource MXDC XPS \_ S0PAGE \_ \_**](mxdcxpss0pageresource.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                                            |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                                                      |
| En-tête<br/>                   | <dl> <dt>Winspool. h (inclure Windows. h)</dt> </dl> |



 

 




