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
ms.openlocfilehash: 0e753974f93539f051465f13a1ea92d7e0e3bfa1
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127517668"
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

## <a name="return-value"></a>Valeur de retour

Cette méthode peut retourner les valeurs de retour standard E \_ INVALIDARG, e \_ OUTOFMEMORY, e \_ inattendue et S \_ OK.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows XP avec les \[ applications de bureau SP2 uniquement\]<br/>          |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 avec les \[ applications de bureau SP1 uniquement\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IContextTransactionInfo**](icontexttransactioninfo.md)
</dt> </dl>

 

 




