---
description: Associe une implémentation de ITransactionProxy avec le contexte actuel.
ms.assetid: 64009632-b536-41fb-95ac-b23e2cbf18da
title: 'IContextTransactionInfo :: RegisterTransactionProxy, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextTransactionInfo.RegisterTransactionProxy
api_type:
- COM
api_location: ''
ms.openlocfilehash: 7b559453b0d4ed75f92f7a421be4c3a47e07fdf7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127517665"
---
# <a name="icontexttransactioninforegistertransactionproxy-method"></a>IContextTransactionInfo :: RegisterTransactionProxy, méthode

Associe une implémentation de [**ITransactionProxy**](/windows/desktop/api/ComSvcs/nn-comsvcs-itransactionproxy) avec le contexte actuel.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT RegisterTransactionProxy(
  [in]  ITransactionProxy *pProxy,
  [out] GUID              *pGuid
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pProxy* \[ dans\]
</dt> <dd>

Implémentation de [**ITransactionProxy**](/windows/desktop/api/ComSvcs/nn-comsvcs-itransactionproxy) à associer au contexte actuel.

</dd> <dt>

*pguid* \[ à\]
</dt> <dd>

GUID qui identifie le proxy de transaction. COM+ utilise ce GUID lors de l’appel de [**ITransactionProxy :: Commit**](/windows/desktop/api/ComSvcs/nf-comsvcs-itransactionproxy-commit) sur le proxy de transaction.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Cette méthode peut retourner les valeurs de retour standard E \_ INVALIDARG, e \_ OUTOFMEMORY et e \_ inattendue, ainsi que les valeurs suivantes.



| Code de retour                                                                                                     | Description                                                                                                             |
|-----------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>                            | La commande s'est correctement terminée.<br/>                                                                           |
| <dl> <dt>**CONTEXTE \_ E \_ ALREADYINTRANSACTION**</dt> </dl> | Le contexte actuel est déjà associé à une implémentation de [**ITransactionProxy**](/windows/desktop/api/ComSvcs/nn-comsvcs-itransactionproxy) .<br/> |
| <dl> <dt>**\_NOTIMPL E**</dt> </dl>                       | Le contexte actuel héberge une transaction BYOT (Bring Your Own Transaction) ou une transaction non racine.<br/>    |



 

## <a name="remarks"></a>Notes

La méthode **RegisterTransactionProxy** peut uniquement être appelée si le contexte actuel est un contexte de transaction racine. Il ne peut pas être appelé si le contexte héberge une transaction BYOT ou une transaction non racine.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows XP avec les \[ applications de bureau SP2 uniquement\]<br/>          |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 avec les \[ applications de bureau SP1 uniquement\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IContextTransactionInfo**](icontexttransactioninfo.md)
</dt> </dl>

 

 




