---
description: la méthode Connecter effectue une connexion à la broche de sortie.
ms.assetid: fb20ef5d-e00a-4154-a6da-25bef663c0e7
title: CPullPin. méthode Connecter (Pullpin. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPullPin.Connect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 37240be1b732410d1e91974922f8ed7dc464b57b2596faa381c646a7513daf26
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119073503"
---
# <a name="cpullpinconnect-method"></a>CPullPin. méthode Connecter

La `Connect` méthode termine une connexion à la broche de sortie.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT Connect(
   IUnknown      *pUnk,
   IMemAllocator *pAlloc,
   BOOL          bSync
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pUnk* 
</dt> <dd>

Pointeur vers l’interface **IUnknown** de la broche de sortie.

</dd> <dt>

*pAlloc* 
</dt> <dd>

Pointeur vers l’interface [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) de l’allocateur préféré du code confidentiel d’entrée, ou **null**.

</dd> <dt>

*bSync* 
</dt> <dd>

Valeur booléenne qui spécifie s’il faut utiliser des lectures synchrones. Si la **valeur est true**, le code PIN effectue des opérations de lecture synchrones sur la broche de sortie. Si la **valeur est false**, le code PIN effectue des requêtes de lecture asynchrones.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne un **HRESULT**. Les valeurs possibles sont les suivantes.



| Code de retour                                                                                               | Description                                                                     |
|-----------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>                      | Réussite.<br/>                                                             |
| <dl> <dt>**VFW \_ E \_ déjà \_ connecté**</dt> </dl> | La broche d’entrée est déjà connectée.<br/>                                  |
| <dl> <dt>**E \_ NOinterface**</dt> </dl>             | La broche de sortie n’expose pas [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader).<br/> |



 

## <a name="remarks"></a>Remarques

Appelez cette méthode pendant le processus de connexion du code confidentiel d’entrée. Si la méthode échoue, le code PIN doit faire échouer la connexion.

Cette méthode interroge la broche de sortie pour l’interface **IAsyncReader** . En cas de réussite, elle appelle [**CPullPin ::D ecideallocator**](cpullpin-decideallocator.md) pour négocier l’allocateur pour la connexion. Si votre code pin d’entrée a un allocateur préféré, spécifiez-le dans le paramètre *pAlloc* ; la méthode **DecideAllocator** transmet ce pointeur à la méthode [**IAsyncReader :: RequestAllocator**](/windows/desktop/api/Strmif/nf-strmif-iasyncreader-requestallocator) de la broche de sortie. Sinon, affectez à *pAlloc* la **valeur null**.

Si la valeur de *bSync* est **true**, l’objet **CPullPin** effectue des requêtes de lecture synchrones, en appelant le [**IAsyncReader :: SyncReadAligned**](/windows/desktop/api/Strmif/nf-strmif-iasyncreader-syncreadaligned)de la broche de sortie. Sinon, elle appelle la méthode [**IAsyncReader :: Request**](/windows/desktop/api/Strmif/nf-strmif-iasyncreader-request) pour effectuer le chevauchement des demandes de lecture.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Pullpin. h</dt> </dl>                                                                                                       |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CPullPin, classe**](cpullpin.md)
</dt> </dl>

 

 




