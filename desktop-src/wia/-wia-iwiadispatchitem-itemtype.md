---
description: Type de cet élément. Lecture seule.
ms.assetid: 6c613a08-41aa-4242-80c0-75e1981a676f
title: Item. ItemType, propriété
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Item.ItemType
api_type:
- COM
api_location:
- Wiascr.dll
ms.openlocfilehash: 9b70f7a1698ecdb4de023786f21a6ef9d55f681d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127524004"
---
# <a name="itemitemtype-property"></a>Item. ItemType, propriété

Type de cet élément. Lecture seule.

Cette propriété est en lecture seule.

## <a name="syntax"></a>Syntaxe


```JScript
propVal = Item.ItemType
```



## <a name="property-value"></a>Valeur de la propriété

Les valeurs suivantes sont possibles :



| Valeur  | Description                                     |
|--------|-------------------------------------------------|
| device | L’élément est un périphérique matériel WIA.              |
| dossier | L’élément est un dossier qui contient d’autres éléments. |
| fichier   | L’élément est un fichier image ou audio.             |
| audio  | L’élément est un clip audio.                      |
| image  | L’élément est une image.                           |



 

## <a name="remarks"></a>Notes

Un élément peut avoir plusieurs types. Par exemple, chaque image est de type « image » et « fichier ». **ItemType** retourne une chaîne qui comprend tous les types valides pour l’élément, séparés par des points-virgules. Par exemple, « image ; fichier ». Il n’y a pas d’espace dans cette chaîne, et il n’y a pas de point-virgule à la fin.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professional, Windows XP \[ desktop apps uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Wiascr.dll (version 4,90 ou ultérieure)</dt> </dl> |



 

 




