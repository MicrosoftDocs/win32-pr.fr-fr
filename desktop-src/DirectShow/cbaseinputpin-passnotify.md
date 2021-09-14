---
description: La méthode PassNotify transmet un message de contrôle qualité à l’objet approprié.
ms.assetid: dbc9a4b7-a522-4fbf-8e3a-af50e11c1d80
title: Méthode CBaseInputPin. PassNotify (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseInputPin.PassNotify
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 36316815ae1d9fde1a18fb36029da92ae6263f20
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127223548"
---
# <a name="cbaseinputpinpassnotify-method"></a>Méthode CBaseInputPin. PassNotify

La `PassNotify` méthode passe un message de contrôle qualité à l’objet approprié.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT PassNotify(
   Quality q
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*question* 
</dt> <dd>

Structure de [**qualité**](/windows/win32/api/strmif/ns-strmif-quality) qui contient le message de contrôle qualité.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Retourne une valeur **HRESULT** . Les valeurs possibles sont les suivantes :



| Code de retour                                                                                       | Description                                                |
|---------------------------------------------------------------------------------------------------|------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>              | Réussite.<br/>                                        |
| <dl> <dt>**VFW \_ E \_ \_ introuvable**</dt> </dl> | Impossible de trouver un objet pour accepter le message.<br/> |



 

## <a name="remarks"></a>Notes

Appelez cette méthode si le filtre ne gère pas les messages de contrôle de qualité. Cette méthode transmet le message à l’un des objets suivants, par ordre de préférence :

-   Gestionnaire de contrôle de qualité externe, si la méthode [**IQualityControl :: SetSink**](/windows/desktop/api/Strmif/nf-strmif-iqualitycontrol-setsink) a été appelée.
-   Broche de sortie en amont.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Amfilter. h (inclure Flux. h)</dt> </dl>                                                                                  |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseInputPin, classe**](cbaseinputpin.md)
</dt> <dt>

[Gestion du contrôle de la qualité](quality-control-management.md)
</dt> </dl>

 

 




