---
description: Force le convertisseur de vidéo amélioré (EVR) à limiter sa sortie pour qu’il corresponde à la bande passante GPU.
ms.assetid: e81e67d6-aa72-44c1-90e9-72ab18bca1c9
title: Attribut EVRConfig_ForceThrottle (UUID. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ad09d0c3133039975a04a026ec84233987dfd4033b120a4b8fc6272e2fd72b9f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119346139"
---
# <a name="evrconfig_forcethrottle-attribute"></a>\_Attribut EVRConfig ForceThrottle

Force le convertisseur de vidéo amélioré (EVR) à limiter sa sortie pour qu’il corresponde à la bande passante GPU.

## <a name="data-type"></a>Type de données

**UINT32**

## <a name="getset"></a>Obtenir/définir

Pour récupérer cet attribut, appelez [**IMFAttributes :: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Pour définir cet attribut, appelez [**IMFAttributes :: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="remarks"></a>Remarques

Cet attribut peut être défini sur le récepteur multimédia EVR. Pour définir l’attribut, utilisez **IUnknown :: QueryInterface** pour interroger le récepteur multimédia EVR pour l’interface [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) .

La définition de cet attribut a le même effet que la définition de l’indicateur **MFVideoRenderPrefs \_ FORCEOUTPUTTHROTTLING** sur EVR. Pour obtenir une description de cet indicateur, consultez [**MFVideoRenderPrefs**](/windows/desktop/api/evr/ne-evr-mfvideorenderprefs) .

La constante GUID de cet attribut est exportée à partir de strmiids. lib.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | applications de \[ bureau Windows 7 uniquement\]<br/>                                         |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 R2, \[ applications de bureau uniquement\]<br/>                            |
| En-tête<br/>                   | <dl> <dt>UUID. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Liste alphabétique des attributs Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Attributs EVR](enhanced-video-renderer-attributes.md)
</dt> <dt>

[Gestion de la qualité vidéo](video-quality-management.md)
</dt> </dl>

 

 




