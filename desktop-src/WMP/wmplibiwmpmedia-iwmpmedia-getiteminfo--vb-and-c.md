---
title: Méthode IWMPMedia getItemInfo
description: La méthode getItemInfo retourne la valeur de l’attribut spécifié pour l’élément multimédia.
ms.assetid: b95fa61d-a600-4f31-a930-d80516204034
keywords:
- méthode getItemInfo lecteur Windows Media
- méthode getItemInfo lecteur Windows Media, interface IWMPMedia
- Interface IWMPMedia lecteur Windows Media, méthode getItemInfo
topic_type:
- apiref
api_name:
- IWMPMedia.getItemInfo
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 523e57e68d13df55395cd4deca6e09904723bbaf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541725"
---
# <a name="iwmpmediagetiteminfo-method"></a>IWMPMedia :: getItemInfo, méthode

La méthode **getItemInfo** retourne la valeur de l’attribut spécifié pour l’élément multimédia.

## <a name="syntax"></a>Syntaxe


```CSharp
public System.String getItemInfo(
  System.String bstrItemName
);
```


```VB

Public Function getItemInfo( _
  ByVal bstrItemName As System.String _
) As System.String
Implements IWMPMedia.getItemInfo
```





## <a name="parameters"></a>Paramètres

<dl> <dt>

*bstrItemName* \[ dans\]
</dt> <dd>

**System. String** qui est le nom de l’attribut. Pour plus d’informations sur les attributs pris en charge par le lecteur Windows Media, consultez la [référence d’attribut](attribute-reference.md).

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

**System. String** qui est la valeur de l’attribut spécifié.

## <a name="remarks"></a>Notes

Cette méthode retourne les métadonnées pour un élément multimédia individuel ou un élément multimédia qui fait partie d’une sélection.

La propriété **attributeCount** obtient le nombre de noms d’attribut disponibles pour un élément multimédia donné. Les numéros d’index peuvent ensuite être utilisés avec la méthode **getAttributeName** pour déterminer le nom de chaque attribut disponible. Les noms d’attributs individuels peuvent être passés à **getItemInfo**.

Pour récupérer des attributs avec plusieurs valeurs et attributs avec des valeurs complexes, utilisez la méthode **getItemInfoByType** .

Si l’élément multimédia provient d’une bibliothèque qui a été récupérée en appelant [IWMPLibrary. mediaCollection](wmplibiwmplibrary-iwmplibrary-mediacollection--vb-and-c.md), l’ensemble des attributs disponibles diffère de ceux qui peuvent être interrogés à partir de la bibliothèque locale récupérée en appelant [AxWindowsMediaPlayer. mediaCollection](axwmplib-axwindowsmediaplayer-mediacollection--vb-and-c.md). Par exemple, les attributs disponibles à partir de la bibliothèque locale récupéré à l’aide de **IWMPLibrary** seront un sous-ensemble des attributs disponibles à partir de la bibliothèque locale Récupérée à l’aide de **IWMPCore**. L’ensemble d’attributs disponibles à partir d’autres sources (bibliothèques distantes, appareils mobiles ou CDs) est défini par les autres sources.

Avant d’appeler cette méthode, vous devez disposer d’un accès en lecture à la bibliothèque. Pour plus d’informations, consultez [accès à la bibliothèque](library-access.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Version<br/>   | Lecteur Windows Media série 9 ou version ultérieure<br/>                                                                      |
| Espace de noms<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Référence d’attribut**](attribute-reference.md)
</dt> <dt>

[**Interface IWMPMedia (VB et C#)**](iwmpmedia--vb-and-c.md)
</dt> <dt>

[**IWMPMedia. attributeCount (VB et C#)**](wmplibiwmpmedia-iwmpmedia-attributecount--vb-and-c.md)
</dt> <dt>

[**IWMPMedia. getAttributeName (VB et C#)**](wmplibiwmpmedia-iwmpmedia-getattributename--vb-and-c.md)
</dt> <dt>

[**IWMPMedia. setItemInfo (VB et C#)**](wmplibiwmpmedia-iwmpmedia-setiteminfo--vb-and-c.md)
</dt> <dt>

[**IWMPMedia3. getItemInfoByType (VB et C#)**](wmplibiwmpmedia3-iwmpmedia3-getiteminfobytype--vb-and-c.md)
</dt> </dl>

 

 





