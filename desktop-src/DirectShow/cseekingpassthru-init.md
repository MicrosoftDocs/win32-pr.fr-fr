---
description: La méthode Init Initialise l’objet.
ms.assetid: a919adfa-0ffb-4241-b709-ad0e8d55476a
title: Méthode CSeekingPassThru.Init (Seekpt. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSeekingPassThru.Init
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 78176a6966f379240b5b7edd1ef5b73d7fa75b3f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106539515"
---
# <a name="cseekingpassthruinit-method"></a>Méthode CSeekingPassThru.Init

La `Init` méthode initialise l’objet.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT Init(
  [in] BOOL bSupportRendering,
       IPin *pPin
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*bSupportRendering* \[ dans\]
</dt> <dd>

Valeur booléenne qui spécifie si le filtre est un convertisseur. Utilisez la valeur **true** si le filtre est un convertisseur, ou **false** dans le cas contraire.

</dd> <dt>

*pPin* 
</dt> <dd>

Pointeur vers l’interface [**IPIN**](/windows/desktop/api/Strmif/nn-strmif-ipin) sur la broche d’entrée du filtre.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne l’une des valeurs **HRESULT** indiquées dans le tableau suivant.



| Code de retour                                                                                   | Description                                        |
|-----------------------------------------------------------------------------------------------|----------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>          | Opération réussie.<br/>                                |
| <dl> <dt>**E \_ échec**</dt> </dl>        | L’objet a déjà été initialisé.<br/>         |
| <dl> <dt>**\_OUTOFMEMORY E**</dt> </dl> | Mémoire insuffisante pour créer l’objet.<br/> |



 

## <a name="remarks"></a>Notes

Si la valeur de *bSupportRendering* est **true**, cette méthode crée une instance de la classe [**CRendererPosPassThru**](crendererpospassthru.md) . Sinon, elle crée une instance de la classe [**CPosPassThru**](cpospassthru.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Seekpt. h (include streams. h)</dt> </dl>                                                                                    |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CSeekingPassThru, classe**](cseekingpassthru.md)
</dt> </dl>

 

 




