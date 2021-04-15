---
description: La méthode de neuroinitialize doit être implémentée par l’analyse. Le MCSVC appelle cette méthode pour obtenir un filtre de capture immédiatement avant d’appeler la méthode NPPs IRTCConnect.
ms.assetid: 5e43be75-21b3-4f37-ad53-3ffdd55f56a1
title: Méthode IMonitorDoInitialize (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMonitor.DoInitialize
api_type:
- COM
api_location:
- Netmon.h
ms.openlocfilehash: 93133ce8204e49d080f87635ad6952685f2ba82d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525114"
---
# <a name="imonitordoinitialize-method"></a>IMonitor ::D méthode oInitialize

La méthode de **neuroinitialize** doit être implémentée par l’analyse. Le MCSVC appelle cette méthode pour obtenir un filtre de capture immédiatement avant d’appeler la méthode [IRTC :: Connect](irtc-connect.md) du NPP.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT DoInitialize(
  [in]      IUnknown *pUnkMonitorCtrl,
  [in, out] HBLOB    hNPPBlob
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pUnkMonitorCtrl* \[ dans\]
</dt> <dd>

Pointeur [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) passé par MCSVC. Pour obtenir une interface de contrôle d’analyse prise en charge, l’analyse doit appeler [IUnknown :: QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) sur le pointeur.

</dd> <dt>

*hNPPBlob* \[ in, out\]
</dt> <dd>

En entrée, handle vers un objet BLOB NPP.

Lors de la sortie, un objet BLOB NPP contenant un filtre de capture.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la méthode réussit, la valeur de retour est S \_ OK (ce qui est identique à la valeur de l’erreur).

Si la méthode échoue, la valeur de retour est un code d’erreur. En cas d’erreur, MCSVC ne crée pas le moniteur ni n’appelle [IUnknown :: Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) sur le pointeur d’interface.

## <a name="remarks"></a>Notes

MCSVC appelle la méthode **noinitialize** pour effectuer toute initialisation de moniteur nécessaire.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                          |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                |
| En-tête<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



 

