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
ms.openlocfilehash: 0944edff81a62652851bc2c18b58f47f5d33d09ad7da6ba5a2eda95919c54dd2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118963708"
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

Cette méthode retourne un code **HRESULT**. Les valeurs possibles sont notamment celles figurant dans le tableau suivant.



| Code de retour                                                                          | Description                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**\_OK**</dt> </dl> | S_OK<br/> |



 

## <a name="remarks"></a>Remarques

Cette méthode convertit automatiquement toutes les valeurs **VT \_ BSTR** en valeurs **VT \_ LPWStr** .

De nombreuses applications ou composants externes qui communiquent avec votre application, tels que certaines applications de l’interpréteur de commandes, utilisent l’interface **IPropertyStore** . Cette méthode offre un moyen simple et rapide d’échanger des données avec ces programmes.

cette méthode est prise en charge dans Windows Vista et les versions ultérieures de Windows.

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

 

 




