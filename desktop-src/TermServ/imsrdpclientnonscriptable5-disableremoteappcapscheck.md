---
title: IMsRdpClientNonScriptable5 propriété DisableRemoteAppCapsCheck
description: Spécifie si le contrôle ActiveX Bureau à distance ne doit pas vérifier les fonctionnalités RemoteApp du serveur.
ms.assetid: dcc44d4b-ece5-4f5b-a00a-f90d7a2fa11a
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété DisableRemoteAppCapsCheck
- Services Bureau à distance de la propriété DisableRemoteAppCapsCheck, interface IMsRdpClientNonScriptable5
- Services Bureau à distance de l’interface IMsRdpClientNonScriptable5, propriété DisableRemoteAppCapsCheck
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable5.DisableRemoteAppCapsCheck
- IMsRdpClientNonScriptable5.get_DisableRemoteAppCapsCheck
- IMsRdpClientNonScriptable5.put_DisableRemoteAppCapsCheck
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d4f65b0e1b56b3a1152f71aff25d4cf65a4420d1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104467022"
---
# <a name="imsrdpclientnonscriptable5disableremoteappcapscheck-property"></a>IMsRdpClientNonScriptable5 ::D propriété isableRemoteAppCapsCheck

Spécifie si le contrôle ActiveX Bureau à distance ne doit pas vérifier les fonctionnalités RemoteApp du serveur. Si cette propriété contient **la \_ valeur variant true**, le contrôle ne doit pas vérifier les fonctionnalités RemoteApp du serveur. Si cette propriété contient **la \_ valeur false**, le contrôle peut vérifier les fonctionnalités RemoteApp du serveur.

Cette propriété est en lecture/écriture.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT put_DisableRemoteAppCapsCheck(
  [in]          VARIANT_BOOL fDisableRemoteAppCapsCheck
);

HRESULT get_DisableRemoteAppCapsCheck(
  [out, retval] VARIANT_BOOL *pfDisableRemoteAppCapsCheck
);
```



## <a name="property-value"></a>Valeur de la propriété

Spécifie la nouvelle valeur de la propriété.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 7<br/>                                                                          |
| Serveur minimal pris en charge<br/> | Windows Server 2008 R2<br/>                                                             |
| Bibliothèque de types<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>        |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>        |
| IID<br/>                      | IID \_ IMsRdpClientNonScriptable5 est défini en tant que 4f6996d5-d7b1-412c-b0ff-063718566907<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IMsRdpClientNonScriptable5**](imsrdpclientnonscriptable5.md)
</dt> </dl>

 

 





