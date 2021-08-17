---
description: Spécifie le format de sortie d’un appareil.
ms.assetid: 33a1b546-ece2-44ef-a1c0-5579c32be0bc
title: Attribut MF_DEVSOURCE_ATTRIBUTE_MEDIA_TYPE (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eb4685f419658ecf77782a4cef770fd205119bb6cfd95523edb7fbbe001fd700
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119105035"
---
# <a name="mf_devsource_attribute_media_type-attribute"></a>\_Attribut de \_ \_ type de média d’attribut DEVSOURCE MF \_

Spécifie le format de sortie d’un appareil.

## <a name="data-type"></a>Type de données

**[**MFT \_ Enregistrer \_ les \_ informations de type**](/windows/win32/api/mfobjects/ns-mfobjects-mft_register_type_info)** stockées en tant qu' **octets \[ \]**

## <a name="getset"></a>Obtenir/définir

Pour récupérer cet attribut, appelez [**IMFAttributes :: GetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob).

Pour définir cet attribut, appelez [**IMFAttributes :: SetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob).

## <a name="remarks"></a>Remarques

Cet attribut contient une paire de GUID : un type principal et un sous-type. Ces GUID décrivent le format de sortie par défaut de l’appareil. L’appareil peut prendre en charge des formats de sortie supplémentaires.

Par exemple, si un appareil de capture vidéo produit une vidéo RGB-32, la valeur de cet attribut est `{ MFMediaType_Video, MFVideoFormat_RGB32 }` .

Cet attribut est une indication de l’application. Pour obtenir le format de sortie exact, créez la source du média pour l’appareil et récupérez le descripteur de présentation de la source du média.

Cet attribut est défini sur les objets d’activation retournés par les fonctions suivantes :

-   [**MFCreateDeviceSourceActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesourceactivate)
-   [**MFEnumDeviceSources**](/windows/desktop/api/mfidl/nf-mfidl-mfenumdevicesources)

La constante GUID de cet attribut est exportée à partir de mfuuid. lib.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | applications de \[ bureau Windows 7 uniquement\]<br/>                                         |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 R2, \[ applications de bureau uniquement\]<br/>                            |
| En-tête<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Liste alphabétique des attributs Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Capture audio/vidéo](audio-video-capture.md)
</dt> <dt>

[Capturer les attributs de l’appareil](capture-device-attributes.md)
</dt> </dl>

 

 




