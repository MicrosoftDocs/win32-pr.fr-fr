---
description: La méthode SetBufferValue ajoute une nouvelle valeur d’octet \* (tapez VT \_ Vector \| VT \_ UI1) ou remplace une valeur existante.
ms.assetid: 6c421240-2ff8-4862-bd90-1feee5d15a8d
title: 'IPortableDeviceValues :: SetBufferValue, méthode (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.SetBufferValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: e04b41fdd397d8d03e7e0576d2ba8fb3b6ad1401
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127219412"
---
# <a name="iportabledevicevaluessetbuffervalue-method"></a>IPortableDeviceValues :: SetBufferValue, méthode

La méthode **SetBufferValue** ajoute une nouvelle valeur d' **octet** \* (tapez VT \_ Vector \| VT \_ UI1) ou remplace une valeur existante.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT SetBufferValue(
  [in] REFPROPERTYKEY key,
  [in] BYTE           *pValue,
  [in] DWORD          cbValue
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

**Octet \*** qui contient les données à écrire dans l’élément. Les données de mémoire tampon envoyées sont copiées dans l’interface, de sorte que l’appelant peut libérer cette mémoire tampon après avoir effectué cet appel.

</dd> <dt>

*cbValue* \[ dans\]
</dt> <dd>

Taille de la valeur vers laquelle pointe *pValue*, en octets.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Cette méthode retourne un code **HRESULT**. Les valeurs possibles sont notamment celles figurant dans le tableau suivant.



| Code de retour                                                                          | Description                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**\_OK**</dt> </dl> | S_OK<br/> |



 

## <a name="remarks"></a>Notes

Si une valeur existante a la même clé que celle spécifiée par le paramètre de *clé* , elle remplace la valeur existante sans avertissement. La mémoire clé existante est libérée de manière appropriée.

La définition d’une **valeur null** ou d’une mémoire tampon de taille zéro n’est pas prise en charge.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>PortableDeviceTypes. h</dt> </dl>   |
| Bibliothèque<br/> | <dl> <dt>PortableDeviceGUIDs. lib</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Interface IPortableDeviceValues**](iportabledevicevalues.md)
</dt> <dt>

[**IPortableDeviceValues::GetBufferValue**](iportabledevicevalues-getbuffervalue.md)
</dt> </dl>

 

 




