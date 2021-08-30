---
description: Autorise le convertisseur vidéo amélioré (EVR) à limiter sa sortie pour qu’il corresponde à la bande passante GPU.
ms.assetid: d591af2e-d47d-4220-a4f6-968f2ac45284
title: Attribut EVRConfig_AllowDropToThrottle (UUID. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bab11159141e1e3ef0f019b0f56f884e02b329d40765bdf01e49962936513e75
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120061599"
---
# <a name="evrconfig_allowdroptothrottle-attribute"></a>\_Attribut EVRConfig AllowDropToThrottle

Autorise le convertisseur vidéo amélioré (EVR) à limiter sa sortie pour qu’il corresponde à la bande passante GPU.

## <a name="data-type"></a>Type de données

**UINT32**

## <a name="getset"></a>Obtenir/définir

Pour récupérer cet attribut, appelez [**IMFAttributes :: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Pour définir cet attribut, appelez [**IMFAttributes :: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="remarks"></a>Remarques

Cet attribut peut être défini sur le récepteur multimédia EVR. Pour définir l’attribut, utilisez **QueryInterface** pour interroger le récepteur multimédia EVR pour l’interface [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) .

La définition de cet attribut a le même effet que la définition de l’indicateur **MFVideoRenderPrefs \_ ALLOWOUTPUTTHROTTLING** sur EVR. Pour obtenir une description de cet indicateur, consultez [**MFVideoRenderPrefs**](/windows/desktop/api/evr/ne-evr-mfvideorenderprefs) .

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

 

 




