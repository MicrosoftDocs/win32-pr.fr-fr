---
title: gluErrorString, fonction (Glu. h)
description: La fonction gluErrorString génère une chaîne d’erreur à partir d’un code d’erreur OpenGL ou GLU. La chaîne d’erreur est ANSI uniquement.
ms.assetid: 6d71a6d5-ac00-49f9-a56c-cfeeb88963eb
keywords:
- gluErrorString fonction OpenGL
topic_type:
- apiref
api_name:
- gluErrorString
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: beef90cfced2b33b612e15c1ef6918de81997520483acfb141f3a307ad64096d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119777649"
---
# <a name="gluerrorstring-function"></a>gluErrorString fonction)

La fonction **gluErrorString** génère une chaîne d’erreur à partir d’un code d’erreur OpenGL ou Glu. La chaîne d’erreur est ANSI uniquement.

## <a name="syntax"></a>Syntaxe


```C++
const GLubyte* WINAPI gluErrorString(
   GLenum errCode
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*errCode* 
</dt> <dd>

Code d’erreur OpenGL ou GLU.

</dd> </dl>

## <a name="remarks"></a>Remarques

La fonction **gluErrorString** génère une chaîne d’erreur à partir d’un code d’erreur OpenGL ou Glu. La chaîne est au format ISO Latin 1. Par exemple, **gluErrorString**(GL \_ de mémoire insuffisante \_ \_ ) retourne la chaîne « mémoire insuffisante ».

Les codes d’erreur GLU standard sont \_ Glu \_ enum non valide, Glu \_ valeur non valide \_ et Glu \_ mémoire insuffisante \_ \_ . Certaines autres fonctions GLU peuvent retourner des codes d’erreur spécialisés par le biais de rappels. Pour obtenir la liste des codes d’erreur OpenGL, consultez [**glGetError**](glgeterror.md).

La fonction **gluErrorString** génère des chaînes d’erreur en ANSI uniquement. Dans la mesure du possible, utilisez **gluErrorStringWIN**, qui autorise les chaînes d’erreur ANSI ou Unicode. Cela facilite la localisation de votre programme en vue de son utilisation dans un autre langage.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                           |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                 |
| En-tête<br/>                   | <dl> <dt>Glu. h</dt> </dl>     |
| Bibliothèque<br/>                  | <dl> <dt>Glu32. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Glu32.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**glGetError**](glgeterror.md)
</dt> <dt>

[*gluNurbsCallback*](glunurbs.md)
</dt> <dt>

[*gluQuadricCallback*](gluquadric.md)
</dt> <dt>

[*gluTessCallback*](glutess.md)
</dt> </dl>

 

 





