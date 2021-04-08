---
title: fonction glTexEnviv (GL. h)
description: La fonction glTexEnviv définit un paramètre d’environnement de texture.
ms.assetid: e98ce736-cc68-4687-8c1b-6b0fef7a677a
keywords:
- glTexEnviv fonction OpenGL
topic_type:
- apiref
api_name:
- glTexEnviv
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b5ec232f559e8d4af10369ebe98dd0aea71e36b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103844389"
---
# <a name="gltexenviv-function"></a>glTexEnviv fonction)

La fonction **glTexEnviv** définit un paramètre d’environnement de texture.

## <a name="syntax"></a>Syntaxe


```C++
void WINAPI glTexEnviv(
         GLenum target,
         GLenum pname,
   const GLint  *params
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*cible* 
</dt> <dd>

Environnement de texture. Doit être une \_ texture GL \_ env.

</dd> <dt>

*pname* 
</dt> <dd>

Nom symbolique d’un paramètre d’environnement de texture à valeur unique. Les valeurs acceptées sont \_ le \_ mode env de la texture du GL \_ et la couleur de la \_ texture GL \_ env \_ .

</dd> <dt>

*params* 
</dt> <dd>

Pointeur vers un tableau de paramètres : une constante symbolique unique ou une couleur RVBA.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Cette fonction ne retourne pas de valeur.

## <a name="error-codes"></a>Codes d’erreur

Les codes d’erreur suivants peuvent être récupérés par la fonction [**glGetError**](glgeterror.md) .



| Nom                                                                                                  | Signification                                                                                                                                                                           |
|-------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_enum GL non valide \_**</dt> </dl>      | *target* ou *pname* ne faisait pas partie des valeurs définies acceptées, ou lorsque les *paramètres* devaient avoir une valeur de constante définie (basée sur la valeur de *pname*) et ne l’a pas fait.<br/> |
| <dl> <dt>**\_opération non valide du GL \_**</dt> </dl> | La fonction a été appelée entre un appel à [**glBegin**](glbegin.md) et l’appel correspondant à [**glEnd**](glend.md).<br/>                                             |



## <a name="remarks"></a>Notes

Un environnement de texture spécifie la manière dont les valeurs de texture sont interprétées lorsqu’un fragment est texturé. Le paramètre *cible* doit être de la \_ texture GL \_ env. Le paramètre *pname* peut être le \_ mode env de la texture GL ou la \_ \_ couleur de la texture du GL \_ \_ \_ .

Si *pname* est \_ \_ \_ le mode de texture GL env, alors *params* est (ou pointe vers) le nom symbolique d’une fonction de texture. Trois fonctions de texture sont définies : \_ module de comptabilité GL, \_ décalque GL et fusion du GL \_ .

Une fonction de texture agit sur le fragment pour être texturée à l’aide de la valeur d’image de texture qui s’applique au fragment (voir [**glTexParameter**](gltexparameter-functions.md)) et produit une couleur RVBA pour ce fragment. Le tableau suivant montre comment la couleur RVBA est produite pour chacune des trois fonctions de texture qui peuvent être choisies. *C* est une triple des valeurs de couleur (RGB) et *a* est la valeur alpha associée. Les valeurs RVBA extraites d’une image de texture sont comprises dans la plage \[ 0, 1 \] . L’indice *f* fait référence au fragment entrant, l’indice *t* à l’image de texture, l’indice *c* à la couleur de l’environnement de texture et l’indice *v* indique une valeur produite par la fonction de texture.

Une image de texture peut avoir jusqu’à quatre composants par élément de texture (consultez [**glTexImage1D**](glteximage1d.md) et [**glTexImage2D**](glteximage2d.md)). Dans une image à un composant, lt indique que seul un composant. Une image à deux composants utilise *L ?*  et *un ?* . Une image à trois composants a uniquement une valeur de couleur, *C ?* . Une image à quatre composants a-t-elle une valeur de couleur *C ?*  et une valeur alpha *A ?* .



<table>
<thead>
<tr class="header">
<th>Nombre de composants</th>
<th>GL_MODULATE</th>
<th>GL_DECAL</th>
<th>GL_BLEND</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td rowspan="2">1 $ {REMOVE} $<br />
</td>
<td><em>C<sub>v</sub> </em>   =  <em>L ?</em> <em>C<sub>f</sub></em></td>
<td rowspan="2">$ {REMOVE} $ non défini<br />
</td>
<td><em>C<sub>v</sub> </em>   =  <em>(1</em> - <em>L ?</em> <em>) C<sub>f</sub> </em> + <em></em> <em>C<sub>c</sub></em></td>
</tr>
<tr class="even">
<td><em>Un<sub>v</sub> </em>   =  <em>Un<sub>f</sub> </em></td>
<td><em>Un<sub>v</sub> </em>   =  <em>Un<sub>f</sub> </em></td>


</tr>
<tr class="odd">
<td rowspan="2">2 $ {REMOVE} $<br />
</td>
<td><em>C<sub>v</sub> </em>   =  <em>L ?</em> <em>C<sub>f</sub></em></td>
<td rowspan="2">$ {REMOVE} $ non défini<br />
</td>
<td><em>C<sub>v</sub> </em>   =  <em>(1</em> - <em>L ?</em> <em>) C<sub>f</sub> </em> + <em></em> <em>C<sub>c</sub></em></td>
</tr>
<tr class="even">
<td><em>Un<sub>v</sub> </em>   =  <em>Un<sub>f</sub> </em></td>
<td><em>Un<sub>v</sub> </em>   =  <em>Un<sub>f</sub> </em></td>


</tr>
<tr class="odd">
<td rowspan="2">3 $ {REMOVE} $<br />
</td>
<td><em>C<sub>v</sub> </em>   =  <em>C ?</em> <em>C<sub>f</sub></em></td>
<td><em>C<sub>v</sub> </em>   =  <em>C ?</em></td>
<td rowspan="2">$ {REMOVE} $ non défini<br />
</td>
</tr>
<tr class="even">
<td><em>Un<sub>v</sub> </em>   =  <em>Un<sub>f</sub> </em> </td>
<td><em>Un<sub>v</sub> </em>   =  <em>Un<sub>f</sub> </em></td>


</tr>
<tr class="odd">
<td rowspan="2">4 $ {REMOVE} $<br />
</td>
<td><em>C<sub>v</sub> </em>   =  <em>C ?</em> <em>C<sub>f</sub></em></td>
<td><em>C<sub>v</sub> </em> = (1- <em>A ?</em> <em>) C<sub>f</sub> </em> + <em>A ?</em> <em>Secteur?</em></td>
<td rowspan="2">$ {REMOVE} $ non défini<br />
</td>
</tr>
<tr class="even">
<td><em>Un<sub>v</sub> </em>   =  <em>R ?</em> <em>Un<sub>f</sub></em> </td>
<td><em>Un<sub>v</sub> </em>   =  <em>Un<sub>f</sub> </em></td>


</tr>
</tbody>
</table>



 

Si pname correspond \_ \_ \_ à la couleur de la texture du GL, *params* est un pointeur vers un tableau qui contient une couleur RVBA composée de quatre valeurs. Les composants de couleur entier sont interprétés de manière linéaire de telle sorte que l’entier le plus positif est mappé à 1,0, et l’entier le plus négatif est mappé à-1,0. Les valeurs sont ancrées à la plage \[ 0, 1 \] quand elles sont spécifiées. *C <sub>c</sub>* accepte ces quatre valeurs.

Le \_ \_ mode env de la texture GL \_ est défini par défaut sur la valeur par défaut du module comptabilité GL \_ et la \_ couleur de la texture de la comptabilité \_ env \_ est (0, 0, 0, 0).

La fonction suivante récupère des informations relatives à **glTexEnviv**:

[**glTexGetEnviv**](glgettexenviv.md)

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

[**glTexImage1D**](glteximage1d.md)
</dt> <dt>

[**glTexImage2D**](glteximage2d.md)
</dt> <dt>

[**glTexParameter**](gltexparameter-functions.md)
</dt> </dl>

 

 





