---
description: La méthode GetPropById de l’objet DeviceInfo utilise l’ID d’une propriété d’appareil pour retourner sa valeur.
ms.assetid: 9c68e6af-446c-4750-89e6-70862b23b296
title: Méthode DeviceInfo. GetPropById
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DeviceInfo.GetPropById
api_type:
- COM
api_location:
- Wiascr.dll
ms.openlocfilehash: c996989661703c4a9c7416cd63904c376fdb7fcca3071d4558551bdd78470d3a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118208785"
---
# <a name="deviceinfogetpropbyid-method"></a>Méthode DeviceInfo. GetPropById

La méthode **GetPropById** de l’objet [**DEVICEINFO**](-wia-deviceinfo.md) utilise l’ID d’une propriété d’appareil pour retourner sa valeur.

## <a name="syntax"></a>Syntaxe


```JScript
retVal = DeviceInfo.GetPropById(
  Id
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*ID* \[ dans\]
</dt> <dd>

Type : **[WiaDeviceInfoPropertyId](-wia-wiadeviceinfopropertyid.md)**

Spécifie l’ID de la propriété.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **variante**

Cette méthode retourne la valeur de la propriété spécifiée par *ID*.

## <a name="remarks"></a>Remarques

Utilisez cette méthode pour rechercher la valeur d’une propriété d’appareil à partir de son ID. Pour obtenir la liste des ID de propriété, consultez [définitions de constante de propriété WIA](-wia-wia-property-constant-definitions.md). pour plus d’informations sur les propriétés d’Acquisition d’images (wia) Windows elles-mêmes, consultez [constantes de propriété wia](-wia-wia-property-constants.md).

pour les applications Microsoft Visual Basic, ajoutez une référence à « Windows bibliothèque de types d’Acquisition d’Image 1,01 ». Les constantes suivantes définies dans ce fichier sont valides pour cette méthode :

``` syntax
const DeviceID = 2
const Manufacturer = 3
const Description = 4
const Type = 5
const Port = 6
const Name = 7
const Server = 8
const RemoteDevID = 9
const UIClassID = 10
```

## <a name="examples"></a>Exemples

L’exemple suivant illustre l’utilisation de la méthode **GetPropById** pour récupérer une valeur de propriété.


```JScript
<SCRIPT LANGUAGE="VBScript">
const WIA_DIP_DEV_TYPE = 5
Dim objWia
Dim objDeviceInfoCollection
Dim objDeviceInfo
Dim PropValue
 
Set objWIA = CreateObject("Wia.Script")
 
Set objDeviceInfoCollection = objWia.Devices
 
For Each objDeviceInfo In objDeviceInfoCollection
    PropValue = objDeviceInfo.GetPropById(WIA_DIP_DEV_TYPE)
Next
</SCRIPT>
```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professional, Windows XP \[ desktop apps uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Wiascr.dll (version 4,90 ou ultérieure)</dt> </dl> |



 

 




