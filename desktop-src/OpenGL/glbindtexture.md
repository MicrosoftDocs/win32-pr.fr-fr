---
title: fonction glBindTexture (GL. h)
description: La fonction glBindTexture permet la création d’une texture nommée qui est liée à une cible de texture.
ms.assetid: 800f2360-b40e-4911-9a45-6f310aeeefeb
keywords:
- glBindTexture fonction OpenGL
topic_type:
- apiref
api_name:
- glBindTexture
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e76009a486e3903ad8230891af8b7593ab8aaa47
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384828"
---
# <a name="glbindtexture-function"></a>glBindTexture fonction)

La fonction **glBindTexture** permet la création d’une texture nommée qui est liée à une cible de texture.

## <a name="syntax"></a>Syntaxe


```C++
void WINAPI glBindTexture(
   GLenum target,
   GLuint texture
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*cible* 
</dt> <dd>

Cible à laquelle la texture est liée. Doit avoir la texture GL \_ valeur \_ 1D ou la \_ texture GL \_ 2D.

</dd> <dt>

*motif* 
</dt> <dd>

Nom d’une texture ; le nom de la texture ne peut pas être actuellement utilisé.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Cette fonction ne retourne pas de valeur.

## <a name="error-codes"></a>Codes d’erreur

Les codes d’erreur suivants peuvent être récupérés par la fonction [**glGetError**](glgeterror.md) .



| Nom                                                                                                  | Signification                                                                                                                                                                                                            |
|-------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_enum GL non valide \_**</dt> </dl>      | La *cible* du paramètre n’est pas une valeur acceptée.<br/>                                                                                                                                                       |
| <dl> <dt>**\_opération non valide du GL \_**</dt> </dl> | La *texture* de paramètre n’a pas la même dimensionnalité que la *cible*, ou la fonction a été appelée entre un appel à [**glBegin**](glbegin.md) et l’appel correspondant à [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Notes

La fonction **glBindTexture** vous permet de créer une texture nommée. L’appel de **glBindTexture** avec *target* défini sur la texture GL \_ \_ 1J ou GL \_ texture \_ 2D, et *texture* définie sur le nom de la nouvelle texture que vous avez créée lie le nom de la texture à la cible de texture appropriée. Quand une texture est liée à une cible, la liaison précédente pour cette cible n’est plus appliquée.

Les noms de texture sont des entiers non signés dont la valeur zéro est réservée pour représenter la texture par défaut de chaque cible de texture. Les noms de texture et le contenu de texture correspondant sont locaux à l’espace de liste d’affichage partagé du contexte de rendu OpenGL actuel ; deux contextes de rendu partagent des noms de texture uniquement s’ils partagent également des listes d’affichage. Vous pouvez générer un ensemble de nouveaux noms de texture à l’aide de [**glGenTextures**](glgentextures.md).

Lorsqu’une texture est liée pour la première fois, elle suppose la dimensionnalité de sa cible de texture ; une texture liée à une \_ texture GL \_ 1D devient unidimensionnelle et une texture liée à la \_ texture GL \_ 2D devient à deux dimensions. Les opérations que vous effectuez sur une cible de texture affectent également une texture liée à la cible. Lorsque vous interrogez une cible de texture, la valeur de retour est l’état de la texture qui lui est liée. Les cibles de texture deviennent des alias des textures actuellement liées.

Lorsque vous liez une texture à **glBindTexture**, la liaison reste active jusqu’à ce qu’une texture différente soit liée à la même cible ou que vous supprimiez la texture liée avec la fonction [**glDeleteTextures**](gldeletetextures.md) . Une fois que vous avez créé une texture nommée, vous pouvez la lier à une cible de texture qui a la même dimensionnalité que le plus souvent nécessaire.

Il est généralement beaucoup plus rapide d’utiliser **glBindTexture** pour lier une texture nommée existante à l’une des cibles de texture que de recharger l’image de texture à l’aide de [**glTexImage1D**](glteximage1d.md) ou [**glTexImage2D**](glteximage2d.md). Pour contrôler davantage les performances de la texturation, utilisez [**glPrioritizeTextures**](glprioritizetextures.md).

Vous pouvez inclure des appels à **glBindTexture** dans des listes d’affichage.

> [!Note]  
> La fonction **glBindTexture** est disponible uniquement dans OpenGL version 1,1 ou ultérieure.

 

Les fonctions suivantes récupèrent les informations relatives à **glBindTexture**:

-   [**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) avec l’argument \_ Binding GL texture \_ 1D \_

**glGet** avec argument GL \_ texture \_ 2D \_ liaison

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

[**glAreTexturesResident**](glaretexturesresident.md)
</dt> <dt>

[**glDeleteTextures**](gldeletetextures.md)
</dt> <dt>

[**glGenTextures**](glgentextures.md)
</dt> <dt>

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[**glGetTexParameter**](glgettexparameter.md)
</dt> <dt>

[**glIsTexture**](glistexture.md)
</dt> <dt>

[**glPrioritizeTextures**](glprioritizetextures.md)
</dt> <dt>

[**glTexImage1D**](glteximage1d.md)
</dt> <dt>

[**glTexImage2D**](glteximage2d.md)
</dt> <dt>

[**glTexParameter**](gltexparameter-functions.md)
</dt> </dl>

 

 





