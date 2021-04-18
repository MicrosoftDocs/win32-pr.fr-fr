---
title: Type de vecteur (HLSL)
description: Un vecteur contient entre un et quatre composants scalaires ; chaque composant d’un vecteur doit être du même type.
ms.assetid: 16e66f3c-c513-4d03-8adf-463dc8d83e12
keywords:
- Type de vecteur HLSL
topic_type:
- apiref
api_name:
- Vector Type
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 76d07da5d22dfb44215f70a7620d6519b5c8a802
ms.sourcegitcommit: 3d9dce1bd6c84e2b51759e940aa95aa9b459cd20
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/04/2021
ms.locfileid: "104991853"
---
# <a name="vector-type"></a>Type de vecteur

Un vecteur contient entre un et quatre composants scalaires ; chaque composant d’un vecteur doit être du même type.



|                     |
|---------------------|
| **Nom de TypeNumber** |



 


```
TypeComponents Name
```



## <a name="components"></a>Components



| Élément                                                                                                                             | Description                                                                                                                                                                                                           |
|----------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TypeComponents"></span><span id="typecomponents"></span><span id="TYPECOMPONENTS"></span>**TypeComponents**<br/> | Nom unique qui contient deux parties. La première partie est l’un des types [scalaires](dx-graphics-hlsl-data-types.md) . La deuxième partie est le nombre de composants, qui doit être compris entre 1 et 4 inclus.<br/> |
| <span id="Name"></span><span id="name"></span><span id="NAME"></span>**Nomme**<br/>                                         | Chaîne ASCII qui identifie de façon unique le nom de la variable.<br/>                                                                                                                                                |



 

## <a name="examples"></a>Exemples

Voici quelques exemples :


```
bool    bVector;   // scalar containing 1 Boolean
int1    iVector = 1;
float3  fVector = { 0.2f, 0.3f, 0.4f };
```



Un vecteur peut être déclaré à l’aide de cette syntaxe également :


```
vector <Type, Number> VariableName
```



Voici quelques exemples :


```
vector <int,    1> iVector = 1;
vector <double, 4> dVector = { 0.2, 0.3, 0.4, 0.5 };
```

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Types de données (DirectX HLSL)](dx-graphics-hlsl-data-types.md)
</dt> </dl>

 

 





