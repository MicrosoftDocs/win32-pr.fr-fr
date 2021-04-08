---
title: fonction glEvalMesh2 (GL. h)
description: Calcule une grille à deux dimensions de points ou de lignes.
ms.assetid: 21e94388-903e-4b9d-8e54-9c914d0ce372
keywords:
- glEvalMesh2 fonction OpenGL
topic_type:
- apiref
api_name:
- glEvalMesh2
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 531e9f1f6288116d052c728654cd2cf03f38550a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740669"
---
# <a name="glevalmesh2-function"></a>glEvalMesh2 fonction)

Calcule une grille à deux dimensions de points ou de lignes.

## <a name="syntax"></a>Syntaxe


```C++
void WINAPI glEvalMesh2(
   GLenum mode,
   GLint  i1,
   GLint  i2,
   GLint  j1,
   GLint  j2
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*mode* 
</dt> <dd>

Valeur qui spécifie s’il faut calculer un maillage à deux dimensions de points, de lignes ou de polygones. Les constantes symboliques suivantes sont acceptées : \_ point GL, \_ ligne GL et \_ remplissage GL.

</dd> <dt>

*I1* 
</dt> <dd>

Première valeur entière pour la variable de domaine Grid i.

</dd> <dt>

*I2* 
</dt> <dd>

Dernière valeur entière pour la variable de domaine Grid i.

</dd> <dt>

*j1* 
</dt> <dd>

Première valeur entière pour la variable de domaine Grid j.

</dd> <dt>

*J2* 
</dt> <dd>

Dernière valeur entière pour la variable de domaine Grid j.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Cette fonction ne retourne pas de valeur.

## <a name="error-codes"></a>Codes d’erreur

Les codes d’erreur suivants peuvent être récupérés par la fonction [**glGetError**](glgeterror.md) .



| Nom                                                                                                  | Signification                                                                                                                                |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_enum GL non valide \_**</dt> </dl>      | Indique que le *mode* n’est pas une valeur acceptée. <br/>                                                                            |
| <dl> <dt>**\_opération non valide du GL \_**</dt> </dl> | La fonction a été appelée entre un appel à [**glBegin**](glbegin.md) et l’appel correspondant à [**glEnd**](glend.md). <br/> |



## <a name="remarks"></a>Notes

Utilisez [**glMapGrid**](glmapgrid-functions.md) et [**glEvalMesh**](glevalmesh-functions.md) en tandem pour générer et évaluer efficacement une série de valeurs de domaine de mappage uniformément espacées. La fonction **glEvalMesh** effectue un pas à pas dans le domaine entier d’une grille unidimensionnelle ou à deux dimensions, dont la plage est le domaine des mappages d’évaluation spécifiés par [**glMap1**](glmap1.md) et [**glMap2**](glmap2.md). Le paramètre mode détermine si les vertex résultants sont connectés en tant que points, lignes ou polygones pleins.

Dans le cas à deux dimensions, **glEvalMesh2**, Let

? u = (U2 U1)/n

? v = (V2 V1)/m,

où n, U1, U2, m, v1 et v2 sont les arguments de la fonction [**glMapGrid2**](glmapgrid-functions.md) la plus récente. Ensuite, si le *mode* est \_ remplissage GL, **glEvalMesh2** est équivalent à :

pour (j = J1 ; j < J2 ; j + = 1)

{

[**glBegin**](glbegin.md)( \_ bande à quatre processeurs GL \_ );

pour (i = I1 ; i <= i2 ; i + = 1)

{

[**glEvalCoord2**](glevalcoord2d.md)(i ? u + U1 (), j ? v + v1);

[**glEvalCoord2**](glevalcoord2d.md)(i ? u + U1 (), (j + 1) ? v + v1);

}

[**glEnd**](glend.md)(); }

Si le *mode* est \_ line GL, un appel à **glEvalMesh2** est équivalent à :

pour (j = J1 ; j <= J2 ; j + = 1)

{

[**glBegin**](glbegin.md)( \_ bande de lignes GL \_ );

pour (i = I1 ; i <= i2 ; i + = 1)

{

[**glEvalCoord2**](glevalcoord2d.md)(i ? u + U1, j ? v + v1);

}

[**glEnd**](glend.md)();

}

pour (i = I1 ; i <= i2 ; i + = 1)

{

[**glBegin**](glbegin.md)( \_ bande de lignes GL \_ );

pour (j = J1 ; j <= J1 ; j + = 1)

{

[**glEvalCoord2**](glevalcoord2d.md)(i ? u + U1, j ? v + v1);

}

glEnd( );

}

Enfin, si le *mode* est \_ point GL, un appel à **glEvalMesh2** est équivalent à :

[**glBegin**](glbegin.md)(points du GL \_ );

pour (j = J1 ; j <= J2 ; j + = 1)

{

pour (i = I1 ; i <= i2 ; i + = 1)

{

[**glEvalCoord2**](glevalcoord2d.md)(i ? u + U1, j ? v + v1);

}

}

[**glEnd**](glend.md)();

Dans les trois cas, les seules exigences numériques absolues sont que si i = n, la valeur est calculée à partir de i ? u + U1 est exactement U2 et, si j = m, la valeur est-elle calculée à partir de j ? v + v1 est exactement v2. Les fonctions suivantes récupèrent des informations relatives à **glEvalMesh**:

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) avec argument GL \_ Map1 \_ Grid \_ Domain

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) avec argument GL \_ map2 \_ Grid \_ Domain

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) avec des \_ segments de \_ grille \_ Map1 d’argument GL

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) avec des \_ segments de \_ grille \_ map2 d’argument GL

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                              |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                    |
| En-tête<br/>                   | <dl> <dt>GL. h</dt> </dl>         |
| Bibliothèque<br/>                  | <dl> <dt>Opengl32. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Opengl32.dll</dt> </dl> |



 

 





