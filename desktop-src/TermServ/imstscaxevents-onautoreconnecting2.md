---
title: Méthode IMsTscAxEvents OnAutoReconnecting2
description: Appelée lorsqu’un client se trouve dans le processus de reconnexion automatique d’une session à un serveur hôte de session Bureau à distance (hôte de session Bureau à distance). | Méthode IMsTscAxEvents OnAutoReconnecting2
ms.assetid: 20F69798-5397-440C-9D0D-45AE417623A7
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode OnAutoReconnecting2
- Méthode OnAutoReconnecting2 Services Bureau à distance, interface IMsTscAxEvents
- Services Bureau à distance de l’interface IMsTscAxEvents, méthode OnAutoReconnecting2
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnAutoReconnecting2
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 901bb196922d1772782ab7f1c911c96573c88b36
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126919871"
---
# <a name="imstscaxeventsonautoreconnecting2-method"></a>IMsTscAxEvents :: OnAutoReconnecting2, méthode

Appelée lorsqu’un client se trouve dans le processus de reconnexion automatique d’une session à un serveur hôte de session Bureau à distance (hôte de session Bureau à distance). Il s’agit d’une version améliorée de la méthode [**OnAutoReconnecting**](-imstscaxevents--onautoreconnecting.md) .

## <a name="syntax"></a>Syntaxe


```C++
void OnAutoReconnecting2(
  [in] LONG         disconnectReason,
  [in] VARIANT_BOOL networkAvailable,
  [in] LONG         attemptCount,
  [in] LONG         maxAttemptCount
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*disconnectReason* \[ dans\]
</dt> <dd>

Code qui décrit la raison de la dernière déconnexion de la session.

</dd> <dt>

*networkAvailable* \[ dans\]
</dt> <dd>

Spécifie si le réseau est disponible.

</dd> <dt>

*attemptCount* \[ dans\]
</dt> <dd>

Nombre de tentatives effectuées dans le processus de reconnexion automatique en cours. Ce nombre augmente d’une unité pour chaque tentative effectuée.

</dd> <dt>

*maxAttemptCount* \[ dans\]
</dt> <dd>

Nombre maximal de tentatives qui seront effectuées dans le processus de reconnexion automatique actuel.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Cette méthode ne retourne pas de valeur.

## <a name="requirements"></a>Spécifications



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

 

 





