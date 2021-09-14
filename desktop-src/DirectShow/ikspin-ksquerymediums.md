---
description: La méthode KsQueryMediums récupère les supports pris en charge par un code confidentiel.
ms.assetid: 554bf968-6054-4f9d-95db-facf0444641f
title: 'IKsPin :: KsQueryMediums, méthode (ksproxy. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IKsPin.KsQueryMediums
api_type:
- COM
api_location:
- Strmiids.lib
- Strmiids.dll
ms.openlocfilehash: f037317b49bc54f5ea9db5b7a4ae039ec0a9970d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127296646"
---
# <a name="ikspinksquerymediums-method"></a>IKsPin :: KsQueryMediums, méthode

La `KsQueryMediums` méthode récupère les supports pris en charge par un code confidentiel.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT KsQueryMediums(
  [out] KSMULTIPLE_ITEM **ppmi
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*PPMI* \[ à\]
</dt> <dd>

Adresse d’un pointeur vers une structure d' [**\_ élément KSMULTIPLE**](ksmultiple-item.md) .

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Si la méthode est réussie, elle retourne la valeur \_ OK. En cas d’échec, elle retourne un code d’erreur **HRESULT** .

## <a name="remarks"></a>Notes

Cette méthode retourne une structure d' [**\_ élément KSMULTIPLE**](ksmultiple-item.md) allouée par la tâche, qui est suivie par zéro ou plusieurs structures [**REGPINMEDIUM**](/windows/desktop/api/strmif/ns-strmif-regpinmedium) . Le membre **Count** de la structure de l' **\_ élément KSMULTIPLE** spécifie le nombre de structures **REGPINMEDIUM** . Chaque structure **REGPINMEDIUM** définit un support pris en charge par le code confidentiel.

L’appelant doit libérer les structures retournées, à l’aide de la fonction **CoTaskMemFree** .

Vous devez inclure KS. h avant ksproxy. h.

## <a name="examples"></a>Exemples

La fonction d’assistance suivante tente de faire correspondre un code confidentiel par rapport à un support spécifié.


```C++
HRESULT FindMatchingMedium(
    IPin *pPin, 
    REGPINMEDIUM *pMedium, 
    bool *pfMatch)
{
    IKsPin* pKsPin = NULL;
    KSMULTIPLE_ITEM *pmi;

    *pfMatch = false;
    HRESULT hr = pPin->QueryInterface(IID_IKsPin, (void **)&pKsPin);
    if (FAILED(hr)) 
        return hr;  // Pin does not support IKsPin.

    hr = pKsPin->KsQueryMediums(&pmi);
    pKsPin->Release();
    if (FAILED(hr))
        return hr;  // Pin does not support mediums.

    if (pmi->Count) 
    {
        // Use pointer arithmetic to reference the first medium structure.
        REGPINMEDIUM *pTemp = (REGPINMEDIUM*)(pmi + 1);
        for (ULONG i = 0; i < pmi->Count; i++, pTemp++) 
        {
            if (pMedium->clsMedium == pTemp->clsMedium) 
            {
                *pfMatch = true;
                break;
            }
        }
    }        
    CoTaskMemFree(pmi);
    return S_OK;
}
```



## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                              |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                    |
| En-tête<br/>                   | <dl> <dt>Ksproxy. h</dt> </dl>    |
| Bibliothèque<br/>                  | <dl> <dt>Strmiids. lib</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Codes d’erreur et de réussite](error-and-success-codes.md)
</dt> <dt>

[**Interface IKsPin**](ikspin.md)
</dt> <dt>

[Filtres de pilote de classe WDM](wdm-class-driver-filters.md)
</dt> </dl>

 

 




