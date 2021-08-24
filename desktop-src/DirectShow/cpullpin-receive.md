---
description: La méthode Receive est appelée lorsque l’objet reçoit un échantillon de support à partir de la broche de sortie. La classe dérivée doit implémenter cette méthode.
ms.assetid: ef45388b-b038-4838-b76b-dbbdc5388495
title: CPullPin. Receive, méthode (Pullpin. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPullPin.Receive
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: fdf38c9c873dd8d95ae60341fc2f7dba02abff1f8b34fd89d0d1f720dc59b55f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119831539"
---
# <a name="cpullpinreceive-method"></a>CPullPin. Receive, méthode

La `Receive` méthode est appelée lorsque l’objet reçoit un échantillon de média à partir de la broche de sortie. La classe dérivée doit implémenter cette méthode.

## <a name="syntax"></a>Syntaxe


```C++
virtual HRESULT Receive(
   IMediaSample *pSample
) = 0;
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pSample* 
</dt> <dd>

Pointeur vers l’interface [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) de l’exemple de média.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne une valeur **HRESULT** . Le retour d’une valeur autre que S \_ OK arrête le thread d’extraction de données.

## <a name="remarks"></a>Remarques

Cette méthode est appelée chaque fois qu’un nouvel exemple arrive à partir de la broche de sortie. Écrivez cette méthode de la même manière que la méthode [**IMemInputPin :: Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) .

Les horodatages de l’échantillon spécifient les décalages d’octets par rapport à la position de début d’origine qui a été spécifiée dans la méthode [**CPullPin :: Seek**](cpullpin-seek.md) .

La position de début est arrondie à la limite d’alignement la plus proche et la position d’arrêt est arrondie à la limite d’alignement la plus proche. En outre, si la position d’arrêt dépasse la durée totale, la durée est utilisée à la place.

Tous les horodatages sont fournis sous la forme d’un décalage d’octet multiplié par 10 millions, défini comme unités constantes. Par conséquent, une seconde est un octet. Pour rechercher les décalages d’octets réels, appelez [**IMediaSample :: getTime**](/windows/desktop/api/Strmif/nf-strmif-imediasample-gettime) et divisez les résultats par unités.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Pullpin. h</dt> </dl>                                                                                                       |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CPullPin, classe**](cpullpin.md)
</dt> </dl>

 

 




