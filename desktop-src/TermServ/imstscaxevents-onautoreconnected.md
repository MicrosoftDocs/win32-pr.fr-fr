---
title: Méthode IMsTscAxEvents OnAutoReconnected
description: Appelé lorsque le contrôle client se reconnecte automatiquement à une session à distance. | Méthode IMsTscAxEvents OnAutoReconnected
ms.assetid: 50307002-33F9-453C-A880-AF4111412854
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode OnAutoReconnected
- Méthode OnAutoReconnected Services Bureau à distance, interface IMsTscAxEvents
- Services Bureau à distance de l’interface IMsTscAxEvents, méthode OnAutoReconnected
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnAutoReconnected
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: df16cbb2976bdbf5518a56bc90e4978772deb81608d5d24fba5516f9f538d6dc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120125199"
---
# <a name="imstscaxeventsonautoreconnected-method"></a>IMsTscAxEvents :: OnAutoReconnected, méthode

Appelé lorsque le contrôle client se reconnecte automatiquement à une session à distance.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT OnAutoReconnected();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Si cette méthode est réussie, elle retourne la valeur **\_ OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8<br/>                                                                   |
| Serveur minimal pris en charge<br/> | Windows Server 2012<br/>                                                         |
| Bibliothèque de types<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IMsTscAxEvents**](imstscaxevents-interface.md)
</dt> </dl>

 

 





