---
description: 'La méthode Apply applique les valeurs de page de propriétés actuelles à l’objet associé à la page de propriétés. Cette méthode implémente la méthode IPropertyPage :: apply.'
ms.assetid: 9fe759d1-2b46-4489-b7b8-b5a35330091d
title: CBasePropertyPage. Apply, méthode (Cprop. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePropertyPage.Apply
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9350aa7aaa4e2bfdcb72385d26b09b9d7a9bdf33deb05e273b0663485da1a5bd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117823230"
---
# <a name="cbasepropertypageapply-method"></a>CBasePropertyPage. Apply, méthode

La `Apply` méthode applique les valeurs de page de propriétés actuelles à l’objet associé à la page de propriétés. Cette méthode implémente la méthode **IPropertyPage :: apply** .

## <a name="syntax"></a>Syntaxe


```C++
HRESULT Apply();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Retourne une valeur **HRESULT** . Les valeurs possibles sont les suivantes.



| Code de retour                                                                                  | Description                    |
|----------------------------------------------------------------------------------------------|--------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>         | Réussite.<br/>            |
| <dl> <dt>**E \_ inattendu**</dt> </dl> | Erreur inattendue.<br/> |



 

## <a name="remarks"></a>Remarques

Si l’indicateur [**CBasePropertyPage :: m \_ bDirty**](cbasepropertypage-m-bdirty.md) a la **valeur true**, cette méthode appelle la méthode [**CBasePropertyPage :: OnApplyChanges**](cbasepropertypage-onapplychanges.md) . Remplacez **OnApplyChanges** pour appliquer les modifications à l’objet.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Cprop. h (inclure Flux. h)</dt> </dl>                                                                                     |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBasePropertyPage, classe**](cbasepropertypage.md)
</dt> </dl>

 

 




