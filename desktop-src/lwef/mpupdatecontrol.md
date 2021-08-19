---
title: MpUpdateControl, fonction (MpClient. h)
description: Autorise le contrôle d’une opération de mise à jour de signature qui a été lancée de manière asynchrone via MpUpdateStart.
ms.assetid: 2780E472-6E8D-4839-88EE-46E3448C6BF5
keywords:
- fonctionnalités d’environnement Windows hérités de la fonction MpUpdateControl
topic_type:
- apiref
api_name:
- MpUpdateControl
api_location:
- MpClient.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 69926f26b470ba41226883bdb32fab13c5d776858595c256fe70e7f95e898c04
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118476271"
---
# <a name="mpupdatecontrol-function"></a>MpUpdateControl fonction)

Autorise le contrôle d’une opération de mise à jour de signature qui a été lancée de manière asynchrone via [**MpUpdateStart**](mpupdatestart.md). L’appel de cette fonction requiert des privilèges d’administrateur, car elle permet l’annulation d’une mise à jour de signature à l’ensemble du système.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT WINAPI MpUpdateControl(
  _In_ MPHANDLE  hUpdateHandle,
  _In_ MPCONTROL UpdateControl
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*hUpdateHandle* \[ dans\]
</dt> <dd>

Type : **MPHANDLE**

Handle vers une opération de mise à jour de signature asynchrone. Ce descripteur est retourné par la fonction [**MpScanStart**](mpscanstart.md) .

</dd> <dt>

*UpdateControl* \[ dans\]
</dt> <dd>

Type : **fichier mpcontrol**

Spécifie l’option de contrôle de mise à jour de signature. Il doit s’agir de la valeur suivante :



| Valeur                                                                                                                                                               | Signification                                          |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------|
| <span id="MPCONTROL_ABORT"></span><span id="mpcontrol_abort"></span><dl> <dt>**\_abandon fichier mpcontrol**</dt> </dl> | Abandonner l’opération de mise à jour de signature.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **HRESULT**

Si la fonction s’exécute correctement, la valeur de retour est **\_ OK**.

Si la fonction échoue, la valeur de retour est un code **HRESULT** en échec. L’appelant peut utiliser la fonction [**MpErrorMessageFormat**](mperrormessageformat.md) pour obtenir une description générique du message d’erreur.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8 \[ applications de bureau uniquement\]<br/>                                              |
| Serveur minimal pris en charge<br/> | Windows Server 2012 \[ applications de bureau uniquement\]<br/>                                    |
| En-tête<br/>                   | <dl> <dt>MpClient. h</dt> </dl>   |
| DLL<br/>                      | <dl> <dt>MpClient.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**MpErrorMessageFormat**](mperrormessageformat.md)
</dt> <dt>

[**MpScanStart**](mpscanstart.md)
</dt> </dl>

 

 





