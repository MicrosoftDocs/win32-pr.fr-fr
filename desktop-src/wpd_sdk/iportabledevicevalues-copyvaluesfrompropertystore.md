---
description: La méthode CopyValuesFromPropertyStore copie le contenu d’un IPropertyStore dans la collection.
ms.assetid: 887c9569-ff76-41cf-8782-62c59c04e831
title: 'IPortableDeviceValues :: CopyValuesFromPropertyStore, méthode (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.CopyValuesFromPropertyStore
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: fbc2508d300fe4d0680d539153fde5f86603e04d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106533154"
---
# <a name="iportabledevicevaluescopyvaluesfrompropertystore-method"></a>IPortableDeviceValues :: CopyValuesFromPropertyStore, méthode

La méthode **CopyValuesFromPropertyStore** copie le contenu d’un **IPropertyStore** dans la collection.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT CopyValuesFromPropertyStore(
  [in] IPropertyStore *pStore
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pStore* \[ dans\]
</dt> <dd>

Pointeur vers un **IPropertyStore** à copier dans la collection.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

La méthode retourne un **HRESULT**. Les valeurs possibles sont notamment celles figurant dans le tableau suivant.



| Code de retour                                                                          | Description                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**\_OK**</dt> </dl> | S_OK<br/> |



 

## <a name="remarks"></a>Notes

Cette méthode convertit automatiquement toutes les valeurs **VT \_ BSTR** en valeurs **VT \_ LPWStr** .

De nombreuses applications ou composants externes qui communiquent avec votre application, tels que certaines applications de l’interpréteur de commandes, utilisent l’interface **IPropertyStore** . Cette méthode offre un moyen simple et rapide d’échanger des données avec ces programmes.

Cette méthode est prise en charge dans Windows Vista et les versions ultérieures de Windows.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>PortableDeviceTypes. h</dt> </dl>   |
| Bibliothèque<br/> | <dl> <dt>PortableDeviceGUIDs. lib</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Interface IPortableDeviceValues**](iportabledevicevalues.md)
</dt> <dt>

[**IPortableDeviceValues::CopyValuesToPropertyStore**](iportabledevicevalues-copyvaluestopropertystore.md)
</dt> </dl>

 

 




