---
description: La méthode SetKeyValue ajoute une nouvelle valeur REFPROPERTYKEY (type VT \_ inconnu) ou remplace celle qui existe déjà.
ms.assetid: 344c52ec-91b1-43f9-b16a-28c24971d805
title: 'IPortableDeviceValues :: SetKeyValue, méthode (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.SetKeyValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: ae55b47687043bba92afbab09f25de8a5fc679d7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127404429"
---
# <a name="iportabledevicevaluessetkeyvalue-method"></a>IPortableDeviceValues :: SetKeyValue, méthode

La méthode **SetKeyValue** ajoute une nouvelle valeur **REFPROPERTYKEY** (type VT \_ inconnu) ou remplace celle qui existe déjà.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT SetKeyValue(
  [in] REFPROPERTYKEY key,
  [in] REFPROPERTYKEY Value
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*clé* \[ dans\]
</dt> <dd>

**REFPROPERTYKEY** qui spécifie l’élément à créer ou à remplacer.

</dd> <dt>

*Valeur* \[ dans\]
</dt> <dd>

**REFPROPERTYKEY** qui spécifie la nouvelle valeur.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Cette méthode retourne un code **HRESULT**. Les valeurs possibles sont notamment celles figurant dans le tableau suivant.



| Code de retour                                                                          | Description                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**\_OK**</dt> </dl> | S_OK<br/> |



 

## <a name="remarks"></a>Notes

Si une valeur existante a la même clé que celle spécifiée par le paramètre de *clé* , elle remplace la valeur existante sans avertissement. La mémoire clé existante est libérée de manière appropriée.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>PortableDeviceTypes. h</dt> </dl>   |
| Bibliothèque<br/> | <dl> <dt>PortableDeviceGUIDs. lib</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Ajout d’une ressource à un objet](adding-a-resource-to-an-object.md)
</dt> <dt>

[**Interface IPortableDeviceValues**](iportabledevicevalues.md)
</dt> <dt>

[**IPortableDeviceValues::GetKeyValue**](iportabledevicevalues-getkeyvalue.md)
</dt> </dl>

 

 




