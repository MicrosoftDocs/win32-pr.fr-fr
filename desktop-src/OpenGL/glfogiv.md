---
title: glFogiv, fonction (Gl.h)
description: La fonction glFogiv spécifie des paramètres de brouillard. | fonction glFogiv (GL. h)
ms.assetid: 8d920ddc-6155-412d-af10-585932cb149f
keywords:
- glFogiv fonction OpenGL
topic_type:
- apiref
api_name:
- glFogiv
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fd4e22fddbd6c89a219c296c4fa0161f3992be195a91b38ab512c493241430fc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119061712"
---
# <a name="glfogiv-function"></a>glFogiv fonction)

La fonction **glFogfv** spécifie des paramètres de brouillard.

## <a name="syntax"></a>Syntaxe


```C++
void WINAPI glFogiv(
         GLenum pname,
   const GLint  *params
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pname* 
</dt> <dd>

Spécifie un paramètre de brouillard.

Accepte l’une des valeurs suivantes.



| Valeur                                                                                                                                                             | Signification                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_FOG_MODE"></span><span id="gl_fog_mode"></span><dl> <dt>**\_mode de brouillard GL \_**</dt> </dl>          | Le paramètre *params* est une valeur entière unique qui spécifie l’équation à utiliser pour calculer le facteur de mélange de brouillard, *f*. Trois constantes symboliques sont acceptées : GL \_ Linear, GL \_ exp et GL \_ EXP2. Les équations correspondant à ces constantes symboliques sont définies dans la section Notes suivante. Le mode de brouillard par défaut est GL \_ exp.<br/>                                                                                      |
| <span id="GL_FOG_DENSITY"></span><span id="gl_fog_density"></span><dl> <dt>**\_densité de brouillard GL \_**</dt> </dl> | Le paramètre *params* est une valeur entière unique qui spécifie la *densité*, la densité de brouillards utilisée dans les deux équations de brouillard exponentiel. Seules les densités non négatives sont acceptées. La densité de brouillard par défaut est 1,0.<br/>                                                                                                                                                                                                                         |
| <span id="GL_FOG_START"></span><span id="gl_fog_start"></span><dl> <dt>**\_début du brouillard GL \_**</dt> </dl>       | Le paramètre *params* est une valeur entière unique qui spécifie *Start*, la distance la plus proche utilisée dans l’équation de brouillard linéaire. La distance proche par défaut est 0,0.<br/>                                                                                                                                                                                                                                                                       |
| <span id="GL_FOG_END"></span><span id="gl_fog_end"></span><dl> <dt>**\_fin du brouillard comptable \_**</dt> </dl>             | Le paramètre *params* est une valeur entière unique qui spécifie *end*, la distance utilisée dans l’équation de brouillard linéaire. La distance éloignée par défaut est 1,0.<br/>                                                                                                                                                                                                                                                                           |
| <span id="GL_FOG_INDEX"></span><span id="gl_fog_index"></span><dl> <dt>**\_index de brouillard GL \_**</dt> </dl>       | Le paramètre *params* est une valeur entière unique qui spécifie *i*<sub>f</sub> , l’index de couleur de brouillard. L’index de brouillard par défaut est 0,0.<br/>                                                                                                                                                                                                                                                                                                |
| <span id="GL_FOG_COLOR"></span><span id="gl_fog_color"></span><dl> <dt>**\_couleur de brouillard GL \_**</dt> </dl>       | Le paramètre *params* contient quatre valeurs entières ou à virgule flottante qui spécifient *C*<sub>f</sub> , la couleur de brouillard. Les valeurs entières sont mappées de façon linéaire de telle sorte que la valeur représentable la plus positive corresponde à 1,0, et la valeur représentable la plus négative correspond à-1,0. Les valeurs à virgule flottante sont mappées directement. Après la conversion, tous les composants de couleur sont ancrés à la plage \[ 0, 1 \] . La couleur de brouillard par défaut est (0, 0, 0, 0).<br/> |



 

</dd> <dt>

*params* 
</dt> <dd>

Spécifie la ou les valeurs à assigner à *pname*. La \_ \_ couleur de brouillard GL requiert un tableau de quatre valeurs. Tous les autres paramètres acceptent un tableau contenant une seule valeur.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Cette fonction ne retourne pas de valeur.

## <a name="error-codes"></a>Codes d’erreur

Les codes d’erreur suivants peuvent être récupérés par la fonction [**glGetError**](glgeterror.md) .



| Nom                                                                                                  | Signification                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_enum GL non valide \_**</dt> </dl>      | *pname* n’est pas une valeur acceptée.<br/>                                                                                         |
| <dl> <dt>**\_opération non valide du GL \_**</dt> </dl> | La fonction a été appelée entre un appel à [**glBegin**](glbegin.md) et l’appel correspondant à [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Remarques

Vous activez et désactivez le brouillard avec [**glEnable**](glenable.md) et [**glDisable**](gldisable.md), à l’aide de l’argument GL \_ Fog. Bien qu’activé, le brouillard affecte les géométries pixellisées, les bitmaps et les blocs de pixels, mais pas les opérations d’effacement de la mémoire tampon.

La fonction **glFogiv** assigne la ou les *valeurs dans les paramètres au* paramètre de brouillard spécifié par *pname*.

Le brouillard fusionne une couleur de brouillard avec chaque couleur de posttexturing du fragment de pixel pixellisé à l’aide d’un facteur de fusion *f*. Factor *f* est calculé de l’une des trois façons suivantes, en fonction du mode de brouillard. Indiquez *z* comme distance en coordonnées oculaires à partir de l’origine jusqu’au fragment à la une. L’équation du \_ brouillard linéaire du GL est la suivante :

![Équation représentant la valeur du facteur de fusion en GL_LINEAR mode de brouillard en tant que fonction de distance.](images/fog01.png)

L’équation du brouillard du GL \_ exp est la suivante :

![Équation représentant la valeur du facteur de fusion en GL_EXP mode de brouillard.](images/fog02.png)

L’équation du \_ brouillard EXP2 GL est la suivante :

![Équation représentant la valeur du facteur de fusion en GL_EXP2 mode de brouillard.](images/fog03.png)

Quel que soit le mode de brouillard, *f* est ancré à la plage \[ 0, 1 \] après le calcul. Ensuite, si OpenGL est en mode de couleurs RVBA, la couleur du fragment *C*<sub>r</sub> est remplacée par

![Équation qui indique la couleur du fragment-brouillard en fonction du facteur de fusion et de la couleur de brouillard.](images/fog04.png)

En mode *d’index des* couleurs, l’index de couleurs du <sub>fragment est remplacé</sub> par

![Équation représentant l’index de couleurs du fragment à l’échelle du monde en tant que fonction du facteur de fusion et de la couleur indexée.](images/fog05.png)

Les fonctions suivantes récupèrent les informations relatives aux fonctions **glFog** :

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) avec argument GL \_ - \_ couleur de brouillard

**glGet** avec l' \_ index de brouillard de GL d’argument \_

**glGet** avec argument GL \_ - \_ densité de brouillard

**glGet** avec argument de \_ début de brouillard GL \_

**glGet** avec argument GL de \_ brouillard de \_ fin

**glGet** avec argument GL de \_ brouillard \_ en mode

[**glIsEnabled**](glisenabled.md) avec argument de brouillard de la comptabilité \_

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

[**glDisable**](gldisable.md)
</dt> <dt>

[**glEnable**](glenable.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[**glIsEnabled**](glisenabled.md)
</dt> </dl>

 

 





