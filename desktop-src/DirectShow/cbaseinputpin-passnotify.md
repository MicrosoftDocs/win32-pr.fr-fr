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
ms.openlocfilehash: 760ec066a9d4876dd6ef754783c41ae12765db10c1595d08aef0a73258de087f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119016997"
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

## <a name="return-value"></a>Valeur retournée

Retourne une valeur **HRESULT** . Les valeurs possibles sont les suivantes :



| Code de retour                                                                                       | Description                                                |
|---------------------------------------------------------------------------------------------------|------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>              | Réussite.<br/>                                        |
| <dl> <dt>**VFW \_ E \_ \_ introuvable**</dt> </dl> | Impossible de trouver un objet pour accepter le message.<br/> |



 

## <a name="remarks"></a>Remarques

Appelez cette méthode si le filtre ne gère pas les messages de contrôle de qualité. Cette méthode transmet le message à l’un des objets suivants, par ordre de préférence :

-   Gestionnaire de contrôle de qualité externe, si la méthode [**IQualityControl :: SetSink**](/windows/desktop/api/Strmif/nf-strmif-iqualitycontrol-setsink) a été appelée.
-   Broche de sortie en amont.

## <a name="requirements"></a>Configuration requise



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

 

 




