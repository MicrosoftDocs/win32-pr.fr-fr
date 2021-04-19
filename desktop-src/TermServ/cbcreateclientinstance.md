---
title: CBCreateClientInstance, fonction (Cbclient. h)
description: Crée une instance du client RPC Connexion Bureau à distance Broker.
ms.assetid: 700E47BC-C547-44AB-8607-B9797D542AA7
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la fonction CBCreateClientInstance
topic_type:
- apiref
api_name:
- CBCreateClientInstance
api_location:
- Cbclient.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d2b30f2d236bcc90dfa4977f54d56a5d1717d18a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106542794"
---
# <a name="cbcreateclientinstance-function"></a>CBCreateClientInstance fonction)

Crée une instance du client RPC Connexion Bureau à distance Broker.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT CBCreateClientInstance(
  _In_  DWORD                   Version,
  _Out_ IConnectionBrokerClient **ppCbClient
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Version* \[ de dans\]
</dt> <dd>

Spécifie la version de l’interface du client Connexion Bureau à distance Broker demandée. Il doit s’agir de la valeur suivante.

<dt>

1
</dt> <dd>

Version 1 du client Connexion Bureau à distance Broker.

</dd> </dl> </dd> <dt>

*ppCbClient* \[ à\]
</dt> <dd>

Adresse d’un pointeur d’interface [**IConnectionBrokerClient**](iconnectionbrokerclient.md) qui reçoit l’objet client Connexion Bureau à distance Broker.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si cette fonction est correctement exécutée, elle retourne la valeur **\_ OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|-----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Cbclient. h</dt> </dl>   |
| Bibliothèque<br/> | <dl> <dt>Cbclient. lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>Cbclient.dll</dt> </dl> |



 

 





