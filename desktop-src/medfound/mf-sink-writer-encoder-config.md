---
description: Contient un pointeur vers une banque de propriétés avec des propriétés d’encodage.
ms.assetid: 28AC864C-C63C-4BD4-9770-B7B48A2815C6
title: Attribut MF_SINK_WRITER_ENCODER_CONFIG (Mfreadwrite. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1703eaa93254c5703f544641edd0063e2190a342
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103757401"
---
# <a name="mf_sink_writer_encoder_config-attribute"></a>Attribut de configuration de l' \_ \_ \_ encodeur du récepteur MF \_

Contient un pointeur vers une banque de propriétés avec des propriétés d’encodage.

## <a name="data-type"></a>Type de données

**IUnknown \** _

## <a name="remarks"></a>Notes

La valeur de cet attribut est un pointeur [_ *IPropertyStore* *](/windows/win32/api/propsys/nn-propsys-ipropertystore) .

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
| Client minimal pris en charge<br/> | Applications Windows 8 \[ Desktop Apps \| UWP\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2012 \[ \| apps UWP\]<br/>                              |
| En-tête<br/>                   | <dl> <dt>Mfreadwrite. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Liste alphabétique des attributs Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**IMFSinkWriter**](/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsinkwriter)
</dt> <dt>

[Attributs du writer du récepteur](sink-writer-attributes.md)
</dt> </dl>

 

 
