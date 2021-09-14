---
description: La méthode GetPropById de l’objet Item utilise l’ID d’une propriété Item pour retourner sa valeur.
ms.assetid: 00f7a91c-fd55-4016-a932-f710045a14b8
title: Item. GetPropById, méthode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Item.GetPropById
api_type:
- COM
api_location:
- Wiascr.dll
ms.openlocfilehash: 54eb329d51005893b89a9fd28f160ff616e682df
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127231054"
---
# <a name="itemgetpropbyid-method"></a>Item. GetPropById, méthode

La méthode **GetPropById** de l’objet [**Item**](-wia-item.md) utilise l’ID d’une propriété Item pour retourner sa valeur.

## <a name="syntax"></a>Syntaxe


```JScript
retVal = Item.GetPropById(
  Id
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*ID* \[ dans\]
</dt> <dd>

Type : **[WiaItemPropertyId](-wia-wiaitempropertyid.md)**

Spécifie l’ID de la propriété.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Type : **variante**

Cette méthode retourne la valeur de la propriété spécifiée par *ID*.

## <a name="remarks"></a>Notes

Utilisez cette méthode pour rechercher la valeur d’une propriété d’élément à partir de son ID. Pour obtenir la liste des ID de propriété, consultez [définitions de constante de propriété WIA](-wia-wia-property-constant-definitions.md). Pour plus d’informations sur les propriétés elles-mêmes, consultez [constantes de propriété WIA](-wia-wia-property-constants.md).

pour les applications Microsoft Visual Basic, ajoutez une référence à « Windows bibliothèque de types d’Acquisition d’Image 1,01 ». Les constantes suivantes définies dans ce fichier sont valides uniquement pour les éléments racine (éléments de périphérique) :

``` syntax
const FirmwareVersion = 1026
const ConnectStatus = 1027
const DeviceTime = 1028
const PicturesTaken = 2050
const PicturesRemaining = 2051
const ExposureMode = 2052
const ExposureCompensation = 2053
const ExposureTime = 2054
const FNumber = 2055
const FlashMode = 2056
const FocusMode = 2057
const FocusManualDist = 2058
const ZoomPosition = 2059
const PanPosition = 2060
const TiltPostion = 2061
const TimerMode = 2062
const TimerValue = 2063
const PowerMode = 2064
const BatteryStatus = 2065
const Dimension = 2070
const HorizontalBedSize = 3074
const VerticalBedSize = 3075
const HorizontalSheetFeedSize = 3076
const VerticalSheetFeedSize = 3077
const SheetFeederRegistration = 3078
const HorizontalBedRegistration = 3079
const VerticalBedRegistraion = 3080
const PlatenColor = 3081
const PadColor = 3082
const FilterSelect = 3083
const DitherSelect = 3084
const DitherPatternData = 3085
const DocumentHandlingCapabilities = 3086
const DocumentHandlingStatus = 3087
const DocumentHandlingSelect = 3088
const DocumentHandlingCapacity = 3089
const HorizontalOpticalResolution = 3090
const VerticalOpticalResolution = 3091
const EndorserCharacters = 3092
const EndorserString = 3093
const ScanAheadPages = 3094
const MaxScanTime = 3095
const Pages = 3096
const PageSize = 3097
const PageWidth = 3098
const PageHeight = 3099
const Preview = 3100
const TransparencyAdapter = 3101
const TransparecnyAdapterSelect = 3102
```

## <a name="examples"></a>Exemples

L’exemple suivant illustre l’utilisation de la méthode **GetPropById** pour récupérer une valeur de propriété.


```JScript
<SCRIPT LANGUAGE="VBScript">
const DeviceType = 5
Dim objWia
Dim objDeviceInfoCollection
Dim objDeviceInfo
Dim objRootItem
Dim objSelectedItems
Dim objItem
Dim PropValue
 
Set objWIA = CreateObject("Wia.Script")
 
Set objDeviceInfoCollection = objWia.Devices
 
For Each objDeviceInfo In objDeviceInfoCollection
    objRootItem=objDeviceInfo.Create()
    objSelectedItems=objRootItem.GetItemsFromUI(0, 0)
    For Each objItem In objSelectedItem
    PropValue = objItem.GetPropById(DeviceType)
    Next
Next
</SCRIPT>
```



## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professional, Windows XP \[ desktop apps uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Wiascr.dll (version 4,90 ou ultérieure)</dt> </dl> |



 

 




