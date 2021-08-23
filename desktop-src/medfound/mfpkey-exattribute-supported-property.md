---
description: Spécifie si une transformation de Media Foundation (MFT) copie les attributs des exemples d’entrée vers les exemples de sortie.
ms.assetid: 039ecb35-9aa9-4e8a-bbbc-042b9c4c874c
title: MFPKEY_EXATTRIBUTE_SUPPORTED, propriété (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 248609828df3ef977112058ffe0d169104e68c181fa455ef27f2adcea0220aaa
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119663508"
---
# <a name="mfpkey_exattribute_supported-property"></a>\_Propriété MFPKEY EXattribute \_ prise en charge

Spécifie si une transformation de Media Foundation (MFT) copie les attributs des exemples d’entrée vers les exemples de sortie.



Type de données

Type de PROPVARIANT (VT)

Membre PROPVARIANT

**VARIANT \_ booléen**

VT \_ bool

**boolVal**



## <a name="remarks"></a>Remarques

Cet attribut peut avoir les valeurs suivantes.



| Valeur              | Description                                                                                                                                             |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| **VARIANTE \_ true**  | La table MFT copie les attributs des exemples d’entrée vers les exemples de sortie.                                                                                 |
| **VARIANTE \_ false** | La session multimédia copie les attributs des exemples d’entrée vers les exemples de sortie. Elle ne remplace pas les attributs définis par la table MFT sur les exemples de sortie. |



 

Pour obtenir cet attribut, appelez **QueryInterface** sur la MFT de l’interface **IPropertyStore** .

La valeur par défaut **est \_ false**. Si la MFT n’expose pas l’interface **IPropertyStore** , ou si cette propriété n’est pas définie, traitez la valeur comme **Variant \_ false**.

Cette propriété est en lecture seule.

> [!NOTE] 
> Cet attribut ne s’applique pas aux MFTs asynchrones. Les attributs ne seront pas copiés des exemples d’entrée vers les exemples de sortie pour les MFTs asynchrones, quelle que soit la valeur de cet attribut.

## <a name="examples"></a>Exemples

L’exemple suivant retourne la \_ valeur variant true si une table MFT copie des attributs d’exemple.


```C++
BOOL TransformCopiesSampleAttributes(IMFTransform *pMFT)
{
    BOOL bCopiesAttributes = FALSE;

    IPropertyStore *pProps = NULL;

    HRESULT hr = pMFT->QueryInterface(IID_PPV_ARGS(&pProps));
    
    if (SUCCEEDED(hr))
    {
        PROPVARIANT var;
        hr = pProps->GetValue(MFPKEY_EXATTRIBUTE_SUPPORTED, &var);

        if (SUCCEEDED(hr))
        {
            bCopiesAttributes = 
                (var.vt == VT_BOOL && var.boolVal == VARIANT_TRUE);

            PropVariantClear(&var);
        }
        pProps->Release();
    }
    return bCopiesAttributes;
}
```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                           |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                     |
| En-tête<br/>                   | <dl> <dt>Mftransform. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Propriétés de la Media Foundation](media-foundation-properties.md)
</dt> <dt>

[Exemples d’attributs](sample-attributes.md)
</dt> <dt>

[**IMFTransform ::P rocessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput)
</dt> </dl>

 

 




