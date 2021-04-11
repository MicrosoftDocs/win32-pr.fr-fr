---
description: La méthode OnStart est une méthode facultative qui peut être implémentée par l’analyse. Le MCSVC appelle cette méthode pour demander que le moniteur démarre la capture.
ms.assetid: 992ee27e-aaba-4e65-989b-e3f0fbd542ea
title: 'IMonitor :: OnStart, méthode (NetMon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMonitor.OnStart
api_type:
- COM
api_location:
- Netmon.h
ms.openlocfilehash: ca9e5e17de1d6baf2c79cc0077c5e2036a2a6246
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112207"
---
# <a name="imonitoronstart-method"></a>IMonitor :: OnStart, méthode

La méthode **OnStart** est une méthode facultative qui peut être implémentée par l’analyse. Le MCSVC appelle cette méthode pour demander que le moniteur démarre la capture.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT OnStart(
  [in] IUnknown *pUnkNPP
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pUnkNPP* \[ dans\]
</dt> <dd>

Pointeur [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) vers l’interface [IRTC](irtc.md) . Le moniteur peut utiliser cette interface pour obtenir des statistiques qui peuvent être utilisées pour déterminer si la capture doit être démarrée.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la méthode réussit, la valeur de retour est S \_ OK (ce qui est identique à la valeur de l’erreur). Lorsque \_ la méthode S OK est retournée, MCSVC appelle la méthode [IRTC :: Start](irtc-start.md) .

Si la méthode échoue, la valeur de retour est un code d’erreur. Le MCSVC ne démarre pas la capture si un code d’erreur est retourné.

## <a name="remarks"></a>Notes

Le MCSVC appelle cette méthode avant que la méthode [IRTC :: Start](irtc-start.md) du NPP soit appelée pour démarrer la capture.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                          |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                |
| En-tête<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[IMonitor](imonitor.md)
</dt> <dt>

[Fournisseurs de paquets réseau](network-packet-providers.md)
</dt> </dl>

 

