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
ms.openlocfilehash: adbc8b6a29f97066c8dc5b2e45b7ddc5834f2b60
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106527904"
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

## <a name="remarks"></a>Notes

Utilisez cette méthode pour rechercher la valeur d’une propriété d’appareil à partir de son ID. Pour obtenir la liste des ID de propriété, consultez [définitions de constante de propriété WIA](-wia-wia-property-constant-definitions.md). Pour plus d’informations sur les propriétés WIA (Windows Image Acquisition) elles-mêmes, consultez [constantes de propriété WIA](-wia-wia-property-constants.md).

Pour les applications Microsoft Visual Basic, ajoutez une référence à « Bibliothèque de types Windows Image Acquisition 1,01 ». Les constantes suivantes définies dans ce fichier sont valides pour cette méthode :

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
| Client minimal pris en charge<br/> | Windows 2000 professionnel, applications de \[ Bureau Windows XP uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Wiascr.dll (version 4,90 ou ultérieure)</dt> </dl> |



 

 




