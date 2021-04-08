---
title: fonction glGetLightfv (GL. h)
description: Les fonctions glGetLightfv et glGetLightiv retournent des valeurs de paramètre de source lumineuse. | fonction glGetLightfv (GL. h)
ms.assetid: 81049726-426e-4f90-bb8e-e5d467870260
keywords:
- glGetLightfv fonction OpenGL
topic_type:
- apiref
api_name:
- glGetLightfv
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: faf90cb9567822ef578bdf01805648a2dabd02db
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "103869785"
---
# <a name="glgetlightfv-function"></a>glGetLightfv fonction)

Les fonctions **glGetLightfv** et [**glGetLightiv**](glgetlightiv.md) retournent des valeurs de paramètre de source lumineuse.

## <a name="syntax"></a>Syntaxe


```C++
void WINAPI glGetLightfv(
   GLenum  light,
   GLenum  pname,
   GLfloat *params
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*light* 
</dt> <dd>

Source de lumière. Le nombre d’éclairages possibles dépend de l’implémentation, mais au moins huit lumières sont prises en charge. Ils sont identifiés par des noms symboliques de la forme livre- \_ lumière *i* , où 0 = *i* < les lumières du GL \_ Max \_ .

</dd> <dt>

*pname* 
</dt> <dd>

Paramètre de source de lumière pour la *lumière*. Les noms symboliques suivants sont acceptés.



| Valeur                                                                                                                                                                                           | Signification                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_AMBIENT"></span><span id="gl_ambient"></span><dl> <dt>**ambiant du GL \_**</dt> </dl>                                            | Le paramètre *params* retourne quatre valeurs entières ou à virgule flottante représentant l’intensité ambiante de la source de lumière. Les valeurs entières, quand elles sont demandées, sont mappées de façon linéaire à partir de la représentation interne à virgule flottante, de sorte que 1,0 correspond à la valeur entière représentable la plus positive, et-1,0 correspond à la valeur entière représentable la plus négative. Si la valeur interne est en dehors de la plage \[ -1, 1 \] , la valeur de retour de l’entier correspondant n’est pas définie.<br/>                                                                                                                                                                  |
| <span id="GL_DIFFUSE"></span><span id="gl_diffuse"></span><dl> <dt>**\_diffusion GL**</dt> </dl>                                            | Le paramètre *params* retourne quatre valeurs entières ou à virgule flottante représentant l’intensité diffuse de la source de lumière. Les valeurs entières, quand elles sont demandées, sont mappées de façon linéaire à partir de la représentation interne à virgule flottante, de sorte que 1,0 correspond à la valeur entière représentable la plus positive, et-1,0 correspond à la valeur entière représentable la plus négative. Si la valeur interne est en dehors de la plage \[ -1, 1 \] , la valeur de retour de l’entier correspondant n’est pas définie.<br/>                                                                                                                                                                  |
| <span id="GL_SPECULAR"></span><span id="gl_specular"></span><dl> <dt>**\_spéculaire GL**</dt> </dl>                                         | Le paramètre *params* retourne quatre valeurs entières ou à virgule flottante représentant l’intensité spéculaire de la source de lumière. Les valeurs entières, quand elles sont demandées, sont mappées de façon linéaire à partir de la représentation interne à virgule flottante, de sorte que 1,0 correspond à la valeur entière représentable la plus positive, et-1,0 correspond à la valeur entière représentable la plus négative. Si la valeur interne est en dehors de la plage \[ -1, 1 \] , la valeur de retour de l’entier correspondant n’est pas définie.<br/>                                                                                                                                                                 |
| <span id="GL_POSITION"></span><span id="gl_position"></span><dl> <dt>**\_position GL**</dt> </dl>                                         | Le paramètre *params* retourne quatre valeurs entières ou à virgule flottante représentant la position de la source de lumière. Les valeurs entières, quand elles sont demandées, sont calculées en arrondissant les valeurs à virgule flottante internes à la valeur entière la plus proche. Les valeurs retournées sont celles qui sont gérées en coordonnées oculaires. Elles ne sont pas égales aux valeurs spécifiées à l’aide de [**glLight**](gllight-functions.md), sauf si la matrice modelview a été identifiée au moment de l’appel de **glLight** .<br/>                                                                                                                                                             |
| <span id="GL_SPOT_DIRECTION"></span><span id="gl_spot_direction"></span><dl> <dt>**\_sens du spot GL \_**</dt> </dl>                      | Le paramètre *params* retourne trois valeurs entières ou à virgule flottante représentant le sens de la source de lumière. Les valeurs entières, quand elles sont demandées, sont calculées en arrondissant les valeurs à virgule flottante internes à la valeur entière la plus proche. Les valeurs retournées sont celles qui sont gérées en coordonnées oculaires. Elles ne sont pas égales aux valeurs spécifiées à l’aide de **glLight**, sauf si la matrice modelview a été identifiée au moment de l’appel de **glLight** . Bien que la direction de l’emplacement soit normalisée avant d’être utilisée dans l’équation d’éclairage, les valeurs retournées sont les versions transformées des valeurs spécifiées avant la normalisation.<br/> |
| <span id="GL_SPOT_EXPONENT"></span><span id="gl_spot_exponent"></span><dl> <dt>**exposant de point comptable \_ \_**</dt> </dl>                         | Le paramètre *params* retourne un entier unique ou une valeur à virgule flottante représentant l’exposant de la lumière. Une valeur entière, quand elle est demandée, est calculée en arrondissant la représentation à virgule flottante interne à l’entier le plus proche.<br/>                                                                                                                                                                                                                                                                                                                                                                                                |
| <span id="GL_SPOT_CUTOFF"></span><span id="gl_spot_cutoff"></span><dl> <dt>**coupure de l' \_ emplacement GL \_**</dt> </dl>                               | Le paramètre *params* retourne un entier unique ou une valeur à virgule flottante représentant l’angle de coupure de la lumière. Une valeur entière, quand elle est demandée, est calculée en arrondissant la représentation à virgule flottante interne à l’entier le plus proche.<br/>                                                                                                                                                                                                                                                                                                                                                                                            |
| <span id="GL_CONSTANT_ATTENUATION"></span><span id="gl_constant_attenuation"></span><dl> <dt>**\_atténuation constante du GL \_**</dt> </dl>    | Le paramètre *params* retourne un entier unique ou une valeur à virgule flottante représentant l’atténuation de la lumière constante (et non liée à la distance). Une valeur entière, quand elle est demandée, est calculée en arrondissant la représentation à virgule flottante interne à l’entier le plus proche.<br/>                                                                                                                                                                                                                                                                                                                                                                  |
| <span id="GL_LINEAR_ATTENUATION"></span><span id="gl_linear_attenuation"></span><dl> <dt>**\_atténuation linéaire du GL \_**</dt> </dl>          | Le paramètre *params* retourne un entier unique ou une valeur à virgule flottante représentant l’atténuation linéaire de la lumière. Une valeur entière, quand elle est demandée, est calculée en arrondissant la représentation à virgule flottante interne à l’entier le plus proche.<br/>                                                                                                                                                                                                                                                                                                                                                                                           |
| <span id="GL_QUADRATIC_ATTENUATION"></span><span id="gl_quadratic_attenuation"></span><dl> <dt>**\_atténuation quadratique du \_ GL**</dt> </dl> | Le paramètre *params* retourne un entier unique ou une valeur à virgule flottante représentant l’atténuation quadratique de la lumière. Une valeur entière, quand elle est demandée, est calculée en arrondissant la représentation à virgule flottante interne à l’entier le plus proche.<br/>                                                                                                                                                                                                                                                                                                                                                                                        |



 

</dd> <dt>

*params* 
</dt> <dd>

Retourne les données demandées.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Cette fonction ne retourne pas de valeur.

## <a name="remarks"></a>Notes

La fonction **glGetLight** retourne dans *params* la ou les valeurs d’un paramètre de source lumineuse. Le paramètre *Light* nomme la lumière et est un nom symbolique de la forme GL \_ Light *i* pour 0 = *i* < \_ lumières Max GL \_ , où les \_ lumières Max GL \_ sont une constante dépendante de l’implémentation supérieure ou égale à huit. Le paramètre *pname* spécifie l’un des dix paramètres de la source lumineuse, à nouveau par le nom symbolique.

C’est toujours le cas que GL \_ Light *i* = GL \_ LIGHT0 + *i*.

Si une erreur est générée, aucune modification n’est apportée au contenu des *paramètres*.

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

[**glLight**](gllight-functions.md)
</dt> </dl>

 

 





