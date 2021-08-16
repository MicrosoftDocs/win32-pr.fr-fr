---
description: La méthode de transfert de l’objet Item transfère les données d’un appareil vers un fichier. Cette méthode s’applique uniquement aux éléments de type périphérique.
ms.assetid: ed9696da-bd94-4063-80c2-311a7a441b10
title: Item. Transfer, méthode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Item.Transfer
api_type:
- COM
api_location:
- Wiascr.dll
ms.openlocfilehash: efef054a324244553748b75659820f582100a01ed6f56f9a2f80b0ef0c08f105
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119706319"
---
# <a name="itemtransfer-method"></a>Item. Transfer, méthode

La méthode de **transfert** de l’objet [**Item**](-wia-item.md) transfère les données d’un appareil vers un fichier. Cette méthode s’applique uniquement aux éléments de type périphérique.

## <a name="syntax"></a>Syntaxe


```JScript
Item.Transfer(
  Filename,
  AsyncTransfer = VARIANT_BOOL
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Nom du fichier* \[ dans\]
</dt> <dd>

Type : **BSTR**

Spécifie le nom du fichier dans lequel les données sont transférées.

</dd> <dt>

*AsyncTransfer* \[ dans\]
</dt> <dd>

Type : **Variant \_ bool**

Valeur booléenne qui spécifie si le transfert doit être exécuté en tant qu’appel asynchrone.

<dt>



 (Variante \_ Boolean


</dt> <dd>

Par défaut. Définissez cette valeur sur **true** si l’appel doit être asynchrone (consultez la **section Notes**).

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Remarques

Cette méthode s’applique uniquement aux éléments de type de fichier. La méthode vérifie que l’élément prend en charge cette méthode avant de tenter d’effectuer le transfert de données.

Utilisez « Clipboard » comme paramètre de *nom de fichier* pour transférer un élément dans le presse-papiers.

affectez la valeur **false** à *AsyncTransfer* pour les transferts au sein d’une application ou d’un script qui s’exécute dans un environnement qui termine un processus à la fin d’un script, tel que Windows script Host (WSH). Dans le cas contraire, le script peut se terminer et le processus se terminer avant la fin du transfert.

La méthode de **transfert** n’a pas de valeur de retour. Une fois le transfert terminé, cette méthode envoie un événement [**OnTransferComplete**](-wia--iwiaevents-ontransfercomplete.md) au script ou à l’application.

## <a name="examples"></a>Exemples

L’exemple suivant illustre l’utilisation de la méthode de **transfert** pour transférer des données à partir d’un appareil.


```JScript
<SCRIPT LANGUAGE="VBScript">
Dim objWia
Dim objDeviceInfoCollection
Dim objDeviceInfo
Dim objRootItem
Dim objSelectedItems
Dim objItem
 
Set objWIA = CreateObject("Wia.Script")
 
Set objDeviceInfoCollection = objWia.Devices
 
For Each objDeviceInfo In objDeviceInfoCollection
    Set objRootItem = objWia.Create(objDeviceInfo)
    Set objSelectedItems = objRootItem.GetItemsFromUI(0, 0)
    For Each objItem In objSelectedItems
        objItem.Transfer("c:\Folder\Filename.bmp")
    Next
Next
</SCRIPT>
```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professional, Windows XP \[ desktop apps uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Wiascr.dll (version 4,90 ou ultérieure)</dt> </dl> |



 

 




