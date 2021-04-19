---
title: Méthode MediaCollection. getMediaAtom
description: La méthode getMediaAtom récupère l’index auquel un attribut spécifié réside dans le jeu d’attributs disponibles.
ms.assetid: 17501a95-1196-43ff-9a4e-a78cf28e7a2d
keywords:
- méthode getMediaAtom lecteur Windows Media
- méthode getMediaAtom lecteur Windows Media, classe MediaCollection
- Classe MediaCollection lecteur Windows Media, méthode getMediaAtom
topic_type:
- apiref
api_name:
- MediaCollection.getMediaAtom
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 16728b20c26b90c10f144f278f7dec24195b536a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106542558"
---
# <a name="mediacollectiongetmediaatom-method"></a>Méthode MediaCollection. getMediaAtom

La méthode **getMediaAtom** récupère l’index auquel un attribut spécifié réside dans le jeu d’attributs disponibles.

## <a name="syntax"></a>Syntaxe


```JScript
retVal = MediaCollection.getMediaAtom(
  attribute
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*attribut* \[ dans\]
</dt> <dd>

**Chaîne** contenant le nom de l’attribut. Pour plus d’informations sur les attributs pris en charge par le lecteur Windows Media, consultez la page [référence des attributs](attribute-reference.md)du lecteur Windows Media.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode retourne un **nombre** (**long**).

## <a name="remarks"></a>Notes

Le numéro d’index récupéré avec cette méthode peut être passé au *média*. méthode **getItemInfoByAtom** pour accéder aux valeurs d’attribut. Cette technique est généralement plus efficace lorsque vous utilisez des sélections volumineuses que l’accès à une valeur d’attribut par son nom par le biais d’un *média*. **getItemInfo** ou *Media*. **getItemInfoByType**.

Pour utiliser cette méthode, l’accès en lecture à la bibliothèque est requis. Pour plus d’informations, consultez [accès à la bibliothèque](library-access.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Lecteur Windows Media version 7,0 ou ultérieure.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Media. getItemInfo**](media-getiteminfo.md)
</dt> <dt>

[**Media. getItemInfoByAtom**](media-getiteminfobyatom.md)
</dt> <dt>

[**Media. getItemInfoByType**](media-getiteminfobytype.md)
</dt> <dt>

[**Objet MediaCollection**](mediacollection-object.md)
</dt> <dt>

[**Paramètres. mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Paramètres. requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





