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
ms.openlocfilehash: 0c2e7a197612b56eb5ae966da3cd4cc224edd2bd07e3fded3d0b72907f717d5a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119987249"
---
# <a name="d3dissue_end"></a>Fin de D3DISSUE \_

Cette macro crée une valeur utilisée par le [**problème**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-issue) pour émettre une fin de requête.

``` syntax
#define D3DISSUE_END (1 << 0)
```

## <a name="parameters"></a>Paramètres





 

## <a name="remarks"></a>Remarques

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

 

 
