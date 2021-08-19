---
title: IMsRdpClientShell2 propriété MsRdpWorkspace
description: Récupère un pointeur vers l’interface IMsRdpWorkspace, qui est utilisée pour gérer les informations d’identification et les connexions de Connexions aux programmes RemoteApp et aux services Bureau à distance.
ms.assetid: 5d505ce0-18cf-4e38-b1b8-026303f7069b
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété MsRdpWorkspace
- Services Bureau à distance de la propriété MsRdpWorkspace, interface IMsRdpClientShell2
- Services Bureau à distance de l’interface IMsRdpClientShell2, propriété MsRdpWorkspace
topic_type:
- apiref
api_name:
- IMsRdpClientShell2.MsRdpWorkspace
- IMsRdpClientShell2.get_MsRdpWorkspace
api_location:
- MsRdpWebAccess.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6470f51ccae2efb6dc3d44a7b0a2a0310ad4230861d7d86262f34fd312fcfc5c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118854433"
---
# <a name="imsrdpclientshell2msrdpworkspace-property"></a>IMsRdpClientShell2 :: MsRdpWorkspace, propriété

Récupère un pointeur vers l’interface [**IMsRdpWorkspace**](imsrdpworkspace.md) , qui est utilisée pour gérer les informations d’identification et les connexions de connexions aux programmes RemoteApp et aux services Bureau à distance.

Cette propriété est en lecture seule.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT get_MsRdpWorkspace(
  [out, retval] IMsRdpWorkspace **pVal
);
```



## <a name="property-value"></a>Valeur de la propriété

Adresse d’un pointeur vers l’interface [**IMsRdpWorkspace**](imsrdpworkspace.md) .

## <a name="remarks"></a>Remarques

L’interface [**IMsRdpWorkspace**](imsrdpworkspace.md) n’est pas exposée en tant qu’interface personnalisée. Il est accessible uniquement par le biais des méthodes [IDispatch](/windows/desktop/com/exposing-methods-through-idispatch) .

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

 

