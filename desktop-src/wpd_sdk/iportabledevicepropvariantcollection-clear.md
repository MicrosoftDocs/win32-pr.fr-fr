---
description: La méthode Clear libère, puis supprime tous les éléments de la collection. La collection est considérée comme vide après l’appel de cette méthode.
ms.assetid: f4b46713-8224-443a-99cc-13fa75e59e5d
title: 'IPortableDevicePropVariantCollection :: Clear, méthode (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDevicePropVariantCollection.Clear
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: fa7c2a8dddeb74b5ac666da2561bd6ee6536821a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526576"
---
# <a name="iportabledevicepropvariantcollectionclear-method"></a>IPortableDevicePropVariantCollection :: Clear, méthode

La méthode **Clear** libère, puis supprime tous les éléments de la collection. La collection est considérée comme vide après l’appel de cette méthode.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT Clear();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

La méthode retourne un **HRESULT**. Les valeurs possibles sont notamment celles figurant dans le tableau suivant.



| Code de retour                                                                          | Description                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**\_OK**</dt> </dl> | S_OK<br/> |



 

## <a name="remarks"></a>Notes

Après l’appel de **Clear**, la collection est considérée comme étant sans type, ce qui signifie que le VarType auquel elle a été précédemment définie ne restreint plus les opérations **Add** . Un appel à **Add** après l’appel de **Clear** est considéré comme « First » **Add** pour cette collection.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>PortableDeviceTypes. h</dt> </dl>   |
| Bibliothèque<br/> | <dl> <dt>PortableDeviceGUIDs. lib</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Interface IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md)
</dt> </dl>

 

 




