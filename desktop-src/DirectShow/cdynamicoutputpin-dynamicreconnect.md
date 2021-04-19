---
description: La méthode DynamicReconnect effectue une reconnexion dynamique avec un nouveau type de média. La reconnexion peut se produire pendant l’exécution du graphique de filtre.
ms.assetid: 1fe9f1cc-1f5d-407e-8c80-fea6cd1cb16f
title: Méthode CDynamicOutputPin. DynamicReconnect (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDynamicOutputPin.DynamicReconnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: dd595748380a35f74e591283ed3d03273c683e97
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106538751"
---
# <a name="cdynamicoutputpindynamicreconnect-method"></a>Méthode CDynamicOutputPin. DynamicReconnect

La `DynamicReconnect` méthode effectue une reconnexion dynamique avec un nouveau type de média. La reconnexion peut se produire pendant l’exécution du graphique de filtre.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT DynamicReconnect(
   const CMediaType *pmt
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*crédit* 
</dt> <dd>

Pointeur vers une structure de [**\_ \_ type de média am**](/windows/win32/api/strmif/ns-strmif-am_media_type) qui spécifie le type de média.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne une valeur **HRESULT** . Les valeurs possibles sont les suivantes :



| Code de retour                                                                            | Description                                                                                                                                         |
|----------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>   | Opération réussie.<br/>                                                                                                                                 |
| <dl> <dt>**E \_ échec**</dt> </dl> | Échec. Le filtre propriétaire n’a peut-être pas appelé la méthode [**CDynamicOutputPin :: SetConfigInfo**](cdynamicoutputpin-setconfiginfo.md) .<br/> |



 

## <a name="remarks"></a>Notes

Cette méthode doit être appelée à partir du thread qui remet les données au code confidentiel. Une fois cette méthode appelée, les exemples avec l’ancien type de média ne peuvent pas être remis. L’appelant doit s’assurer qu’aucun ancien échantillon n’est en attente.

Appelez [**CDynamicOutputPin :: StartUsingOutputPin**](cdynamicoutputpin-startusingoutputpin.md) avant d’appeler cette méthode.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Amfilter. h (include streams. h)</dt> </dl>                                                                                  |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CDynamicOutputPin, classe**](cdynamicoutputpin.md)
</dt> </dl>

 

 




