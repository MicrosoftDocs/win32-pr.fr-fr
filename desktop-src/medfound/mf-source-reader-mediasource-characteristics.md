---
description: Obtient les caractéristiques de la source du média à partir du lecteur source.
ms.assetid: 4cd48b69-6f7b-4b13-86f3-b38969025f70
title: Attribut MF_SOURCE_READER_MEDIASOURCE_CHARACTERISTICS (Mfreadwrite. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5ec5461bc289517490ae11bdd507895cd1ad434c53b1665ac5c6394907f15a5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118739964"
---
# <a name="mf_source_reader_mediasource_characteristics-attribute"></a>Attribut des caractéristiques de l' \_ \_ \_ attribut MEDIASOURCE du lecteur source MF \_

Obtient les caractéristiques de la source du média à partir du [lecteur source](source-reader.md).

## <a name="data-type"></a>Type de données

**UINT32**

La valeur est **une opération or** au niveau du bit des indicateurs de l’énumération des [**\_ caractéristiques MFMEDIASOURCE**](/windows/desktop/api/mfidl/ne-mfidl-mfmediasource_characteristics) .

## <a name="remarks"></a>Remarques

Pour récupérer cet attribut, appelez la méthode [**IMFSourceReader :: GetPresentationAttribute**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-getpresentationattribute) sur le lecteur source. Définissez le paramètre *dwStreamIndex* sur **MF \_ source \_ Reader \_ MediaSource** et le paramètre *guidAttribute* sur les \_ caractéristiques du lecteur source MF \_ \_ \_ .

Le type **PROPVARIANT** pour cet attribut est **VT \_ UI4**.

## <a name="examples"></a>Exemples


```C++
HRESULT GetSourceFlags(IMFSourceReader *pReader, ULONG *pulFlags)
{
    ULONG flags = 0;

    PROPVARIANT var;
    PropVariantInit(&var);

    HRESULT hr = pReader->GetPresentationAttribute(
        MF_SOURCE_READER_MEDIASOURCE, 
        MF_SOURCE_READER_MEDIASOURCE_CHARACTERISTICS, 
        &var);

    if (SUCCEEDED(hr))
    {
        hr = PropVariantToUInt32(var, &flags);
    }
    if (SUCCEEDED(hr))
    {
        *pulFlags = flags;
    }

    PropVariantClear(&var);
    return hr;
}
```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | applications de \[ bureau Windows 7 \| applications UWP\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Applications du serveur 2008 R2 \[ Desktop Apps \| UWP\]<br/>                           |
| En-tête<br/>                   | <dl> <dt>Mfreadwrite. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Liste alphabétique des attributs Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Lecteur source](source-reader.md)
</dt> </dl>

 

 




