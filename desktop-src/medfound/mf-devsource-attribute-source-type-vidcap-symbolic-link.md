---
description: Contient le lien symbolique pour un pilote de capture vidéo.
ms.assetid: 3d256dec-ec8c-4c62-883b-e2c292fd90eb
title: Attribut MF_DEVSOURCE_ATTRIBUTE_SOURCE_TYPE_VIDCAP_SYMBOLIC_LINK (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 48e1c854ee070713462676482cc04690c2bdde2d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127414200"
---
# <a name="mf_devsource_attribute_source_type_vidcap_symbolic_link-attribute"></a>Attribut \_ de \_ \_ \_ \_ \_ lien symbolique VIDCAP du type de source \_ de l’attribut MF DEVSOURCE

Contient le lien symbolique pour un pilote de capture vidéo.

## <a name="data-type"></a>Type de données

**WCHAR\***

## <a name="getset"></a>Obtenir/définir

Pour récupérer cet attribut, appelez [**IMFAttributes :: GetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring).

Pour définir cet attribut, appelez [**IMFAttributes :: SetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring).

## <a name="remarks"></a>Notes

Utilisez cet attribut comme entrée de la fonction [**MFCreateDeviceSourceActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesourceactivate) .

En outre, cet attribut est défini sur les objets d’activation retournés par les fonctions suivantes :

-   [**MFCreateDeviceSourceActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesourceactivate)
-   [**MFEnumDeviceSources**](/windows/desktop/api/mfidl/nf-mfidl-mfenumdevicesources)

Le lien symbolique doit être considéré comme une chaîne opaque. Le nom complet lisible pour un appareil est contenu dans l’attribut de [ \_ \_ \_ \_ nom convivial de l’attribut MF DEVSOURCE](mf-devsource-attribute-friendly-name.md) .

L’attribut \_ \_ \_ de lien symbolique VIDCAP du type de source de l’attribut MF DEVSOURCE \_ \_ \_ \_ peut être transmis en tant que valeur de l’argument DevicePath de la fonction [**SetupDiOpenDeviceInterface**](/windows/win32/api/setupapi/nf-setupapi-setupdiopendeviceinterfacea) .

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

 

 
