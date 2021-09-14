---
title: Méthode Media. getItemInfo
description: La méthode getItemInfo récupère la valeur de l’attribut spécifié pour l’élément multimédia actuel.
ms.assetid: a1ee0d40-b979-424b-bd4e-d1acf6354d8d
keywords:
- Lecteur Windows Media de la méthode getItemInfo
- méthode getItemInfo Lecteur Windows Media, classe multimédia
- Lecteur Windows Media de classe de média, méthode getItemInfo
topic_type:
- apiref
api_name:
- Media.getItemInfo
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ef7e7348e73e3550ed668f6694ccfe9ed615215b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127008421"
---
# <a name="mediagetiteminfo-method"></a>Méthode Media. getItemInfo

La méthode **getItemInfo** récupère la valeur de l’attribut spécifié pour l’élément multimédia actuel.

## <a name="syntax"></a>Syntaxe


```JScript
strRetVal = Media.getItemInfo(
  name
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*nom* \[ dans\]
</dt> <dd>

**Chaîne** contenant le nom de l’attribut. pour plus d’informations sur les attributs pris en charge par Lecteur Windows Media, consultez la [référence d’attribut](attribute-reference.md)Lecteur Windows Media.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Cette méthode retourne une **chaîne** représentant la valeur de l’attribut spécifié. Pour les attributs dont la valeur sous-jacente est **booléenne**, elle retourne la chaîne « true » ou « false ».

## <a name="remarks"></a>Notes

Cette méthode récupère les métadonnées pour un élément multimédia numérique individuel ou un élément multimédia qui fait partie d’une sélection.

La propriété **attributeCount** contient le nombre de noms d’attribut disponibles pour un objet **multimédia** donné. Les numéros d’index peuvent ensuite être utilisés avec la méthode **getAttributeName** pour déterminer le nom de chaque attribut disponible. Les noms d’attributs individuels peuvent être passés à **getItemInfo**.

Pour récupérer des attributs avec plusieurs valeurs et attributs avec des valeurs complexes, utilisez la méthode **getItemInfoByType** .

Pour utiliser cette méthode, l’accès en lecture à la bibliothèque est requis. Pour plus d’informations, consultez [accès à la bibliothèque](library-access.md).

pour partager les Windows les bibliothèques multimédias via upnp, Lecteur Windows Media crée un service d’annuaire de contenu (CDS) exposé sur upnp. Les autres appareils peuvent alors parcourir les bibliothèques et y accéder.

dans Windows 7, une application peut utiliser les attributs Lecteur Windows Media [**TrackingID**](trackingid-attribute.md) et [**MediaType**](mediatype-attribute.md) pour construire l’ID d’objet de chaque élément dans les CDS. Notez que cette construction peut changer dans les versions ultérieures de Windows. L’application passe chacune de ces chaînes d’attributs dans le paramètre *Name* dans un appel à **getItemInfo**. **getItemInfo** retourne la valeur de chaque attribut de la valeur de retour. L’application utilise ensuite la syntaxe suivante pour construire chaque ID d’objet :

*TrackingID*. 0. *MediaTypeID*

La signification de cette syntaxe est la suivante :

-   *TrackingID* est la chaîne stockée dans l’attribut Lecteur Windows Media [**TrackingID**](trackingid-attribute.md) de l’élément multimédia.
-   *MediaTypeID* dépend de la valeur de l’attribut [**MediaType**](mediatype-attribute.md) , comme indiqué dans le tableau suivant :

    | MediaType (attribut)                      | MediaTypeID |
    |------------------------------------------|-------------|
    | [Éléments audio](audio-item-attributes.md) | 4           |
    | [Éléments de photo](photo-item-attributes.md) | B           |
    | [Éléments vidéo](video-item-attributes.md) | 8           |

    

     

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

[**Media. getAttributeName**](media-getattributename.md)
</dt> <dt>

[**Media. getItemInfoByType**](media-getiteminfobytype.md)
</dt> <dt>

[**Media. setItemInfo**](media-setiteminfo.md)
</dt> <dt>

[**Lecture des valeurs d’attribut**](reading-attribute-values.md)
</dt> <dt>

[**Paramètres. mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Paramètres. requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





