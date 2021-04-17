---
title: Interface IConnectionBrokerClient (Cbclient. h)
description: Fournit les méthodes nécessaires pour utiliser le client Connexion Bureau à distance Broker.
ms.assetid: AFFE0157-DEF5-480D-8CE0-D89E9EF70EAF
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de l’interface IConnectionBrokerClient
- Services Bureau à distance de l’interface IConnectionBrokerClient, Description
topic_type:
- apiref
api_name:
- IConnectionBrokerClient
api_location:
- Cbclient.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4a062059f7aa1f16e32514b3bacbfb31dc0a350f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466758"
---
# <a name="iconnectionbrokerclient-interface"></a>Interface IConnectionBrokerClient

Fournit les méthodes nécessaires pour utiliser le client Connexion Bureau à distance Broker.

Cette interface est implémentée par le système. Pour obtenir une instance de cette interface, utilisez la fonction [**CBCreateClientInstance**](cbcreateclientinstance.md) .

## <a name="members"></a>Membres

L’interface **IConnectionBrokerClient** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **IConnectionBrokerClient** a également les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **IConnectionBrokerClient** possède ces méthodes.



| Méthode                                                         | Description                                                                                          |
|:---------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------|
| [**GetTargetInfo**](iconnectionbrokerclient-gettargetinfo.md) | Demande des informations sur l’ordinateur cible sur lequel la connexion doit être redirigée.<br/> |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8<br/>                                                                       |
| Serveur minimal pris en charge<br/> | Windows Server 2012<br/>                                                             |
| En-tête<br/>                   | <dl> <dt>Cbclient. h</dt> </dl>      |
| Bibliothèque<br/>                  | <dl> <dt>Cbclient. lib</dt> </dl>    |
| DLL<br/>                      | <dl> <dt>Cbclient.dll</dt> </dl>    |
| IID<br/>                      | IID \_ IConnectionBrokerClient est défini en tant que D6818DF2-8338-4EB7-AD77-DE210817987C<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBCreateClientInstance**](cbcreateclientinstance.md)
</dt> </dl>

 

