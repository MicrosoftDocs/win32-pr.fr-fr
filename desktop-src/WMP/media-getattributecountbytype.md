---
title: Méthode Media. getAttributeCountByType
description: La méthode getAttributeCountByType récupère le nombre d’attributs associés au nom et à la langue de l’attribut spécifiés.
ms.assetid: 5644e823-a9b1-4b02-9dd6-015e524fde64
keywords:
- méthode getAttributeCountByType lecteur Windows Media
- méthode getAttributeCountByType lecteur Windows Media, classe multimédia
- Classe multimédia lecteur Windows Media, méthode getAttributeCountByType
topic_type:
- apiref
api_name:
- Media.getAttributeCountByType
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 613dca43c32322cd5e7de2b2b04605789009cbf6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106525630"
---
# <a name="mediagetattributecountbytype-method"></a>Méthode Media. getAttributeCountByType

La méthode **getAttributeCountByType** récupère le nombre d’attributs associés au nom et à la langue de l’attribut spécifiés.

## <a name="syntax"></a>Syntaxe


```JScript
retVal = Media.getAttributeCountByType(
  name,
  language
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

**Chaîne** représentant la langue. Si la valeur est définie sur null ou «» (chaîne vide), la chaîne de paramètres régionaux active est utilisée. Dans le cas contraire, la valeur doit être une chaîne valide du langage RFC 1766, par exemple « en-US ».

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode retourne un **nombre** (**long**) contenant le nombre d’attributs.

## <a name="remarks"></a>Notes

Cette méthode est utilisée pour déterminer le nombre d’attributs correspondant à un nom d’attribut particulier pour un objet **multimédia** donné. Les numéros d’index peuvent ensuite être passés à la méthode **getItemInfoByType** . Cela est utile, par exemple, lorsqu’un élément multimédia a été catégorisé sous plusieurs genres.

Pour utiliser cette méthode, l’accès en lecture à la bibliothèque est requis. Pour plus d’informations, consultez [accès à la bibliothèque](library-access.md).

**Lecteur Windows Media 10 Mobile :** Cette propriété retourne toujours 0.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Lecteur Windows Media série 9 ou version ultérieure.<br/>                                 |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**MediaObject**](media-object.md)
</dt> <dt>

[**Media. getItemInfoByType**](media-getiteminfobytype.md)
</dt> <dt>

[**Paramètres. mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Paramètres. requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





