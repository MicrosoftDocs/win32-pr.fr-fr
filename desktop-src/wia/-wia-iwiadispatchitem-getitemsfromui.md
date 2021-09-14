---
description: La méthode GetItemsFromUI de l’objet Item affiche une boîte de dialogue qui permet à un utilisateur de sélectionner des images et de l’audio à transférer à partir d’un appareil.
ms.assetid: 0ee9a248-20ed-4e1f-a8ce-615c4a6a2bce
title: Item. GetItemsFromUI, méthode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Item.GetItemsFromUI
api_type:
- COM
api_location:
- Wiascr.dll
ms.openlocfilehash: 25bb24fd2b4c6b8d3d7f8cc08c23a42257399a14
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127231059"
---
# <a name="itemgetitemsfromui-method"></a>Item. GetItemsFromUI, méthode

La méthode **GetItemsFromUI** de l’objet [**Item**](-wia-item.md) affiche une boîte de dialogue qui permet à un utilisateur de sélectionner des images et de l’audio à transférer à partir d’un appareil.

## <a name="syntax"></a>Syntaxe


```JScript
retVal = Item.GetItemsFromUI(
  Flags = 0,
  Intent = 0
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Indicateurs* \[ dans\]
</dt> <dd>

Type : **[ **WiaFlag**](-wia-wiaflag.md)**

<dt>



  (0)


</dt> <dd>

Par défaut. \[dans \] spécifie le comportement de la boîte de dialogue. Les valeurs valides pour ce paramètre sont les mêmes que pour le paramètre *lFlags* de la méthode [**DeviceDlg**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiaitem-devicedlg) .

</dd> </dl> </dd> <dt>

*Intention* \[ dans\]
</dt> <dd>

Type : **WiaIntent**

<dt>



  (0)


</dt> <dd>

Par défaut. \[dans \] spécifie le type de données que l’image doit représenter. Pour obtenir la liste des valeurs d’intention d’image, consultez [**constantes d’intention d’image**](-wia-imageintentconstants.md).

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valeur de retour

Type : **ICollection**

Cette méthode retourne une collection d’objets [**Item**](-wia-item.md) qui représentent les éléments sélectionnés par l’utilisateur. Si aucun élément n’est sélectionné, la collection est vide.

## <a name="remarks"></a>Notes

pour les applications Microsoft Visual Basic, ajoutez une référence à « Windows bibliothèque de types d’Acquisition d’Image 1,01 ».

Cette méthode s’applique uniquement aux périphériques (éléments racine). La méthode retourne une collection d’objets [**Item**](-wia-item.md) qui représentent les images ou les clips audio sélectionnés par l’utilisateur.

Si aucun élément n’est sélectionné par l’utilisateur, la méthode retourne une collection vide.

## <a name="examples"></a>Exemples

L’exemple suivant illustre l’utilisation de la méthode **GetItemsFromUI** pour permettre à un utilisateur de sélectionner des images à partir d’une boîte de dialogue.


```JScript
<SCRIPT LANGUAGE="VBScript">
Dim objWia
Dim objDeviceInfoCollection
Dim objDeviceInfo
Dim objRootItem
Dim objSelectedItems
 
Set objWIA = CreateObject("Wia.Script")
 
Set objDeviceInfoCollection = objWia.Devices
 
For Each objDeviceInfo In objDeviceInfoCollection
    Set objRootItem = objWia.Create(objDeviceInfo)
    Set objSelectedItems = objRootItem.GetItemsFromUI(0, 0)
    ' Do something with selected items.
Next
</SCRIPT>
```



## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professional, Windows XP \[ desktop apps uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Wiascr.dll (version 4,90 ou ultérieure)</dt> </dl> |



 

 




