---
title: Méthode IWMPPlaylist getItemInfo
description: La méthode getItemInfo retourne la valeur d’un attribut playlist spécifié par Name.
ms.assetid: 62e882d6-66bb-450c-9700-b99d30dd42fa
keywords:
- Lecteur Windows Media de la méthode getItemInfo
- méthode getItemInfo Lecteur Windows Media, interface IWMPPlaylist
- Lecteur Windows Media de l’interface IWMPPlaylist, méthode getItemInfo
topic_type:
- apiref
api_name:
- IWMPPlaylist.getItemInfo
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ced433b13f5af2d1df8c12dba023b7fbb55c5f7d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127411299"
---
# <a name="iwmpplaylistgetiteminfo-method"></a>IWMPPlaylist :: getItemInfo, méthode

La méthode **getItemInfo** retourne la valeur d’un attribut playlist spécifié par Name.

## <a name="syntax"></a>Syntaxe


```CSharp
public System.String getItemInfo(
  System.String bstrName
);
```


```VB

Public Function getItemInfo( _
  ByVal bstrName As System.String _
) As System.String
Implements IWMPPlaylist.getItemInfo
```





## <a name="parameters"></a>Paramètres

<dl> <dt>

*bstrName* \[ dans\]
</dt> <dd>

**System. String** qui est le nom de l’attribut playlist.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

**System. String** qui est la valeur de l’attribut playlist.

## <a name="remarks"></a>Notes

Avant d’utiliser cette méthode, vous devez disposer d’un accès en lecture à la bibliothèque. Pour plus d’informations, consultez [accès à la bibliothèque](library-access.md).

Consultez la propriété [attributeCount](wmplibiwmpplaylist-iwmpplaylist-attributecount--vb-and-c.md) pour obtenir un exemple de code qui utilise cette propriété.

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

[**IWMPPlaylist. setItemInfo (VB et C#)**](wmplibiwmpplaylist-iwmpplaylist-setiteminfo--vb-and-c.md)
</dt> </dl>

 

 





