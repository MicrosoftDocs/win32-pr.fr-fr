---
title: fonction glDrawElements (GL. h)
description: La fonction glDrawElements restitue les primitives à partir des données de tableau.
ms.assetid: fb433294-106e-48d5-ad49-4434934fe072
keywords:
- glDrawElements fonction OpenGL
topic_type:
- apiref
api_name:
- glDrawElements
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 976e779235dc330467d610406156534b5e72841d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127311769"
---
# <a name="gldrawelements-function"></a>glDrawElements fonction)

La fonction **glDrawElements** restitue les primitives à partir des données de tableau.

## <a name="syntax"></a>Syntaxe


```C++
void WINAPI glDrawElements(
         GLenum  mode,
         GLsizei count,
         GLenum  type,
   const GLvoid  *indices
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*mode* 
</dt> <dd>

Type de primitives à restituer. Elle peut prendre l’une des valeurs symboliques suivantes : les \_ points de la comptabilité, la bande de facturation GL, la \_ \_ boucle de lignes GL, les \_ \_ \_ lignes de GL, la \_ bande triangulaire GL \_ , le \_ \_ ventilateur de triangle GL, \_ les triangles GL, le GL \_ Quad \_ Strip, \_ les quads GL et le \_ polygone GL.

</dd> <dt>

*count* 
</dt> <dd>

Nombre d’éléments à rendre.

</dd> <dt>

*type* 
</dt> <dd>

Type des valeurs dans les index. Doit être l’un des \_ octets non signés GL \_ , GL \_ unsigned \_ short ou GL \_ unsigned \_ int.

</dd> <dt>

*indices* 
</dt> <dd>

Pointeur vers l’emplacement où les index sont stockés.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Cette fonction ne retourne pas de valeur.

## <a name="error-codes"></a>Codes d’erreur

Les codes d’erreur suivants peuvent être récupérés par la fonction [**glGetError**](glgeterror.md) .



| Nom                                                                                                  | Signification                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_enum GL non valide \_**</dt> </dl>      | le *mode* n’était pas une valeur acceptée.<br/>                                                                                          |
| <dl> <dt>**\_valeur non valide du GL \_**</dt> </dl>     | *Count* est une valeur négative.<br/>                                                                                              |
| <dl> <dt>**\_opération non valide du GL \_**</dt> </dl> | La fonction a été appelée entre un appel à [**glBegin**](glbegin.md) et l’appel correspondant à [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Notes

La fonction **glDrawElements** vous permet de spécifier plusieurs primitives géométriques avec très peu d’appels de fonction. Au lieu d’appeler une fonction OpenGL pour passer chaque vertex, normal ou couleur, vous pouvez spécifier des tableaux distincts de vertex, de normales et de couleurs à l’avance, et les utiliser pour définir une séquence de primitives (tout du même type) à l’aide d’un seul appel à **glDrawElements**.

Quand vous appelez la fonction **glDrawElements** , elle utilise des éléments séquentiels *Count* d' *index* pour construire une séquence de primitives géométriques. Le paramètre *mode* spécifie le type de primitives construites et la façon dont les éléments de tableau sont utilisés pour construire ces Primitives. Si le \_ \_ tableau de vertex GL n’est pas activé, aucune primitive géométrique n’est générée.

Les attributs de vertex modifiés par **glDrawElements** ont une valeur non spécifiée après le retour de **glDrawElements** . Par exemple, si le \_ tableau de couleurs GL \_ est activé, la valeur de la couleur actuelle est non définie après l’exécution de **glDrawElements** . Les attributs qui ne sont pas modifiés restent inchangés.

Vous pouvez inclure la fonction **glDrawElements** dans les listes d’affichage. Lorsque **glDrawElements** est inclus dans une liste d’affichage, les données de tableau nécessaires (déterminées par les pointeurs de tableau et activés) sont également entrées dans la liste d’affichage. Étant donné que les pointeurs de tableau et active sont des variables d’État côté client, leurs valeurs affectent les listes d’affichage quand les listes sont créées, et non lors de l’exécution des listes.

> [!Note]  
> La fonction **glDrawElements** est disponible uniquement dans OpenGL version 1,1 ou ultérieure.

 

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

[**glArrayElement**](glarrayelement.md)
</dt> <dt>

[**glBegin**](glbegin.md)
</dt> <dt>

[**glColorPointer**](glcolorpointer.md)
</dt> <dt>

[**glDrawArrays**](gldrawarrays.md)
</dt> <dt>

[**glEdgeFlagPointer**](gledgeflagpointer.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glGetPointerv**](glgetpointerv.md)
</dt> <dt>

[**glIndexPointer**](glindexpointer.md)
</dt> <dt>

[**glNormalPointer**](glnormalpointer.md)
</dt> <dt>

[**glTexCoordPointer**](gltexcoordpointer.md)
</dt> <dt>

[**glVertexPointer**](glvertexpointer.md)
</dt> </dl>

 

 





