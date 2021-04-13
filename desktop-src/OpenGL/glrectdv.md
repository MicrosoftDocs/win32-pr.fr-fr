---
title: fonction glRectdv (GL. h)
description: La fonction glRectdv dessine un rectangle.
ms.assetid: 53000734-bfc3-42c3-aa80-0a54e3dd36ec
keywords:
- glRectdv fonction OpenGL
topic_type:
- apiref
api_name:
- glRectdv
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de2956a1f658101a384ae69b05ed50418492d264
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104383908"
---
# <a name="glrectdv-function"></a>glRectdv fonction)

La fonction **glRectdv** dessine un rectangle.

## <a name="syntax"></a>Syntaxe


```C++
void WINAPI glRectdv(
   const GLdouble *v1,
   const GLdouble *v2
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*v1* 
</dt> <dd>

Pointeur vers un sommet d’un rectangle.

</dd> <dt>

*v2* 
</dt> <dd>

pointeur vers le vertex opposé du rectangle.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Cette fonction ne retourne pas de valeur.

## <a name="error-codes"></a>Codes d’erreur

Le code d’erreur suivant peut être récupéré par la fonction [**glGetError**](glgeterror.md) .



| Nom                                                                                                  | Signification                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_opération non valide du GL \_**</dt> </dl> | La fonction a été appelée entre un appel à [**glBegin**](glbegin.md) et l’appel correspondant à [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Notes

La fonction **glRectd** prend en charge une spécification efficace des rectangles sous la forme de deux points d’angle. Chaque commande de rectangle accepte quatre arguments, organisés en deux paires consécutives de coordonnées (*x*, *y*), ou en tant que deux pointeurs vers des tableaux, chacun contenant une paire (*x*, *y*). Le rectangle résultant est défini dans le plan *z* = 0.

La fonction **glRectd**(*x1,* *Y1,* *x2,* *Y2*) est exactement équivalente à la séquence suivante :

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

 

 





