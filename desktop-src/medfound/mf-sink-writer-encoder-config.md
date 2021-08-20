---
description: Contient un pointeur vers une banque de propriétés avec des propriétés d’encodage.
ms.assetid: 28AC864C-C63C-4BD4-9770-B7B48A2815C6
title: Attribut MF_SINK_WRITER_ENCODER_CONFIG (Mfreadwrite. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6fb68348987ac406643cbe709dc6052d1add3c04e63b4e1f38d7c681a95c3ae7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118059083"
---
# <a name="mf_sink_writer_encoder_config-attribute"></a>Attribut de configuration de l' \_ \_ \_ encodeur du récepteur MF \_

Contient un pointeur vers une banque de propriétés avec des propriétés d’encodage.

## <a name="data-type"></a>Type de données

**IUnknown\***

## <a name="remarks"></a>Remarques

La valeur de cet attribut est un pointeur [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) .

Cet attribut permet à une application de définir des propriétés d’encodage lors de l’utilisation du [writer du récepteur](sink-writer.md). Pour définir cet attribut, procédez comme suit :

1.  Appelez [**PSCreateMemoryPropertyStore**](/windows/win32/api/propsys/nf-propsys-pscreatememorypropertystore) pour créer une banque de propriétés.
2.  Définissez les propriétés de l’encodeur dans la Banque de propriétés. Les propriétés disponibles dépendent de l’encodeur. Pour plus d’informations, consultez la page [objets codec](codecobjects.md).
3.  Appelez [**MFCreateAttributes**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes) pour créer un nouveau magasin d’attributs.
4.  Appelez [**IMFAttributes :: setunknown,**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown) pour définir le pointeur [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) sur le magasin d’attributs.
5.  Créez une nouvelle instance de l’enregistreur du récepteur. Transmettez le pointeur [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) à la fonction de création. Pour plus d’informations, consultez [attributs du writer du récepteur](sink-writer-attributes.md).

L’enregistreur du récepteur définit les propriétés sur l’encodeur avant de définir les types de média.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8 \[ applications de bureau \| UWP apps\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Server 2012 \[ applications de bureau \| UWP apps\]<br/>                              |
| En-tête<br/>                   | <dl> <dt>Mfreadwrite. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Liste alphabétique des attributs Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**IMFSinkWriter**](/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsinkwriter)
</dt> <dt>

[Attributs du writer du récepteur](sink-writer-attributes.md)
</dt> </dl>

 

 
