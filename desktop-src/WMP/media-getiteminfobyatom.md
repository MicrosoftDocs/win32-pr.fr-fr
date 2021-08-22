---
title: Méthode Media. getItemInfoByAtom
description: La méthode getItemInfoByAtom récupère la valeur de l’attribut avec le numéro d’index spécifié.
ms.assetid: 6e2dea0c-c722-4737-9e8e-f5cb74156cea
keywords:
- Lecteur Windows Media de la méthode getItemInfoByAtom
- méthode getItemInfoByAtom Lecteur Windows Media, classe multimédia
- Lecteur Windows Media de classe de média, méthode getItemInfoByAtom
topic_type:
- apiref
api_name:
- Media.getItemInfoByAtom
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 26db8e87a52c0d8c8236b5e4b8b5e7325fb3bb0a995dcbd81da668ea760df660
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119135132"
---
# <a name="mediagetiteminfobyatom-method"></a>Méthode Media. getItemInfoByAtom

La méthode **getItemInfoByAtom** récupère la valeur de l’attribut avec le numéro d’index spécifié.

## <a name="syntax"></a>Syntaxe


```JScript
strRetVal = Media.getItemInfoByAtom(
  index
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*index* \[ dans\]
</dt> <dd>

**Nombre** (**long**) spécifiant l’index auquel un attribut donné réside dans le jeu d’attributs disponibles.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode retourne une **chaîne** représentant la valeur de l’attribut spécifié. Pour les attributs dont la valeur sous-jacente est **booléenne**, elle retourne la chaîne « true » ou « false ».

## <a name="remarks"></a>Remarques

Cette méthode peut être utilisée pour récupérer des métadonnées pour un élément multimédia numérique spécifique à l’aide d’un numéro d’index d’attribut. La propriété **attributeCount** peut être utilisée pour déterminer le nombre d’attributs disponibles pour l’élément multimédia.

La méthode **getMediaAtom** de l’objet **MediaCollection** peut également être utilisée pour récupérer l’index d’un attribut particulier. Cette technique est généralement plus efficace que les méthodes **getItemInfo** ou **getItemInfoByType** lorsque vous utilisez des sélections volumineuses.

Pour utiliser cette méthode, l’accès en lecture à la bibliothèque est requis. Pour plus d’informations, consultez [accès à la bibliothèque](library-access.md).

pour plus d’informations sur les attributs pris en charge par Lecteur Windows Media, consultez la [référence d’attribut](attribute-reference.md)Lecteur Windows Media.

**Lecteur Windows Media 10 Mobile :** Les attributs d’un élément multimédia sont disponibles uniquement lors de la lecture, sauf s’ils sont récupérés à partir de l’élément via la collection de supports.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Lecteur Windows Media version 7,0 ou ultérieure.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Objet Media**](media-object.md)
</dt> <dt>

[**Media. attributeCount**](media-attributecount.md)
</dt> <dt>

[**Media. getItemInfo**](media-getiteminfo.md)
</dt> <dt>

[**Media. getItemInfoByType**](media-getiteminfobytype.md)
</dt> <dt>

[**Media. setItemInfo**](media-setiteminfo.md)
</dt> <dt>

[**MediaCollection.getMediaAtom**](mediacollection-getmediaatom.md)
</dt> <dt>

[**Lecture des valeurs d’attribut**](reading-attribute-values.md)
</dt> <dt>

[**Paramètres. mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Paramètres. requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





