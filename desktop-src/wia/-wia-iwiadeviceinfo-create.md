---
description: La méthode Create de l’objet DeviceInfo établit une connexion à l’appareil WIA (Windows Image Acquisition) spécifiée par l’objet DeviceInfo et retourne un objet Item qui représente l’appareil.
ms.assetid: 57f3698c-3f9f-4775-8b53-a65a5591aa3d
title: DeviceInfo. Create, méthode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DeviceInfo.Create
api_type:
- COM
api_location:
- Wiascr.dll
ms.openlocfilehash: 1efc36ea8794de4b64c9af616320b09d547f6490
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106533761"
---
# <a name="deviceinfocreate-method"></a>DeviceInfo. Create, méthode

La méthode **Create** de l’objet [**DeviceInfo**](-wia-deviceinfo.md) établit une connexion à l’appareil WIA (Windows Image Acquisition) spécifiée par l’objet **DeviceInfo** et retourne un objet [**Item**](-wia-item.md) qui représente l’appareil.

## <a name="syntax"></a>Syntaxe


```JScript
retVal = DeviceInfo.Create()
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Type : **IWiaDispatchItem**

Cette méthode retourne l’objet d' [**élément**](-wia-item.md) qui représente l’appareil créé.

## <a name="remarks"></a>Notes

Utilisez la méthode **Create** pour créer une connexion à un périphérique matériel WIA après l’énumération du regroupement [**Devices**](-wia-iwia-devices.md) . La méthode retourne un objet d' [**élément**](-wia-item.md) qui représente l’appareil (élément racine).

## <a name="examples"></a>Exemples

L’exemple suivant illustre l’utilisation de la méthode **Create** .


```JScript
<SCRIPT LANGUAGE="VBScript">
Dim objWia
Dim objDeviceInfoCollection
Dim objDeviceInfo
Dim objItem
 
Set objWIA = CreateObject("Wia.Script")
 
Set objDeviceInfoCollection = objWia.Devices
 
For Each objDeviceInfo In objDeviceInfoCollection
    Set objItem = objDeviceInfo.Create()
Next
</SCRIPT>
```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 professionnel, applications de \[ Bureau Windows XP uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Wiascr.dll (version 4,90 ou ultérieure)</dt> </dl> |



 

 




