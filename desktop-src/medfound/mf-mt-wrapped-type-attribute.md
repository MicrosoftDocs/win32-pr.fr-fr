---
description: Contient un type de média encapsulé dans un autre type de média.
ms.assetid: 3bd94523-0206-44d8-83a2-e569e4ab7815
title: Attribut MF_MT_WRAPPED_TYPE (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 69ec0b86f985e40f808862091d3ea4506d8c456ffbf05ebd749f15e8ba8bf0c4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119356359"
---
# <a name="mf_mt_wrapped_type-attribute"></a>\_Attribut de \_ \_ type encapsulé pour MF MT

Contient un type de média encapsulé dans un autre type de média.

## <a name="data-type"></a>Type de données

Tableau d’octets

## <a name="remarks"></a>Remarques

Cet attribut est utilisé dans la fonction [**MFWrapMediaType**](/windows/desktop/api/mfapi/nf-mfapi-mfwrapmediatype) , qui encapsule un type de média à l’intérieur d’un autre type de média.

La fonction [**MFWrapMediaType**](/windows/desktop/api/mfapi/nf-mfapi-mfwrapmediatype) effectue les opérations suivantes :

1.  Convertit le type de média d’origine en tableau binaire.
2.  Définit l’attribut de **\_ \_ \_ type encapsulé MT Wrapped** sur le nouveau type de média. La valeur de l’attribut est le tableau binaire.

En général, les applications n’utilisent pas cet attribut directement. Pour désencapsuler le type de média d’origine, appelez [**MFUnwrapMediaType**](/windows/desktop/api/mfapi/nf-mfapi-mfunwrapmediatype).

La constante GUID de cet attribut est exportée à partir de mfuuid. lib.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications UWP pour applications de bureau Vista \|\]<br/>                              |
| Serveur minimal pris en charge<br/> | Windows Applications de bureau du serveur 2008 \[ \| applications UWP\]<br/>                        |
| En-tête<br/>                   | <dl> <dt>Mfapi. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Liste alphabétique des attributs Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**IMFAttributes :: GetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)
</dt> <dt>

[**IMFAttributes :: SetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)
</dt> <dt>

[**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[Attributs du type de média](media-type-attributes.md)
</dt> </dl>

 

 




