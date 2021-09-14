---
title: Méthode IWMDRMDevice GetSecureClock
description: La méthode GetSecureClock récupère l’horloge sécurisée, de sorte que les licences basées sur le temps peuvent être appliquées.
ms.assetid: 6de9b7ce-9c2a-44e5-9de7-40cfbaf4d92c
keywords:
- Méthode GetSecureClock Gestionnaire de périphériques Windows Media
- Méthode GetSecureClock Gestionnaire de périphériques Windows Media, interface IWMDRMDevice
- Interface IWMDRMDevice Windows Media Gestionnaire de périphériques, méthode GetSecureClock
topic_type:
- apiref
api_name:
- IWMDRMDevice.GetSecureClock
api_location:
- mssachlp.lib
- mssachlp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aaa92c3bc2ee82facf2f2e1043e71467a0c55bd8
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127008508"
---
# <a name="iwmdrmdevicegetsecureclock-method"></a>IWMDRMDevice :: GetSecureClock, méthode

La méthode **GetSecureClock** récupère l’horloge sécurisée, de sorte que les licences basées sur le temps peuvent être appliquées.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetSecureClock(
  [out] BYTE  **ppbSecureClock,
  [out] DWORD *pcbSecureClock,
  [out] DWORD *pdwFlags
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*ppbSecureClock* \[ à\]
</dt> <dd>

Horloge sécurisée récupérée.

</dd> <dt>

*pcbSecureClock* \[ à\]
</dt> <dd>

Taille de l’horloge sécurisée, en octets.

</dd> <dt>

*pdwFlags* \[ à\]
</dt> <dd>

Indicateurs d’état de l’appareil. Cette valeur doit être l’un des indicateurs suivants.



| Indicateur                     | Description                            |
|--------------------------|----------------------------------------|
| \_ISWMDRM d’appareil WMDRM \_   | l’appareil prend en charge Windows DRM Media. |
| \_NEEDCLOCK d’appareil WMDRM \_ | L’appareil a besoin d’une horloge.                |
| \_appareil WMDRM \_ révoqué   | L’appareil a été révoqué.           |



 

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Cette méthode retourne un code **HRESULT**. Les valeurs possibles sont notamment celles figurant dans le tableau suivant.



| Code de retour                                                                          | Description                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**\_OK**</dt> </dl> | S_OK<br/> |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|-----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>WMDDRMSP. idl</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>Mssachlp. lib</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**GetSecureClockChallenge**](iwmdrmdevice-getsecureclockchallenge.md)
</dt> <dt>

[**Interface IWMDRMDevice**](iwmdrmdevice.md)
</dt> <dt>

[**SetSecureClockResponse**](iwmdrmdevice-setsecureclockresponse.md)
</dt> </dl>

 

 





