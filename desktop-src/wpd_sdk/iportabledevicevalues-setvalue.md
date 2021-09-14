---
description: La méthode SetValue ajoute une nouvelle valeur PROPVARIANT ou remplace celle qui existe déjà.
ms.assetid: 69630a21-79e9-4c96-8ed7-9a41ebb991cd
title: 'IPortableDeviceValues :: SetValue, méthode (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.SetValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 4c2ba6c5b6f015e5961356ff8e246605bfeddd31
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127234486"
---
# <a name="iportabledevicevaluessetvalue-method"></a>IPortableDeviceValues :: SetValue, méthode

La méthode **SetValue** ajoute une nouvelle valeur **PROPVARIANT** ou remplace celle qui existe déjà.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT SetValue(
  [in]       REFPROPERTYKEY key,
  [in] const PROPVARIANT    *pValue
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*clé* \[ dans\]
</dt> <dd>

**REFPROPERTYKEY** qui spécifie l’élément à créer ou à remplacer.

</dd> <dt>

*pValue* \[ dans\]
</dt> <dd>

**PROPVARIANT** qui spécifie la nouvelle valeur. Le kit de développement logiciel (SDK) copie la valeur, de sorte que l’appelant peut libérer la variable locale en appelant **PropVariantClear** après avoir appelé cette méthode.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Cette méthode retourne un code **HRESULT**. Les valeurs possibles sont notamment celles figurant dans le tableau suivant.



| Code de retour                                                                          | Description                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**\_OK**</dt> </dl> | S_OK<br/> |



 

## <a name="remarks"></a>Notes

Lorsque le VARTYPE de *pValue* est VT \_ Vector ou VT \_ UI1, la définition  d’une mémoire tampon de taille zéro ou nulle n’est pas prise en charge. Par exemple, ni pValue. CAUB. pElems = **null** , ni pValue. CAUB. cElems = 0 n’est autorisé.

Cette méthode peut être utilisée pour récupérer une valeur de n’importe quel type de la collection. Toutefois, si vous connaissez le type de valeur à l’avance, utilisez l’une des méthodes **Set...** spécialisées de cette interface pour éviter la surcharge liée à l’utilisation directe des valeurs PROPVARIANT.

Si une valeur existante a la même clé que celle spécifiée par le paramètre de *clé* , elle remplace la valeur existante sans avertissement. La mémoire clé existante est libérée de manière appropriée.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>PortableDeviceTypes. h</dt> </dl>   |
| Bibliothèque<br/> | <dl> <dt>PortableDeviceGUIDs. lib</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Interface IPortableDeviceValues**](iportabledevicevalues.md)
</dt> <dt>

[**IPortableDeviceValues :: GetValue**](iportabledevicevalues-getvalue.md)
</dt> <dt>

[**IPortableDeviceValues::RemoveValue**](iportabledevicevalues-removevalue.md)
</dt> </dl>

 

 




