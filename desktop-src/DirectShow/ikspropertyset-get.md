---
description: La méthode obtenir récupère une propriété identifiée par un GUID de jeu de propriétés et un ID de propriété.
ms.assetid: f39862db-0659-4533-8cee-aee2f778e085
title: 'IKsPropertySet :: méthode d’extraction (ksproxy. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IKsPropertySet.Get
api_type:
- COM
api_location:
- Strmiids.lib
- Strmiids.dll
ms.openlocfilehash: 9c4461e8c5886d84bcf3b7faa6675b749bc0c37d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127240714"
---
# <a name="ikspropertysetget-method"></a>IKsPropertySet :: méthode d’extraction

La méthode **obtenir** récupère une propriété identifiée par un GUID de jeu de propriétés et un ID de propriété.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT Get(
  [in]  REFGUID guidPropSet,
  [in]  DWORD   dwPropID,
  [in]  LPVOID  pInstanceData,
  [in]  DWORD   cbInstanceData,
  [out] LPVOID  pPropData,
  [in]  DWORD   cbPropData,
  [out] DWORD   *pcbReturned
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*guidPropSet* \[ dans\]
</dt> <dd>

GUID de la propriété définie.

</dd> <dt>

*dwPropID* \[ dans\]
</dt> <dd>

Identificateur de la propriété dans la propriété définie.

</dd> <dt>

*pInstanceData* \[ dans\]
</dt> <dd>

Pointeur vers un tableau d’octets qui contient les données d’instance de la propriété.

</dd> <dt>

*cbInstanceData* \[ dans\]
</dt> <dd>

Taille du tableau donnée dans *pInstanceData*, en octets.

</dd> <dt>

*pPropData* \[ à\]
</dt> <dd>

Pointeur vers un tableau d’octets qui reçoit les données de propriété.

</dd> <dt>

*cbPropData* \[ dans\]
</dt> <dd>

Taille du tableau donnée dans *pPropData*, en octets.

</dd> <dt>

*pcbReturned* \[ à\]
</dt> <dd>

Reçoit le nombre d’octets que la méthode copie dans le tableau *pPropData* .

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Retourne une valeur **HRESULT** . Les valeurs possibles sont les suivantes.



| Code de retour                                                                                              | Description                                                                 |
|----------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>                     | Réussite.<br/>                                                         |
| <dl> <dt>**jeu d’E \_ props \_ \_ non pris en charge**</dt> </dl> | Le jeu de propriétés n’est pas pris en charge.<br/>                               |
| <dl> <dt>**\_ID prop \_ \_ non pris en charge**</dt> </dl>  | L’ID de propriété n’est pas pris en charge pour le jeu de propriétés spécifié.<br/> |



 

## <a name="remarks"></a>Notes

> [!Note]  
> Une autre interface portant ce nom existe dans le fichier d’en-tête dsound. h. Les deux interfaces ne sont pas compatibles. l’interface [IKsControl](/windows-hardware/drivers/ddi/ksproxy/nn-ksproxy-ikscontrol) , documentée dans le DirectShow DDK, est désormais l’interface recommandée pour passer des jeux de propriétés entre les pilotes WDM et les composants en mode utilisateur.

 

Pour récupérer une propriété, allouez une mémoire tampon dans laquelle cette méthode sera remplie. Pour déterminer la taille de mémoire tampon nécessaire, spécifiez **null** pour *pPropData* et zéro (0) pour *cbPropData*. Cette méthode retourne la taille de mémoire tampon nécessaire dans *pcbReturned*.

Vous devez inclure KS. h avant ksproxy. h.

## <a name="examples"></a>Exemples

L’exemple suivant interroge un code confidentiel pour sa catégorie de code confidentiel, en extrayant la propriété de **\_ \_ catégorie de code confidentiel AMPROPERTY** . (Consultez [pin Property Set](pin-property-set.md).)


```C++
HRESULT GetPinCategory(IPin *pPin, GUID *pPinCategory)
{
    IKsPropertySet *pKs = NULL;

    HRESULT hr = pPin->QueryInterface(IID_PPV_ARGS(&pKs));
    if (FAILED(hr))
    {
        return hr;
    }

    // Try to retrieve the pin category.
    DWORD cbReturned = 0;
    hr = pKs->Get(AMPROPSETID_Pin, AMPROPERTY_PIN_CATEGORY, NULL, 0, 
        pPinCategory, sizeof(GUID), &cbReturned);
    
    // If this succeeded, pPinCategory now contains the category GUID.

    SafeRelease(&pKs);
    return hr;
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

[**Interface IKsPropertySet**](ikspropertyset.md)
</dt> <dt>

[Jeux de propriétés](property-sets.md)
</dt> </dl>

 

 
