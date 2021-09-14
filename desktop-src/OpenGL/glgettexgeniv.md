---
title: fonction glGetTexGeniv (GL. h)
description: Les fonctions glGetTexGendv, glGetTexGenfv et glGetTexGeniv retournent des paramètres de génération de coordonnées de texture. | fonction glGetTexGeniv (GL. h)
ms.assetid: 62c481d1-4862-43bb-9319-5a282c4e47d3
keywords:
- glGetTexGeniv fonction OpenGL
topic_type:
- apiref
api_name:
- glGetTexGeniv
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 29569c84d21dbb2cd69579c78747e844cfd23ba4
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127229457"
---
# <a name="glgettexgeniv-function"></a>glGetTexGeniv fonction)

Les fonctions [**glGetTexGendv**](glgettexgendv.md), [**glGetTexGenfv**](glgettexgenfv.md)et **glGetTexGeniv** retournent des paramètres de génération de coordonnées de texture.

## <a name="syntax"></a>Syntaxe


```C++
void WINAPI glGetTexGeniv(
   GLenum coord,
   GLenum pname,
   GLint  *params
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*coordonnées* 
</dt> <dd>

Coordonnée de texture. Doit être GL \_ S, GL \_ T, GL \_ R ou GL \_ Q.

</dd> <dt>

*pname* 
</dt> <dd>

Nom symbolique de la ou des valeurs à retourner. Il doit s’agir \_ \_ \_ du mode de la génération de texture GL ou du nom de l’une des équations du plan de génération de texture : plan d' \_ objet GL \_ ou \_ plan oculaire GL \_ . Ces valeurs sont les suivantes.



| Valeur                                                                                                                                                                             | Signification                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_TEXTURE_GEN_MODE"></span><span id="gl_texture_gen_mode"></span><dl> <dt>**\_mode de génération de textures GL \_ \_**</dt> </dl> | Le paramètre *params* retourne la fonction de génération de texture à valeur unique, une constante symbolique.<br/>                                                                                                                                                                                                                                                                                                                                                            |
| <span id="GL_OBJECT_PLANE"></span><span id="gl_object_plane"></span><dl> <dt>**\_plan d’objet GL \_**</dt> </dl>              | Le paramètre *params* retourne les quatre coefficients d’équation plan qui spécifient la génération de la coordonnée linéaire de l’objet. Les valeurs entières, quand elles sont demandées, sont mappées directement à partir de la représentation à virgule flottante interne.<br/>                                                                                                                                                                                                                                    |
| <span id="GL_EYE_PLANE"></span><span id="gl_eye_plane"></span><dl> <dt>**\_plan oculaire \_ GL**</dt> </dl>                       | Le paramètre *params* retourne les quatre coefficients d’équation plan qui spécifient la génération de coordonnées linéaires oculaires. Les valeurs entières, quand elles sont demandées, sont mappées directement à partir de la représentation à virgule flottante interne. Les valeurs retournées sont celles qui sont gérées en coordonnées oculaires. Ils ne sont pas égaux aux valeurs spécifiées à l’aide de [**glTexGen**](gltexgen-functions.md), sauf si la matrice modelview a été identifiée au moment de l’appel de **glTexGen** .<br/> |



 

</dd> <dt>

*params* 
</dt> <dd>

Retourne les données demandées.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Cette fonction ne retourne pas de valeur.

## <a name="error-codes"></a>Codes d’erreur

Les codes d’erreur suivants peuvent être récupérés par la fonction [**glGetError**](glgeterror.md) .



| Nom                                                                                                  | Signification                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_enum GL non valide \_**</dt> </dl>      | *Coord* ou *pname* n’est pas une valeur acceptée.<br/>                                                                              |
| <dl> <dt>**\_opération non valide du GL \_**</dt> </dl> | La fonction a été appelée entre un appel à [**glBegin**](glbegin.md) et l’appel correspondant à [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Notes

La fonction **glGetTexGen** retourne dans *params* les paramètres sélectionnés d’une fonction de génération de coordonnées de texture que vous avez spécifiée avec **glTexGen**. Le paramètre *Coord* nomme une des coordonnées de texture (*s*, *t*, *r*, *q*) à l’aide de la constante symbolique GL \_ s, GL \_ t, GL \_ r ou GL \_ q.

Si une erreur est générée, aucune modification n’est apportée au contenu des *paramètres*.

## <a name="requirements"></a>Spécifications



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

[**glTexGen**](gltexgen-functions.md)
</dt> </dl>

 

 





