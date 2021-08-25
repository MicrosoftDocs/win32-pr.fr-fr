---
description: Le \_ message DEVSPECIFICEX de ligne TAPI est envoyé pour notifier l’application des événements spécifiques à l’appareil qui se produisent sur une ligne, une adresse ou un appel. La signification du message et l’interprétation des paramètres sont spécifiques à l’appareil.
ms.assetid: 137e91fd-a09e-430c-9d46-8e5be65f03d1
title: Message LINE_DEVSPECIFICEX (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a0b65b322b265b6bbd9717a9fc5b3c0eccf46bb3802fef7684a58d2d69645cdf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119867069"
---
# <a name="line_devspecificex-message"></a>\_Message DEVSPECIFICEX de ligne

Le message **\_ DEVSPECIFICEX de ligne** TAPI est envoyé pour notifier l’application des événements spécifiques à l’appareil qui se produisent sur une ligne, une adresse ou un appel. La signification du message et l’interprétation des paramètres sont spécifiques à l’appareil.


```C++
            
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*hDevice* 
</dt> <dd>

Handle vers un périphérique de ligne ou un appel. Ce paramètre est spécifique à l’appareil.

</dd> <dt>

*dwCallbackInstance* 
</dt> <dd>

Instance de rappel fournie lors de l’ouverture de la ligne.

</dd> <dt>

*dwParam1* 
</dt> <dd>

Spécifique à l’appareil.

</dd> <dt>

*dwParam2* 
</dt> <dd>

Spécifique à l’appareil.

</dd> <dt>

*dwParam3* 
</dt> <dd>

Spécifique à l’appareil.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Pas de valeur de retour.

## <a name="remarks"></a>Remarques

Le message de **ligne \_ DEVSPECIFICEX** est utilisé par un fournisseur de services conjointement avec la fonction [**lineDevSpecific**](/windows/desktop/api/Tapi/nf-tapi-linedevspecific) . Sa signification est spécifique à l’appareil.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------|-----------------------------------------------------------------------------------|
| Version TAPI<br/> | Nécessite TAPI 2,2<br/>                                                      |
| En-tête<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



 

 




