---
title: fonction glDrawArrays (GL. h)
description: La fonction glDrawArrays spécifie plusieurs primitives à restituer.
ms.assetid: 6ebd467b-5a63-43e4-b3fd-242c704d7d13
keywords:
- glDrawArrays fonction OpenGL
topic_type:
- apiref
api_name:
- glDrawArrays
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 349ba3407d84d66afd431d14c3fc97b151661f4f783a05734a55d9ba1dc313ce
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118616991"
---
# <a name="gldrawarrays-function"></a>glDrawArrays fonction)

La fonction **glDrawArrays** spécifie plusieurs primitives à restituer.

## <a name="syntax"></a>Syntaxe


```C++
void WINAPI glDrawArrays(
   GLenum  mode,
   GLint   first,
   GLsizei count
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*mode* 
</dt> <dd>

Type de primitives à restituer. Les constantes suivantes spécifient des types de primitives acceptables : les points de GL, le quadrillage de \_ \_ ligne GL, le \_ \_ \_ Bouclage de ligne GL, les \_ lignes de GL, la \_ bande triangulaire GL \_ , le ventilateur de \_ \_ triangle GL, \_ les triangles GL, le GL \_ Quad \_ Strip, \_ les quads GL et le \_ polygone GL.

</dd> <dt>

*first* 
</dt> <dd>

Index de départ dans les tableaux activés.

</dd> <dt>

*count* 
</dt> <dd>

Nombre d’index à restituer.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Cette fonction ne retourne pas de valeur.

## <a name="error-codes"></a>Codes d’erreur

Les codes d’erreur suivants peuvent être récupérés par la fonction [**glGetError**](glgeterror.md) .



| Nom                                                                                                  | Signification                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_valeur non valide du GL \_**</dt> </dl>     | le *nombre* était négatif.<br/>                                                                                                      |
| <dl> <dt>**\_enum GL non valide \_**</dt> </dl>      | le *mode* n’était pas une valeur acceptée.<br/>                                                                                          |
| <dl> <dt>**\_opération non valide du GL \_**</dt> </dl> | La fonction a été appelée entre un appel à [**glBegin**](glbegin.md) et l’appel correspondant à [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Remarques

Avec **glDrawArrays**, vous pouvez spécifier plusieurs primitives géométriques à restituer. Au lieu d’appeler des fonctions OpenGL distinctes pour passer chaque vertex, normal ou couleur individuel, vous pouvez spécifier des tableaux distincts de vertex, de normales et de couleurs pour définir une séquence de primitives (le même type) avec un appel unique à **glDrawArrays**.

Quand vous appelez **glDrawArrays**, le *nombre* d’éléments séquentiels de chaque tableau activé est utilisé pour construire une séquence de primitives géométriques, en commençant par le *premier* élément. Le paramètre *mode* spécifie le type de primitive à construire et comment utiliser les éléments de tableau pour construire les primitives.

Une fois **glDrawArrays** retourné, les valeurs des attributs vertex modifiés par **glDrawArrays** ne sont pas définies. Par exemple, si le \_ tableau de couleurs GL \_ est activé, la valeur de la couleur actuelle est non définie après le retour de **glDrawArrays** . Les attributs non modifiés par **glDrawArrays** restent définis. Lorsque \_ \_ le tableau de vertex GL n’est pas activé, aucune primitive géométrique n’est générée, mais les attributs correspondant aux tableaux activés sont modifiés.

Vous pouvez inclure des **glDrawArrays** dans des listes d’affichage. Lorsque vous incluez **glDrawArrays** dans une liste d’affichage, les données de tableau nécessaires, déterminées par les pointeurs de tableau et les activent, sont générées et entrées dans la liste d’affichage. Les valeurs des pointeurs de tableau et des activations sont déterminées lors de la création de listes d’affichage.

Vous pouvez lire les données du tableau statique à tout moment. Si des éléments de tableau statique sont modifiés et que le tableau n’est pas spécifié de nouveau, les résultats de tous les appels suivants à **glDrawArrays** ne sont pas définis.

Bien qu’aucune erreur ne soit générée lorsque vous spécifiez un tableau plusieurs fois dans les paires [**glBegin**](glbegin.md) et [**Glend**](glend.md) , les résultats ne sont pas définis.

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

[**glArrayElement**](glarrayelement.md)
</dt> <dt>

[**glBegin**](glbegin.md)
</dt> <dt>

[**glColorPointer**](glcolorpointer.md)
</dt> <dt>

[**glEdgeFlagPointer**](gledgeflagpointer.md)
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

 

 





