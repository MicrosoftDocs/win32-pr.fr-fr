---
description: Récupère le niveau d’isolation et la valeur de délai d’attente d’une transaction qui est hébergée dans le contexte de transaction racine.
ms.assetid: bb3ff03e-e69e-4a50-af36-4938eb4323df
title: 'IContextTransactionInfo :: GetTxIsolationLevelAndTimeout, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextTransactionInfo.GetTxIsolationLevelAndTimeout
api_type:
- COM
api_location: ''
ms.openlocfilehash: b8545a697e672af7206a69ffa19618d5b70e055c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127008186"
---
# <a name="icontexttransactioninfogettxisolationlevelandtimeout-method"></a>IContextTransactionInfo :: GetTxIsolationLevelAndTimeout, méthode

Récupère le niveau d’isolation et la valeur de délai d’attente d’une transaction qui est hébergée dans le contexte de transaction racine.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetTxIsolationLevelAndTimeout(
  [out] ISOLEVEL *pIsoLevel,
  [out] DWORD    *dwTime
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pIsoLevel* \[ à\]
</dt> <dd>

Valeur [ISOLATIONLEVEL](/previous-versions/windows/desktop/ms679234(v=vs.85)) de la transaction.

</dd> <dt>

*dwTime* \[ à\]
</dt> <dd>

Délai d’expiration de la transaction, en secondes.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

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

 

