---
title: Méthode IWMPMedia3 getItemInfoByType
description: La méthode getItemInfoByType retourne la valeur de l’attribut correspondant au type d’attribut et à l’index spécifiés.
ms.assetid: e4cf14b4-3c59-485f-a573-734a0076647b
keywords:
- Lecteur Windows Media de la méthode getItemInfoByType
- méthode getItemInfoByType Lecteur Windows Media, interface IWMPMedia3
- Lecteur Windows Media de l’interface IWMPMedia3, méthode getItemInfoByType
topic_type:
- apiref
api_name:
- IWMPMedia3.getItemInfoByType
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b2f37992201d5d19397724071f8c2a4b8e851aac
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127122666"
---
# <a name="iwmpmedia3getiteminfobytype-method"></a>IWMPMedia3 :: getItemInfoByType, méthode

La méthode **getItemInfoByType** retourne la valeur de l’attribut correspondant au type d’attribut et à l’index spécifiés.

## <a name="syntax"></a>Syntaxe


```CSharp
public System.Object getItemInfoByType(
  System.String bstrType,
  System.String bstrLanguage,
  System.Int32 lIndex
);
```


```VB

Public Function getItemInfoByType( _
  ByVal bstrType As System.String, _
  ByVal bstrLanguage As System.String, _
  ByVal lIndex As System.Int32 _
) As System.Object
Implements IWMPMedia3.getItemInfoByType
```





## <a name="parameters"></a>Paramètres

<dl> <dt>

*bstrType* \[ dans\]
</dt> <dd>

**System. String** qui est le type d’attribut.

</dd> <dt>

*bstrLanguage* \[ dans\]
</dt> <dd>

**System. String** qui est le langage. Si la valeur est définie sur null ou sur une chaîne de longueur nulle (""), la chaîne de paramètres régionaux active est utilisée. Dans le cas contraire, la valeur doit être une chaîne valide du langage RFC 1766, par exemple « en-US ».

</dd> <dt>

*Lindex* \[ dans\]
</dt> <dd>

**System. Int32** qui est l’index d’attribut.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

**System. Object** qui est la valeur de l’attribut. Le type de conversion de cet objet dépend du type de l’attribut.

## <a name="remarks"></a>Notes

Cette méthode retourne les métadonnées pour un élément multimédia numérique individuel ou un élément multimédia qui fait partie d’une sélection.

Cette méthode prend en charge des attributs avec plusieurs valeurs et attributs avec des valeurs complexes. La méthode **getItemInfo** ne prend pas en charge les attributs avec plusieurs valeurs et attributs avec des valeurs complexes.

La propriété **attributeCount** obtient le nombre de noms d’attribut disponibles pour un élément multimédia donné. Les numéros d’index peuvent ensuite être utilisés avec la méthode **getAttributeName** pour déterminer le nom de chaque attribut disponible. Les noms d’attributs individuels peuvent être passés au paramètre *Name* de **getItemInfoByType**.

La méthode **getAttributeCountByType** retourne le nombre d’attributs qui correspondent à un nom d’attribut particulier pour un élément multimédia donné. Les numéros d’index peuvent ensuite être passés au paramètre d' *index* de **getItemInfoByType**. Cela est utile lorsqu’un élément multimédia a été catégorisé dans plusieurs genres, par exemple.

Si l’élément multimédia provient d’une bibliothèque qui a été récupérée en appelant [IWMPLibrary. mediaCollection](wmplibiwmplibrary-iwmplibrary-mediacollection--vb-and-c.md), l’ensemble des attributs disponibles diffère de ceux qui peuvent être interrogés à partir de la bibliothèque locale récupérée en appelant [AxWindowsMediaPlayer. mediaCollection](axwmplib-axwindowsmediaplayer-mediacollection--vb-and-c.md). Par exemple, les attributs disponibles à partir de la bibliothèque locale récupéré à l’aide de **IWMPLibrary** seront un sous-ensemble des attributs disponibles à partir de la bibliothèque locale Récupérée à l’aide de **AxWindowsMediaPlayer**. L’ensemble d’attributs disponibles à partir d’autres sources (bibliothèques distantes, périphériques portables ou CDs) est défini par les autres sources.

Avant d’appeler cette méthode, vous devez disposer d’un accès en lecture à la bibliothèque. Pour plus d’informations, consultez [accès à la bibliothèque](library-access.md).

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Version<br/>   | Lecteur Windows Media série 9 ou version ultérieure<br/>                                                                      |
| Espace de noms<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Interface IWMPMedia3 (VB et C#)**](iwmpmedia3--vb-and-c.md)
</dt> <dt>

[**IWMPMedia. attributeCount (VB et C#)**](wmplibiwmpmedia-iwmpmedia-attributecount--vb-and-c.md)
</dt> <dt>

[**IWMPMedia. getAttributeName (VB et C#)**](wmplibiwmpmedia-iwmpmedia-getattributename--vb-and-c.md)
</dt> <dt>

[**IWMPMedia. getItemInfo (VB et C#)**](wmplibiwmpmedia-iwmpmedia-getiteminfo--vb-and-c.md)
</dt> <dt>

[**IWMPMedia3. getAttributeCountByType (VB et C#)**](wmplibiwmpmedia3-iwmpmedia3-getattributecountbytype--vb-and-c.md)
</dt> </dl>

 

 





