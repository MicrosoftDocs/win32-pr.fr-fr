---
title: Méthode ActiveBasicDevice GetEffectiveBandwidth (PlayToDevice. h)
description: Obtient la bande passante effective actuelle pour l’appareil.
ms.assetid: 88CE03AB-6F87-4E43-B673-2C693D351F10
keywords:
- API de diffusion multimédia en continu de méthode GetEffectiveBandwidth
- API de diffusion multimédia en continu de méthode GetEffectiveBandwidth, interface ActiveBasicDevice
- API de diffusion multimédia en continu de l’interface ActiveBasicDevice, méthode GetEffectiveBandwidth
topic_type:
- apiref
api_name:
- ActiveBasicDevice.GetEffectiveBandwidth
api_location:
- playtodevice.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7ac51318997e80c043e36dc87b052a5e21bf9933f93e34f2e5071fb20d4bb75b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118236781"
---
# <a name="activebasicdevicegeteffectivebandwidth-method"></a>ActiveBasicDevice :: GetEffectiveBandwidth, méthode

Obtient la bande passante effective actuelle pour l’appareil.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetEffectiveBandwidth(
  [in, retval] boolean transmitSpeed,
  [out]        ULONG64 *currentSpeed
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*transmitSpeed* \[ dans, retval\]
</dt> <dd>

Spécifie si la vitesse de transmission est récupérée ou si la vitesse de réception est récupérée.

**true** pour récupérer la vitesse de transmission. **false** pour récupérer la vitesse de réception.

</dd> <dt>

*currentSpeed* \[ à\]
</dt> <dd>

Reçoit la bande passante effective actuelle.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Si cette méthode est réussie, elle retourne la valeur **\_ OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8.1 les \[ applications de bureau uniquement\]<br/>                                                |
| Serveur minimal pris en charge<br/> | Windows Server 2012 \[Applications de bureau R2 uniquement\]<br/>                                     |
| En-tête<br/>                   | <dl> <dt>PlayToDevice. h</dt> </dl>   |
| MIDL<br/>                      | <dl> <dt>PlayToDevice. idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Playtodevice.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**ActiveBasicDevice**](/previous-versions/windows/desktop/legacy/dn385755(v=vs.85))
</dt> </dl>

 

