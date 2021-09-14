---
description: Spécifie l’ID de point de terminaison pour un périphérique de capture audio.
ms.assetid: a0d8b54b-7a05-4307-a756-a34bb22f1afd
title: Attribut MF_DEVSOURCE_ATTRIBUTE_SOURCE_TYPE_AUDCAP_ENDPOINT_ID (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a1448dc753a8e3b8221fa040309d3f5b60c4879
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127314065"
---
# <a name="mf_devsource_attribute_source_type_audcap_endpoint_id-attribute"></a>Attribut \_ d' \_ ID de \_ point de \_ \_ \_ terminaison \_ AUDCAP de type de l’attribut DEVSOURCE MF

Spécifie l’ID de point de terminaison pour un périphérique de capture audio.

## <a name="data-type"></a>Type de données

**WCHAR\***

## <a name="getset"></a>Obtenir/définir

Pour récupérer cet attribut, appelez [**IMFAttributes :: GetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring).

Pour définir cet attribut, appelez [**IMFAttributes :: SetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring).

## <a name="remarks"></a>Notes

La valeur de l’attribut est un ID de point de terminaison. Cet attribut est utilisé avec les fonctions suivantes :

-   Il peut être utilisé comme entrée pour les fonctions [**MFCreateDeviceSource**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesource) et [**MFCreateDeviceSourceActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesourceactivate) . Dans ce contexte, l’attribut spécifie le périphérique de capture audio pour la fonction. Vous pouvez obtenir l’ID de point de terminaison d’un appareil donné en appelant la méthode [**IMMDevice :: GetId**](/windows/win32/api/mmdeviceapi/nf-mmdeviceapi-immdevice-getid) . Pour plus d’informations, consultez la documentation de l’API audio principale.
-   Lorsque la fonction [**MFEnumDeviceSources**](/windows/desktop/api/mfidl/nf-mfidl-mfenumdevicesources) énumère les périphériques audio, les objets d’activation retournés contiennent cet attribut. L’attribut est utilisé en interne par l’objet d’activation lorsqu’il crée la source du média.

La constante GUID de cet attribut est exportée à partir de mfuuid. lib.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------|------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Liste alphabétique des attributs Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Capture audio/vidéo](audio-video-capture.md)
</dt> <dt>

[Capturer les attributs de l’appareil](capture-device-attributes.md)
</dt> </dl>

 

 
