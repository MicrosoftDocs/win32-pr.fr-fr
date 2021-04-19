---
description: Définit l’Gestionnaire de périphériques de l’infrastructure Microsoft DirectX Graphics (DXGI) sur le moteur multimédia.
ms.assetid: CB952492-0ACF-4501-BD8B-133E26FCE8F7
title: Attribut MF_MEDIA_ENGINE_DXGI_MANAGER (Mfmediaengine. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 98e731b5aa2449ae772427c6743ec4f97b5d7601
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/03/2021
ms.locfileid: "106523749"
---
# <a name="mf_media_engine_dxgi_manager-attribute"></a>\_Attribut du \_ \_ Gestionnaire de dxgi du moteur multimédia MF \_

Définit l’Gestionnaire de périphériques de l’infrastructure Microsoft DirectX Graphics (DXGI) sur le moteur multimédia.

## <a name="data-type"></a>Type de données

**IMFDXGIDeviceManager \* *_ stocké en tant que _* IUnknown\***

## <a name="getset"></a>Obtenir/définir

Pour récupérer cet attribut, appelez [**IMFAttributes :: GetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown).

Pour définir cet attribut, appelez [**IMFAttributes :: setunknown,**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown).

## <a name="remarks"></a>Notes

La valeur de cet attribut est un pointeur vers l’interface [**IMFDXGIDeviceManager**](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager) .

En mode serveur Frame, cet attribut permet au moteur multimédia d’utiliser l’accélération matérielle pour le décodage vidéo et le traitement vidéo. Si l’attribut n’est pas défini, le moteur multimédia utilise le décodage et le traitement des logiciels.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications Windows 8 \[ Desktop Apps \| UWP\]<br/>                                          |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2012 \[ \| apps UWP\]<br/>                                |
| En-tête<br/>                   | <dl> <dt>Mfmediaengine. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Liste alphabétique des attributs Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**IMFMediaEngineClassFactory :: CreateInstance**](/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineclassfactory-createinstance)
</dt> </dl>

 

 




