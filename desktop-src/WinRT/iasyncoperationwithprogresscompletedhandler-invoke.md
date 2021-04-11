---
description: Appelle la méthode qui est appelée lorsque l’opération asynchrone spécifiée signale la progression.
ms.assetid: FB60DDC0-7521-4999-8DD8-175556004198
title: 'IAsyncOperationWithProgressCompletedHandler<TResult, TProgress> :: Invoke, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAsyncOperationWithProgressCompletedHandler<TResult,TProgress>.Invoke
api_type:
- COM
api_location: ''
ms.openlocfilehash: 469686cbd96dedc7f816fdd1f482d3474362688e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113119"
---
# <a name="iasyncoperationwithprogresscompletedhandlertresulttprogressinvoke-method"></a>IAsyncOperationWithProgressCompletedHandler<TResult, TProgress> :: Invoke, méthode

Appelle la méthode qui est appelée lorsque l’opération asynchrone spécifiée signale la progression.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT Invoke(
  [in] IAsyncOperationWithProgress<TResult,TProgress> *asyncInfo
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*asyncInfo* \[ dans\]
</dt> <dd>

Type : **[**IAsyncOperationWithProgress<TResult, TProgress>**](/previous-versions//br205807(v=vs.85)) \** _

Action asynchrone qui signale la fin de l’opération.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : _ *HRESULT**

Si cette méthode est réussie, elle retourne la valeur **\_ OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------|
| Client minimal pris en charge<br/> | Windows 8<br/>           |
| Serveur minimal pris en charge<br/> | Windows Server 2012<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IAsyncOperationWithProgressCompletedHandler<TResult, TProgress>**](/previous-versions//br205808(v=vs.85))
</dt> </dl>

 

 
