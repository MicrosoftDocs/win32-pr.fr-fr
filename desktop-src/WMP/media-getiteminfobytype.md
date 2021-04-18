---
title: Méthode Media. getItemInfoByType
description: La méthode getItemInfoByType récupère la valeur de l’attribut correspondant au nom, à la langue et à l’index spécifiés de l’attribut.
ms.assetid: 9d3377c2-7ae8-48ce-a42e-9c965f6b79f9
keywords:
- méthode getItemInfoByType lecteur Windows Media
- méthode getItemInfoByType lecteur Windows Media, classe multimédia
- Classe multimédia lecteur Windows Media, méthode getItemInfoByType
topic_type:
- apiref
api_name:
- Media.getItemInfoByType
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc2aff2bee7641075bbac1dd04526ee751ea077a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526857"
---
# <a name="mediagetiteminfobytype-method"></a>Méthode Media. getItemInfoByType

La méthode **getItemInfoByType** récupère la valeur de l’attribut correspondant au nom, à la langue et à l’index spécifiés de l’attribut.

## <a name="syntax"></a>Syntaxe


```JScript
retVal = Media.getItemInfoByType(
  name,
  language,
  index
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*nom* \[ dans\]
</dt> <dd>

**Chaîne** contenant le nom de l’attribut. Pour plus d’informations sur les attributs pris en charge par le lecteur Windows Media, consultez la page [référence des attributs](attribute-reference.md)du lecteur Windows Media.

</dd> <dt>

*langue* \[ dans\]
</dt> <dd>

**Chaîne** représentant la langue. Si la valeur est définie sur null ou «» (chaîne vide), la chaîne de paramètres régionaux actuelle est utilisée. Dans le cas contraire, la valeur doit être une chaîne valide du langage RFC 1766, par exemple « en-US ».

</dd> <dt>

*index* \[ dans\]
</dt> <dd>

**Nombre** (**long**) contenant l’index de base zéro de la valeur à récupérer de l’attribut.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode retourne un **nombre**, une **chaîne**, un objet **MetadataPicture** ou un objet **MetadataText** comme indiqué dans le tableau suivant.



| Attribut                   | Valeur retournée                   |
|-----------------------------|--------------------------------|
| **SyncState**               | **Number** (**unsigned long**) |
| **Synchronisation des WM et des paroles \_** | Objet **MetadataText**        |
| **WM/image**              | Objet **MetadataPicture**     |
| **WM/UserWebURL**           | Objet **MetadataText**        |
| Tous les autres attributs        | **Chaîne**                     |



 

Pour les attributs dont la valeur sous-jacente est **booléenne**, cette méthode retourne la chaîne « true » ou « false ».

## <a name="remarks"></a>Notes

Cette méthode récupère les métadonnées pour un élément multimédia numérique individuel ou un élément multimédia qui fait partie d’une sélection.

Cette méthode prend en charge des attributs avec plusieurs valeurs et attributs avec des valeurs complexes. La méthode **getItemInfo** ne prend pas en charge les attributs avec plusieurs valeurs et attributs avec des valeurs complexes.

La propriété **attributeCount** contient le nombre de noms d’attribut disponibles pour un objet **multimédia** donné. Les numéros d’index peuvent ensuite être utilisés avec la méthode **getAttributeName** pour déterminer le nom de chaque attribut disponible. Les noms d’attributs individuels peuvent être passés au paramètre *Name* de **getItemInfoByType**.

La méthode **getAttributeCountByType** retourne le nombre d’attributs qui correspondent à un nom d’attribut particulier pour un objet **multimédia** donné. Les numéros d’index peuvent ensuite être passés au paramètre d' *index* de **getItemInfoByType**. Cela est utile lorsqu’un élément multimédia numérique a été catégorisé dans plusieurs genres, par exemple.

Pour utiliser cette méthode, l’accès en lecture à la bibliothèque est requis. Pour plus d’informations, consultez [accès à la bibliothèque](library-access.md).

Cette méthode peut provoquer des erreurs. Vous devez inclure le code de gestion des erreurs lorsque vous appelez cette méthode. Par exemple, dans JScript, vous pouvez implémenter la gestion des erreurs à l’aide du **bloc try... catch... finally** , structure.

**Lecteur Windows Media 10 Mobile :** Cette méthode n’est pas prise en charge.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Lecteur Windows Media série 9 ou version ultérieure.<br/>                                 |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Objet Media**](media-object.md)
</dt> <dt>

[**Media. attributeCount**](media-attributecount.md)
</dt> <dt>

[**Media. getAttributeCountByType**](media-getattributecountbytype.md)
</dt> <dt>

[**Media. getAttributeName**](media-getattributename.md)
</dt> <dt>

[**Media. getItemInfo**](media-getiteminfo.md)
</dt> <dt>

[**Media. setItemInfo**](media-setiteminfo.md)
</dt> <dt>

[**Objet MetadataPicture**](metadatapicture-object.md)
</dt> <dt>

[**Objet MetadataText**](metadatatext-object.md)
</dt> <dt>

[**Lecture des valeurs d’attribut**](reading-attribute-values.md)
</dt> <dt>

[**Paramètres. mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Paramètres. requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





