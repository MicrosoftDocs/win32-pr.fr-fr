---
title: ITSRemoteProgram propriété RemoteProgramMode
description: Mode RemoteApp de Windows Server 2008 R2.
ms.assetid: 9ebdf966-db9c-4a14-8469-f8b153c6ea78
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété RemoteProgramMode
- Services Bureau à distance de la propriété RemoteProgramMode, interface ITSRemoteProgram
- Services Bureau à distance de l’interface ITSRemoteProgram, propriété RemoteProgramMode
- Services Bureau à distance de la propriété RemoteProgramMode, interface ITSRemoteProgram2
- Services Bureau à distance de l’interface ITSRemoteProgram2, propriété RemoteProgramMode
- Services Bureau à distance de la propriété RemoteProgramMode, interface ITSRemoteProgram3
- Services Bureau à distance de l’interface ITSRemoteProgram3, propriété RemoteProgramMode
topic_type:
- apiref
api_name:
- ITSRemoteProgram.RemoteProgramMode
- ITSRemoteProgram.get_RemoteProgramMode
- ITSRemoteProgram.put_RemoteProgramMode
- ITSRemoteProgram2.RemoteProgramMode
- ITSRemoteProgram2.get_RemoteProgramMode
- ITSRemoteProgram2.put_RemoteProgramMode
- ITSRemoteProgram3.RemoteProgramMode
- ITSRemoteProgram3.get_RemoteProgramMode
- ITSRemoteProgram3.put_RemoteProgramMode
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e8582824e2f6349e37b125ffd974847b602ad6fa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106512583"
---
# <a name="itsremoteprogramremoteprogrammode-property"></a>ITSRemoteProgram :: RemoteProgramMode, propriété

Mode RemoteApp de Windows Server 2008 R2.

Cette propriété est en lecture/écriture.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT put_RemoteProgramMode(
  [in]  VARIANT_BOOL vboolRemoteProgramMode
);

HRESULT get_RemoteProgramMode(
  [out] VARIANT_BOOL *pvboolRemoteProgramMode
);
```



## <a name="property-value"></a>Valeur de la propriété

Mode RemoteApp. Si la valeur **est \_ true**, le mode RemoteApp est activé et la session à distance héberge les programmes RemoteApp. Si la valeur **Variant est \_ false** (valeur par défaut), le mode RemoteApp n’est pas activé. La session à distance hébergera un bureau à distance.

## <a name="error-codes"></a>Codes d’erreur

Retourne **S \_ OK** en cas de réussite.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                               |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                         |
| Bibliothèque de types<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IID \_ ITSRemoteProgram est défini en tant que FDD029F9-467A-4c49-8529-64B521DBD1B4<br/>    |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**ITSRemoteProgram2**](itsremoteprogram2.md)
</dt> <dt>

[**ITSRemoteProgram3**](itsremoteprogram3.md)
</dt> <dt>

[**ITSRemoteProgram**](itsremoteprogram.md)
</dt> </dl>

 

 





