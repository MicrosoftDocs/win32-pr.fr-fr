---
title: Méthode MediaCollection. getByAttributeAndMediaType
description: La méthode getByAttributeAndMediaType récupère un objet de sélection contenant des objets multimédias avec l’attribut et le type de média spécifiés.
ms.assetid: 75241b38-ae0e-4216-b405-af9a9c71f5ec
keywords:
- Lecteur Windows Media de la méthode getByAttributeAndMediaType
- méthode getByAttributeAndMediaType Lecteur Windows Media, classe MediaCollection
- Lecteur Windows Media de la classe MediaCollection, méthode getByAttributeAndMediaType
topic_type:
- apiref
api_name:
- MediaCollection.getByAttributeAndMediaType
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 46dab1bdcb511e4c96374b17bc6a98be95e48fd64d005eb856c9ec247af48f2f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119647879"
---
# <a name="mediacollectiongetbyattributeandmediatype-method"></a>Méthode MediaCollection. getByAttributeAndMediaType

La méthode **getByAttributeAndMediaType** récupère un objet de **sélection** contenant des objets **multimédias** avec l’attribut et le type de média spécifiés.

## <a name="syntax"></a>Syntaxe


```JScript
retVal = MediaCollection.getByAttributeAndMediaType(
  attribute,
  value,
  mediaType
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*attribut* \[ dans\]
</dt> <dd>

**Chaîne** contenant l’attribut.

</dd> <dt>

*valeur* \[ dans\]
</dt> <dd>

**Chaîne** contenant la valeur.

</dd> <dt>

*MediaType* \[ dans\]
</dt> <dd>

**Chaîne** contenant le type de média. Doit contenir l’une des valeurs suivantes : « audio », « Video », « photo », « playlist » ou « other ».

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode retourne un objet **playlist**

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Lecteur Windows Media 11.<br/>                                                |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Référence d’attribut**](attribute-reference.md)
</dt> <dt>

[**Objet MediaCollection**](mediacollection-object.md)
</dt> <dt>

[**Objet playlist**](playlist-object.md)
</dt> </dl>

 

 





