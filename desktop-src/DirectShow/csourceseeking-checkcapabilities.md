---
description: 'La méthode CheckCapabilities interroge si le flux a spécifié des fonctionnalités de recherche. Cette méthode implémente la méthode IMediaSeeking :: CheckCapabilities.'
ms.assetid: 5d37e179-9e04-44e1-acbc-dfd2682830c0
title: Méthode CSourceSeeking. CheckCapabilities (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceSeeking.CheckCapabilities
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2f537973ac6c8f084ea42ba915a6293e581debef
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126923575"
---
# <a name="csourceseekingcheckcapabilities-method"></a>Méthode CSourceSeeking. CheckCapabilities

La `CheckCapabilities` méthode interroge si le flux a spécifié des fonctionnalités de recherche. Cette méthode implémente la méthode [**IMediaSeeking :: CheckCapabilities**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-checkcapabilities) .

## <a name="syntax"></a>Syntaxe


```C++
HRESULT CheckCapabilities(
   DWORD *pCapabilities
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pCapabilities* 
</dt> <dd>

Pointeur vers une combinaison d’opérations de bits d’un ou de plusieurs attributs de [**\_ \_ \_ capacités de recherche**](/windows/win32/api/strmif/ne-strmif-am_seeking_seeking_capabilities) de recherche.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Retourne l’une des valeurs **HRESULT** listées dans le tableau suivant.



| Code de retour                                                                               | Description                                                            |
|-------------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| <dl> <dt>**S \_ false**</dt> </dl>   | Toutes les fonctionnalités de *pCapabilities* ne sont pas présentes.<br/> |
| <dl> <dt>**\_OK**</dt> </dl>      | Toutes les fonctionnalités de *pCapabilities* sont présentes.<br/>            |
| <dl> <dt>**\_pointeur E**</dt> </dl> | Argument de pointeur **null** .<br/>                                  |



 

## <a name="remarks"></a>Notes

Comme elle est implémentée, cette méthode vérifie la valeur de *\* pCapabilities* par rapport à la variable membre [**CSourceSeeking :: m \_ dwSeekingCaps**](csourceseeking-m-dwseekingcaps.md) . Toutefois, il ne définit pas *\* pCapabilities* égal à **m \_ dwSeekingCaps**, comme décrit pour la méthode [**IMediaSeeking :: CheckCapabilities**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-checkcapabilities) . En outre, dans le cas où aucune des fonctionnalités spécifiées n’est disponible, la méthode ne retourne pas E \_ Fail. Une implémentation plus complète serait la suivante :


```C++
STDMETHODIMP CheckCapabilities(DWORD *pCapabilities)
{
    CheckPointer(pCapabilities, E_POINTER)
;
    DWORD dwCaps;
    HRESULT hr = GetCapabilities(&dwCaps);
    if (SUCCEEDED(hr))
    {
        dwCaps &= *pCapabilities;
        if (dwCaps)
        {
            hr =  (dwCaps == *pCapabilities ? S_OK : S_FALSE );
        }
        else 
        {
            hr = E_FAIL;
        }
        *pCapabilities = dwCaps;
    }
    else 
    {
        *pCapabilities = 0;
    }
    return hr;
}
```



## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Ctlutil. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CSourceSeeking, classe**](csourceseeking.md)
</dt> </dl>

 

 




