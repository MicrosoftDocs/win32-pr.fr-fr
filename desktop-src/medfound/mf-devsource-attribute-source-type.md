---
description: Spécifie un type d’appareil, tel que la capture audio ou la capture vidéo.
ms.assetid: c6c05267-1c93-48e2-b463-b5a1514f1b7b
title: Attribut MF_DEVSOURCE_ATTRIBUTE_SOURCE_TYPE (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3445c74b1a77472bad564f6988f9ae2f4696fef7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127414199"
---
# <a name="mf_devsource_attribute_source_type-attribute"></a>Attribut de type de source de l' \_ attribut DEVSOURCE MF \_ \_ \_

Spécifie le type d’un appareil, tel que la capture audio ou la capture vidéo.

## <a name="data-type"></a>Type de données

**GUID**

Les valeurs suivantes sont définies pour cet attribut :



| Valeur                                                                                                                                                                                                                                                                 | Signification                          |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------|
| <span id="MF_DEVSOURCE_ATTRIBUTE_SOURCE_TYPE_AUDCAP_GUID"></span><span id="mf_devsource_attribute_source_type_audcap_guid"></span><dl> <dt>**TYPE de source de l' \_ attribut DEVSOURCE MF \_ \_ \_ \_ AUDCAP \_ GUID**</dt> </dl> | Périphérique de capture audio.<br/> |
| <span id="MF_DEVSOURCE_ATTRIBUTE_SOURCE_TYPE_VIDCAP_GUID"></span><span id="mf_devsource_attribute_source_type_vidcap_guid"></span><dl> <dt>**TYPE de source de l' \_ attribut DEVSOURCE MF \_ \_ \_ \_ VIDCAP \_ GUID**</dt> </dl> | Périphérique de capture vidéo.<br/> |



 

## <a name="getset"></a>Obtenir/définir

Pour récupérer cet attribut, appelez [**IMFAttributes :: GetGuid**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid).

Pour définir cet attribut, appelez [**IMFAttributes :: SetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid).

## <a name="remarks"></a>Notes

Utilisez cet attribut comme entrée pour les fonctions suivantes :

-   [**MFCreateDeviceSource**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesource)
-   [**MFCreateDeviceSourceActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesourceactivate)
-   [**MFEnumDeviceSources**](/windows/desktop/api/mfidl/nf-mfidl-mfenumdevicesources)

En outre, cet attribut est défini sur les objets d’activation retournés par la fonction [**MFEnumDeviceSources**](/windows/desktop/api/mfidl/nf-mfidl-mfenumdevicesources) .

La constante GUID de cet attribut est exportée à partir de mfuuid. lib.

## <a name="requirements"></a>Spécifications



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

 

 




