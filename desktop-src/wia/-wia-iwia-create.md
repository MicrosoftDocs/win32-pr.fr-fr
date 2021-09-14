---
description: la méthode create de l’objet wia établit une connexion à l’appareil Windows d’Acquisition d’images (wia) spécifié et retourne un objet Item qui représente l’appareil.
ms.assetid: c33c635a-159c-4ac3-8ad5-6f21a1986702
title: WIA. Create, méthode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Wia.Create
- SafeWia.Create
api_type:
- COM
api_location:
- Wiascr.dll
ms.openlocfilehash: d22d45e473cec1d5186c300f97cbdb4661237ab9
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127219956"
---
# <a name="wiacreate-method"></a>WIA. Create, méthode

la méthode **create** de l’objet [**wia**](-wia-wia.md) établit une connexion à l’appareil Windows d’Acquisition d’images (wia) spécifié et retourne un objet [**Item**](-wia-item.md) qui représente l’appareil.

## <a name="syntax"></a>Syntaxe


```JScript
retVal = Wia.Create(
  Device
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Appareil mobile* \[ dans\]
</dt> <dd>

Type : **variante \***

Spécifie l’appareil WIA auquel se connecter.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Type : **IWiaDispatchItem**

En cas de réussite, cette méthode retourne un objet d' [**élément**](-wia-item.md) qui représente un périphérique matériel WIA (élément racine).

## <a name="remarks"></a>Notes

Le paramètre *Device* spécifie un objet [**DeviceInfo**](-wia-deviceinfo.md) en passant l’objet lui-même, son index d’un objet collection ou la valeur de sa propriété [**ID**](-wia-iwiadeviceinfo-id.md) . **Ne rien** faire pour afficher une boîte de dialogue qui permet à un utilisateur de sélectionner un appareil.

## <a name="examples"></a>Exemples

Les exemples VBScript suivants illustrent l’utilisation de la méthode **Create** .

Le premier exemple passe un objet [**DeviceInfo**](-wia-deviceinfo.md) à la méthode **Create** . Notez que le passage de la propriété [**ID**](-wia-iwiadeviceinfo-id.md) de l’objet provoque exactement le même comportement.


```JScript
<SCRIPT LANGUAGE="VBScript">
Dim objWia
Dim objDeviceInfoCollection
Dim objDeviceInfo
Dim objItem
 
Set objWIA = CreateObject("Wia.Script")
 
Set objDeviceInfoCollection = objWia.Devices
 
For Each objDeviceInfo In objDeviceInfoCollection
    Set objItem = objWia.Create(objDeviceInfo)
Next
</SCRIPT>
```



Dans l’exemple suivant, l’application appelante passe l’index de l’objet [**DeviceInfo**](-wia-deviceinfo.md) de la collection à la méthode **Create** .


```JScript
<SCRIPT LANGUAGE = "VBScript">
Dim objWia
Dim objDeviceInfoCollection
Dim objItem
 
Set objWia = CreateObject("Wia.Script")
 
Set objDeviceInfoCollection = objWia.Devices
 
For i = 0 To objDeviceInfoCollection.Count-1
    Set objItem = objWia.Create(i)
Next
</SCRIPT>
```



L’exemple suivant passe **Nothing** à la méthode **Create** pour afficher une boîte de dialogue qui permet à un utilisateur de sélectionner un appareil.


```JScript
<SCRIPT LANGUAGE = "VBScript">
Dim objWia
Dim objItem
 
Set objWia = objWia.Create(Nothing)
</SCRIPT>
```



## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professional, Windows XP \[ desktop apps uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Wiascr.dll (version 4,90 ou ultérieure)</dt> </dl> |



 

 




