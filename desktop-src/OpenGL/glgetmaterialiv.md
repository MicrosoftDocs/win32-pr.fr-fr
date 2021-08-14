---
title: fonction glGetMaterialiv (GL. h)
description: Les fonctions glGetMaterialfv et glGetMaterialiv retournent des paramètres Material. | fonction glGetMaterialiv (GL. h)
ms.assetid: 459cbe8a-a51a-496e-bdd1-89b8cf486a46
keywords:
- glGetMaterialiv fonction OpenGL
topic_type:
- apiref
api_name:
- glGetMaterialiv
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: df6babcac908d59c5a5a51b0a23736b760ed25ec542f58339182d3a7536050be
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118360073"
---
# <a name="glgetmaterialiv-function"></a>glGetMaterialiv fonction)

Les fonctions [**glGetMaterialfv**](glgetmaterialfv.md) et **glGetMaterialiv** retournent des paramètres Material.

## <a name="syntax"></a>Syntaxe


```C++
void WINAPI glGetMaterialiv(
   GLenum face,
   GLenum pname,
   GLint  *params
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*se* 
</dt> <dd>

Spécifie les deux documents en cours d’interrogation. \_Les arrière-plan \_ du GL ou du GL sont acceptés, représentant respectivement les matériaux avant et arrière.

</dd> <dt>

*pname* 
</dt> <dd>

Paramètre Material à retourner. Les valeurs suivantes sont acceptées.



| Valeur                                                                                                                                                                   | Signification                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_AMBIENT"></span><span id="gl_ambient"></span><dl> <dt>**ambiant du GL \_**</dt> </dl>                    | Le paramètre *params* retourne quatre valeurs entières ou à virgule flottante représentant la réflexion ambiante du matériau. Les valeurs entières, quand elles sont demandées, sont mappées de façon linéaire à partir de la représentation interne à virgule flottante, de sorte que 1,0 correspond à la valeur entière représentable la plus positive, et-1,0 correspond à la valeur entière représentable la plus négative. Si la valeur interne est en dehors de la plage \[ -1, 1 \] , la valeur de retour de l’entier correspondant n’est pas définie.<br/>     |
| <span id="GL_DIFFUSE"></span><span id="gl_diffuse"></span><dl> <dt>**\_diffusion GL**</dt> </dl>                    | Le paramètre *params* retourne quatre valeurs entières ou à virgule flottante représentant la réflexion diffuse du matériau. Les valeurs entières, quand elles sont demandées, sont mappées de façon linéaire à partir de la représentation interne à virgule flottante, de sorte que 1,0 correspond à la valeur entière représentable la plus positive, et-1,0 correspond à la valeur entière représentable la plus négative. Si la valeur interne est en dehors de la plage \[ -1, 1 \] , la valeur de retour de l’entier correspondant n’est pas définie.<br/>     |
| <span id="GL_SPECULAR"></span><span id="gl_specular"></span><dl> <dt>**\_spéculaire GL**</dt> </dl>                 | Le paramètre *params* retourne quatre valeurs entières ou à virgule flottante représentant la réflectivité spéculaire du matériau. Les valeurs entières, quand elles sont demandées, sont mappées de façon linéaire à partir de la représentation interne à virgule flottante, de sorte que 1,0 correspond à la valeur entière représentable la plus positive, et-1,0 correspond à la valeur entière représentable la plus négative. Si la valeur interne est en dehors de la plage \[ -1, 1 \] , la valeur de retour de l’entier correspondant n’est pas définie.<br/>    |
| <span id="GL_EMISSION"></span><span id="gl_emission"></span><dl> <dt>**\_émission GL**</dt> </dl>                 | Le paramètre *params* retourne quatre valeurs entières ou à virgule flottante représentant l’intensité lumineuse émise du matériau. Les valeurs entières, quand elles sont demandées, sont mappées de façon linéaire à partir de la représentation interne à virgule flottante, de sorte que 1,0 correspond à la valeur entière représentable la plus positive, et-1,0 correspond à la valeur entière représentable la plus négative. Si la valeur interne est en dehors de la plage \[ -1, 1 \] , la valeur de retour de l’entier correspondant n’est pas définie.<br/> |
| <span id="GL_SHININESS"></span><span id="gl_shininess"></span><dl> <dt>**\_éclat GL**</dt> </dl>              | Le paramètre *params* retourne un entier ou une valeur à virgule flottante représentant l’exposant spéculaire du matériau. Les valeurs entières, quand elles sont demandées, sont calculées en arrondissant la valeur à virgule flottante interne à la valeur entière la plus proche.<br/>                                                                                                                                                                                                                                   |
| <span id="GL_COLOR_INDEXES"></span><span id="gl_color_indexes"></span><dl> <dt>**\_index de couleurs GL \_**</dt> </dl> | Le paramètre *params* retourne trois valeurs entières ou à virgule flottante représentant les index ambiant, diffus et spéculaire du matériau. Utilisez ces index uniquement pour l’éclairage d’index de couleurs. (Les autres paramètres sont utilisés uniquement pour l’éclairage RVBA.) Les valeurs entières, quand elles sont demandées, sont calculées en arrondissant les valeurs à virgule flottante internes aux valeurs entières les plus proches.<br/>                                                                                            |



 

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
| <dl> <dt>**\_enum GL non valide \_**</dt> </dl>      | la *cible* ou la *requête* n’était pas une valeur acceptée.<br/>                                                                             |
| <dl> <dt>**\_opération non valide du GL \_**</dt> </dl> | La fonction a été appelée entre un appel à [**glBegin**](glbegin.md) et l’appel correspondant à [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Remarques

La fonction **glGetMaterial** *retourne dans les paramètres la* valeur ou les valeurs du paramètre *pname* de la *facette* matérielle.

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

[**glMaterial**](glmaterial-functions.md)
</dt> </dl>

 

 





