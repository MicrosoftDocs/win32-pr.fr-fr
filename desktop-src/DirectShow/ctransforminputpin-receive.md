---
description: 'CTransformInputPin. Receive, méthode : la méthode Receive reçoit l’exemple de support suivant dans le flux. Cette méthode implémente la méthode IMemInputPin :: Receive.'
ms.assetid: 65e4f8f5-2aa2-435b-84b4-e65af3f51afc
title: CTransformInputPin. Receive, méthode (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformInputPin.Receive
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2a6a3c5dd4c9f11d45e1b719498d515a536e5ef8
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127224796"
---
# <a name="ctransforminputpinreceive-method"></a>CTransformInputPin. Receive, méthode

La `Receive` méthode reçoit l’échantillon de média suivant dans le flux. Cette méthode implémente la méthode [**IMemInputPin :: Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) .

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

Pointeur vers l’interface [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) de l’exemple.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Retourne une valeur **HRESULT** . Les valeurs possibles sont les suivantes :



| Code de retour                                                                             | Description                                                |
|-----------------------------------------------------------------------------------------|------------------------------------------------------------|
| <dl> <dt>**S \_ false**</dt> </dl> | Le code PIN est en cours de vidage ; l’exemple a été rejeté.<br/> |
| <dl> <dt>**\_OK**</dt> </dl>    | Réussite.<br/>                                        |



 

## <a name="remarks"></a>Notes

Cette méthode appelle la méthode [**CBaseInputPin :: Receive**](cbaseinputpin-receive.md) du pin, qui vérifie l’état de diffusion en continu du pin et vérifie les modifications de format dans le type de média. Elle appelle ensuite la méthode [**CTransformFilter :: Receive**](ctransformfilter-receive.md) du filtre, qui traite l’exemple et le remet en aval.

Si le filtre doit accéder à l’exemple après le retour de cette méthode, il doit contenir un décompte de références en appelant la méthode **IUnknown :: AddRef** sur l’exemple. Par exemple, certains filtres de décodeur ont besoin de l’exemple actuel pour décoder l’exemple suivant.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Transfrm. h (inclure Flux. h)</dt> </dl>                                                                                  |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



 

 




