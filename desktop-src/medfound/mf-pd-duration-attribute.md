---
description: Spécifie la durée d’une présentation, en unités de 100 nanosecondes.
ms.assetid: abc21696-ea97-41ff-9341-6d9e9dcb19ec
title: Attribut MF_PD_DURATION (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9662e68c2380ad1ef9d009302a08d8798ab228fae0fe2b00528d37a4f7269c33
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119664099"
---
# <a name="mf_pd_duration-attribute"></a>\_ \_ Attribut durée MF PD

Spécifie la durée d’une présentation, en unités de 100 nanosecondes.

## <a name="data-type"></a>Type de données

**UINT64**

Traiter en tant que valeur **LongLong** .

## <a name="remarks"></a>Remarques

Les sources multimédias peuvent définir cet attribut sur un descripteur de présentation pour indiquer la durée de la présentation.

Cet attribut est une valeur signée, bien qu’il soit stocké en tant que **UINT64**. Toutefois, l’attribut ne doit jamais contenir une valeur négative.

La constante GUID de cet attribut est exportée à partir de mfuuid. lib.

## <a name="examples"></a>Exemples

L’exemple suivant montre comment obtenir la durée d’une présentation à partir d’une source multimédia.


```C++
HRESULT GetSourceDuration(IMFMediaSource *pSource, MFTIME *pDuration)
{
    *pDuration = 0;

    IMFPresentationDescriptor *pPD = NULL;

    HRESULT hr = pSource->CreatePresentationDescriptor(&pPD);
    if (SUCCEEDED(hr))
    {
        hr = pPD->GetUINT64(MF_PD_DURATION, (UINT64*)pDuration);
        pPD->Release();
    }
    return hr;
}
```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications UWP pour applications de bureau Vista \|\]<br/>                              |
| Serveur minimal pris en charge<br/> | Windows Applications de bureau du serveur 2008 \[ \| applications UWP\]<br/>                        |
| En-tête<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Liste alphabétique des attributs Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**IMFAttributes::GetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64)
</dt> <dt>

[**IMFAttributes::SetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64)
</dt> <dt>

[**IMFPresentationDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[Attributs du descripteur de présentation](presentation-descriptor-attributes.md)
</dt> <dt>

[Descripteurs de présentation](presentation-descriptors.md)
</dt> </dl>

 

 




