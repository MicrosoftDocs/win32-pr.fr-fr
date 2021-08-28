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
ms.openlocfilehash: d418df76de38313d681f9f01a4dea33ba0803ad67e42d92d90d2ba5a354a8eac
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119870879"
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

 

 





