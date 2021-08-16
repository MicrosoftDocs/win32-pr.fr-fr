---
description: L’interface TAPI envoie le \_ message DEVSPECIFIC de téléphone à une application pour notifier l’application des événements spécifiques à l’appareil qui se produisent au téléphone. La signification du message et l’interprétation des paramètres sont définies par l’implémentation.
ms.assetid: e3e803dd-b041-48b7-9acf-a89989370204
title: Message PHONE_DEVSPECIFIC (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 578ba0960963f85ff597d9a6bc87ff3369a6c837ed58367bd82d62a13341e988
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120072899"
---
# <a name="phone_devspecific-message"></a>\_Message DEVSPECIFIC téléphone

L’interface TAPI envoie le message **\_ DEVSPECIFIC de téléphone** à une application pour notifier l’application des événements spécifiques à l’appareil qui se produisent au téléphone. La signification du message et l’interprétation des paramètres sont définies par l’implémentation.


```C++
            
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*hPhone* 
</dt> <dd>

Handle vers l’appareil mobile.

</dd> <dt>

*dwCallbackInstance* 
</dt> <dd>

Instance de rappel de l’application fournie lors de l’ouverture du périphérique téléphonique.

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

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------|-----------------------------------------------------------------------------------|
| Version TAPI<br/> | Nécessite TAPI 2,0 ou une version ultérieure<br/>                                             |
| En-tête<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



 

 




