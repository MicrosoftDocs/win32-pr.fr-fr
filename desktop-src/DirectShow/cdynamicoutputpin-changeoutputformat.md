---
description: La méthode ChangeOutputFormat modifie dynamiquement le type de média pour la connexion et fournit de nouvelles informations de segment.
ms.assetid: d1204ca0-a489-48a0-8fe5-3ade04f51c93
title: Méthode CDynamicOutputPin. ChangeOutputFormat (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDynamicOutputPin.ChangeOutputFormat
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 57421b2fd9624d9798037151a5656343e386a497
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526884"
---
# <a name="cdynamicoutputpinchangeoutputformat-method"></a>Méthode CDynamicOutputPin. ChangeOutputFormat

La `ChangeOutputFormat` méthode modifie dynamiquement le type de média pour la connexion et fournit de nouvelles informations de segment. La modification peut se produire pendant l’exécution du graphique de filtre. Une fois cette méthode appelée, les exemples avec l’ancien type de média ne peuvent pas être remis. L’appelant doit s’assurer qu’aucun ancien échantillon n’est en attente.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT ChangeOutputFormat(
   const AM_MEDIA_TYPE  *pmt,
         REFERENCE_TIME tSegmentStart,
         REFERENCE_TIME tSegmentStop,
         double         dSegmentRate
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*crédit* 
</dt> <dd>

Pointeur vers une structure de [**\_ \_ type de média am**](/windows/win32/api/strmif/ns-strmif-am_media_type) qui spécifie le type de média.

</dd> <dt>

*tSegmentStart* 
</dt> <dd>

Heure de début du segment.

</dd> <dt>

*tSegmentStop* 
</dt> <dd>

Heure d’arrêt du segment.

</dd> <dt>

*dSegmentRate* 
</dt> <dd>

Taux de segment.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne une valeur **HRESULT** . Les valeurs possibles sont les suivantes :



| Code de retour                                                                                           | Description                                                                                                                              |
|-------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>                  | Opération réussie.<br/>                                                                                                                      |
| <dl> <dt>**E \_ échec**</dt> </dl>                | Échec. Le filtre propriétaire n’a peut-être pas appelé [**CDynamicOutputPin :: SetConfigInfo**](cdynamicoutputpin-setconfiginfo.md).<br/> |
| <dl> <dt>**VFW \_ E \_ non \_ connecté**</dt> </dl> | Le pin n’est pas connecté.<br/>                                                                                                     |



 

## <a name="remarks"></a>Notes

Cette méthode modifie le type de format pendant que le filtre est en cours d’exécution. Si le code pin en aval accepte le nouveau format, aucune reconnexion n’est nécessaire. Dans le cas contraire, la méthode tente de reconnecter le code confidentiel. Si la méthode modifie correctement le format, il remet les nouvelles informations sur le segment. Cette méthode appelle la méthode [**CDynamicOutputPin :: ChangeMediaType**](cdynamicoutputpin-changemediatype.md) pour effectuer la modification de format.

Vous devez appeler la méthode [**CDynamicOutputPin :: StartUsingOutputPin**](cdynamicoutputpin-startusingoutputpin.md) avant d’appeler cette méthode.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Amfilter. h (include streams. h)</dt> </dl>                                                                                  |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CDynamicOutputPin, classe**](cdynamicoutputpin.md)
</dt> </dl>

 

 




