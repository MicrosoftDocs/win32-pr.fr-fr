---
title: IRemoteDesktopClientTouchPointer, propriété activée
description: Indique si la fonctionnalité de pointeur tactile est activée sur le contrôle client du conteneur d’applications RDP.
ms.assetid: f1e2f2f2-1b96-4c5a-b0dd-fd57627c5ec3
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété Enabled
- Propriété Enabled Services Bureau à distance, IRemoteDesktopClientTouchPointer, interface
- Services Bureau à distance de l’interface IRemoteDesktopClientTouchPointer, propriété Enabled
topic_type:
- apiref
api_name:
- IRemoteDesktopClientTouchPointer.Enabled
- IRemoteDesktopClientTouchPointer.get_Enabled
- IRemoteDesktopClientTouchPointer.put_Enabled
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d7ce04e38b41fce462973606f40f0099f010e6f4ab785900039e6771b0a9aaf4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120124849"
---
# <a name="iremotedesktopclienttouchpointerenabled-property"></a>IRemoteDesktopClientTouchPointer :: Enabled, propriété

Indique si la fonctionnalité de pointeur tactile est activée sur le contrôle client du conteneur d’applications RDP.

Cette propriété est en lecture/écriture.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT put_Enabled(
  [in]          VARIANT_BOOL Enabled
);

HRESULT get_Enabled(
  [out, retval] VARIANT_BOOL *Enabled
);
```



## <a name="property-value"></a>Valeur de la propriété

**true** si la fonctionnalité du pointeur tactile est activée ; Sinon, **false**.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8<br/>                                                                                |
| Serveur minimal pris en charge<br/> | Windows Server 2012<br/>                                                                      |
| Bibliothèque de types<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>              |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>              |
| IID<br/>                      | IID \_ IRemoteDesktopClientTouchPointer est défini en tant que 260EC22D-8CBC-44B5-9E88-2A37F6C93AE9<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IRemoteDesktopClientTouchPointer**](/windows/win32/api/rdpappcontainerclient/nn-rdpappcontainerclient-iremotedesktopclienttouchpointer)
</dt> </dl>

 

