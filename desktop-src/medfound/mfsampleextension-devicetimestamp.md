---
description: Contient l’horodatage du pilote de périphérique.
ms.assetid: 8904d104-ebcc-474d-b6b5-b262b6f62ee9
title: Attribut MFSampleExtension_DeviceTimestamp (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 285b354ecd0e399fc297d3677d29b88847f9eba8
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127414067"
---
# <a name="mfsampleextension_devicetimestamp-attribute"></a>\_Attribut MFSampleExtension DeviceTimestamp

Contient l’horodatage du pilote de périphérique.

## <a name="data-type"></a>Type de données

**UINT64**

## <a name="getset"></a>Obtenir/définir

Pour récupérer cet attribut, appelez [**IMFAttributes :: GetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64).

Pour définir cet attribut, appelez [**IMFAttributes :: SetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64).

## <a name="applies-to"></a>S’applique à

[**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)

## <a name="remarks"></a>Notes

Cet attribut est défini sur les exemples de supports créés par une source de média pour un appareil de capture. La valeur de cet attribut se trouve dans le domaine [**MFTIME**](mftime.md) , en partageant une époque avec l’heure du compteur de performance des requêtes (QPC) et toujours exprimé en unités de 100 ns. Cet attribut est disponible pour les MFTs insérés dans le pipeline de capture.

Pour connaître l’horodatage relatif au début de la diffusion en continu, appelez la méthode [**IMFSample :: GetSampleTime**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-getsampletime) .

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

[Capture audio/vidéo en Media Foundation](audio-video-capture-in-media-foundation.md)
</dt> <dt>

[Exemples d’attributs](sample-attributes.md)
</dt> </dl>

 

 




