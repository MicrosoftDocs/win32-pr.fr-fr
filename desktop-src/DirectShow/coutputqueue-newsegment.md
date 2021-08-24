---
description: La méthode NewSegment fournit un nouveau segment à la broche d’entrée.
ms.assetid: 53189729-9f47-425e-9df6-faea01dd4482
title: Méthode COutputQueue. NewSegment (Outputq. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COutputQueue.NewSegment
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4057cafa3962c85fbca9342debbf7bb0e92355fc083e693889df298e53509259
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119768139"
---
# <a name="coutputqueuenewsegment-method"></a>Méthode COutputQueue. NewSegment

La `NewSegment` méthode remet un nouveau segment à la broche d’entrée.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT NewSegment(
   REFERENCE_TIME tStart,
   REFERENCE_TIME tStop,
   double         dRate
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*tStart* 
</dt> <dd>

Position du média de départ du segment, en unités de 100 nanosecondes.

</dd> <dt>

*tStop* 
</dt> <dd>

Position du média de fin du segment, en unités de 100 nanosecondes.

</dd> <dt>

*dRate* 
</dt> <dd>

Taux auquel ce segment doit être traité, sous la forme d’un pourcentage du taux d’origine.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne une valeur **HRESULT** .

## <a name="remarks"></a>Remarques

Si l’objet utilise un thread, il met en file d’attente les éléments suivants, dans l’ordre :

-   NOUVEAU \_ message de contrôle de segment.
-   Données de segment.

Le nouveau \_ message de segment avertit le thread que l’élément suivant de la file d’attente contiendra les données de segment. Les données de segment sont regroupées dans une structure, déclarée comme suit :


```C++
struct NewSegmentPacket {
    REFERENCE_TIME tStart;
    REFERENCE_TIME tStop;
    double dRate;
}; 
```



Le thread appelle la méthode [**IPIN :: NewSegment**](/windows/desktop/api/Strmif/nf-strmif-ipin-newsegment) sur la broche d’entrée, à l’aide des données fournies dans la structure.

Si l’objet n’utilise pas de thread, il appelle la méthode [**COutputQueue :: SendAnyway**](coutputqueue-sendanyway.md) pour remettre tous les échantillons en attente. Ensuite, il appelle **IPIN :: NewSegment** sur la broche d’entrée.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Outputq. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**COutputQueue, classe**](coutputqueue.md)
</dt> </dl>

 

 




