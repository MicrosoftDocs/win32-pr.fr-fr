---
description: ID3DXInclude est une interface implémentée par l’utilisateur pour fournir des rappels pour les \# directives include pendant la compilation du nuanceur.
ms.assetid: 8e0bfff1-8d6d-4381-b9fd-f5f64f854712
title: Interface ID3DXInclude (D3DX9Shader. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXInclude
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: d4b0a34eb5b4c3ab20a57a5089de1d6d1ebbdf51
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106520351"
---
# <a name="id3dxinclude-interface"></a>Interface ID3DXInclude

ID3DXInclude est une interface implémentée par l’utilisateur pour fournir des rappels pour les \# directives include pendant la compilation du nuanceur. Chacune des méthodes dans cette interface doit être implémentée par l’utilisateur qui sera ensuite utilisé comme rappels de l’application lorsque l’un des éléments suivants se produit :

-   Un nuanceur HLSL qui contient un \# include est compilé en appelant l’une des \* \* \* fonctions D3DXCompileShader.
-   Un nuanceur \# d’assembly inclut est assemblé en appelant l’une des \* \* \* fonctions D3DXAssembleShader.
-   Un effet qui contient un \# include est compilé par en appelant l’une des \* \* \* fonctions D3DXCreateEffect ou D3DXCreateEffectCompiler \* \* \* .

## <a name="members"></a>Membres

L’interface **ID3DXInclude** hérite de l’interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **ID3DXInclude** a également les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **ID3DXInclude** possède ces méthodes.



| Méthode                               | Description                                                                                           |
|:-------------------------------------|:------------------------------------------------------------------------------------------------------|
| [**Fermer**](id3dxinclude--close.md) | Méthode implémentée par l’utilisateur pour la fermeture d’un \# fichier include de nuanceur.<br/>                             |
| [**Afficher**](id3dxinclude--open.md)   | Méthode implémentée par l’utilisateur pour ouvrir et lire le contenu d’un \# fichier include de nuanceur.<br/> |



 

## <a name="remarks"></a>Notes

Un utilisateur crée une interface ID3DXInclude en implémentant une classe qui dérive de cette interface et en implémentant toutes les méthodes d’interface.

Le type LPD3DXINCLUDE est défini en tant que pointeur vers cette interface.


```
typedef interface ID3DXInclude ID3DXInclude;
typedef interface ID3DXInclude *LPD3DXINCLUDE;
```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3DX9Shader. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Interfaces d’effet](dx9-graphics-reference-effects-interfaces.md)
</dt> </dl>

 

 
