---
description: 'Récupère un pointeur d’interface et incrémente le décompte de références. Cette méthode implémente la méthode INonDelegatingUnknown :: NonDelegatingQueryInterface.'
ms.assetid: 451ca350-f40b-4cbf-ac39-e86dadb48a24
title: Méthode CUnknown. NonDelegatingQueryInterface (ComBase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CUnknown.NonDelegatingQueryInterface
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 26e13d9d30c3da208bb702427ee99a9648a7f538ba0d5a6a1b359db41e2cd155
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120076009"
---
# <a name="cunknownnondelegatingqueryinterface-method"></a>Méthode CUnknown. NonDelegatingQueryInterface

Récupère un pointeur d’interface et incrémente le décompte de références. Cette méthode implémente la méthode **INonDelegatingUnknown :: NonDelegatingQueryInterface** .

## <a name="syntax"></a>Syntaxe


```C++
HRESULT NonDelegatingQueryInterface(
   REFIID riid,
   void   **ppv
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*riid* 
</dt> <dd>

Identificateur de l’interface.

</dd> <dt>

*ppv* 
</dt> <dd>

Adresse d’un pointeur pour recevoir l’interface.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne l’une des valeurs **HRESULT** indiquées dans le tableau suivant.



| Code de retour                                                                                   | Description                                        |
|-----------------------------------------------------------------------------------------------|----------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>          | Réussite.<br/>                                |
| <dl> <dt>**E \_ NOinterface**</dt> </dl> | L’objet ne prend pas en charge cette interface.<br/> |
| <dl> <dt>**\_pointeur E**</dt> </dl>     | Argument de pointeur **null** .<br/>              |



 

## <a name="remarks"></a>Remarques

La classe **CUnknown** expose uniquement l’interface **IUknown** . Substituez cette méthode pour exposer des interfaces supplémentaires. Pour plus d’informations sur la façon de substituer cette méthode, consultez [How to implement IUnknown](how-to-implement-iunknown.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>combase. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



 

 




