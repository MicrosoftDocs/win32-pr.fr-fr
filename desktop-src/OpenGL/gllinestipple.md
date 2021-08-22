---
title: fonction glLineStipple (GL. h)
description: La fonction glLineStipple spécifie le modèle de stipple de ligne.
ms.assetid: 256d968c-9e72-4aec-9faf-afe70f1087a8
keywords:
- glLineStipple fonction OpenGL
topic_type:
- apiref
api_name:
- glLineStipple
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 33f350611afa0621c1bf883e8f2ac7dc24e50362912296f15d1443e2c638b7bf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119493019"
---
# <a name="gllinestipple-function"></a>glLineStipple fonction)

La fonction **glLineStipple** spécifie le modèle de stipple de ligne.

## <a name="syntax"></a>Syntaxe


```C++
void WINAPI glLineStipple(
   GLint    factor,
   GLushort pattern
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*factorisés* 
</dt> <dd>

Multiplicateur pour chaque bit dans le modèle stipple de la ligne. Si *Factor* est égal à 3, par exemple, chaque bit du modèle sera utilisé trois fois avant l’utilisation du bit suivant dans le modèle. Le paramètre *Factor* est ancré à la plage \[ 1, 256 \] et prend par défaut la valeur un.

</dd> <dt>

*pattern* 
</dt> <dd>

Entier 16 bits dont le modèle de bits détermine les fragments d’une ligne qui seront dessinés lorsque la ligne est pixellisée. Le bit zéro est utilisé en premier, et le modèle par défaut est All.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Cette fonction ne retourne pas de valeur.

## <a name="error-codes"></a>Codes d’erreur

Le code d’erreur suivant peut être récupéré par la fonction [**glGetError**](glgeterror.md) .



| Name                                                                                                  | Signification                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_opération non valide du GL \_**</dt> </dl> | La fonction a été appelée entre un appel à [**glBegin**](glbegin.md) et l’appel correspondant à [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Remarques

La fonction **glLineStipple** spécifie le modèle de stipple de ligne. La ligne stippling masque certains fragments produits par la pixellisation ; ces fragments ne seront pas dessinés. Le masquage est effectué à l’aide de trois paramètres : *le modèle de modèle stipple* de ligne de 16 bits, le *facteur* nombre de répétitions et *un compteur stipple* entier.

Le compteur *s* est remis à zéro chaque fois que [**glBegin**](glbegin.md) est appelé, et avant que chaque segment de ligne d’une séquence **glBegin**( \_ lignes GL)/**glEnd** soit généré. Il est incrémenté après la génération de chaque fragment d’un segment de ligne avec alias de largeur d’unité, ou après la génération *de chaque fragment* d’un segment de ligne de largeur *i* . Les fragments *i* associés à Count *s* sont masqués si le bit de *motif* (  /  *facteur* s) mod 16 est égal à zéro. Dans le cas contraire, ces fragments sont envoyés au trame. Le bit zéro du *modèle* est le bit le moins significatif.

Les lignes avec un alias sont traitées comme une séquence de rectangles de *largeur* 1x à des fins de stippling. Rectangle *s* est pixellisé ou non en fonction de la règle de fragmentation décrite pour les lignes avec alias ; elle compte des rectangles plutôt que des groupes de fragments.

La ligne stippling est activée ou désactivée à l’aide de [**glEnable**](glenable.md) et **glDisable** avec l’argument, \_ ligne \_ STIPPLE. Quand cette option est activée, le modèle de stipple de ligne est appliqué comme décrit ci-dessus. Quand elle est désactivée, elle est comme si le modèle était tous des. Au départ, la ligne stippling est désactivée.

Les fonctions suivantes récupèrent les informations relatives à **glLineStipple**:

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) avec argument \_ modèle de \_ STIPPLE de ligne de GL \_

**glGet** avec argument GL \_ line \_ STIPPLE \_ REPEAT

[**glIsEnabled**](glisenabled.md) avec argument GL \_ ligne \_ STIPPLE

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

[**glLineWidth**](gllinewidth.md)
</dt> <dt>

[**glPolygonStipple**](glpolygonstipple.md)
</dt> </dl>

 

 





