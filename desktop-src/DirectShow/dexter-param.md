---
description: Spécifie la valeur supposée par une propriété à un moment donné.
ms.assetid: 117868b7-65e5-4b3b-9e50-4106ee6a65d0
title: Structure DEXTER_PARAM (qedit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DEXTER_PARAM
api_type:
- HeaderDef
api_location:
- Qedit.h
ms.openlocfilehash: 22b0f6ef0a91f9a6d9163a03c17f6e86ee8b5f4e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106535258"
---
# <a name="dexter_param-structure"></a>\_Structure de paramètre Dexter

> [!Note]  
> \[Action déconseillée. Cette API peut être supprimée dans les versions futures de Windows.\]

 

Spécifie la valeur supposée par une propriété à un moment donné.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct {
  BSTR   Name;
  DISPID dispID;
  LONG   nValues;
} DEXTER_PARAM;
```



## <a name="members"></a>Membres

<dl> <dt>

**Nom**
</dt> <dd>

Nom de la propriété.

</dd> <dt>

**Égal**
</dt> <dd>

Réservé. Définit la valeur zéro.

</dd> <dt>

**Nvaleurs**
</dt> <dd>

Nombre de valeurs supposées par la propriété.

</dd> </dl>

## <a name="remarks"></a>Notes

L’objet doit prendre en charge l’interface **IDispatch** .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>Qedit. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IPropertySetter**](ipropertysetter.md)
</dt> <dt>

[**valeur de DEXTERity \_**](dexter-value.md)
</dt> </dl>

 

 




