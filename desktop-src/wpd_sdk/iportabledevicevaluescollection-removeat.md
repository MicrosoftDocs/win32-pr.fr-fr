---
description: 'IPortableDeviceValuesCollection :: RemoveAt, méthode-la méthode RemoveAt supprime l’élément stocké à l’emplacement spécifié par l’index donné.'
ms.assetid: 380212b6-5e71-406b-8236-e06672505f17
title: 'IPortableDeviceValuesCollection :: RemoveAt, méthode (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValuesCollection.RemoveAt
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 7db15480906bee8181bb0fc589c4f3e30ce4753c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127234480"
---
# <a name="iportabledevicevaluescollectionremoveat-method"></a>IPortableDeviceValuesCollection :: RemoveAt, méthode

La méthode **RemoveAt** supprime l’élément stocké à l’emplacement spécifié par l’index donné.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT RemoveAt(
  [in] const DWORD dwIndex
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*dwIndex* \[ dans\]
</dt> <dd>

Spécifie l’index de l’élément à supprimer.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Cette méthode retourne un code **HRESULT**. Les valeurs possibles sont notamment celles figurant dans le tableau suivant.



| Code de retour                                                                                  | Description                                      |
|----------------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>         | S_OK<br/>                 |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | L’index spécifié était hors limites.<br/> |



 

## <a name="remarks"></a>Notes

Vous devez spécifier un index de base zéro.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>PortableDeviceTypes. h</dt> </dl>   |
| Bibliothèque<br/> | <dl> <dt>PortableDeviceGUIDs. lib</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Interface IPortableDeviceValuesCollection**](iportabledevicevaluescollection.md)
</dt> </dl>

 

 




