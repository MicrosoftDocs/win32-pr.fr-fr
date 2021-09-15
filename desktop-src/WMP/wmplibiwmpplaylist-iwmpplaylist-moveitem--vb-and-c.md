---
title: Méthode IWMPPlaylist moveItem
description: La méthode moveItem modifie l’emplacement d’un élément multimédia dans la sélection.
ms.assetid: e82c820f-4640-4289-88c1-79a92e520f00
keywords:
- Lecteur Windows Media de la méthode moveItem
- méthode moveItem Lecteur Windows Media, interface IWMPPlaylist
- Lecteur Windows Media de l’interface IWMPPlaylist, méthode moveItem
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127411292"
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

## <a name="return-value"></a>Valeur de retour

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Notes

Tous les éléments après l’élément inséré auront leurs numéros d’index augmentés d’une unité.

Avant d’appeler cette méthode, vous devez disposer d’un accès complet à la bibliothèque. Pour plus d’informations, consultez [accès à la bibliothèque](library-access.md).

## <a name="requirements"></a>Spécifications



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

 

 





