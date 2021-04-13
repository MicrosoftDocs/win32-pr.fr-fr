---
title: Méthode IMsTscAxEvents OnAutoReconnecting
description: Appelée lorsqu’un client se trouve dans le processus de reconnexion automatique d’une session à un serveur hôte de session Bureau à distance (hôte de session Bureau à distance). | Méthode IMsTscAxEvents OnAutoReconnecting
ms.assetid: 9cb36052-8010-47df-bb46-f4ad81f47a73
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode OnAutoReconnecting
- Méthode OnAutoReconnecting Services Bureau à distance, interface IMsTscAxEvents
- Services Bureau à distance de l’interface IMsTscAxEvents, méthode OnAutoReconnecting
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnAutoReconnecting
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3435be46f2bb2c7bcf8ca662b039f3e5ef856d8b
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104322370"
---
# <a name="imstscaxeventsonautoreconnecting-method"></a>IMsTscAxEvents :: OnAutoReconnecting, méthode

Appelée lorsqu’un client se trouve dans le processus de reconnexion automatique d’une session à un serveur hôte de session Bureau à distance (hôte de session Bureau à distance).

## <a name="syntax"></a>Syntaxe


```C++
void OnAutoReconnecting(
  [in]  LONG                       disconnectReason,
  [in]  LONG                       attemptCount,
  [out] AutoReconnectContinueState *pArcContinueStatus
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*disconnectReason* \[ dans\]
</dt> <dd>

Code décrivant la raison de la dernière déconnexion de la session.

</dd> <dt>

*attemptCount* \[ dans\]
</dt> <dd>

Nombre de tentatives effectuées dans le processus de reconnexion automatique en cours. Ce nombre augmente d’une unité pour chaque tentative effectuée.

</dd> <dt>

*pArcContinueStatus* \[ à\]
</dt> <dd>

Pointeur vers un code retourné qui spécifie l’état du processus de reconnexion automatique. Ce code peut être réinitialisé pour modifier l’état du processus de reconnexion automatique en cours.

Pour plus d’informations sur la réinitialisation de ce code, reportez-vous à la section Notes.

<dt>

<span id="autoReconnectContinueAutomatic"></span><span id="autoreconnectcontinueautomatic"></span><span id="AUTORECONNECTCONTINUEAUTOMATIC"></span>

<span id="autoReconnectContinueAutomatic"></span><span id="autoreconnectcontinueautomatic"></span><span id="AUTORECONNECTCONTINUEAUTOMATIC"></span>autoReconnectContinueAutomatic * * * * (0)


</dt> <dd>

Le processus de reconnexion se produit automatiquement. Il s’agit de la valeur par défaut.

</dd> <dt>

<span id="autoReconnectContinueStop"></span><span id="autoreconnectcontinuestop"></span><span id="AUTORECONNECTCONTINUESTOP"></span>

<span id="autoReconnectContinueStop"></span><span id="autoreconnectcontinuestop"></span><span id="AUTORECONNECTCONTINUESTOP"></span>autoReconnectContinueStop * * * * (1)


</dt> <dd>

Le processus de reconnexion a été arrêté.

</dd> <dt>

<span id="autoReconnectContinueManual"></span><span id="autoreconnectcontinuemanual"></span><span id="AUTORECONNECTCONTINUEMANUAL"></span>

<span id="autoReconnectContinueManual"></span><span id="autoreconnectcontinuemanual"></span><span id="AUTORECONNECTCONTINUEMANUAL"></span>autoReconnectContinueManual * * * * (2)


</dt> <dd>

Le processus de reconnexion se produit manuellement.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Notes

Implémentez cette méthode dans votre récepteur d’événements pour recevoir une notification indiquant que le contrôle rétablit une connexion avec un serveur hôte de session Bureau à distance.

Lorsque l’état du processus de reconnexion automatique est modifié en affectant à la valeur du paramètre *pArcContinueStatus* la valeur **autoReconnectContinueAutomatic**, cette méthode fonctionne en mode purement consultatif. Les conteneurs peuvent écouter cet événement pour les notifications que le processus de reconnexion automatique est en cours. Le contrôle continue automatiquement d’essayer de rétablir une connexion en fonction de son propre minutage interne et des nombres de tentatives. Cette méthode est appelée lors de chaque tentative de reconnexion automatique afin d’avertir le conteneur.

Lorsque l’état du processus de reconnexion automatique est modifié en définissant la valeur du paramètre *pArcContinueStatus* sur **autoReconnectContinueStop**, la tentative de reconnexion automatique en cours sera interrompue, une notification de déconnexion sera envoyée au conteneur et aucune autre notification de reconnexion automatique n’est émise.

> [!Note]  
> Utilisez la propriété [**EnableAutoReconnect**](imsrdpclientadvancedsettings2-enableautoreconnect.md) pour activer ou désactiver la reconnexion automatique.

 

Lorsque l’état du processus de reconnexion automatique est modifié en affectant à la valeur du paramètre *pArcContinueStatus* la valeur **autoReconnectContinueManual**, le conteneur contrôle manuellement le processus de reconnexion automatique en appelant [**Connect**](imstscax-connect.md) pour déclencher une tentative de connexion ou se [**déconnecter**](imstscax-disconnect.md) pour annuler le processus de reconnexion automatique. Une fois défini sur cette valeur, le contrôle cesse d’effectuer des tentatives de reconnexion automatique et devient la stratégie du conteneur pour effectuer des appels de **connexion** afin de déclencher des tentatives de reconnexion automatique. Cette opération est effectuée lorsque le conteneur fournit un comportement personnalisé d’interface utilisateur pour la reconnexion automatique, par exemple le redémarrage d’une connexion RAS ou VPN abandonnée avant le processus de reconnexion automatique.

Pour plus d’informations sur la Connexion Bureau à distance par le Web, consultez [Requirements for connexion Bureau à distance par le Web](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                               |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                         |
| Bibliothèque de types<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IMsTscAxEvents**](imstscaxevents-interface.md)
</dt> </dl>

 

 





