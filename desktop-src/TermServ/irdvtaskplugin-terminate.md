---
title: IRDVTaskPlugin Terminate (méthode)
description: Appelé lorsque l’agent de tâche est arrêté.
ms.assetid: b693a318-1da7-4207-8046-a62b7ccca471
ms.tgt_platform: multiple
keywords:
- Terminate, méthode Services Bureau à distance
- Terminate, méthode Services Bureau à distance, IRDVTaskPlugin, interface
- Services Bureau à distance de l’interface IRDVTaskPlugin, méthode Terminate
topic_type:
- apiref
api_name:
- IRDVTaskPlugin.Terminate
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0ccfcb1a59f0db6d29881d139d16bd08308a40df2c1233beab66b0b4814caa84
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118129266"
---
# <a name="irdvtaskpluginterminate-method"></a>IRDVTaskPlugin :: Terminate, méthode

Appelé lorsque l’agent de tâche est arrêté.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT Terminate(
  [in] HRESULT hr
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*RH* \[ dans\]
</dt> <dd>

Indique si l’arrêt est dû à un arrêt normal ou à un échec. Si l’arrêt est normal, cela indique que **est \_ OK**. Sinon, elle contient un code d’erreur **HRESULT** .

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si cette méthode est réussie, elle retourne la valeur **\_ OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------|
| Client minimal pris en charge<br/> | Windows 7 Entreprise<br/>   |
| Serveur minimal pris en charge<br/> | Windows Server 2008 R2<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IRDVTaskPlugin**](irdvtaskplugin.md)
</dt> </dl>

 

 





