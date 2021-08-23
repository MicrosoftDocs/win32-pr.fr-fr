---
title: fonction glRects (GL. h)
description: La fonction glRects dessine un rectangle.
ms.assetid: cf56352a-3396-4061-aa5e-dada986cf4ca
keywords:
- glRects fonction OpenGL
topic_type:
- apiref
api_name:
- glRects
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 97e7207f46ec8bb25f22b3b620f00994bf88e929dac318abf14bd09af78cd3f5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118937919"
---
# <a name="glrects-function"></a>glRects fonction)

La fonction **glRects** dessine un rectangle.

## <a name="syntax"></a>Syntaxe


```C++
void WINAPI glRects(
   GLshort x1,
   GLshort y1,
   GLshort x2,
   GLshort y2
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*x1* 
</dt> <dd>

Coordonnée *x* du vertex d’un rectangle.

</dd> <dt>

*y1* 
</dt> <dd>

Coordonnée *y* du vertex d’un rectangle.

</dd> <dt>

*x2* 
</dt> <dd>

Coordonnée *x* du vertex opposé du rectangle.

</dd> <dt>

*Y2* 
</dt> <dd>

Coordonnée *y* du vertex opposé du rectangle.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Cette fonction ne retourne pas de valeur.

## <a name="error-codes"></a>Codes d’erreur

Le code d’erreur suivant peut être récupéré par la fonction [**glGetError**](glgeterror.md) .



| Nom                                                                                                  | Signification                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_opération non valide du GL \_**</dt> </dl> | La fonction a été appelée entre un appel à [**glBegin**](glbegin.md) et l’appel correspondant à [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Remarques

La fonction **glRects** prend en charge une spécification efficace des rectangles sous la forme de deux points d’angle. Chaque commande de rectangle accepte quatre arguments, organisés en deux paires consécutives de coordonnées (x, *y*), ou en tant que deux pointeurs vers des tableaux, chacun contenant une paire (*x*, *y*). Le rectangle résultant est défini dans le plan *z* = 0.

La fonction **glRects**(*x1,* *Y1,* *x2,* *Y2*) est exactement équivalente à la séquence suivante :

**glBegin**( \_ polygone GL);

**glVertex2**( *x1,* *Y1* );

**glVertex2**( *x2,* *Y1* );

**glVertex2**( *x2,* *Y2* );

**glVertex2**( *x1,* *Y2* );

**glEnd**();

Notez que si le deuxième vertex est au-dessus et à droite du premier vertex, le rectangle est construit avec un enroulement dans le sens inverse des aiguilles d’une passe.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                              |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                    |
| En-tête<br/>                   | <dl> <dt>GL. h</dt> </dl>         |
| Bibliothèque<br/>                  | <dl> <dt>Opengl32. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Opengl32.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**glBegin**](glbegin.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glVertex**](glvertex-functions.md)
</dt> </dl>

 

 





