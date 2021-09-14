---
title: Méthode IWMDRMEventGenerator CancelAsyncOperation (wmdrmsdk. h)
description: La méthode CancelAsyncOperation annule une opération asynchrone.
ms.assetid: 95c59e03-b6c8-40c2-b1dc-381cb6d8d558
keywords:
- Méthode CancelAsyncOperation format Windows Media
- Méthode CancelAsyncOperation format Windows Media, interface IWMDRMEventGenerator
- Interface IWMDRMEventGenerator Windows Media format, méthode CancelAsyncOperation
topic_type:
- apiref
api_name:
- IWMDRMEventGenerator.CancelAsyncOperation
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1223f56e820eb5927eeb972f28056baa14824774
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127219505"
---
# <a name="iwmdrmeventgeneratorcancelasyncoperation-method"></a>IWMDRMEventGenerator :: CancelAsyncOperation, méthode

La méthode **CancelAsyncOperation** annule une opération asynchrone.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT CancelAsyncOperation(
  [in] IUnknown *punkCancelationCookie
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*punkCancelationCookie* \[ dans\]
</dt> <dd>

Pointeur vers le cookie d’annulation qui identifie l’opération asynchrone à annuler. Ce cookie est fourni par la méthode utilisée pour démarrer l’opération.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Cette méthode retourne un code **HRESULT**. Les valeurs possibles sont notamment celles figurant dans le tableau suivant.



| Code de retour                                                                          | Description                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**\_OK**</dt> </dl> | S_OK<br/> |



 

## <a name="remarks"></a>Notes

Aucun.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|-----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Wmdrmsdk. h</dt> </dl>   |
| Bibliothèque<br/> | <dl> <dt>Wmdrmsdk. lib</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Interface IWMDRMEventGenerator**](iwmdrmeventgenerator.md)
</dt> </dl>

 

 





