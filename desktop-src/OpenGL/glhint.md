---
title: fonction glHint (GL. h)
description: La fonction glHint spécifie des indicateurs spécifiques à l’implémentation.
ms.assetid: 6d03e107-321a-45ee-9ce7-25fa9cab32d9
keywords:
- glHint fonction OpenGL
topic_type:
- apiref
api_name:
- glHint
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2772c76868c741660486184e5ab51bd193d3667a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103197"
---
# <a name="glhint-function"></a>glHint fonction)

La fonction **glHint** spécifie des indicateurs spécifiques à l’implémentation.

## <a name="syntax"></a>Syntaxe


```C++
void WINAPI glHint(
   GLenum target,
   GLenum mode
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*cible* 
</dt> <dd>

Constante symbolique indiquant le comportement à contrôler. Les constantes symboliques suivantes, ainsi que la sémantique suggérée, sont acceptées.



| Valeur                                                                                                                                                                                                              | Signification                                                                                                                                                                                                                                                                                                           |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_FOG_HINT"></span><span id="gl_fog_hint"></span><dl> <dt>**\_indicateur de brouillard GL \_**</dt> </dl>                                                           | Indique l’exactitude du calcul du brouillard. Si le calcul du brouillard par pixel n’est pas efficacement pris en charge par l’implémentation OpenGL, l’affinement du GL sans \_ \_ souci ou le GL le \_ plus rapide peut entraîner un calcul par vertex des effets de brouillard.<br/>                                                                          |
| <span id="GL_LINE_SMOOTH_HINT"></span><span id="gl_line_smooth_hint"></span><dl> <dt>**\_ \_ indicateur lisse de la ligne GL \_**</dt> </dl>                                  | Indique la qualité d’échantillonnage des lignes avec anticrénelage. L’affinement \_ du grand livre peut entraîner la génération d’un plus grand nombre de fragments de pixels au cours de la pixellisation, si une fonction de filtre plus grande est appliquée.<br/>                                                                                                               |
| <span id="GL_PERSPECTIVE_CORRECTION_HINT"></span><span id="gl_perspective_correction_hint"></span><dl> <dt>**indicateur de correction de la \_ perspective GL \_ \_**</dt> </dl> | Indique la qualité de l’interpolation des coordonnées de couleur et de texture. Si l’interpolation des paramètres corrigés par la perspective n’est pas efficacement prise en charge par l’implémentation OpenGL, l’affinement du GL sans \_ \_ souci ou le GL le \_ plus rapide peut entraîner une interpolation linéaire simple des couleurs et/ou des coordonnées de texture.<br/> |
| <span id="GL_POINT_SMOOTH_HINT"></span><span id="gl_point_smooth_hint"></span><dl> <dt>**\_indicateur de \_ lissage du point GL \_**</dt> </dl>                               | Indique la qualité d’échantillonnage des points antialiasés. L’affinement \_ du grand livre peut entraîner la génération d’un plus grand nombre de fragments de pixels au cours de la pixellisation, si une fonction de filtre plus grande est appliquée.<br/>                                                                                                              |
| <span id="GL_POLYGON_SMOOTH_HINT"></span><span id="gl_polygon_smooth_hint"></span><dl> <dt>**\_ \_ indicateur lisse de polygone GL \_**</dt> </dl>                         | Indique la qualité d’échantillonnage des polygones avec anticrénelage. L’affinement \_ du grand livre peut entraîner la génération d’un plus grand nombre de fragments de pixels au cours de la pixellisation, si une fonction de filtre plus grande est appliquée.<br/>                                                                                                            |



 

</dd> <dt>

*mode* 
</dt> <dd>

Constante symbolique indiquant le comportement souhaité. Les constantes symboliques suivantes sont acceptées.



| Valeur                                                                                                                                                       | Signification                                                                   |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <span id="GL_FASTEST"></span><span id="gl_fastest"></span><dl> <dt>**GL \_ plus rapide**</dt> </dl>        | L’option la plus efficace doit être choisie.<br/>                    |
| <span id="GL_NICEST"></span><span id="gl_nicest"></span><dl> <dt>**GL plus \_ agréable**</dt> </dl>           | L’option la plus correcte, ou la meilleure, doit être choisie.<br/> |
| <span id="GL_DONT_CARE"></span><span id="gl_dont_care"></span><dl> <dt>**comptabilité \_ générale \_**</dt> </dl> | Le client n’a pas de préférence.<br/>                          |



 

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Cette fonction ne retourne pas de valeur.

## <a name="error-codes"></a>Codes d’erreur

Les codes d’erreur suivants peuvent être récupérés par la fonction [**glGetError**](glgeterror.md) .



| Nom                                                                                                  | Signification                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_enum GL non valide \_**</dt> </dl>      | la *cible* ou le *mode* n’était pas une valeur acceptée.<br/>                                                                              |
| <dl> <dt>**\_opération non valide du GL \_**</dt> </dl> | La fonction a été appelée entre un appel à [**glBegin**](glbegin.md) et l’appel correspondant à [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Notes

Lorsqu’il y a de la place pour l’interprétation, vous pouvez contrôler certains aspects du comportement OpenGL avec des indicateurs. Vous spécifiez un indicateur avec deux arguments. Le paramètre *target* est une constante symbolique indiquant le comportement à contrôler et le *mode* est une autre constante symbolique indiquant le comportement souhaité.

Bien que les aspects d’implémentation qui peuvent être Hints soient bien définis, l’interprétation des indications dépend de l’implémentation.

La fonction **glHint** peut être ignorée.

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
</dt> </dl>

 

 





