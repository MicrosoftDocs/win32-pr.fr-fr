---
description: L’interface IPortableDeviceValues contient une collection de paires PROPERTYKEY/PROPVARIANT.
ms.assetid: a73cbb4e-15d2-4c8d-9267-aaec9a0fd09f
title: Interface IPortableDeviceValues (PortableDeviceTypes. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 7f7aaceff66cd817666dd05b92243239f860b2f59a993e4afca1831fc8085de0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119929999"
---
# <a name="iportabledevicevalues-interface"></a>Interface IPortableDeviceValues

L’interface **IPortableDeviceValues** contient une collection de paires **PROPERTYKEY** / **PROPVARIANT** . Les valeurs de la collection n’ont pas besoin d’être du même VARTYPE.

Les valeurs sont stockées sous forme de paires clé-valeur. chaque clé doit être unique dans la collection. Les clients peuvent rechercher des éléments par **PROPERTYKEY** ou un index de base zéro. Les valeurs de données sont stockées en tant que structures **PROPVARIANT** . Vous pouvez ajouter ou récupérer des valeurs de n’importe quel type à l’aide des méthodes génériques **SetValue** et **GetValue**, ou vous pouvez ajouter des éléments à l’aide de la méthode propre au type de données ajoutées.

Les méthodes **obten...** requièrent que l’appelant libère toutes les valeurs récupérées de manière appropriée. Les méthodes **Set...** copient la valeur dans la collection.

Quand une interface **IPortableDeviceValues** est libérée, elle appelle **Clear**, qui libère la mémoire allouée pour tous ses membres de manière appropriée.

Cette interface peut être récupérée à partir d’une méthode ou, si un nouvel objet est requis, appeler **CoCreate** avec **CLSID \_ PortableDeviceValues**.

## <a name="members"></a>Membres

L’interface **IPortableDeviceValues** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **IPortableDeviceValues** a également les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **IPortableDeviceValues** possède ces méthodes.



| Méthode                                                                                                                     | Description                                                                                                            |
|:---------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------|
| [**Effacer**](iportabledevicevalues-clear.md)                                                                               | Supprime tous les éléments de la collection.<br/>                                                                      |
| [**CopyValuesFromPropertyStore**](iportabledevicevalues-copyvaluesfrompropertystore.md)                                   | Copie le contenu d’un **IPropertyStore** dans la collection.<br/>                                           |
| [**CopyValuesToPropertyStore**](iportabledevicevalues-copyvaluestopropertystore.md)                                       | Copie toutes les valeurs d’une collection dans une interface **IPropertyStore** .<br/>                               |
| [**GetAt**](iportabledevicevalues-getat.md)                                                                               | Récupère une valeur de la collection à l’aide de l’index de base zéro fourni.<br/>                                  |
| [**GetBoolValue**](iportabledevicevalues-getboolvalue.md)                                                                 | Récupère une valeur **bool** (type VT \_ bool) spécifiée par une clé.<br/>                                              |
| [**GetBufferValue**](iportabledevicevalues-getbuffervalue.md)                                                             | Récupère une valeur de tableau d’octets (type \_ VT \| VT \_ UI1) spécifiée par une clé.<br/>                               |
| [**GetCount**](iportabledevicevalues-getcount.md)                                                                         | Récupère le nombre d’éléments dans la collection.<br/>                                                            |
| [**GetErrorValue**](iportabledevicevalues-geterrorvalue.md)                                                               | Récupère une valeur **HRESULT** (type VT \_ Error) spécifiée par une clé.<br/>                                         |
| [**GetFloatValue**](iportabledevicevalues-getfloatvalue.md)                                                               | Récupère une valeur **flottante** (type VT \_ R4) spécifiée par une clé.<br/>                                               |
| [**GetGuidValue**](iportabledevicevalues-getguidvalue.md)                                                                 | Récupère une valeur **GUID** (type VT \_ CLSID) spécifiée par une clé.<br/>                                             |
| [**GetIPortableDeviceKeyCollectionValue**](iportabledevicevalues-getiportabledevicekeycollectionvalue.md)                 | Récupère une valeur **IPortableDeviceKeyCollection** (type VT \_ inconnu) spécifiée par une clé.<br/>                  |
| [**GetIPortableDevicePropVariantCollectionValue**](iportabledevicevalues-getiportabledevicepropvariantcollectionvalue.md) | Récupère une valeur **IPortableDevicePropVariantCollection** (type VT \_ inconnu) spécifiée par une clé.<br/>          |
| [**GetIPortableDeviceValuesCollectionValue**](iportabledevicevalues-getiportabledevicevaluescollectionvalue.md)           | Récupère une valeur **IPortableDeviceValuesCollection** (type VT \_ inconnu) spécifiée par une clé.<br/>               |
| [**GetIPortableDeviceValuesValue**](iportabledevicevalues-getiportabledevicevaluesvalue.md)                               | Récupère une valeur **IPortableDeviceValues** (type VT \_ inconnu) spécifiée par une clé.<br/>                         |
| [**GetIUnknownValue**](iportabledevicevalues-getiunknownvalue.md)                                                         | Récupère une valeur d’interface **IUnknown** (type VT \_ inconnu) spécifiée par une clé.<br/>                            |
| [**GetKeyValue**](iportabledevicevalues-getkeyvalue.md)                                                                   | Récupère une valeur **PROPERTYKEY** spécifiée par une clé.<br/>                                                       |
| [**GetSignedIntegerValue**](iportabledevicevalues-getsignedintegervalue.md)                                               | Récupère une valeur de type **long** (type VT \_ I4) spécifiée par une clé.<br/>                                                |
| [**GetSignedLargeIntegerValue**](iportabledevicevalues-getsignedlargeintegervalue.md)                                     | Récupère une valeur **LongLong** (type VT \_ I8) spécifiée par une clé.<br/>                                            |
| [**GetStringValue**](iportabledevicevalues-getstringvalue.md)                                                             | Récupère une valeur de chaîne (type VT \_ LPWStr) spécifiée par une clé.<br/>                                              |
| [**GetUnsignedIntegerValue**](iportabledevicevalues-getunsignedintegervalue.md)                                           | Récupère une valeur **ULong** (type VT \_ UI4) spécifiée par une clé.<br/>                                              |
| [**GetUnsignedLargeIntegerValue**](iportabledevicevalues-getunsignedlargeintegervalue.md)                                 | Récupère une valeur **ULONGLONG** (type VT \_ UI8) spécifiée par une clé.<br/>                                          |
| [**GetValue**](iportabledevicevalues-getvalue.md)                                                                         | Récupère une valeur **PROPVARIANT** spécifiée par une clé.<br/>                                                       |
| [**RemoveValue**](iportabledevicevalues-removevalue.md)                                                                   | Supprime un élément de la collection.<br/>                                                                        |
| [**SetBoolValue,**](iportabledevicevalues-setboolvalue.md)                                                                 | Ajoute une nouvelle valeur **booléenne** (type VT \_ bool) ou remplace une valeur existante.<br/>                                 |
| [**SetBufferValue**](iportabledevicevalues-setbuffervalue.md)                                                             | Ajoute une nouvelle valeur d' **octet** \* (type \_ VT \| VT \_ UI1) ou remplace celle qui existe déjà.<br/>                     |
| [**SetErrorValue**](iportabledevicevalues-seterrorvalue.md)                                                               | Ajoute une nouvelle valeur **HRESULT** (type VT \_ Error) ou remplace une valeur existante.<br/>                                |
| [**SetFloatValue**](iportabledevicevalues-setfloatvalue.md)                                                               | Ajoute une nouvelle valeur **flottante** (type VT \_ R4) ou remplace une valeur existante.<br/>                                     |
| [**SetGuidValue**](iportabledevicevalues-setguidvalue.md)                                                                 | Ajoute une nouvelle valeur de **GUID** (type VT \_ CLSID) ou remplace une valeur existante.<br/>                                   |
| [**SetIPortableDeviceKeyCollectionValue**](iportabledevicevalues-setiportabledevicekeycollectionvalue.md)                 | Ajoute une nouvelle valeur **IPortableDeviceKeyCollectionValue** (type VT \_ inconnu) ou remplace celle qui existe déjà.<br/>    |
| [**SetIPortableDevicePropVariantCollectionValue**](iportabledevicevalues-setiportabledevicepropvariantcollectionvalue.md) | Ajoute une nouvelle valeur **IPortableDevicePropVariantCollection** (type VT \_ inconnu) ou remplace celle qui existe déjà.<br/> |
| [**SetIPortableDeviceValuesCollectionValue**](iportabledevicevalues-setiportabledevicevaluescollectionvalue.md)           | Ajoute une nouvelle valeur **IPortableDeviceValuesCollection** (type VT \_ inconnu) ou remplace celle qui existe déjà.<br/>      |
| [**SetIPortableDeviceValuesValue**](iportabledevicevalues-setiportabledevicevaluesvalue.md)                               | Ajoute une nouvelle valeur **IPortableDeviceValues** (type VT \_ inconnu) ou remplace celle qui existe déjà.<br/>                |
| [**SetIUnknownValue**](iportabledevicevalues-setiunknownvalue.md)                                                         | Ajoute une nouvelle valeur **IUnknown** (type VT \_ inconnu) ou remplace une valeur existante.<br/>                             |
| [**SetKeyValue**](iportabledevicevalues-setkeyvalue.md)                                                                   | Ajoute une nouvelle valeur **PROPERTYKEY** (type VT \_ inconnu) ou remplace celle qui existe déjà.<br/>                          |
| [**SetSignedIntegerValue**](iportabledevicevalues-setsignedintegervalue.md)                                               | Ajoute une nouvelle valeur **long** (type VT \_ I4) ou remplace une valeur existante.<br/>                                      |
| [**SetSignedLargeIntegerValue**](iportabledevicevalues-setsignedlargeintegervalue.md)                                     | Ajoute une nouvelle valeur **LongLong** (type VT \_ I8) ou remplace une valeur existante.<br/>                                  |
| [**SetStringValue**](iportabledevicevalues-setstringvalue.md)                                                             | Ajoute une nouvelle valeur de chaîne (type VT \_ LPWStr) ou remplace une valeur existante.<br/>                                    |
| [**SetUnsignedIntegerValue**](iportabledevicevalues-setunsignedintegervalue.md)                                           | Ajoute une nouvelle valeur **ULong** (type VT \_ UI4) ou remplace une valeur existante.<br/>                                    |
| [**SetUnsignedLargeIntegerValue**](iportabledevicevalues-setunsignedlargeintegervalue.md)                                 | Ajoute une nouvelle valeur **ULONGLONG** (type VT \_ UI8) ou remplace une valeur existante.<br/>                                |
| [**SetValue**](iportabledevicevalues-setvalue.md)                                                                         | Ajoute une nouvelle valeur **PROPVARIANT** ou remplace une valeur existante.<br/>                                             |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>PortableDeviceTypes. h</dt> </dl>   |
| Bibliothèque<br/> | <dl> <dt>PortableDeviceGUIDs. lib</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Interfaces de collection**](collection-interfaces.md)
</dt> </dl>

 

