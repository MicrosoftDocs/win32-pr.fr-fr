---
title: Méthode ITSRemoteProgram3 ServerStartApp
description: Spécifie une application à démarrer dans la session à distance.
ms.assetid: 55a05d05-66d5-48a1-b3a6-f087aeb62925
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode ServerStartApp
- Méthode ServerStartApp Services Bureau à distance, interface ITSRemoteProgram3
- Services Bureau à distance de l’interface ITSRemoteProgram3, méthode ServerStartApp
topic_type:
- apiref
api_name:
- ITSRemoteProgram3.ServerStartApp
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ef1822fa98094870ebebe607528cdc69a8a201f5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106545757"
---
# <a name="itsremoteprogram3serverstartapp-method"></a>ITSRemoteProgram3 :: ServerStartApp, méthode

Spécifie une application à démarrer dans la session à distance.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT ServerStartApp(
  [in] BSTR         bstrAppUserModelId,
  [in] BSTR         bstrArguments,
  [in] VARIANT_BOOL vbExpandEnvVarInArgumentsOnServer
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*bstrAppUserModelId* \[ dans\]
</dt> <dd></dd> <dt>

*bstrArguments* \[ dans\]
</dt> <dd></dd> <dt>

*vbExpandEnvVarInArgumentsOnServer* \[ dans\]
</dt> <dd></dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si cette méthode est réussie, elle retourne la valeur **\_ OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 10 uniquement\]<br/>                                            |
| Serveur minimal pris en charge<br/> | Windows Server 2016<br/>                                                         |
| Bibliothèque de types<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**ITSRemoteProgram3**](itsremoteprogram3.md)
</dt> </dl>

 

 





