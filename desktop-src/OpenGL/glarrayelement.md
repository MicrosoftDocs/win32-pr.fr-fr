---
title: fonction glArrayElement (GL. h)
description: La fonction glArrayElement spécifie les éléments de tableau utilisés pour le rendu d’un vertex.
ms.assetid: 2c4d76bb-e4c9-4baa-a190-66298b8a4335
keywords:
- glArrayElement fonction OpenGL
topic_type:
- apiref
api_name:
- glArrayElement
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6a20aff9fcaa5bf922bc9447f7b7022a8cd1a9c2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106512402"
---
# <a name="glarrayelement-function"></a>glArrayElement fonction)

La fonction **glArrayElement** spécifie les éléments de tableau utilisés pour le rendu d’un vertex.

## <a name="syntax"></a>Syntaxe


```C++
void WINAPI glArrayElement(
   GLint index
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*index* 
</dt> <dd>

Index dans les tableaux activés.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Cette fonction ne retourne pas de valeur.

## <a name="remarks"></a>Notes

Utilisez la fonction **glArrayElement** dans les paires [**glBegin**](glbegin.md) et [**glEnd**](glend.md) pour spécifier les données de vertex et d’attribut pour les primitives de point, de ligne et de polygone. La fonction **glArrayElement** spécifie les données d’un vertex unique à l’aide de données de vertex et d’attribut situées à l' *index* des tableaux de vertex activés.

Vous pouvez utiliser **glArrayElement** pour construire des primitives en indexant les données de vertex, plutôt que par diffusion en continu dans les tableaux de données de premier à dernier ordre. Étant donné que **glArrayElement** spécifie un seul vertex uniquement, vous pouvez spécifier explicitement des attributs pour des primitives individuelles. Par exemple, vous pouvez définir un seul normal pour chaque triangle.

Lorsque vous incluez des appels à **glArrayElement** dans des listes d’affichage, les données de tableau nécessaires, déterminées par les pointeurs de tableau et les valeurs Enable, sont également entrées dans la liste d’affichage. Les valeurs de pointeur de tableau et d’activation sont déterminées lors de la création des listes d’affichage, et non lors de l’exécution des listes d’affichage.

Vous pouvez lire et mettre en cache les données du tableau statique à tout moment avec **glArrayElement**. Lorsque vous modifiez les éléments d’un tableau statique sans spécifier à nouveau le tableau, les résultats de tous les appels suivants à **glArrayElement** ne sont pas définis.

Quand vous appelez **glArrayElement** sans appeler d’abord **glEnableClientState**( \_ tableau de vertex GL \_ ), aucun dessin ne se produit, mais les attributs correspondant aux tableaux activés sont modifiés. Bien qu’aucune erreur ne soit générée lorsque vous spécifiez un tableau dans les paires **glBegin** et **glEnd** , les résultats ne sont pas définis.

> [!Note]  
> La fonction **glArrayElement** est disponible uniquement dans OpenGL version 1,1 ou ultérieure.

 

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

[**glColorPointer**](glcolorpointer.md)
</dt> <dt>

[**glDrawArrays**](gldrawarrays.md)
</dt> <dt>

[**glEdgeFlagPointer**](gledgeflagpointer.md)
</dt> <dt>

[**glEnableClientState**](glenableclientstate.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glGetPointerv**](glgetpointerv.md)
</dt> <dt>

[**glGetString**](glgetstring.md)
</dt> <dt>

[**glIndexPointer**](glindexpointer.md)
</dt> <dt>

[**glNormalPointer**](glnormalpointer.md)
</dt> <dt>

[**glTexCoordPointer**](gltexcoordpointer.md)
</dt> <dt>

[**glVertexPointer**](glvertexpointer.md)
</dt> </dl>

 

 





