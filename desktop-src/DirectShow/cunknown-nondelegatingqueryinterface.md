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
ms.openlocfilehash: b41810eb52db38644bda472907228cd812f76f6a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106521682"
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
| <dl> <dt>**\_OK**</dt> </dl>          | Opération réussie.<br/>                                |
| <dl> <dt>**E \_ NOinterface**</dt> </dl> | L’objet ne prend pas en charge cette interface.<br/> |
| <dl> <dt>**\_pointeur E**</dt> </dl>     | Argument de pointeur **null** .<br/>              |



 

## <a name="remarks"></a>Notes

La classe **CUnknown** expose uniquement l’interface **IUknown** . Substituez cette méthode pour exposer des interfaces supplémentaires. Pour plus d’informations sur la façon de substituer cette méthode, consultez [How to implement IUnknown](how-to-implement-iunknown.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>ComBase. h (include streams. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



 

 




