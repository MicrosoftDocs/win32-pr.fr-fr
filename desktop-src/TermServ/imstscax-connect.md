---
title: IMsTscAx Connect, méthode
description: Établit une connexion à l’aide des propriétés actuellement définies sur le contrôle.
ms.assetid: 9bcbdc13-6c66-4737-82a4-98329f173743
ms.tgt_platform: multiple
keywords:
- Méthode Connect Services Bureau à distance
- Connect, méthode Services Bureau à distance, IMsTscAx, interface
- Services Bureau à distance de l’interface IMsTscAx, méthode Connect
- Connect, méthode Services Bureau à distance, IMsRdpClient, interface
- Services Bureau à distance de l’interface IMsRdpClient, méthode Connect
- Connect, méthode Services Bureau à distance, IMsRdpClient2, interface
- Services Bureau à distance de l’interface IMsRdpClient2, méthode Connect
- Connect, méthode Services Bureau à distance, IMsRdpClient3, interface
- Services Bureau à distance de l’interface IMsRdpClient3, méthode Connect
- Connect, méthode Services Bureau à distance, IMsRdpClient4, interface
- Services Bureau à distance de l’interface IMsRdpClient4, méthode Connect
- Connect, méthode Services Bureau à distance, IMsRdpClient5, interface
- Services Bureau à distance de l’interface IMsRdpClient5, méthode Connect
- Connect, méthode Services Bureau à distance, IMsRdpClient6, interface
- Services Bureau à distance de l’interface IMsRdpClient6, méthode Connect
- Connect, méthode Services Bureau à distance, IMsRdpClient7, interface
- Services Bureau à distance de l’interface IMsRdpClient7, méthode Connect
- Connect, méthode Services Bureau à distance, IMsRdpClient8, interface
- Services Bureau à distance de l’interface IMsRdpClient8, méthode Connect
- Connect, méthode Services Bureau à distance, IMsRdpClient9, interface
- Services Bureau à distance de l’interface IMsRdpClient9, méthode Connect
topic_type:
- apiref
api_name:
- IMsTscAx.Connect
- IMsRdpClient.Connect
- IMsRdpClient2.Connect
- IMsRdpClient3.Connect
- IMsRdpClient4.Connect
- IMsRdpClient5.Connect
- IMsRdpClient6.Connect
- IMsRdpClient7.Connect
- IMsRdpClient8.Connect
- IMsRdpClient9.Connect
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c267b24c3dd27dd875d895674d98e1350f757c82
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103941873"
---
# <a name="imstscaxconnect-method"></a>IMsTscAx :: Connect, méthode

Établit une connexion à l’aide des propriétés actuellement définies sur le contrôle.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT Connect();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Retourne **S \_ OK** en cas de réussite.

## <a name="remarks"></a>Notes

La seule propriété requise est le nom du serveur. Reportez-vous à la propriété de [**serveur**](imstscax-server.md) .

Le contrôle se connecte de manière asynchrone, de sorte qu’un retour d’un appel de connexion indique uniquement que la connexion a été lancée avec succès, et non qu’elle est terminée. Vous devez répondre aux événements sur l’interface [**IMsTscAxEvents**](imstscaxevents-interface.md) pour déterminer quand le contrôle s’est connecté avec succès (ou a été déconnecté).

Cette méthode retourne **E \_ Fail** si elle est appelée alors que le contrôle est déjà connecté ou à l’état de connexion.

Une fois que la **connexion** a été appelée, la plupart des propriétés de contrôle ne peuvent plus être définies tant que le contrôle n’est pas retourné à l’État Disconnected.

Pour plus d’informations sur la Connexion Bureau à distance par le Web, consultez [Requirements for connexion Bureau à distance par le Web](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                               |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                         |
| Bibliothèque de types<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IID \_ IMsTscAx est défini en tant que 8C11EFAE-92C3-11D1-BC1E-00C04FA31489<br/>            |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IMsRdpClient**](imsrdpclient-interface.md)
</dt> <dt>

[**IMsRdpClient2**](imsrdpclient2.md)
</dt> <dt>

[**IMsRdpClient3**](imsrdpclient3.md)
</dt> <dt>

[**IMsRdpClient4**](imsrdpclient4.md)
</dt> <dt>

[**IMsRdpClient5**](imsrdpclient5.md)
</dt> <dt>

[**IMsRdpClient6**](imsrdpclient6.md)
</dt> <dt>

[**IMsRdpClient7**](imsrdpclient7.md)
</dt> <dt>

[**IMsRdpClient8**](imsrdpclient8.md)
</dt> <dt>

[**IMsRdpClient9**](imsrdpclient9.md)
</dt> <dt>

[**Déconnecter**](imstscax-disconnect.md)
</dt> <dt>

[**IMsTscAx**](imstscax-interface.md)
</dt> </dl>

 

 





