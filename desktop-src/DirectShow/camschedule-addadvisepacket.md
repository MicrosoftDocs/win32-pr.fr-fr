---
description: La méthode AddAdvisePacket ajoute une demande de notification à la liste des demandes en attente.
ms.assetid: 138d8404-7d28-47cc-91b4-4733a113ac7a
title: Méthode CAMSchedule. AddAdvisePacket (Dsschedule. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMSchedule.AddAdvisePacket
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5dd9586b09586c12f1a30f45b512336831372295
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106525508"
---
# <a name="camscheduleaddadvisepacket-method"></a>Méthode CAMSchedule. AddAdvisePacket

La `AddAdvisePacket` méthode ajoute une demande de notification à la liste des demandes en attente.

## <a name="syntax"></a>Syntaxe


```C++
DWORD_PTR AddAdvisePacket(
  [ref] const REFERENCE_TIME &time1,
  [ref] const REFERENCE_TIME &time2,
              HANDLE         hNotify,
              BOOL           bPeriodic
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*time1* \[ Réf\]
</dt> <dd>

Heure demandée pour la notification.

</dd> <dt>

*TIME2 ?* \[ Réf\]
</dt> <dd>

Pour les demandes de notification périodiques, délai entre les notifications. Ce paramètre est ignoré si *bPeriodic* a la **valeur false**.

</dd> <dt>

*hNotify* 
</dt> <dd>

Handle vers un sémaphore si *bPeriodic* a la **valeur true** ou handle vers un événement si *bPeriodic* a la **valeur false**.

</dd> <dt>

*bPeriodic* 
</dt> <dd>

Valeur booléenne qui spécifie s’il faut ajouter une notification périodique ou une notification d’une seule capture. Si la **valeur est true**, la notification est périodique ; le paramètre *TIME2 ?* spécifie le délai entre les notifications. Si la **valeur est false**, la notification se produit une seule fois.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne un identificateur pour la demande de notification (le « cookie »). Si la méthode échoue, la valeur de retour est zéro.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Dsschedule. h (include streams. h)</dt> </dl>                                                                                |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CAMSchedule, classe**](camschedule.md)
</dt> </dl>

 

 




