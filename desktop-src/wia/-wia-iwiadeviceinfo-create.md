---
description: la méthode create de l’objet DeviceInfo établit une connexion à l’appareil d’Acquisition d’images Windows (WIA) spécifié par l’objet DeviceInfo et retourne un objet Item qui représente l’appareil.
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127522225"
---
# <a name="deviceinfocreate-method"></a>DeviceInfo. Create, méthode

la méthode **create** de l’objet [**DeviceInfo**](-wia-deviceinfo.md) établit une connexion à l’appareil d’Acquisition d’images Windows (WIA) spécifié par l’objet **DeviceInfo** et retourne un objet [**Item**](-wia-item.md) qui représente l’appareil.

## <a name="syntax"></a>Syntaxe


```JScript
retVal = DeviceInfo.Create()
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur de retour

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



## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professional, Windows XP \[ desktop apps uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Wiascr.dll (version 4,90 ou ultérieure)</dt> </dl> |



 

 




