---
description: Spécifie si une Media Foundation transformation (MFT) effectue un traitement asynchrone.
ms.assetid: fcc70282-cfac-487c-b9ff-39e62c836f8b
title: Attribut MF_TRANSFORM_ASYNC (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e92a647ca122c138f2ef7e90670798200fc3fa629be48d6242b4e71dbc93151e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119714348"
---
# <a name="mf_transform_async-attribute"></a>\_Attribut Async de transformation MF \_

Spécifie si une Media Foundation transformation (MFT) effectue un traitement asynchrone.

## <a name="data-type"></a>Type de données

**UINT32**

## <a name="getset"></a>Obtenir/définir

Pour récupérer cet attribut, appelez [**IMFAttributes :: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Pour définir cet attribut, appelez [**IMFAttributes :: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="remarks"></a>Remarques

L’attribut est une valeur booléenne :

-   Si l’attribut est différent de zéro, la table MFT effectue un traitement asynchrone.
-   Si l’attribut a la valeur 0 ou n’est pas défini, la table MFT est synchrone.

Pour récupérer cet attribut, appelez d’abord [**IMFTransform :: GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) pour récupérer le magasin d’attributs de la MFT. Si cette méthode est réussie, appelez [**IMFAttributes :: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32) pour récupérer la valeur de l’attribut. Si l’une ou l’autre des deux méthodes échoue, la table MFT est synchrone.

Pour les MFTs asynchrones, cet attribut doit être défini sur une valeur différente de zéro. Pour les MFTs synchrones, cet attribut est facultatif, mais il doit avoir la valeur 0 s’il est présent.

Les MFTs asynchrones ne sont pas compatibles avec les versions antérieures de Media Foundation. Pour utiliser une table MFT asynchrone, le client doit définir l’attribut de [**\_ \_ \_ déverrouillage asynchrone de transformation MF**](mf-transform-async-unlock.md) sur la table MFT. (Le pipeline Microsoft Media Foundation effectue cette étape automatiquement.)

## <a name="examples"></a>Exemples

Le code suivant teste si une table MFT effectue un traitement asynchrone.


```C++
BOOL IsTransformAsync(IMFTransform *pMFT)
{
    BOOL bAsync = FALSE;
    IMFAttributes *pAttributes = NULL;

    HRESULT hr = pMFT->GetAttributes(&pAttributes);
    if (SUCCEEDED(hr))
    {
        bAsync = MFGetAttributeUINT32(pAttributes, MF_TRANSFORM_ASYNC, FALSE);
        pAttributes->Release();
    }

    return (bAsync != FALSE);
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
</dt> <dt>

[**mode \_ de \_ déverrouillage asynchrone de la transformation MF \_**](mf-transform-async-unlock.md)
</dt> </dl>

 

 




