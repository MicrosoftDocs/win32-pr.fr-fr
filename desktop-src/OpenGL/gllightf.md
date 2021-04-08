---
title: fonction glLightf (GL. h)
description: La fonction glLightf retourne des valeurs de paramètre de source lumineuse.
ms.assetid: d9f93fd9-6674-486f-a3fc-c10255dd37e7
keywords:
- glLightf fonction OpenGL
topic_type:
- apiref
api_name:
- glLightf
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 099490461f5fbf6feb009e98c0228165938326d3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743124"
---
# <a name="gllightf-function"></a>glLightf fonction)

La fonction **glLightf** retourne des valeurs de paramètre de source lumineuse.

## <a name="syntax"></a>Syntaxe


```C++
void WINAPI glLightf(
   GLenum  light,
   GLenum  pname,
   GLfloat param
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*light* 
</dt> <dd>

Identificateur d’une lumière. Le nombre d’éclairages possibles dépend de l’implémentation, mais au moins huit lumières sont prises en charge. Ils sont identifiés par des noms symboliques de la forme livre \_ -lumière *i* , où *i* est une valeur : 0 aux \_ indicateurs Max GL \_ -1.

</dd> <dt>

*pname* 
</dt> <dd>

Paramètre de source de lumière à valeur unique pour la *lumière*. Les noms symboliques suivants sont acceptés.



| Valeur                                                                                                                                                                                                                                                                                                                                               | Signification                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_SPOT_EXPONENT"></span><span id="gl_spot_exponent"></span><dl> <dt>**exposant de point comptable \_ \_**</dt> </dl>                                                                                                                                                                             | Le paramètre *param* est une valeur à virgule flottante unique qui spécifie la distribution d’intensité de la lumière. Les valeurs à virgule flottante sont mappées directement. Seules les valeurs de la plage \[ 0, 128 \] sont acceptées. <br/> L’intensité de la lumière réelle est atténuée par le cosinus de l’angle entre la direction de la lumière et la direction de la lumière jusqu’au sommet qui est éclairé, élevé à la puissance de l’exposant. Par conséquent, les exposants de point plus élevés produisent une source de lumière plus ciblée, quel que soit l’angle de coupure des points. L’exposant de point par défaut est 0, ce qui entraîne une distribution uniforme de la lumière.<br/> |
| <span id="GL_SPOT_CUTOFF"></span><span id="gl_spot_cutoff"></span><dl> <dt>**coupure de l' \_ emplacement GL \_**</dt> </dl>                                                                                                                                                                                   | Le paramètre *param* est une valeur à virgule flottante unique qui spécifie l’angle d’étalement maximal d’une source de lumière. Les valeurs à virgule flottante sont mappées directement. Seules les valeurs comprises dans la plage \[ 0, 90 \] et la valeur spéciale 180 sont acceptées. <br/> Si l’angle entre la direction de la lumière et la direction de la lumière vers le vertex en clair est supérieur à l’angle de coupure de l’emplacement, la lumière est entièrement masquée. Dans le cas contraire, son intensité est contrôlée par l’exposant ponctuel et les facteurs d’atténuation. Le point de coupure par défaut est de 180, ce qui aboutit à une distribution de la lumière uniforme.<br/>       |
| <span id="GL_CONSTANT_ATTENUATION__GL_LINEAR_ATTENUATION__GL_QUADRATIC_ATTENUATION"></span><span id="gl_constant_attenuation__gl_linear_attenuation__gl_quadratic_attenuation"></span><dl> <dt>**\_atténuation constante du GL \_ , \_ atténuation linéaire du GL \_ , \_ \_ atténuation quadratique du GL**</dt> </dl> | Le paramètre *param* est une valeur à virgule flottante unique qui spécifie l’un des trois facteurs d’atténuation légère. Les valeurs à virgule flottante sont mappées directement. Seules les valeurs non négatives sont acceptées. <br/> Si la lumière est positionnelle plutôt que directionnelle, son intensité est atténuée par la réciproque de la somme de : le facteur de constante, le facteur linéaire multiplié par la distance entre la lumière et le vertex qui est éclairé et le facteur quadratique multiplié par le carré de la même distance. Les facteurs d’atténuation par défaut sont (1, 0, 0), ce qui n’entraîne aucune atténuation.<br/>                   |



 

</dd> <dt>

*param* 
</dt> <dd>

Spécifie la valeur affectée au paramètre *pname* de Light source *Light* .

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Cette fonction ne retourne pas de valeur.

## <a name="error-codes"></a>Codes d’erreur

Les codes d’erreur suivants peuvent être récupérés par la fonction [**glGetError**](glgeterror.md) .



| Nom                                                                                                  | Signification                                                                                                                                                                                                                   |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_enum GL non valide \_**</dt> </dl>      | *Light* ou *pname* n’était pas une valeur acceptée.<br/>                                                                                                                                                                  |
| <dl> <dt>**\_valeur non valide du GL \_**</dt> </dl>     | Une valeur d’exposant de point a été spécifiée en dehors de la plage \[ 0, 128 \] ou la coupure de place a été spécifiée en dehors de la plage \[ 0, 90 \] (à l’exception de la valeur spéciale 180) ou un facteur d’atténuation négatif a été spécifié.<br/> |
| <dl> <dt>**\_opération non valide du GL \_**</dt> </dl> | La fonction a été appelée entre un appel à [**glBegin**](glbegin.md) et l’appel correspondant à [**glEnd**](glend.md).<br/>                                                                                     |



## <a name="remarks"></a>Notes

La fonction **glLightf** définit la valeur ou les valeurs des paramètres de la source lumineuse individuelle. Le paramètre *Light* nomme la lumière et est un nom symbolique de la forme GL \_ Light *i*, où 0 = *i* < \_ lumières Max GL \_ .

Le paramètre *pname* spécifie l’un des paramètres de la source légère, à nouveau par son nom symbolique. Le paramètre *param* est soit une valeur unique, soit un pointeur vers un tableau qui contient les nouvelles valeurs.

Le calcul de l’éclairage est activé et désactivé à l’aide de [**glEnable**](glenable.md) et [**glDisable**](gldisable.md) avec l’éclairage de l’argument GL \_ . Lorsque l’éclairage est activé, les sources lumineuses activées contribuent au calcul de l’éclairage. Source de lumière *i* est activée et désactivée à l’aide de **glEnable** et **glDisable** avec l’argument GL \_ Light *i*.

C’est toujours le cas que GL \_ Light *i* = GL \_ LIGHT0 + *i*.

Les fonctions suivantes récupèrent les informations relatives à la fonction **glLightf** :

[**glGetLight**](glgetlight.md)

[**glIsEnabled**](glisenabled.md) avec argument GL \_ Lighting

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

[**glColorMaterial**](glcolormaterial.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glLightModel**](gllightmodel-functions.md)
</dt> <dt>

[**glMaterial**](glmaterial-functions.md)
</dt> </dl>

 

 





