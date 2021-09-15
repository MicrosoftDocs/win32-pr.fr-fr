---
description: La propriété Children de l’objet Item récupère une collection d’objets Item. Les éléments de cette collection représentent des éléments qui sont des enfants directs de cet élément dans l’arborescence hiérarchique. Lecture seule.
ms.assetid: 94ad3385-9ce9-4a44-87bb-1d7170c8d45c
title: Item. Children, propriété
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Item.Children
api_type:
- COM
api_location:
- Wiascr.dll
ms.openlocfilehash: 144b60f1c8e9b500d49b53dfe290565c23023220
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127524017"
---
# <a name="itemchildren-property"></a>Item. Children, propriété

La propriété **Children** de l’objet [**Item**](-wia-item.md) récupère une collection d’objets **Item** . Les éléments de cette collection représentent des éléments qui sont des enfants directs de cet élément dans l’arborescence hiérarchique. Lecture seule.

Cette propriété est en lecture seule.

## <a name="syntax"></a>Syntaxe


```JScript
propVal = Item.Children
```



## <a name="property-value"></a>Valeur de la propriété

Variable qui reçoit les objets.

## <a name="remarks"></a>Notes

Utilisez cette propriété pour naviguer dans l’arborescence hiérarchique des objets d' [**élément**](-wia-item.md) qui représentent un périphérique, les dossiers et les fichiers qui résident sur l’appareil.

La propriété **Children** est une collection d’objets [**Item**](-wia-item.md) uniquement à partir du niveau situé juste au-dessous de cet objet **Item** dans l’arborescence. Pour naviguer dans les niveaux supérieurs de l’arborescence, utilisez cette propriété de manière récursive.

Si l’élément ne peut pas ou n’a pas d’éléments enfants, cette propriété retourne une collection vide.

> [!Note]  
> Cette collection est de base 0.

 

## <a name="examples"></a>Exemples

L’exemple suivant illustre l’utilisation de la propriété **Children** pour récupérer et énumérer une collection d’éléments enfants d’un appareil. Si l’appareil est un appareil photo numérique, le regroupement contient généralement des éléments de dossier et d’image. Si l’appareil est un scanneur, le regroupement contient généralement des éléments qui représentent des lits d’analyse.


```JScript
<SCRIPT LANGUAGE="VBScript">
Dim objWia
Dim objDeviceInfoCollection
Dim objDeviceInfo
Dim objRootItem
Dim objItemCollection
Dim objItem
 
Set objWIA = CreateObject("Wia.Script")
 
Set objDeviceInfoCollection = objWia.Devices
 
For Each objDeviceInfo In objDeviceInfoCollection
    Set objRootItem = objWia.Create(objDeviceInfo)
    objItemCollection = objRootItem.Children
    For Each objItem In objItemCollection
        ' Do something with the child item
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



 

 




