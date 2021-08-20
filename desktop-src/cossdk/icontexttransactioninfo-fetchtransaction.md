---
description: Récupère la transaction ou le proxy de transaction associé au contexte actuel, le cas échéant.
ms.assetid: 2f85f395-3ec5-4c5a-a6db-c902cb8f8486
title: 'IContextTransactionInfo :: FetchTransaction, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextTransactionInfo.FetchTransaction
api_type:
- COM
api_location: ''
ms.openlocfilehash: 6d673483118feb02ec2f1172640b9972d883505f48bc1fd8d8803844b963b02b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119991059"
---
# <a name="icontexttransactioninfofetchtransaction-method"></a>IContextTransactionInfo :: FetchTransaction, méthode

Récupère la transaction ou le proxy de transaction associé au contexte actuel, le cas échéant.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT FetchTransaction(
  [out, retval] IUnknown **pUnk
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*punk* \[ out, retval\]
</dt> <dd>

Transaction ou proxy de transaction associé au contexte actuel ; Sinon, **null**.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode peut retourner les valeurs de retour standard E \_ INVALIDARG, e \_ OUTOFMEMORY, e \_ inattendue et S \_ OK.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows XP avec les \[ applications de bureau SP2 uniquement\]<br/>          |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 avec les \[ applications de bureau SP1 uniquement\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IContextTransactionInfo**](icontexttransactioninfo.md)
</dt> </dl>

 

 




