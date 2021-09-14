---
description: Le \_ message DEVSPECIFIC de ligne TAPI est envoyé pour notifier l’application des événements spécifiques à l’appareil qui se produisent sur une ligne, une adresse ou un appel. La signification du message et l’interprétation des paramètres sont spécifiques à l’appareil.
ms.assetid: 6a58e77b-6ee2-4d2d-aca2-71b239f6a1dc
title: Message LINE_DEVSPECIFIC (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 91907b10c0176258648fa165bbeb922a61a402ed
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127217756"
---
# <a name="line_devspecific-message"></a>\_Message DEVSPECIFIC de ligne

Le message **\_ DEVSPECIFIC de ligne** TAPI est envoyé pour notifier l’application des événements spécifiques à l’appareil qui se produisent sur une ligne, une adresse ou un appel. La signification du message et l’interprétation des paramètres sont spécifiques à l’appareil.


```C++
            
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*hDevice* 
</dt> <dd>

Handle vers un périphérique de ligne ou un appel. Il s’agit d’un périphérique spécifique.

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

## <a name="return-value"></a>Valeur de retour

Pas de valeur de retour.

## <a name="remarks"></a>Notes

Le message de **ligne \_ DEVSPECIFIC** est utilisé par un fournisseur de services conjointement avec la fonction [**lineDevSpecific**](/windows/desktop/api/Tapi/nf-tapi-linedevspecific) . Sa signification est spécifique à l’appareil.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------|-----------------------------------------------------------------------------------|
| Version TAPI<br/> | Nécessite TAPI 2,0 ou une version ultérieure<br/>                                             |
| En-tête<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



 

 




