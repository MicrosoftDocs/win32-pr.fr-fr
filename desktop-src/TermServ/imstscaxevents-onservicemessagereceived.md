---
title: Méthode IMsTscAxEvents OnServiceMessageReceived
description: Appelé lorsque le client reçoit un message système.
ms.assetid: 9D230AA3-30F8-4BDF-89D6-D33AF42D0E85
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode OnServiceMessageReceived
- Méthode OnServiceMessageReceived Services Bureau à distance, interface IMsTscAxEvents
- Services Bureau à distance de l’interface IMsTscAxEvents, méthode OnServiceMessageReceived
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnServiceMessageReceived
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 05a26b78fa31667fb550848d4edd7918aa2bde3e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127228605"
---
# <a name="imstscaxeventsonservicemessagereceived-method"></a>IMsTscAxEvents :: OnServiceMessageReceived, méthode

Appelé lorsque le client reçoit un message système.

## <a name="syntax"></a>Syntaxe


```C++
void OnServiceMessageReceived(
  [in] BSTR serviceMessage
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*serviceMessage* \[ dans\]
</dt> <dd>

Spécifie le message système.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Notes

Pour plus d’informations sur les messages système, consultez [configurer la messagerie pour un serveur de passerelle Bureau à distance](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/dd834700(v=ws.11)).

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 7<br/>                                                                   |
| Serveur minimal pris en charge<br/> | Windows Server 2008 R2<br/>                                                      |
| Bibliothèque de types<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IMsTscAxEvents est défini en tant que 336d5562-efa8-482e-8cb3-c5c0fc7a7db6<br/>           |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IMsTscAxEvents**](imstscaxevents-interface.md)
</dt> </dl>

 

