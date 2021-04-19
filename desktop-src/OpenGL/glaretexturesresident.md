---
title: fonction glAreTexturesResident (GL. h)
description: La fonction glAreTexturesResident détermine si les objets texture spécifiés résident dans la mémoire de texture.
ms.assetid: 55d068a8-d366-4fee-85d5-49373b8c5e02
keywords:
- glAreTexturesResident fonction OpenGL
topic_type:
- apiref
api_name:
- glAreTexturesResident
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8e2e7e5965da9604c690384301de6f1879a98994
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106513790"
---
# <a name="glaretexturesresident-function"></a>glAreTexturesResident fonction)

La fonction **glAreTexturesResident** détermine si les objets texture spécifiés résident dans la mémoire de texture.

## <a name="syntax"></a>Syntaxe


```C++
GLboolean WINAPI glAreTexturesResident(
         GLsizei   n,
   const GLuint    *textures,
         GLboolean *residences
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*n* 
</dt> <dd>

Nombre de textures à interroger.

</dd> <dt>

*texture* 
</dt> <dd>

Adresse d’un tableau contenant les noms des textures à interroger.

</dd> <dt>

*foyers* 
</dt> <dd>

Adresse d’un tableau dans lequel l’état de résidence de la texture est retourné. L’état de résidence d’une texture nommée par un élément de *textures* est retourné dans l’élément correspondant de *résidences*.

</dd> </dl>

## <a name="error-codes"></a>Codes d’erreur

Les codes d’erreur suivants peuvent être récupérés par la fonction [**glGetError**](glgeterror.md) .



| Nom                                                                                                  | Signification                                                                                                                                   |
|-------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_valeur non valide du GL \_**</dt> </dl>     | *n* était une valeur négative, un élément dans *textures* était égal à zéro, ou un élément dans les *textures* ne contenait pas d’identificateur de texture.<br/> |
| <dl> <dt>**\_opération non valide du GL \_**</dt> </dl> | La fonction a été appelée entre un appel à [**glBegin**](glbegin.md) et l’appel correspondant à [**glEnd**](glend.md).<br/>     |



## <a name="remarks"></a>Notes

Sur les ordinateurs avec une quantité limitée de mémoire de texture, OpenGL établit une plage de travail de textures résidant dans la mémoire de texture. Ces textures peuvent être liées à une cible de texture bien plus efficacement que les textures qui ne résident pas.

La fonction **glAreTexturesResident** interroge l’état de résidence des *n* textures désignées par les éléments de *textures*. Si toutes les textures nommées résident, **glAreTexturesResident** retourne \_ la valeur GL true et le contenu des *résidences* n’est pas perturbé. Si l’une des textures nommées n’est pas résidente, **glAreTexturesResident** retourne GL \_ false et l’état détaillé est retourné dans les *n* éléments de *résidences*.

Si un élément de *résidences* est \_ le GL true, la texture nommée par l’élément de *textures* correspondant réside dans la mémoire de texture.

Pour interroger l’état de résidence d’une texture à liaison unique, appelez [**glGetTexParameter**](glgettexparameter.md) avec le paramètre *target* défini sur la texture cible à laquelle la cible est liée et définissez le paramètre *pname* sur la texture du grand livre \_ \_ résident. Vous devez utiliser cette méthode pour interroger l’État résident d’une texture par défaut.

Vous ne pouvez pas inclure des **glAreTexturesResident** dans des listes d’affichage.

La fonction **glAreTexturesResident** retourne l’état de résidence des textures au moment de l’appel. Cela ne garantit pas que les textures restent résidentes à tout moment.

Si les textures résident dans la mémoire virtuelle (il n’y a pas de mémoire de texture), elles sont considérées comme toujours résidentes.

> [!Note]  
> La fonction **glAreTexturesResident** est disponible uniquement dans OpenGL version 1,1 ou ultérieure.

 

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

[**glBindTexture**](glbindtexture.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glGetTexParameter**](glgettexparameter.md)
</dt> <dt>

[**glPrioritizeTextures**](glprioritizetextures.md)
</dt> <dt>

[**glTexImage1D**](glteximage1d.md)
</dt> <dt>

[**glTexImage2D**](glteximage2d.md)
</dt> </dl>

 

 





