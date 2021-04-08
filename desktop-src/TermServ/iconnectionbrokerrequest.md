---
title: Interface IConnectionBrokerRequest (Cbclient. h)
description: Fournit les méthodes nécessaires pour obtenir les résultats de la méthode asynchrone IConnectionBrokerClient GetTargetInfo.
ms.assetid: 20F42FDC-7026-468E-9B8D-25DFFBE229C1
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de l’interface IConnectionBrokerRequest
- Services Bureau à distance de l’interface IConnectionBrokerRequest, Description
topic_type:
- apiref
api_name:
- IConnectionBrokerRequest
api_location:
- Cbclient.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cb95427aee37053b6979cb1a12ce7b5d1942c2fe
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743661"
---
# <a name="iconnectionbrokerrequest-interface"></a>Interface IConnectionBrokerRequest

Fournit les méthodes nécessaires pour obtenir les résultats de la méthode [**IConnectionBrokerClient :: GetTargetInfo**](iconnectionbrokerclient-gettargetinfo.md) asynchrone.

Cette interface est implémentée par le système. Une instance de cette interface est fournie à l’appelant à l’aide de la méthode [**IConnectionBrokerClient :: GetTargetInfo**](iconnectionbrokerclient-gettargetinfo.md) .

## <a name="members"></a>Membres

L’interface **IConnectionBrokerRequest** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **IConnectionBrokerRequest** a également les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **IConnectionBrokerRequest** possède ces méthodes.



| Méthode                                                      | Description                                                           |
|:------------------------------------------------------------|:----------------------------------------------------------------------|
| [**CheckStatus**](iconnectionbrokerrequest-checkstatus.md) | Appelé pour déterminer l’état d’une requête asynchrone.<br/> |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8<br/>                                                                        |
| Serveur minimal pris en charge<br/> | Windows Server 2012<br/>                                                              |
| En-tête<br/>                   | <dl> <dt>Cbclient. h</dt> </dl>       |
| Bibliothèque<br/>                  | <dl> <dt>Cbclient. lib</dt> </dl>     |
| DLL<br/>                      | <dl> <dt>Cbclient.dll</dt> </dl>     |
| IID<br/>                      | IID \_ IConnectionBrokerRequest est défini comme 25114427-ED5D-46a6-AF53-C62D33A4108E<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IConnectionBrokerClient::GetTargetInfo**](iconnectionbrokerclient-gettargetinfo.md)
</dt> </dl>

 

