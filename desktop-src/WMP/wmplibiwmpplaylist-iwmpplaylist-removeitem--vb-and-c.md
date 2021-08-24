---
title: IWMPPlaylist removeItem, méthode
description: La méthode removeItem supprime l’élément multimédia spécifié de la sélection.
ms.assetid: 8b5a4c34-863d-4963-97c8-cc5aa2223ab5
keywords:
- removeItem, méthode Lecteur Windows Media
- removeItem, méthode Lecteur Windows Media, IWMPPlaylist, interface
- Lecteur Windows Media de l’interface IWMPPlaylist, méthode removeItem
topic_type:
- apiref
api_name:
- IWMPPlaylist.removeItem
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 01ea9250cc7e368699a916b4c87f419fc5b0b66001a4d7ca12afd5587a0adda7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119246426"
---
# <a name="iwmpplaylistremoveitem-method"></a>IWMPPlaylist :: removeItem, méthode

La méthode **RemoveItem** supprime l’élément multimédia spécifié de la sélection.

## <a name="syntax"></a>Syntaxe


```CSharp
public void removeItem(
  IWMPMedia pIWMPMedia
);
```


```VB

Public Sub removeItem( _
  ByVal pIWMPMedia As IWMPMedia _
)
Implements IWMPPlaylist.removeItem
```





## <a name="parameters"></a>Paramètres

<dl> <dt>

*pIWMPMedia* \[ dans\]
</dt> <dd>

Interface **wmplib. IWMPMedia** qui représente l’élément multimédia à supprimer de la sélection.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Remarques

Si l’élément supprimé est la piste en cours de lecture, la lecture s’arrête et l’élément suivant dans la sélection devient le suivi actuel.

S’il n’y a pas d’élément suivant, l’élément précédent est utilisé. Si aucun autre élément n’est présent, la propriété **AxWindowsMediaPlayer. currentMedia** retourne la **valeur null**.

Avant d’appeler cette méthode, vous devez disposer d’un accès complet à la bibliothèque. Pour plus d’informations, consultez [accès à la bibliothèque](library-access.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Version<br/>   | Lecteur Windows Media série 9 ou version ultérieure<br/>                                                                      |
| Espace de noms<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**AxWindowsMediaPlayer. currentMedia (VB et C#)**](axwmplib-axwindowsmediaplayer-currentmedia--vb-and-c.md)
</dt> <dt>

[**Interface IWMPMedia (VB et C#)**](iwmpmedia--vb-and-c.md)
</dt> <dt>

[**Interface IWMPPlaylist (VB et C#)**](iwmpplaylist--vb-and-c.md)
</dt> <dt>

[**IWMPPlaylist. insertItem (VB et C#)**](wmplibiwmpplaylist-iwmpplaylist-insertitem--vb-and-c.md)
</dt> <dt>

[**IWMPPlaylist. Item (VB et C#)**](iwmpplaylist-item--vb-and-c.md)
</dt> <dt>

[**IWMPSettings2. mediaAccessRights (VB et C#)**](wmplibiwmpsettings2-iwmpsettings2-mediaaccessrights--vb-and-c.md)
</dt> <dt>

[**IWMPSettings2. requestMediaAccessRights (VB et C#)**](wmplibiwmpsettings2-iwmpsettings2-requestmediaaccessrights--vb-and-c.md)
</dt> </dl>

 

 





