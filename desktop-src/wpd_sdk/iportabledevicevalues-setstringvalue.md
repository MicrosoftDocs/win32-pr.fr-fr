---
description: La méthode SetStringValue ajoute une nouvelle valeur de chaîne (type VT \_ LPWStr) ou remplace une valeur existante.
ms.assetid: a6eba2b9-de18-431e-874e-af68695e8d3f
title: 'IPortableDeviceValues :: SetStringValue, méthode (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.SetStringValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 0c00195823d71a59e706af1c0a627670f583776140772c3b8634ac10d7d95919
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119806859"
---
# <a name="iportabledevicevaluessetstringvalue-method"></a>IPortableDeviceValues :: SetStringValue, méthode

La méthode **SetStringValue** ajoute une nouvelle valeur de chaîne (type VT \_ LPWStr) ou remplace une valeur existante.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT SetStringValue(
  [in] REFPROPERTYKEY key,
  [in] LPCWSTR        Value
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

**LPCWSTR** qui spécifie la nouvelle valeur. La chaîne étant copiée, l’appelant peut libérer la mémoire allouée pour cette valeur après l’appel de cette méthode.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode retourne un code **HRESULT**. Les valeurs possibles sont notamment celles figurant dans le tableau suivant.



| Code de retour                                                                          | Description                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**\_OK**</dt> </dl> | S_OK<br/> |



 

## <a name="remarks"></a>Remarques

Toute mémoire de clé existante sera libérée de manière appropriée.

## <a name="examples"></a>Exemples

Pour obtenir un exemple d’utilisation de cette méthode, consultez [spécification des informations sur le client](specifying-client-information.md).

## <a name="requirements"></a>Configuration requise



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

[**IPortableDeviceValues :: GetStringValue**](iportabledevicevalues-getstringvalue.md)
</dt> <dt>

[Définition des propriétés d’un objet unique](setting-properties-for-a-single-object.md)
</dt> <dt>

[Définition des propriétés de plusieurs objets](setting-properties-for-multiple-objects.md)
</dt> <dt>

[Spécification des informations sur le client](specifying-client-information.md)
</dt> <dt>

[Écriture de propriétés Content-Object](writing-content-object-properties.md)
</dt> </dl>

 

 




