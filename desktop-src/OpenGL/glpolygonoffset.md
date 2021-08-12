---
title: fonction glPolygonOffset (GL. h)
description: La fonction glPolygonOffset définit l’échelle et les unités que OpenGL utilise pour calculer les valeurs de profondeur.
ms.assetid: 06bc1aba-1692-40f0-8535-2cb65b487490
keywords:
- glPolygonOffset fonction OpenGL
topic_type:
- apiref
api_name:
- glPolygonOffset
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 314372c0ce87ef5b75db24e4482d6b621422546abe0c71a34cc9821cb4391997
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118614915"
---
# <a name="glpolygonoffset-function"></a>glPolygonOffset fonction)

La fonction **glPolygonOffset** définit l’échelle et les unités que OpenGL utilise pour calculer les valeurs de profondeur.

## <a name="syntax"></a>Syntaxe


```C++
void WINAPI glPolygonOffset(
   GLfloat factor,
   GLfloat units
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*factorisés* 
</dt> <dd>

Spécifie un facteur d’échelle qui est utilisé pour créer un décalage de profondeur variable pour chaque polygone. La valeur initiale est zéro.

</dd> <dt>

*sections* 
</dt> <dd>

Spécifie une valeur qui est multipliée par une valeur spécifique à l’implémentation pour créer un décalage de profondeur constante. La valeur initiale est 0.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Cette fonction ne retourne pas de valeur.

## <a name="error-codes"></a>Codes d’erreur

Le code d’erreur suivant peut être récupéré par la fonction [**glGetError**](glgeterror.md) .



| Nom                                                                                                  | Signification                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_opération non valide du GL \_**</dt> </dl> | La fonction a été appelée entre un appel à [**glBegin**](glbegin.md) et l’appel correspondant à [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Remarques

Lorsque \_ \_ l’option décalage du polygone GL est activée, la valeur de profondeur de chaque fragment sera décalée après avoir été interpolée à partir des valeurs de profondeur des vertex appropriés. La valeur du décalage est unités *Factor* \* ? z + r \* , où ? z est une mesure du changement de profondeur par rapport à la zone d’écran du polygone, et r est la plus petite valeur qui est garantie pour produire un offset pouvant être résolu pour une implémentation donnée. Le décalage est ajouté avant l’exécution du test de profondeur et avant que la valeur ne soit écrite dans la mémoire tampon de profondeur.

La fonction **glPolygonOffset** est utile pour afficher des images de ligne masquée, pour appliquer des dépassements aux surfaces et pour le rendu de solides avec des bords en surbrillance.

La fonction **glPolygonOffset** n’a aucun effet sur les coordonnées de profondeur placées dans la mémoire tampon de commentaires. Elle n’a pas non plus d’effet sur la sélection.

Les fonctions suivantes récupèrent les informations relatives à **glPolygonOffset**:

-   [**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) avec argument du \_ \_ facteur de décalage du polygone du GL \_
-   [**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) avec arguments GL \_ \_ unité de décalage de polygone \_
-   [**glIsEnabled**](glisenabled.md) avec argument de \_ \_ remplissage de décalage de polygone de GL \_
-   [**glIsEnabled**](glisenabled.md) avec argument GL \_ polygone \_ \_ ligne décalage
-   [**glIsEnabled**](glisenabled.md) avec argument du \_ \_ point de décalage du polygone du GL \_

> [!Note]  
> La fonction **glPolygonOffset** est disponible uniquement dans OpenGl version 1,1 ou ultérieure.

 

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

[**glDepthFunc**](gldepthfunc.md)
</dt> <dt>

[**glDisable**](gldisable.md)
</dt> <dt>

[**glEnable**](glenable.md)
</dt> <dt>

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[**glIsEnabled**](glisenabled.md)
</dt> <dt>

[**glLineWidth**](gllinewidth.md)
</dt> <dt>

[**glStencilOp**](glstencilop.md)
</dt> <dt>

[**glTexEnv**](gltexenv-functions.md)
</dt> </dl>

 

 





