---
title: fonction glColorMaterial (GL. h)
description: La fonction glColorMaterial fait en sorte qu’une couleur matérielle effectue le suivi de la couleur actuelle.
ms.assetid: 6dbef2c2-f902-4f25-8a87-9e3d710dd807
keywords:
- glColorMaterial fonction OpenGL
topic_type:
- apiref
api_name:
- glColorMaterial
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d32823eaa82e6a260790dd6fa23747f2b4228649
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384823"
---
# <a name="glcolormaterial-function"></a>glColorMaterial fonction)

La fonction **glColorMaterial** fait en sorte qu’une couleur matérielle effectue le suivi de la couleur actuelle.

## <a name="syntax"></a>Syntaxe


```C++
void WINAPI glColorMaterial(
   GLenum face,
   GLenum mode
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*se* 
</dt> <dd>

Spécifie si les paramètres front, back ou les deux paramètres de matériau avant et arrière doivent suivre la couleur actuelle. Les valeurs acceptées sont le front GL, l’arrière-plan \_ GL et le \_ \_ recto \_ et l’arrière GL \_ . La valeur par défaut est \_ recto-verso (GL) \_ \_ .

</dd> <dt>

*mode* 
</dt> <dd>

Spécifie quels paramètres de matériau effectuent le suivi de la couleur actuelle. Les valeurs acceptées sont les \_ émissions GL, le GL \_ ambiant, la \_ diffusion GL, la spéculation générale du GL et l' \_ \_ ambiant et la diffusion du GL \_ \_ . La valeur par défaut est \_ ambiant \_ et \_ diffuse du GL.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Cette fonction ne retourne pas de valeur.

## <a name="error-codes"></a>Codes d’erreur

Les codes d’erreur suivants peuvent être récupérés par la fonction [**glGetError**](glgeterror.md) .



| Nom                                                                                                  | Signification                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_enum GL non valide \_**</dt> </dl>      | la *face* ou le *mode* n’était pas une valeur acceptée.<br/>                                                                                |
| <dl> <dt>**\_opération non valide du GL \_**</dt> </dl> | La fonction a été appelée entre un appel à [**glBegin**](glbegin.md) et l’appel correspondant à [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Notes

La fonction **glColorMaterial** spécifie les paramètres de matière qui effectuent le suivi de la couleur actuelle. Lorsque vous activez le \_ \_ matériel de couleur GL, pour chacun des matériaux ou matériaux spécifiés par *visage*, le ou les paramètres du matériau spécifiés par le *mode* suivent à tout moment la couleur actuelle. Activez et désactivez \_ \_ le matériel de couleur GL avec les fonctions [**glEnable**](glenable.md) et [**glDisable**](gldisable.md), que vous appelez avec la documentation de \_ couleur GL \_ comme argument. Par défaut, le \_ matériel de couleur de GL \_ est désactivé.

Avec **glColorMaterial**, vous pouvez modifier un sous-ensemble de paramètres de matériau pour chaque vertex en utilisant uniquement la fonction [**glColor**](glcolor-functions.md) , sans appeler [**glMaterial**](glmaterial-functions.md). Si vous ne spécifiez qu’un seul sous-ensemble de paramètres pour chaque vertex, il est préférable de le faire avec **glColorMaterial** qu’avec **glMaterial**.

Les fonctions suivantes récupèrent les informations relatives à **glColorMaterial**:

[**paramètre glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) avec argument GL \_ Color \_ Material \_

**glGet** avec argument \_ mat couleur de la comptabilité \_ \_

[**glIsEnabled**](glisenabled.md) avec argument de couleur de GL d’argument \_ \_

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

[**glColor**](glcolor-functions.md)
</dt> <dt>

[**glDisable**](gldisable.md)
</dt> <dt>

[**glEnable**](glenable.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[**glIsEnabled**](glisenabled.md)
</dt> <dt>

[**glLight**](gllight-functions.md)
</dt> <dt>

[**glLightModel**](gllightmodel-functions.md)
</dt> <dt>

[**glMaterial**](glmaterial-functions.md)
</dt> </dl>

 

 





