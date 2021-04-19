---
title: Méthode IWMPStringCollection2 getItemInfobyType
description: La méthode getItemInfoByType retourne la valeur correspondant à l’index de l’élément de collection de chaînes, au nom, à la langue et à l’index d’attributs spécifiés.
ms.assetid: 51035fed-51ce-4cd2-a936-4c99802128f2
keywords:
- méthode getItemInfobyType lecteur Windows Media
- méthode getItemInfobyType lecteur Windows Media, interface IWMPStringCollection2
- Interface IWMPStringCollection2 lecteur Windows Media, méthode getItemInfobyType
topic_type:
- apiref
api_name:
- IWMPStringCollection2.getItemInfobyType
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e227d6471ecf41c8f48420ded61c6f4e7eaac8cf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541457"
---
# <a name="iwmpstringcollection2getiteminfobytype-method"></a>IWMPStringCollection2 :: getItemInfobyType, méthode

La méthode **getItemInfoByType** retourne la valeur correspondant à l’index de l’élément de collection de chaînes, au nom, à la langue et à l’index d’attributs spécifiés.

## <a name="syntax"></a>Syntaxe


```CSharp
public System.Object getItemInfobyType(
  System.Int32 lCollectionIndex,
  System.String bstrType,
  System.String bstrLanguage,
  System.Int32 lAttributeIndex
);
```


```VB

Public Function getItemInfobyType( _
  ByVal lCollectionIndex As System.Int32, _
  ByVal bstrType As System.String, _
  ByVal bstrLanguage As System.String, _
  ByVal lAttributeIndex As System.Int32 _
) As System.Object
Implements IWMPStringCollection2.getItemInfobyType
```





## <a name="parameters"></a>Paramètres

<dl> <dt>

*lCollectionIndex* \[ dans\]
</dt> <dd>

**System. Int32** qui est l’index de base zéro de l’élément de collection de chaînes à partir duquel l’attribut doit être obtenu.

</dd> <dt>

*bstrType* \[ dans\]
</dt> <dd>

**System. String** qui est le nom de l’attribut.

</dd> <dt>

*bstrLanguage* \[ dans\]
</dt> <dd>

**System. String** qui indique la langue. Si la valeur est définie sur null ou sur une chaîne de longueur nulle (""), la chaîne de paramètres régionaux active est utilisée. Dans le cas contraire, la valeur doit être une chaîne valide du langage RFC 1766, par exemple « en-US ».

</dd> <dt>

*lAttributeIndex* \[ dans\]
</dt> <dd>

**System. Int32** qui correspond à l’index de base zéro de l’attribut.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

**System. Object** qui est l’élément de collection de chaînes.

## <a name="remarks"></a>Notes

Cette méthode prend en charge des attributs avec plusieurs valeurs et attributs avec des valeurs complexes. La méthode **getItemInfo** ne prend pas en charge les attributs avec plusieurs valeurs ou attributs avec des valeurs complexes.

En passant la valeur « ChildList » dans le paramètre *bstrType* , vous pouvez récupérer une nouvelle collection de chaînes qui contient les enfants de l’un des éléments de la collection de chaînes parente. Par exemple, si la collection parente contient une liste de AlbumIDs, vous pouvez utiliser cette méthode pour obtenir une collection de chaînes enfant qui contient toutes les pistes de l’un des albums. Cette approche est plus rapide et plus efficace que l’appel de la méthode **IWMPMediaCollection2. getStringCollectionByQuery** à deux reprises. une fois pour obtenir une collection de AlbumIDs et une deuxième fois pour obtenir une collection de pistes pour un AlbumID particulier. Pour utiliser ChildList de la manière décrite ci-dessus, la collection de chaînes parent doit être obtenue à partir d’une collection de médias via **IWMPLibraryServices**, et non à l’aide de la propriété **AxWindowsMediaPlayer. mediaCollection** .

Lorsque vous utilisez ChildList, transmettez la valeur « ChildList » dans le paramètre *bstrType* et la valeur 0 dans le paramètre *lAttributeIndex* . Vous pouvez ensuite effectuer un cast de l’objet qui est retourné à une interface **IWMPStringCollection2** pour accéder à la liste enfant.

Pour utiliser cette méthode, vous devez disposer d’un accès en lecture à la bibliothèque. Pour plus d’informations, consultez [accès à la bibliothèque](library-access.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Version<br/>   | Lecteur Windows Media 11.<br/>                                                                                    |
| Espace de noms<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Attribut AlbumID**](albumid-attribute.md)
</dt> <dt>

[**Interface IWMPLibraryServices (VB et C#)**](iwmplibraryservices--vb-and-c.md)
</dt> <dt>

[**IWMPMediaCollection2. getStringCollectionByQuery (VB et C#)**](wmplibiwmpmediacollection2-iwmpmediacollection2-getstringcollectionbyquery--vb-and-c.md)
</dt> <dt>

[**Interface IWMPStringCollection2**](iwmpstringcollection2--vb-and-c.md)
</dt> <dt>

[**IWMPStringCollection2. getItemInfo (VB et C#)**](wmplibiwmpstringcollection2-iwmpstringcollection2-getiteminfo--vb-and-c.md)
</dt> </dl>

 

 





