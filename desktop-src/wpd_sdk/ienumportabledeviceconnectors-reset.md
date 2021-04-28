---
description: 'IEnumPortableDeviceConnectors :: Reset, méthode-réinitialise la séquence d’énumération au début.'
ms.assetid: 1df1ff95-06ae-4e5e-8064-17f832c5f0b3
title: 'IEnumPortableDeviceConnectors :: Reset, méthode (Devpkey. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumPortableDeviceConnectors.Reset
api_type:
- COM
api_location:
- PortableDeviceGuids.lib
- PortableDeviceGuids.dll
ms.openlocfilehash: 10a356fbb8591568a9f99d9b92d681a46754a960
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108083206"
---
# <a name="ienumportabledeviceconnectorsreset-method"></a>IEnumPortableDeviceConnectors :: Reset, méthode

La méthode **Reset** réinitialise la séquence d’énumération au début.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT Reset();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur renvoyée

La méthode retourne un **HRESULT**. Les valeurs possibles sont notamment celles figurant dans le tableau suivant.



| Code de retour                                                                          | Description                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**\_OK**</dt> </dl> | S_OK<br/> |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 7 uniquement\]<br/>                                                                                                                             |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                                                                                              |
| En-tête<br/>                   | <dl> <dt>Devpkey. h ; </dt> <dt>PortableDeviceConnectApi. h</dt> </dl> |
| MIDL<br/>                      | <dl> <dt>PortableDeviceConnectApi. idl</dt> </dl>                                                                |
| Bibliothèque<br/>                  | <dl> <dt>PortableDeviceGuids. lib</dt> </dl>                                                                     |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IEnumPortableDeviceConnectors**](ienumportabledeviceconnectors.md)
</dt> </dl>

 

 




