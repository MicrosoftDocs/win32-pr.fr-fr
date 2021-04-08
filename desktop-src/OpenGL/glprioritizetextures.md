---
title: fonction glPrioritizeTextures (GL. h)
description: La fonction glPrioritizeTextures définit la priorité de résidence des textures.
ms.assetid: 09018c86-c667-4e43-a95a-51a8077aed33
keywords:
- glPrioritizeTextures fonction OpenGL
topic_type:
- apiref
api_name:
- glPrioritizeTextures
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d38ab4b1bd6b5f9682b4d8753e7e84f1f2b58a09
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740645"
---
# <a name="glprioritizetextures-function"></a>glPrioritizeTextures fonction)

La fonction **glPrioritizeTextures** définit la priorité de résidence des textures.

## <a name="syntax"></a>Syntaxe


```C++
void WINAPI glPrioritizeTextures(
         GLsizei  n,
   const GLuint   *textures,
   const GLclampf *priorities
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*n* 
</dt> <dd>

Nombre de textures à classer par ordre de priorité.

</dd> <dt>

*texture* 
</dt> <dd>

Pointeur vers le premier élément d’un tableau contenant les noms des textures à classer par ordre de priorité.

</dd> <dt>

*priorité* 
</dt> <dd>

Pointeur vers le premier élément d’un tableau contenant les priorités de texture. Une priorité donnée dans un élément *du paramètre* Priorities s’applique à la texture nommée par l’élément correspondant du paramètre *textures* .

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Cette fonction ne retourne pas de valeur.

## <a name="error-codes"></a>Codes d’erreur

Les codes d’erreur suivants peuvent être récupérés par la fonction [**glGetError**](glgeterror.md) .



| Nom                                                                                                  | Signification                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_valeur non valide du GL \_**</dt> </dl>     | *n* était une valeur négative.<br/>                                                                                                  |
| <dl> <dt>**\_opération non valide du GL \_**</dt> </dl> | La fonction a été appelée entre un appel à [**glBegin**](glbegin.md) et l’appel correspondant à [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Notes

La fonction **glPrioritizeTextures** affecte *les n textures de texture* spécifiées dans le paramètre *priorités* aux *n* textures nommées dans le paramètre *textures* . Sur les ordinateurs avec une quantité limitée de mémoire de texture, OpenGL établit une « plage de travail » de textures résidant dans la mémoire de texture. Ces textures peuvent être liées à une cible de texture bien plus efficacement que les textures qui ne résident pas.

En spécifiant une priorité pour chaque texture, la fonction **glPrioritizeTextures** vous permet de déterminer les textures qui doivent résider.

Les éléments de priorité de texture des *priorités* sont bloqués à la plage \[ 0,0, 1,0 \] avant d’être attribués. Zéro indique la priorité la plus faible ; par conséquent, les textures avec la priorité zéro sont les moins susceptibles d’être résidentes. La valeur 1,0 indique la priorité la plus élevée ; par conséquent, les textures avec la priorité 1,0 sont très probablement résidentes. Toutefois, il n’est pas garanti que les textures résident tant qu’elles ne sont pas liées.

La fonction **glPrioritizeTextures** ignore les tentatives de hiérarchisation de texture 0, ou tout nom de texture qui ne correspond pas à une texture existante. Aucune des fonctions nommées par le paramètre *textures* ne doit être liée à une cible de texture.

Si une texture est actuellement liée, vous pouvez également utiliser la fonction [**glTexParameter**](gltexparameter-functions.md) pour définir sa priorité. Il s’agit de la seule façon de définir la priorité d’une texture par défaut.

Vous pouvez inclure des **glPrioritizeTextures** dans des listes d’affichage.

La fonction suivante récupère la priorité d’une texture actuellement liée à **glPrioritizeTextures**:

-   [**glGetTexParameter**](glgettexparameter.md) avec le nom de paramètre \_ priorité de texture GL \_

> [!Note]  
> La fonction **glPrioritizeTextures** est disponible uniquement dans OpenGL version 1,1 ou ultérieure.

 

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

[**glBegin**](glbegin.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glGetTexParameter**](glgettexparameter.md)
</dt> <dt>

[**glTexImage1D**](glteximage1d.md)
</dt> <dt>

[**glTexImage2D**](glteximage2d.md)
</dt> <dt>

[**glTexParameter**](gltexparameter-functions.md)
</dt> </dl>

 

 





