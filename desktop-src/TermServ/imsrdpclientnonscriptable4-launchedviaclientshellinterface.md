---
title: IMsRdpClientNonScriptable4 propriété LaunchedViaClientShellInterface
description: Spécifie si l’utilisateur a lancé le contrôle client à l’aide de l’interface Bureau à distance Accès web (RD Accès web).
ms.assetid: bf72c375-0eec-49c7-9f9a-c7545a95bdce
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété LaunchedViaClientShellInterface
- Services Bureau à distance de la propriété LaunchedViaClientShellInterface, interface IMsRdpClientNonScriptable4
- Services Bureau à distance de l’interface IMsRdpClientNonScriptable4, propriété LaunchedViaClientShellInterface
- Services Bureau à distance de la propriété LaunchedViaClientShellInterface, interface IMsRdpClientNonScriptable5
- Services Bureau à distance de l’interface IMsRdpClientNonScriptable5, propriété LaunchedViaClientShellInterface
- Services Bureau à distance de la propriété LaunchedViaClientShellInterface, objet MsRdpClient5
- Services Bureau à distance objet MsRdpClient5, propriété LaunchedViaClientShellInterface
- Services Bureau à distance de la propriété LaunchedViaClientShellInterface, objet MsRdpClient6
- Services Bureau à distance objet MsRdpClient6, propriété LaunchedViaClientShellInterface
- Services Bureau à distance de la propriété LaunchedViaClientShellInterface, objet MsRdpClient7
- Services Bureau à distance objet MsRdpClient7, propriété LaunchedViaClientShellInterface
- Services Bureau à distance de la propriété LaunchedViaClientShellInterface, objet MsRdpClient8
- Services Bureau à distance objet MsRdpClient8, propriété LaunchedViaClientShellInterface
- Services Bureau à distance de la propriété LaunchedViaClientShellInterface, objet MsRdpClient9
- Services Bureau à distance objet MsRdpClient9, propriété LaunchedViaClientShellInterface
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable4.LaunchedViaClientShellInterface
- IMsRdpClientNonScriptable4.get_LaunchedViaClientShellInterface
- IMsRdpClientNonScriptable4.put_LaunchedViaClientShellInterface
- IMsRdpClientNonScriptable5.LaunchedViaClientShellInterface
- IMsRdpClientNonScriptable5.get_LaunchedViaClientShellInterface
- IMsRdpClientNonScriptable5.put_LaunchedViaClientShellInterface
- MsRdpClient5.LaunchedViaClientShellInterface
- MsRdpClient6.LaunchedViaClientShellInterface
- MsRdpClient7.LaunchedViaClientShellInterface
- MsRdpClient8.LaunchedViaClientShellInterface
- MsRdpClient9.LaunchedViaClientShellInterface
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7d5854a4e75be455035fd9a123418bd486932379
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942332"
---
# <a name="imsrdpclientnonscriptable4launchedviaclientshellinterface-property"></a>IMsRdpClientNonScriptable4 :: LaunchedViaClientShellInterface, propriété

Spécifie si l’utilisateur a lancé le contrôle client à l’aide de l’interface Bureau à distance Accès web (RD Accès web).

Cette propriété est en lecture/écriture.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT put_LaunchedViaClientShellInterface(
  [in]  VARIANT_BOOL fLaunchedViaClientShellInterface
);

HRESULT get_LaunchedViaClientShellInterface(
  [out]  VARIANT_BOOL *pfLaunchedViaClientShellInterface
);
```



## <a name="property-value"></a>Valeur de la propriété

Définit la propriété **LaunchedViaClientShellInterface** .

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

 

 





