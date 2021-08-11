---
description: Active l’utilisation d’une transformation de Media Foundation asynchrone (MFT).
ms.assetid: e12ab57e-ebc2-46af-afdf-d78d4db16fcf
title: Attribut MF_TRANSFORM_ASYNC_UNLOCK (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 82a0a8f328095c3a5c567171fa6a625a77e5623d126dfb2be9f34fef556984be
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118244175"
---
# <a name="mf_transform_async_unlock-attribute"></a>\_Attribut de \_ déverrouillage asynchrone de transformation MF \_

Active l’utilisation d’une transformation de Media Foundation asynchrone (MFT).

## <a name="data-type"></a>Type de données

**UINT32**

## <a name="getset"></a>Obtenir/définir

Pour récupérer cet attribut, appelez [**IMFAttributes :: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Pour définir cet attribut, appelez [**IMFAttributes :: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="remarks"></a>Notes

Les MFTs asynchrones ne sont pas compatibles avec les versions antérieures de Microsoft Media Foundation. Pour empêcher les applications existantes d’utiliser accidentellement une table MFT asynchrone, cet attribut doit être défini sur une valeur différente de zéro pour qu’une table MFT asynchrone puisse être utilisée. Le pipeline Media Foundation définit automatiquement l’attribut, de sorte que la plupart des applications n’ont pas besoin d’utiliser cet attribut. Toutefois, si une application utilise une table MFT asynchrone en dehors du pipeline Media Foundation, l’application doit définir cet attribut.

Les MFTs synchrones ne nécessitent pas cet attribut.

Pour tester si une table MFT est asynchrone, récupérez la valeur de l’attribut [ \_ \_ Async de transformation MF](mf-transform-async.md) sur la table MFT.

## <a name="examples"></a>Exemples

Le code suivant déverrouille une table MFT asynchrone.


```C++
HRESULT UnlockAsyncMFT(IMFTransform *pMFT)
{
    IMFAttributes *pAttributes = NULL;

    HRESULT hr = hr = pMFT->GetAttributes(&pAttributes);

    if (SUCCEEDED(hr))
    {
        hr = pAttributes->SetUINT32(MF_TRANSFORM_ASYNC_UNLOCK, TRUE);
        pAttributes->Release();
    }
    
    return hr;
}
```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | applications de \[ bureau Windows 7 \| applications UWP\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Applications du serveur 2008 R2 \[ Desktop Apps \| UWP\]<br/>                           |
| En-tête<br/>                   | <dl> <dt>Mftransform. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Liste alphabétique des attributs Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[MFTs asynchrone](asynchronous-mfts.md)
</dt> <dt>

[Attributs de transformation](transform-attributes.md)
</dt> </dl>

 

 




