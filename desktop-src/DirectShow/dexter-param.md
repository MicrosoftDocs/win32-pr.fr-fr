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
ms.openlocfilehash: 13bd14602b331e334cdec8cd1aedc7250b04c0ae4df2e5e4e9997c67c84d707d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120051959"
---
# <a name="dexter_param-structure"></a>\_Structure de paramètre Dexter

> [!Note]  
> \[Déconseillé. Cette API peut être supprimée des futures versions de Windows.\]

 

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

## <a name="remarks"></a>Remarques

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

 

 




