---
description: La méthode GetMediaPositionInterface récupère les pointeurs d’interface IMediaPosition et IMediaSeeking du filtre.
ms.assetid: aeca4484-cecc-4d07-aa77-56221ff75699
title: Méthode CBaseRenderer. GetMediaPositionInterface (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.GetMediaPositionInterface
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 12e15b297f78b3386ae9ad31e749858bad14b87e59e938ac02a3cf3a9ca002a9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119872329"
---
# <a name="cbaserenderergetmediapositioninterface-method"></a>Méthode CBaseRenderer. GetMediaPositionInterface

La `GetMediaPositionInterface` méthode récupère les pointeurs d’interface [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition) et [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) du filtre.

## <a name="syntax"></a>Syntaxe


```C++
virtual HRESULT GetMediaPositionInterface(
   REFIID riid,
   void   **ppv
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*riid* 
</dt> <dd>

Identificateur de référence de l’interface.

</dd> <dt>

*ppv* 
</dt> <dd>

Adresse d’une variable qui reçoit le pointeur d’interface.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne une valeur **HRESULT** . Les valeurs possibles sont les suivantes :



| Code de retour                                                                                   | Description                         |
|-----------------------------------------------------------------------------------------------|-------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>          | Réussite.<br/>                 |
| <dl> <dt>**\_OUTOFMEMORY E**</dt> </dl> | Mémoire insuffisante.<br/>     |
| <dl> <dt>**E \_ NOinterface**</dt> </dl> | Interface non prise en charge.<br/> |



 

## <a name="remarks"></a>Remarques

Le filtre délègue toutes les commandes de recherche à un objet [**CRendererPosPassThru**](crendererpospassthru.md) , qui les transmet en amont. Cette méthode crée l’objet **CRendererPosPassThru** , s’il n’existe pas encore, et le interroge pour l’interface demandée.

La variable membre [**CBaseRenderer :: m \_ pPosition**](cbaserenderer-m-pposition.md) stocke un pointeur vers l’objet **CRendererPosPassThru** .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Renbase. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseRenderer, classe**](cbaserenderer.md)
</dt> </dl>

 

 




