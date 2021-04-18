---
title: IMsRdpClientShell2 propriété SecuredSettingsEnabled
description: Récupère une valeur qui indique si la page Web active se trouve dans une zone de sécurité d’URL Internet Explorer approuvée.
ms.assetid: 51988473-fff7-4574-bd6e-d05ca452da54
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété SecuredSettingsEnabled
- Services Bureau à distance de la propriété SecuredSettingsEnabled, interface IMsRdpClientShell2
- Services Bureau à distance de l’interface IMsRdpClientShell2, propriété SecuredSettingsEnabled
topic_type:
- apiref
api_name:
- IMsRdpClientShell2.SecuredSettingsEnabled
- IMsRdpClientShell2.get_SecuredSettingsEnabled
api_location:
- MsRdpWebAccess.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1009759051207db7e6b8d741c1dd91e3de1ffc36
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106529083"
---
# <a name="imsrdpclientshell2securedsettingsenabled-property"></a>IMsRdpClientShell2 :: SecuredSettingsEnabled, propriété

Récupère une valeur qui indique si la page Web active se trouve dans une zone de sécurité d’URL Internet Explorer approuvée.

Cette propriété est en lecture seule.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT get_SecuredSettingsEnabled(
  [out, retval] BOOL *pSecuredSettingsEnabled
);
```



## <a name="property-value"></a>Valeur de la propriété

Pointeur vers une valeur booléenne qui indique si la page Web active se trouve dans une zone de sécurité d’URL Internet Explorer approuvée.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 7<br/>                                                                          |
| Serveur minimal pris en charge<br/> | Windows Server 2008 R2<br/>                                                             |
| DLL<br/>                      | <dl> <dt>MsRdpWebAccess.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IMsRdpClientShell2**](imsrdpclientshell2.md)
</dt> </dl>

 

 





