---
title: IMsRdpClientShell propriété IsRemoteProgramClientInstalled
description: récupère si le client Connexion Bureau à distance (RDC) prend en charge les fonctionnalités RemoteApp Windows Server 2008 R2.
ms.assetid: ce2fec74-c567-48e1-91d6-655c539d1fb9
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété IsRemoteProgramClientInstalled
- Services Bureau à distance de la propriété IsRemoteProgramClientInstalled, interface IMsRdpClientShell
- Services Bureau à distance de l’interface IMsRdpClientShell, propriété IsRemoteProgramClientInstalled
topic_type:
- apiref
api_name:
- IMsRdpClientShell.IsRemoteProgramClientInstalled
- IMsRdpClientShell.get_IsRemoteProgramClientInstalled
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3073bb9a9e5890ff7a6a46bb9ea0c03964bf54f1c91550dbb2746385a11fa809
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118129762"
---
# <a name="imsrdpclientshellisremoteprogramclientinstalled-property"></a>IMsRdpClientShell :: IsRemoteProgramClientInstalled, propriété

récupère si le client Connexion Bureau à distance (RDC) prend en charge les fonctionnalités RemoteApp Windows Server 2008 R2.

Cette propriété est en lecture seule.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT get_IsRemoteProgramClientInstalled(
  [out] VARIANT_BOOL *pbClientInstalled
);
```



## <a name="property-value"></a>Valeur de la propriété

Récupère si le client Connexion Bureau à distance (RDC) prend en charge les fonctionnalités RemoteApp.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                               |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                         |
| Bibliothèque de types<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IID \_ IMsRdpClientShell est défini en tant que d012ae6d-C19A-4bfe-b367-201f8911f134<br/>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IMsRdpClientShell**](imsrdpclientshell.md)
</dt> </dl>

 

 





