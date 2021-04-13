---
title: MpHandleClose, fonction (MpClient. h)
description: Ferme le handle retourné par MpManagerOpen, MpScanStart, MpThreatOpen ou MpUpdateStart.
ms.assetid: 335776E2-7598-4DC1-92AB-B49B35222EF6
keywords:
- Fonctionnalités d’environnement Windows hérités de la fonction MpHandleClose
topic_type:
- apiref
api_name:
- MpHandleClose
api_location:
- MpClient.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 43c937548c8e1d3b98aa2e3d10d7577f8c69c1c5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104509226"
---
# <a name="mphandleclose-function"></a>MpHandleClose fonction)

Ferme le handle retourné par [**MpManagerOpen**](mpmanageropen.md), [**MpScanStart**](mpscanstart.md), [**MpThreatOpen**](mpthreatopen.md)ou [**MpUpdateStart**](mpupdatestart.md).

## <a name="syntax"></a>Syntaxe


```C++
HRESULT WINAPI MpHandleClose(
  _In_ MPHANDLE hMpHandle
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*hMpHandle* \[ dans\]
</dt> <dd>

Type : **MPHANDLE**

Handle à fermer.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **HRESULT**

Si la fonction s’exécute correctement, la valeur de retour est **\_ OK**.

Si la fonction échoue, la valeur de retour est un code **HRESULT** en échec. L’appelant peut utiliser la fonction [**MpErrorMessageFormat**](mperrormessageformat.md) pour obtenir une description générique du message d’erreur.

L’erreur spécifique suivante peut être retournée par la fonction :

| Code de retour             | Description                      |
|-------------------------|----------------------------------|
| E \_ remporter un \_ \_ descripteur non valide | Le handle spécifié n’est pas valide. |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 8 uniquement\]<br/>                                              |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2012 \[ uniquement\]<br/>                                    |
| En-tête<br/>                   | <dl> <dt>MpClient. h</dt> </dl>   |
| DLL<br/>                      | <dl> <dt>MpClient.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**MpErrorMessageFormat**](mperrormessageformat.md)
</dt> <dt>

[**MpManagerOpen**](mpmanageropen.md)
</dt> <dt>

[**MpScanStart**](mpscanstart.md)
</dt> <dt>

[**MpThreatOpen**](mpthreatopen.md)
</dt> </dl>

 

 





