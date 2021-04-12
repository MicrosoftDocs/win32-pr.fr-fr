---
title: gluGetString, fonction (Glu. h)
description: La fonction gluGetString obtient une chaîne qui décrit le numéro de version GLU ou les appels d’extension GLU pris en charge.
ms.assetid: e6d9ce03-3218-4145-8bb5-3989afe62436
keywords:
- gluGetString fonction OpenGL
topic_type:
- apiref
api_name:
- gluGetString
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 574ed93c9c6f8d1f964e38ee14541d57bd5c34da
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384460"
---
# <a name="glugetstring-function"></a>gluGetString fonction)

La fonction **gluGetString** obtient une chaîne qui décrit le numéro de version Glu ou les appels d’extension Glu pris en charge.

## <a name="syntax"></a>Syntaxe


```C++
const GLubyte* WINAPI gluGetString(
   GLenum name
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*name* 
</dt> <dd>

Le numéro de version de GLU ( \_ version Glu) ou des appels d’extension spécifiques au fournisseur ( \_ Extensions Glu) disponibles.

</dd> </dl>

## <a name="remarks"></a>Notes

La fonction **gluGetString** retourne un pointeur vers une chaîne statique se terminant par null. Quand le *nom* est Glu \_ version, la chaîne retournée est une valeur qui représente le numéro de version de Glu. Le format du numéro de version est le suivant :

``` syntax
<version number><space><vendor-specific information> 
(for example, "1.2.11 Microsoft Windows")
```

Le numéro de version se présente sous la forme « \_ numéro principal. \_ nombre mineur » ou « numéro majeur. numéro de \_ \_ version secondaire \_ ». Les informations spécifiques au fournisseur sont facultatives, et le format et le contenu dépendent de l’implémentation.

Quand le *nom* est Glu \_ Extensions, la chaîne retournée contient une liste de noms d’extensions Glu prises en charge, séparées par des espaces. Le format de la liste de noms retournée est le suivant :

``` syntax
<extension_name><space><extension_name><space> . . .
(for example, "GLU_NURBS GL_TESSELATION")
```

Les noms d’extension ne peuvent pas contenir d’espaces.

La fonction **gluGetString** est valide pour GLU version 1,1 ou ultérieure.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                           |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                 |
| En-tête<br/>                   | <dl> <dt>Glu. h</dt> </dl>     |
| Bibliothèque<br/>                  | <dl> <dt>Glu32. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Glu32.dll</dt> </dl> |



 

 





