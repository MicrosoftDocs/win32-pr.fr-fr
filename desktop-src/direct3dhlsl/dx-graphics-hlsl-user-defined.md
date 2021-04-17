---
title: Type défini par l'utilisateur
description: Utilisez la syntaxe suivante pour déclarer un type défini par l’utilisateur.
ms.assetid: 8ef18864-f456-4b52-af83-f9b1050a0bba
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 2107e3eb2b2dc2362776a1a9ecd50830519c6627
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104379738"
---
# <a name="user-defined-type"></a>Type défini par l'utilisateur

Utilisez la syntaxe suivante pour déclarer un type défini par l’utilisateur.



|                                           |
|-------------------------------------------|
| **\[ \] \[ index \] de nom de type const** typedef ; |



 

## <a name="parameters"></a>Paramètres



| Élément                                                                                         | Description                                                                            |
|----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span id="_const_"></span><span id="_CONST_"></span>**\[const\]**<br/>                 | facultatif. Ce mot clé marque explicitement le type en tant que constante.<br/>             |
| <span id="Type"></span><span id="type"></span><span id="TYPE"></span>**Entrer**<br/>     | Identifie le type de données ; doit être l’un des types de données intrinsèques HLSL.<br/>     |
| <span id="Name"></span><span id="name"></span><span id="NAME"></span>**Nomme**<br/>     | Chaîne ASCII qui identifie de façon unique le nom de la variable.<br/>                 |
| <span id="Index"></span><span id="index"></span><span id="INDEX"></span>**Évaluer**<br/> | Taille de tableau facultative. Doit être un entier non signé compris entre 1 et 4 inclus.<br/> |



 

En plus des types de données intrinsèques intégrés, le langage HLSL prend en charge les types définis par l’utilisateur ou personnalisés, qui suivent la syntaxe suivante :

## <a name="remarks"></a>Notes

Les types définis par l’utilisateur ne respectent pas la casse. Pour plus de commodité, les types suivants sont définis automatiquement au niveau de la portée Super globale.


```
typedef vector <bool, #> bool#;
typedef vector <int, #> int#;
typedef vector <uint, #> uint#;
typedef vector <half, #> half#;
typedef vector <float, #> float#;
typedef vector <double, #> double#;

typedef matrix <bool, #, #> bool#x#;
typedef matrix <int, #, #> int#x#;
typedef matrix <uint, #, #> uint#x#;
typedef matrix <half, #, #> half#x#;
typedef matrix <float, #, #> float#x#;
typedef matrix <double, #, #> double#x#;
```



Le signe dièse ( \# ) représente un chiffre entier compris entre 1 et 4.

Pour la compatibilité avec les effets DirectX 8, les types suivants sont définis automatiquement au niveau de l’étendue Super globale :


```
typedef int DWORD;
typedef float FLOAT; 
typedef vector <float, 4> VECTOR;
typedef matrix <float, 4, 4> MATRIX;
typedef string STRING;
typedef texture TEXTURE;
typedef pixelshader PIXELSHADER;
typedef vertexshader VERTEXSHADER;
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Types de données (DirectX HLSL)](dx-graphics-hlsl-data-types.md)
</dt> </dl>

 

 





