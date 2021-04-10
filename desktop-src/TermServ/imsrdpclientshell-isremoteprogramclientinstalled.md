---
title: IMsRdpClientShell propriété IsRemoteProgramClientInstalled
description: Récupère si le client Connexion Bureau à distance (RDC) prend en charge les fonctionnalités RemoteApp de Windows Server 2008 R2.
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
ms.openlocfilehash: 787d45f10e109a89429be5032fda245aa3609567
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103269"
---
# <a name="imsrdpclientshellisremoteprogramclientinstalled-property"></a>IMsRdpClientShell :: IsRemoteProgramClientInstalled, propriété

Récupère si le client Connexion Bureau à distance (RDC) prend en charge les fonctionnalités RemoteApp de Windows Server 2008 R2.

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

 

 





