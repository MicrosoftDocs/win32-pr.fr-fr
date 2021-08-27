---
title: MpScanControl, fonction (MpClient. h)
description: Permet le contrôle d’une analyse qui a été initialisée de façon asynchrone par le biais de MpScanStart.
ms.assetid: 00855686-8C46-4B58-829C-AEAB53888704
keywords:
- fonctionnalités d’environnement Windows hérités de la fonction MpScanControl
topic_type:
- apiref
api_name:
- MpScanControl
api_location:
- MpClient.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 893fe1d01f9004c9dc2933a5bbb23c4b13fb8933a6121c41810c6e447e5eebac
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120114549"
---
# <a name="mpscancontrol-function"></a>MpScanControl fonction)

Permet le contrôle d’une analyse qui a été initialisée de façon asynchrone par le biais de [**MpScanStart**](mpscanstart.md).

## <a name="syntax"></a>Syntaxe


```C++
HRESULT WINAPI MpScanControl(
  _In_ MPHANDLE  hScanHandle,
  _In_ MPCONTROL ScanControl
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*hScanHandle* \[ dans\]
</dt> <dd>

Type : **MPHANDLE**

Handle vers une opération d’analyse asynchrone. Ce descripteur est retourné par la fonction [**MpScanStart**](mpscanstart.md) . Ce paramètre peut également être défini sur le descripteur de l’interface du gestionnaire de protection contre les programmes malveillants renvoyé par la fonction [**MpManagerOpen**](mpmanageropen.md) pour contrôler une analyse initiée par le système, auquel cas l’appelant doit avoir des privilèges d’administrateur.

</dd> <dt>

*ScanControl* \[ dans\]
</dt> <dd>

Type : **fichier mpcontrol**

Spécifie une option de contrôle de l’analyse. Ce paramètre doit être l’une des options de contrôle suivantes :



| Valeur                                                                                                                                                                  | Signification                                      |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <span id="MPCONTROL_ABORT"></span><span id="mpcontrol_abort"></span><dl> <dt>**\_abandon fichier mpcontrol**</dt> </dl>    | Abandon de l’opération d’analyse.<br/>         |
| <span id="MPCONTROL_PAUSE"></span><span id="mpcontrol_pause"></span><dl> <dt>**\_Pause fichier mpcontrol**</dt> </dl>    | Interrompez l’opération d’analyse.<br/>         |
| <span id="MPCONTROL_RESUME"></span><span id="mpcontrol_resume"></span><dl> <dt>**FICHIER MPCONTROL \_ Resume**</dt> </dl> | Reprise de l’opération d’analyse en pause.<br/> |



 

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

[**MpManagerOpen**](mpmanageropen.md)
</dt> <dt>

[**MpScanStart**](mpscanstart.md)
</dt> </dl>

 

 





