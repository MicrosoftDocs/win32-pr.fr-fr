---
description: Spécifie si une transformation de Media Foundation (MFT) copie les attributs des exemples d’entrée vers les exemples de sortie.
ms.assetid: 039ecb35-9aa9-4e8a-bbbc-042b9c4c874c
title: MFPKEY_EXATTRIBUTE_SUPPORTED, propriété (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 33017111eba95f54e88671cbcf026b3f40812a08
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864161"
---
# <a name="mfpkey_exattribute_supported-property"></a>\_Propriété MFPKEY EXattribute \_ prise en charge

Spécifie si une transformation de Media Foundation (MFT) copie les attributs des exemples d’entrée vers les exemples de sortie.



Type de données

Type de PROPVARIANT (VT)

Membre PROPVARIANT

**VARIANT \_ booléen**

VT \_ bool

**boolVal**



## <a name="remarks"></a>Notes

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
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                           |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                                     |
| En-tête<br/>                   | <dl> <dt>Mftransform. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Propriétés de la Media Foundation](media-foundation-properties.md)
</dt> <dt>

[Exemples d’attributs](sample-attributes.md)
</dt> <dt>

[**IMFTransform ::P rocessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput)
</dt> </dl>

 

 




