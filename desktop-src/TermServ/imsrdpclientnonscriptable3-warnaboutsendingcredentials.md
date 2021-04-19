---
title: IMsRdpClientNonScriptable3 propriété WarnAboutSendingCredentials
description: Spécifie ou récupère une valeur indiquant si la boîte de dialogue d’avertissement de sécurité doit inclure un avertissement concernant l’envoi d’informations d’identification au serveur distant avant le démarrage d’une session.
ms.assetid: b97baef5-4a51-4e5c-bd53-10cff175533c
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété WarnAboutSendingCredentials
- Services Bureau à distance de la propriété WarnAboutSendingCredentials, interface IMsRdpClientNonScriptable3
- Services Bureau à distance de l’interface IMsRdpClientNonScriptable3, propriété WarnAboutSendingCredentials
- Services Bureau à distance de la propriété WarnAboutSendingCredentials, interface IMsRdpClientNonScriptable4
- Services Bureau à distance de l’interface IMsRdpClientNonScriptable4, propriété WarnAboutSendingCredentials
- Services Bureau à distance de la propriété WarnAboutSendingCredentials, interface IMsRdpClientNonScriptable5
- Services Bureau à distance de l’interface IMsRdpClientNonScriptable5, propriété WarnAboutSendingCredentials
- Services Bureau à distance de la propriété WarnAboutSendingCredentials, objet MsRdpClient5
- Services Bureau à distance objet MsRdpClient5, propriété WarnAboutSendingCredentials
- Services Bureau à distance de la propriété WarnAboutSendingCredentials, objet MsRdpClient6
- Services Bureau à distance objet MsRdpClient6, propriété WarnAboutSendingCredentials
- Services Bureau à distance de la propriété WarnAboutSendingCredentials, objet MsRdpClient7
- Services Bureau à distance objet MsRdpClient7, propriété WarnAboutSendingCredentials
- Services Bureau à distance de la propriété WarnAboutSendingCredentials, objet MsRdpClient8
- Services Bureau à distance objet MsRdpClient8, propriété WarnAboutSendingCredentials
- Services Bureau à distance de la propriété WarnAboutSendingCredentials, objet MsRdpClient9
- Services Bureau à distance objet MsRdpClient9, propriété WarnAboutSendingCredentials
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable3.WarnAboutSendingCredentials
- IMsRdpClientNonScriptable3.get_WarnAboutSendingCredentials
- IMsRdpClientNonScriptable3.put_WarnAboutSendingCredentials
- IMsRdpClientNonScriptable4.WarnAboutSendingCredentials
- IMsRdpClientNonScriptable4.get_WarnAboutSendingCredentials
- IMsRdpClientNonScriptable4.put_WarnAboutSendingCredentials
- IMsRdpClientNonScriptable5.WarnAboutSendingCredentials
- IMsRdpClientNonScriptable5.get_WarnAboutSendingCredentials
- IMsRdpClientNonScriptable5.put_WarnAboutSendingCredentials
- MsRdpClient5.WarnAboutSendingCredentials
- MsRdpClient6.WarnAboutSendingCredentials
- MsRdpClient7.WarnAboutSendingCredentials
- MsRdpClient8.WarnAboutSendingCredentials
- MsRdpClient9.WarnAboutSendingCredentials
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 29d9d2fcfe158f5a0bb6812002bfcc160f1c9009
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106527566"
---
# <a name="imsrdpclientnonscriptable3warnaboutsendingcredentials-property"></a>IMsRdpClientNonScriptable3 :: WarnAboutSendingCredentials, propriété

Spécifie ou récupère une valeur indiquant si la boîte de dialogue d’avertissement de sécurité doit inclure un avertissement concernant l’envoi d’informations d’identification au serveur distant avant le démarrage d’une session.

Cette propriété est en lecture/écriture.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT put_WarnAboutSendingCredentials(
  [in]  VARIANT_BOOL fWarn
);

HRESULT get_WarnAboutSendingCredentials(
  [out] VARIANT_BOOL *pfWarn
);
```



## <a name="property-value"></a>Valeur de la propriété

Spécifie si la boîte de dialogue d’avertissement de sécurité doit inclure un avertissement concernant l’envoi d’informations d’identification au serveur distant avant le démarrage d’une session.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                                      |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                                |
| Bibliothèque de types<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>        |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>        |
| IID<br/>                      | IID \_ IMsRdpClientNonScriptable3 est défini en tant que b3378d90-0728-45c7-8ed7-b6159fb92219<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IMsRdpClientNonScriptable4**](imsrdpclientnonscriptable4.md)
</dt> <dt>

[**IMsRdpClientNonScriptable5**](imsrdpclientnonscriptable5.md)
</dt> <dt>

[**IMsRdpClientNonScriptable3**](imsrdpclientnonscriptable3.md)
</dt> </dl>

 

 





