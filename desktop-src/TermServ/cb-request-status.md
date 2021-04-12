---
title: Énumération CB_REQUEST_STATUS (Cbclient. h)
description: Spécifie l’état d’une demande asynchrone.
ms.assetid: 35FAC8EA-BA17-405F-AE10-33A816029F62
ms.tgt_platform: multiple
keywords:
- Énumération CB_REQUEST_STATUS Services Bureau à distance
topic_type:
- apiref
api_name:
- CB_REQUEST_STATUS
api_location:
- Cbclient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd57efd12d3fb5c708d5c4861ee144543bb49f6a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104317190"
---
# <a name="cb_request_status-enumeration"></a>Énumération de l’état de la \_ demande CB \_

Spécifie l’état d’une demande asynchrone. Cette énumération est utilisée avec la méthode [**IConnectionBrokerRequest :: CheckStatus**](iconnectionbrokerrequest-checkstatus.md) .

## <a name="syntax"></a>Syntaxe


```C++
typedef enum _CB_REQUEST_STATUS { 
  CB_STATUS_INVALID                     = 1,
  CB_STATUS_INITIATING_REQUEST          = 0,
  CB_STATUS_REQUEST_COMPLETED,
  CB_STATUS_REQUEST_FAILED,
  CB_STATUS_REQUEST_ABORTED,
  CB_STATUS_FINDING_DESTINATION,
  CB_STATUS_LOADING_DESTINATION,
  CB_STATUS_BRINGING_SESSION_ONLINE,
  CB_STATUS_REDIRECTING_TO_DESTINATION
} CB_REQUEST_STATUS;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="CB_STATUS_INVALID"></span><span id="cb_status_invalid"></span>**\_État CB \_ non valide**
</dt> <dd>

L’objet de requête n’est pas initialisé.

</dd> <dt>

<span id="CB_STATUS_INITIATING_REQUEST"></span><span id="cb_status_initiating_request"></span>**État CB à l’origine de la \_ \_ \_ demande**
</dt> <dd>

Non utilisé.

</dd> <dt>

<span id="CB_STATUS_REQUEST_COMPLETED"></span><span id="cb_status_request_completed"></span>**\_demande d’État CB \_ \_ terminée**
</dt> <dd>

La demande est terminée.

</dd> <dt>

<span id="CB_STATUS_REQUEST_FAILED"></span><span id="cb_status_request_failed"></span>**échec de la \_ demande d’État CB \_ \_**
</dt> <dd>

La demande a échoué.

</dd> <dt>

<span id="CB_STATUS_REQUEST_ABORTED"></span><span id="cb_status_request_aborted"></span>**\_demande d’État CB \_ \_ abandonnée**
</dt> <dd>

La demande a été abandonnée.

</dd> <dt>

<span id="CB_STATUS_FINDING_DESTINATION"></span><span id="cb_status_finding_destination"></span>**\_État CB \_ recherchant la \_ destination**
</dt> <dd>

Non utilisé.

</dd> <dt>

<span id="CB_STATUS_LOADING_DESTINATION"></span><span id="cb_status_loading_destination"></span>**DESTINATION de chargement de l' \_ État CB \_ \_**
</dt> <dd>

Non utilisé.

</dd> <dt>

<span id="CB_STATUS_BRINGING_SESSION_ONLINE"></span><span id="cb_status_bringing_session_online"></span>**État CB pour la \_ \_ \_ session \_ en ligne**
</dt> <dd>

Non utilisé.

</dd> <dt>

<span id="CB_STATUS_REDIRECTING_TO_DESTINATION"></span><span id="cb_status_redirecting_to_destination"></span>**\_État CB \_ Redirigé \_ vers la \_ destination**
</dt> <dd>

Non utilisé.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8<br/>                                                                  |
| Serveur minimal pris en charge<br/> | Windows Server 2012<br/>                                                        |
| En-tête<br/>                   | <dl> <dt>Cbclient. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IConnectionBrokerRequest :: CheckStatus**](iconnectionbrokerrequest-checkstatus.md)
</dt> </dl>

 

 





