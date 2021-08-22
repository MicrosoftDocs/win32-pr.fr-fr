---
title: IMsRdpClientNonScriptable5 propriété AllowPromptingForCredentials
description: spécifie si le contrôle de ActiveX Bureau à distance peut inviter l’utilisateur à fournir des informations d’identification.
ms.assetid: 9a780886-39ee-4d3b-9a54-fa209708d9f8
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété AllowPromptingForCredentials
- Services Bureau à distance de la propriété AllowPromptingForCredentials, interface IMsRdpClientNonScriptable5
- Services Bureau à distance de l’interface IMsRdpClientNonScriptable5, propriété AllowPromptingForCredentials
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable5.AllowPromptingForCredentials
- IMsRdpClientNonScriptable5.get_AllowPromptingForCredentials
- IMsRdpClientNonScriptable5.put_AllowPromptingForCredentials
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eea0fb854b5bb12533032cd6608228d81584cd8d9f4e99bccd8a5ba76b624f77
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119138752"
---
# <a name="imsrdpclientnonscriptable5allowpromptingforcredentials-property"></a>IMsRdpClientNonScriptable5 :: AllowPromptingForCredentials, propriété

spécifie si le contrôle de ActiveX Bureau à distance peut inviter l’utilisateur à fournir des informations d’identification. Si cette propriété contient **la \_ valeur true**, l’utilisateur peut être invité à entrer des informations d’identification. Si cette propriété contient **la \_ valeur false**, l’utilisateur ne peut pas être invité à entrer ses informations d’identification.

Cette propriété est en lecture/écriture.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT put_AllowPromptingForCredentials(
  [in]          VARIANT_BOOL fAllow
);

HRESULT get_AllowPromptingForCredentials(
  [out, retval] VARIANT_BOOL *pfAllow
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

 

 





