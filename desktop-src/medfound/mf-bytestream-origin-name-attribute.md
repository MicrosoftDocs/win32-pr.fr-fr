---
description: Spécifie l’URL d’origine d’un flux d’octets.
ms.assetid: 31d7de71-5bbb-4c29-8ce0-df3684c56916
title: Attribut MF_BYTESTREAM_ORIGIN_NAME (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fe32602501b3750f709135cf7ca458b6eb6a572f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127414228"
---
# <a name="mf_bytestream_origin_name-attribute"></a>\_Attribut de \_ nom d’origine MF BYTESTREAM \_

Spécifie l’URL d’origine d’un flux d’octets.

## <a name="data-type"></a>Type de données

Chaîne de caractères larges

## <a name="remarks"></a>Notes

Les flux d’octets basés sur des fichiers peuvent prendre en charge cet attribut. La valeur de l’attribut est définie lors de la création du flux d’octets. Pour obtenir la valeur de l’attribut, interrogez l’objet de flux d’octets pour l’interface [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) .

La constante GUID de cet attribut est exportée à partir de mfuuid. lib.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications UWP pour applications de bureau Vista \|\]<br/>                                                    |
| Serveur minimal pris en charge<br/> | Windows Applications de bureau du serveur 2008 \[ \| applications UWP\]<br/>                                              |
| En-tête<br/>                   | <dl> <dt>Mfobjects. h (inclure Mfidl. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Liste alphabétique des attributs Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Attributs de flux d’octets](byte-stream-attributes.md)
</dt> <dt>

[**IMFAttributes :: GetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring)
</dt> <dt>

[**IMFAttributes :: SetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring)
</dt> <dt>

[**IMFByteStream**](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream)
</dt> </dl>

 

 




