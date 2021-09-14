---
title: IMsRdpClientNonScriptable4 propriété PromptForCredsOnClient
description: Spécifie si le contrôle client affiche une boîte de dialogue qui vous invite à entrer des informations d’identification.
ms.assetid: 426676be-0150-4a33-acd0-26423966f32a
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété PromptForCredsOnClient
- Services Bureau à distance de la propriété PromptForCredsOnClient, interface IMsRdpClientNonScriptable4
- Services Bureau à distance de l’interface IMsRdpClientNonScriptable4, propriété PromptForCredsOnClient
- Services Bureau à distance de la propriété PromptForCredsOnClient, interface IMsRdpClientNonScriptable5
- Services Bureau à distance de l’interface IMsRdpClientNonScriptable5, propriété PromptForCredsOnClient
- Services Bureau à distance de la propriété PromptForCredsOnClient, objet MsRdpClient6
- Services Bureau à distance objet MsRdpClient6, propriété PromptForCredsOnClient
- Services Bureau à distance de la propriété PromptForCredsOnClient, objet MsRdpClient7
- Services Bureau à distance objet MsRdpClient7, propriété PromptForCredsOnClient
- Services Bureau à distance de la propriété PromptForCredsOnClient, objet MsRdpClient8
- Services Bureau à distance objet MsRdpClient8, propriété PromptForCredsOnClient
- Services Bureau à distance de la propriété PromptForCredsOnClient, objet MsRdpClient9
- Services Bureau à distance objet MsRdpClient9, propriété PromptForCredsOnClient
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable4.PromptForCredsOnClient
- IMsRdpClientNonScriptable4.get_PromptForCredsOnClient
- IMsRdpClientNonScriptable4.put_PromptForCredsOnClient
- IMsRdpClientNonScriptable5.PromptForCredsOnClient
- IMsRdpClientNonScriptable5.get_PromptForCredsOnClient
- IMsRdpClientNonScriptable5.put_PromptForCredsOnClient
- MsRdpClient6.PromptForCredsOnClient
- MsRdpClient7.PromptForCredsOnClient
- MsRdpClient8.PromptForCredsOnClient
- MsRdpClient9.PromptForCredsOnClient
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6443c503e107bb2edb164a17beedddb1bbbc88a5
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127008615"
---
# <a name="imsrdpclientnonscriptable4promptforcredsonclient-property"></a>IMsRdpClientNonScriptable4 ::P propriété romptForCredsOnClient

Spécifie si le contrôle client affiche une boîte de dialogue qui vous invite à entrer des informations d’identification.

Cette propriété est en lecture/écriture.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT put_PromptForCredsOnClient(
  [in]  VARIANT_BOOL fPromptForCredsOnClient
);

HRESULT get_PromptForCredsOnClient(
  [out] VARIANT_BOOL *pfPromptForCredsOnClient
);
```



## <a name="property-value"></a>Valeur de la propriété

Définit si le contrôle client affiche une boîte de dialogue qui vous invite à entrer des informations d’identification.

## <a name="error-codes"></a>Codes d’erreur

Retourne **S \_ OK** en cas de réussite.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                                 |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                           |
| Bibliothèque de types<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>   |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>   |
| IID<br/>                      | IMsRdpClientNonScriptable4 est défini en tant que f50fa8aa-1c7d-4f59-B15C-a90cacae1fcb<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IMsRdpClientNonScriptable5**](imsrdpclientnonscriptable5.md)
</dt> <dt>

[**IMsRdpClientNonScriptable4**](imsrdpclientnonscriptable4.md)
</dt> </dl>

 

 





