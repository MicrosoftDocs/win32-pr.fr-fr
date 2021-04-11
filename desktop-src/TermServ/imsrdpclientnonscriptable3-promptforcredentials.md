---
title: IMsRdpClientNonScriptable3, propriété PromptForCredentials (wuapi. h)
description: Spécifie ou récupère une valeur indiquant si la boîte de dialogue demander les informations d’identification est activée pour la connexion.
ms.assetid: 252ec5bd-bd52-40d4-ae48-b2c00c0720c0
ms.tgt_platform: multiple
keywords:
- Propriété PromptForCredentials Services Bureau à distance
- Propriété PromptForCredentials Services Bureau à distance, interface IMsRdpClientNonScriptable3
- Services Bureau à distance de l’interface IMsRdpClientNonScriptable3, propriété PromptForCredentials
- Propriété PromptForCredentials Services Bureau à distance, interface IMsRdpClientNonScriptable4
- Services Bureau à distance de l’interface IMsRdpClientNonScriptable4, propriété PromptForCredentials
- Propriété PromptForCredentials Services Bureau à distance, interface IMsRdpClientNonScriptable5
- Services Bureau à distance de l’interface IMsRdpClientNonScriptable5, propriété PromptForCredentials
- Propriété PromptForCredentials Services Bureau à distance, objet MsRdpClient5
- Objet MsRdpClient5 Services Bureau à distance, propriété PromptForCredentials
- Propriété PromptForCredentials Services Bureau à distance, objet MsRdpClient6
- Objet MsRdpClient6 Services Bureau à distance, propriété PromptForCredentials
- Propriété PromptForCredentials Services Bureau à distance, objet MsRdpClient7
- Objet MsRdpClient7 Services Bureau à distance, propriété PromptForCredentials
- Propriété PromptForCredentials Services Bureau à distance, objet MsRdpClient8
- Objet MsRdpClient8 Services Bureau à distance, propriété PromptForCredentials
- Propriété PromptForCredentials Services Bureau à distance, objet MsRdpClient9
- Objet MsRdpClient9 Services Bureau à distance, propriété PromptForCredentials
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable3.PromptForCredentials
- IMsRdpClientNonScriptable3.get_PromptForCredentials
- IMsRdpClientNonScriptable3.put_PromptForCredentials
- IMsRdpClientNonScriptable4.PromptForCredentials
- IMsRdpClientNonScriptable4.get_PromptForCredentials
- IMsRdpClientNonScriptable4.put_PromptForCredentials
- IMsRdpClientNonScriptable5.PromptForCredentials
- IMsRdpClientNonScriptable5.get_PromptForCredentials
- IMsRdpClientNonScriptable5.put_PromptForCredentials
- MsRdpClient5.PromptForCredentials
- MsRdpClient6.PromptForCredentials
- MsRdpClient7.PromptForCredentials
- MsRdpClient8.PromptForCredentials
- MsRdpClient9.PromptForCredentials
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 62f913937c9a2ff01d4aabeaba48dcbdc8ddb21d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104317125"
---
# <a name="imsrdpclientnonscriptable3promptforcredentials-property"></a>IMsRdpClientNonScriptable3 ::P propriété romptForCredentials

Spécifie ou récupère une valeur indiquant si la boîte de dialogue demander les informations d’identification est activée pour la connexion.

Cette propriété est en lecture/écriture.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT put_PromptForCredentials(
  [in]  VARIANT_BOOL fPrompt
);

HRESULT get_PromptForCredentials(
  [out] VARIANT_BOOL *pfPrompt
);
```



## <a name="property-value"></a>Valeur de la propriété

Spécifie si la boîte de dialogue demander les informations d’identification est activée pour la connexion.

## <a name="error-codes"></a>Codes d’erreur

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                                      |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                                |
| En-tête<br/>                   | <dl> <dt>Wuapi. h</dt> </dl>            |
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

 

 





