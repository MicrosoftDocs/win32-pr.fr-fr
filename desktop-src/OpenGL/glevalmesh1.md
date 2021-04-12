---
title: fonction glEvalMesh1 (GL. h)
description: Calcule une grille unidimensionnelle de points ou de lignes.
ms.assetid: 176a4b81-f1a7-42fc-8ecd-bba77a0ec5b3
keywords:
- glEvalMesh1 fonction OpenGL
topic_type:
- apiref
api_name:
- glEvalMesh1
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f8950dcf397816fca8eb5a6add45c45512c48866
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508786"
---
# <a name="glevalmesh1-function"></a>glEvalMesh1 fonction)

Calcule une grille unidimensionnelle de points ou de lignes.

## <a name="syntax"></a>Syntaxe


```C++
void WINAPI glEvalMesh1(
   GLenum mode,
   GLint  i1,
   GLint  i2
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*mode* 
</dt> <dd>

Valeur qui spécifie s’il faut calculer un maillage unidimensionnel de points ou de lignes. Les constantes symboliques suivantes sont acceptées : le \_ point GL et la \_ ligne GL.

</dd> <dt>

*I1* 
</dt> <dd>

Première valeur entière pour la variable de domaine Grid i.

</dd> <dt>

*I2* 
</dt> <dd>

Dernière valeur entière pour la variable de domaine Grid i.

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

Utilisez [**glMapGrid**](glmapgrid-functions.md) et [**glEvalMesh**](glevalmesh-functions.md) ensemble pour générer et évaluer efficacement une série de valeurs de domaine de mappage uniformément espacées. La fonction **glEvalMesh** effectue un pas à pas dans le domaine entier d’une grille unidimensionnelle ou à deux dimensions, dont la plage est le domaine des mappages d’évaluation spécifiés par [**glMap1**](glmap1.md) et [**glMap2**](glmap2.md). Le paramètre mode détermine si les vertex résultants sont connectés en tant que points, lignes ou polygones pleins.

Dans le cas unidimensionnel, **glEvalMesh1**, la maille est générée comme si le fragment de code suivant était exécuté :

[**glBegin**](glbegin.md)(*type*);

pour (i = I1 ; i <= i2 ; i + = 1)

{

[**glEvalCoord1**](glevalcoord1d.md)(i ? u + U1)

}

[**glEnd**](glend.md)();

where

? u = (U2 U1)/n

et n, U1 et U2 sont les arguments de la fonction [**glMapGrid1**](glmapgrid1d.md) la plus récente. Le paramètre de *type* est \_ points du GL si le mode est mode GL \_ , ou \_ lignes GL si le mode est \_ ligne GL. La seule exigence numérique absolue est que si i = n, la valeur calculée à partir de i ? u + U1 est exactement U2.

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
</dt> </dl>

 

 





