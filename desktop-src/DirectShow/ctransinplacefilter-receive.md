---
description: La méthode Receive reçoit un exemple de support, le traite et le remet au filtre en aval.
ms.assetid: 87126353-b73a-45f5-a8e7-b719efdf9d76
title: CTransInPlaceFilter. Receive, méthode (Transip. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceFilter.Receive
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5e7a1f87617b59c31139cb3d857c83d4470fd709
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106533405"
---
# <a name="ctransinplacefilterreceive-method"></a>CTransInPlaceFilter. Receive, méthode

La `Receive` méthode reçoit un exemple de support, le traite et le remet au filtre en aval.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT Receive(
   IMediaSample *pSample
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pSample* 
</dt> <dd>

Pointeur vers l’interface [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) sur l’exemple.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne une valeur **HRESULT** . Les valeurs possibles sont les suivantes :



| Code de retour                                                                                  | Description                 |
|----------------------------------------------------------------------------------------------|-----------------------------|
| <dl> <dt>**\_OK**</dt> </dl>         | Succès<br/>          |
| <dl> <dt>**E \_ inattendu**</dt> </dl> | Erreur inattendue<br/> |



 

## <a name="remarks"></a>Notes

La broche d’entrée du filtre appelle cette méthode lorsqu’elle reçoit un exemple. Le filtre appelle la méthode [**Transform**](ctransinplacefilter-transform.md) , que la classe dérivée doit implémenter. La méthode **Transform** traite les données. Si le filtre n’utilise qu’un seul Allocator, il passe directement *pSample* à la méthode **Transform** . Dans le cas contraire, il copie *pSample* et passe la copie.

Si la méthode **Transform** retourne S \_ false, la `Receive` méthode supprime l’exemple. Sur le premier exemple supprimé, le filtre envoie un événement de [**\_ \_ modification de la qualité ce**](ec-quality-change.md) au gestionnaire de graphes de filtre. Dans le cas contraire, si la méthode **Transform** retourne \_ la valeur OK, le filtre remet l’exemple de sortie. Pour ce faire, il appelle la méthode [**IMemInputPin :: Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) sur la broche d’entrée en aval.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Transip. h (include streams. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CTransInPlaceFilter, classe**](ctransinplacefilter.md)
</dt> </dl>

 

 




