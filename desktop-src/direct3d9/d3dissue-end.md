---
description: Cette macro crée une valeur utilisée par le problème pour émettre une fin de requête.
ms.assetid: 9ced932a-5d98-4bf8-aa11-06560f53546d
title: D3DISSUE_END (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DISSUE_END
api_type:
- HeaderDef
api_location:
- D3d9types.h
ms.openlocfilehash: 7a448346bdc5dcfbbca4cf0d55273bdadc2fdcbb
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104323010"
---
# <a name="d3dissue_end"></a>Fin de D3DISSUE \_

Cette macro crée une valeur utilisée par le [**problème**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-issue) pour émettre une fin de requête.

``` syntax
#define D3DISSUE_END (1 << 0)
```

## <a name="parameters"></a>Paramètres





 

## <a name="remarks"></a>Notes

Cette macro remplace l’état de la requête par non signalé.

D3DISSUE \_ end est valide pour les types de requêtes suivants.

-   D3DQUERYTYPE \_ Vcache
-   D3DQUERYTYPE \_ ResourceManager
-   D3DQUERYTYPE \_ VERTEXSTATS
-   \_Événement D3DQUERYTYPE
-   \_Occlusion D3DQUERYTYPE

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|----------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>D3d9types. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Macros](dx9-graphics-reference-d3d-macros.md)
</dt> <dt>

[**Début de D3DISSUE \_**](d3dissue-begin.md)
</dt> <dt>

[**D3DQUERYTYPE**](./d3dquerytype.md)
</dt> </dl>

 

 
