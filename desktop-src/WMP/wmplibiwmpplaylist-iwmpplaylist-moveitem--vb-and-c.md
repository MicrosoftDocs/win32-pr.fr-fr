---
title: Méthode IWMPPlaylist moveItem
description: La méthode moveItem modifie l’emplacement d’un élément multimédia dans la sélection.
ms.assetid: e82c820f-4640-4289-88c1-79a92e520f00
keywords:
- méthode moveItem lecteur Windows Media
- méthode moveItem lecteur Windows Media, interface IWMPPlaylist
- Interface IWMPPlaylist lecteur Windows Media, méthode moveItem
topic_type:
- apiref
api_name:
- IWMPPlaylist.moveItem
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9c2d5be745fc3dcf799eb7203e607e493b284b4b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541663"
---
# <a name="iwmpplaylistmoveitem-method"></a>IWMPPlaylist :: moveItem, méthode

La méthode **moveItem** modifie l’emplacement d’un élément multimédia dans la sélection.

## <a name="syntax"></a>Syntaxe


```CSharp
public void moveItem(
  System.Int32 lIndexOld,
  System.Int32 lIndexNew
);
```


```VB

Public Sub moveItem( _
  ByVal lIndexOld As System.Int32, _
  ByVal lIndexNew As System.Int32 _
)
Implements IWMPPlaylist.moveItem
```





## <a name="parameters"></a>Paramètres

<dl> <dt>

*lIndexOld* \[ dans\]
</dt> <dd>

**System. Int32** qui est l’index d’origine.

</dd> <dt>

*lIndexNew* \[ dans\]
</dt> <dd>

**System. Int32** qui est le nouvel index.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Notes

Tous les éléments après l’élément inséré auront leurs numéros d’index augmentés d’une unité.

Avant d’appeler cette méthode, vous devez disposer d’un accès complet à la bibliothèque. Pour plus d’informations, consultez [accès à la bibliothèque](library-access.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Version<br/>   | Lecteur Windows Media série 9 ou version ultérieure<br/>                                                                      |
| Espace de noms<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Interface IWMPPlaylist (VB et C#)**](iwmpplaylist--vb-and-c.md)
</dt> <dt>

[**IWMPSettings2. mediaAccessRights (VB et C#)**](wmplibiwmpsettings2-iwmpsettings2-mediaaccessrights--vb-and-c.md)
</dt> <dt>

[**IWMPSettings2. requestMediaAccessRights (VB et C#)**](wmplibiwmpsettings2-iwmpsettings2-requestmediaaccessrights--vb-and-c.md)
</dt> </dl>

 

 





