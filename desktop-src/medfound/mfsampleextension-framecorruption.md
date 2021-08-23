---
description: Spécifie si une image vidéo est endommagée.
ms.assetid: 0218F6F6-6832-445C-B733-6A99E4EA2A3B
title: Attribut MFSampleExtension_FrameCorruption (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 00d61056e22e9600d3ef2b1270c9d72b46c4b241c3de3f1ba0e74748c3bcb0e2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119603119"
---
# <a name="mfsampleextension_framecorruption-attribute"></a>\_Attribut MFSampleExtension FrameCorruption

Spécifie si une image vidéo est endommagée.

## <a name="data-type"></a>Type de données

**UINT32**

## <a name="getset"></a>Obtenir/définir

Pour récupérer cet attribut, appelez [**IMFAttributes :: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Pour définir cet attribut, appelez [**IMFAttributes :: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="applies-to"></a>S’applique à

[**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)

## <a name="remarks"></a>Remarques

Un décodeur vidéo peut définir cet attribut sur ses échantillons de sortie. Si la valeur est 1, le décodeur a détecté une altération des données dans le frame. Si la valeur est 0, il n’y a aucune altération des données, ou aucune n’a été détectée.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8 \[ applications de bureau \| UWP apps\]<br/>                                  |
| Serveur minimal pris en charge<br/> | Windows Server 2012 \[ applications de bureau \| UWP apps\]<br/>                        |
| En-tête<br/>                   | <dl> <dt>Mfapi. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Liste alphabétique des attributs Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Exemples d’attributs](sample-attributes.md)
</dt> <dt>

[Exemples de supports](media-samples.md)
</dt> </dl>

 

 




