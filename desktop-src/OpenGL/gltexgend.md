---
title: fonction glTexGend (GL. h)
description: Contrôle la génération des coordonnées de texture. | fonction glTexGend (GL. h)
ms.assetid: 75ab3468-281d-4c8d-95cc-138d75646cdf
keywords:
- glTexGend fonction OpenGL
topic_type:
- apiref
api_name:
- glTexGend
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 45854eb1e2070f334bfc906c249fbb4341ab74d0
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127233616"
---
# <a name="gltexgend-function"></a>glTexGend fonction)

Contrôle la génération des coordonnées de texture.

## <a name="syntax"></a>Syntaxe


```C++
void WINAPI glTexGend(
   GLenum   coord,
   GLenum   pname,
   GLdouble param
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*coordonnées* 
</dt> <dd>

Coordonnée de texture. Il doit s’agir de l’une des valeurs suivantes : GL \_ S, GL \_ T, GL \_ R ou GL \_ Q.

</dd> <dt>

**pname** 
</dt> <dd>

Nom symbolique de la fonction de génération de coordonnée de texture.

</dd> <dt>

*param* 
</dt> <dd>

Un paramètre de génération de texture à valeur unique, l’un des \_ \_ mappages d’objets linéaires linéaires au GL \_ ou de \_ \_ sphères GL \_ .

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Cette fonction ne retourne pas de valeur.

## <a name="error-codes"></a>Codes d’erreur

Les codes d’erreur suivants peuvent être récupérés par la fonction [**glGetError**](glgeterror.md) .



| Nom                                                                                                  | Signification                                                                                                                                                |
|-------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_enum GL non valide \_**</dt> </dl>      | *Coord* ou *pname* n’était pas une valeur définie acceptée, ou l' *pname* était le \_ \_ mode de la génération de texture GL \_ et les *paramètres* n’étaient pas une valeur définie acceptée.<br/> |
| <dl> <dt>**\_enum GL non valide \_**</dt> </dl>      | *pname* était le \_ \_ mode de représentation GL de la texture GL \_ , *params* était plan de la \_ sphère GL \_ et *Coord* était GL \_ R ou GL \_ Q<br/>                                     |
| <dl> <dt>**\_opération non valide du GL \_**</dt> </dl> | La fonction a été appelée entre un appel à [**glBegin**](glbegin.md) et l’appel correspondant à [**glEnd**](glend.md). <br/>                 |



## <a name="remarks"></a>Notes

La fonction **glTexGen** sélectionne une fonction de génération de coordonnée de texture ou fournit des coefficients pour l’une des fonctions. Le paramètre *Coord* nomme une des coordonnées de la texture (s, t, r, q) et doit être l’un des symboles suivants : GL \_ s, GL \_ t, GL \_ r ou GL \_ q. Le paramètre *pname* doit être l’une des trois constantes symboliques suivantes : \_ mode de la génération de texture GL \_ \_ , plan d' \_ objet GL \_ ou \_ plan oculaire GL \_ . Si *pname* est \_ le mode de la génération de textures du GL \_ \_ , alors *param* spécifie un mode, l’un des \_ \_ mappages d’objets linéaires de GL, d' \_ oculaire \_ linéaire ou de la \_ sphère GL \_ . Si *pname* est un plan \_ d’objet GL \_ ou un \_ plan oculaire GL \_ , *param* contient des coefficients pour la fonction de génération de texture correspondante.

Si la fonction de génération de texture \_ est \_ linéaire d’objet linéaire, la fonction

![Équation qui indique la fonction glTexGen lorsque la fonction de génération de texture est GL_OBJECT_LINEAR.](images/tex02.png)

est utilisé, où g est la valeur calculée pour la coordonnée nommée dans Coord ; P1, P2, P3 et P4 sont les quatre valeurs fournies dans params. et x ?, y ?, z ? et w ? sont les coordonnées d’objet du vertex. Vous pouvez utiliser cette fonction pour texturer la carte à l’aide du niveau de mer comme plan de référence (défini par P1, P2, P3 et P4). La \_ \_ fonction de génération de coordonnées linéaires de l’objet GL calcule l’altitude d’un sommet de terrain en tant que distance par rapport au niveau de la mer ; cette altitude est utilisée pour indexer l’image de texture pour mapper la neige blanche sur les pics et le gazon vert sur Foothills, par exemple.

Si la fonction de génération de texture \_ est \_ linéaire pour le GL, la fonction

![Équation qui indique la fonction glTexGen lorsque la fonction de génération de texture est GL_EYE_LINEAR.](images/tex02.png)

est utilisé, où

![Équation représentant les coordonnées oculaires du vertex.](images/tex03.png)

et x ?, y ?, z ? et w ? les coordonnées oculaires du vertex, P1, P2, P3 et P4 sont les valeurs fournies dans *param*, et M est la matrice modelview quand vous appelez **glTexGen**. Si M est mal conditionné ou singulier, les coordonnées de texture générées par la fonction résultante peuvent être inexactes ou non définies.

Les valeurs dans *param* définissent un plan de référence en coordonnées oculaires. La matrice modelview appliquée à ces derniers ne peut pas être la même en vigueur lorsque les sommets du polygone sont transformés. Cette fonction établit un champ de coordonnées de texture qui peut produire des lignes de contour dynamiques sur les objets mobiles.

Si *pname* est la \_ \_ carte de sphère GL et que le *repère* est GL \_ S ou GL \_ t, des coordonnées de texture s et T sont générées comme suit. Prenons le vecteur d’unité qui pointe de l’origine vers le vertex du polygone (en coordonnées oculaires). Supposons que n est la normale actuelle, après la transformation en coordonnées oculaires. Let f = (FX () FY () FZ) T est le vecteur de réflexion de telle sorte que

![Équation qui montre le vecteur de réflexion comme fonction du vecteur d’unité et normal actuel.](images/tex05.png)

Enfin, laissez

![Équation qui présente m en tant que fonction du vecteur de réflexion.](images/tex07.png)

Les valeurs assignées aux coordonnées de texture i et t sont

![Équation présentant les valeurs affectées aux coordonnées de texture i et t.](images/tex06.png)

Vous pouvez activer ou désactiver une fonction de génération de coordonnées de texture à l’aide de [**glEnable**](glenable.md) ou [**glDisable**](gldisable.md) avec l’un des noms de coordonnées de texture symbolique (GL \_ texture \_ GEN \_ S, GL \_ texture \_ GEN \_ T, GL \_ texture \_ GEN \_ R ou GL \_ texture \_ GEN \_ Q) comme argument. Lorsque cette fonction est activée, la coordonnée de texture spécifiée est calculée en fonction de la fonction de génération associée à cette coordonnée. Lorsque la fonction est désactivée, les vertex suivants prennent la coordonnée de texture spécifiée à partir de l’ensemble actuel de coordonnées de texture. Initialement, toutes les fonctions de génération de texture sont définies sur GL \_ Eye \_ linéaire et sont désactivées. Les deux équations de plan s sont (1,0, 0, 0); les deux équations du plan t sont (0, 1, 0, 0); et toutes les équations du plan r et q sont (0,0).

Les fonctions suivantes récupèrent les informations relatives à glTexGen :

<dl>

[**glGetTexGen**](glgettexgen.md)  
[**glIsEnabled**](glisenabled.md) avec argument GL \_ texture \_ GEN \_ S  
[**glIsEnabled**](glisenabled.md) avec argument GL \_ texture \_ GEN \_ T  
[**glIsEnabled**](glisenabled.md) avec argument GL \_ texture \_ GEN \_ R  
[**glIsEnabled**](glisenabled.md) avec argument GL \_ texture \_ GEN \_ Q  
</dl>

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

[**glCopyTexImage2D**](glcopyteximage2d.md)
</dt> <dt>

[**glCopyTexSubImage2D**](glcopytexsubimage2d.md)
</dt> <dt>

[**glGetTexGen**](glgettexgen.md)
</dt> <dt>

[**glIsEnabled**](glisenabled.md)
</dt> <dt>

[**glTexEnv**](gltexenv-functions.md)
</dt> <dt>

[**glTexImage1D**](glteximage1d.md)
</dt> <dt>

[**glTexParameter**](gltexparameter-functions.md)
</dt> <dt>

[**glTexSubImage1D**](gltexsubimage1d.md)
</dt> <dt>

[**glTexSubImage2D**](gltexsubimage2d.md)
</dt> </dl>

 

 





