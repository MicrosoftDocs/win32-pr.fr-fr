---
title: fonction glTexCoordPointer (GL. h)
description: La fonction glTexCoordPointer définit un tableau de coordonnées de texture.
ms.assetid: c3640a1b-ccc7-4f1a-94a5-a164f7377dbc
keywords:
- glTexCoordPointer fonction OpenGL
topic_type:
- apiref
api_name:
- glTexCoordPointer
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0892f06b3fd5027939710be9ac74a2ae18c0dc0d712572d094b9a54fd6bb5b3e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119888249"
---
# <a name="gltexcoordpointer-function"></a>glTexCoordPointer fonction)

La fonction **glTexCoordPointer** définit un tableau de coordonnées de texture.

## <a name="syntax"></a>Syntaxe


```C++
void WINAPI glTexCoordPointer(
         GLint   size,
         GLenum  type,
         GLsizei stride,
   const GLvoid  *pointer
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*size* 
</dt> <dd>

Nombre de coordonnées par élément de tableau. La valeur de *Size* doit être 1, 2, 3 ou 4.

</dd> <dt>

*type* 
</dt> <dd>

Type de données de chaque coordonnée de texture dans le tableau à l’aide des constantes symboliques suivantes : **GL \_ short**, **GL \_ int**, **GL \_ float** et **GL \_ double**.

</dd> <dt>

*progrès* 
</dt> <dd>

Offset d’octet entre les éléments de tableau consécutifs. Quand *Stride* est égal à zéro, les éléments de tableau sont étroitement empaquetés dans le tableau.

</dd> <dt>

*pointeur* 
</dt> <dd>

Pointeur vers la première coordonnée du premier élément dans le tableau.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Cette fonction ne retourne pas de valeur.

## <a name="error-codes"></a>Codes d’erreur

Les codes d’erreur suivants peuvent être récupérés par la fonction [**glGetError**](glgeterror.md) .



| Nom                                                                                              | Signification                                      |
|---------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>**\_enum GL non valide \_**</dt> </dl>  | le *type* n’est pas une valeur acceptée.<br/> |
| <dl> <dt>**\_valeur non valide du GL \_**</dt> </dl> | la *taille* n’est pas 1, 2, 3 ou 4.<br/>     |
| <dl> <dt>**\_valeur non valide du GL \_**</dt> </dl> | *Stride* était négatif.<br/>            |



## <a name="remarks"></a>Remarques

La fonction **glTexCoordPointer** spécifie l’emplacement et les données d’un tableau de coordonnées de texture à utiliser lors du rendu. Le paramètre *Size* spécifie le nombre de coordonnées utilisées pour chaque élément du tableau. Le paramètre de *type* spécifie le type de données de chaque coordonnée de texture. Le paramètre *Stride* détermine le décalage d’octets d’un élément de tableau à l’autre, ce qui permet d’empaqueter des vertex et des attributs dans un tableau unique ou un stockage dans des tableaux séparés. Dans certaines implémentations, le stockage des vertex et des attributs dans un tableau unique peut être plus efficace que l’utilisation de tableaux séparés. Pour plus d’informations, consultez [**glInterleavedArrays**](glinterleavedarrays.md). Lorsqu’un tableau de coordonnées de texture est spécifié, la taille, le type, la Stride et le pointeur sont enregistrés à l’État côté client.

Un tableau de coordonnées de texture est activé quand vous spécifiez la constante de **\_ \_ \_ tableau** de coordonnées de la texture GL avec [**glEnableClientState**](glenableclientstate.md). Quand cette option est activée, [**glDrawArrays**](gldrawarrays.md), [**glDrawElements**](gldrawelements.md)et [**glArrayElement**](glarrayelement.md) utilisent le tableau de coordonnées de texture. Par défaut, le tableau de coordonnées de texture est désactivé.

Vous ne pouvez pas inclure des **glTexCoordPointer** dans des listes d’affichage.

Lorsque vous spécifiez un tableau de coordonnées de texture à l’aide de **glTexCoordPointer**, les valeurs de tous les paramètres de tableau de coordonnées de texture de la fonction sont enregistrées dans un État côté client et les éléments de tableau statique peuvent être mis en cache. Étant donné que les paramètres de tableau de coordonnées de texture sont des États côté client, leurs valeurs ne sont pas enregistrées ou restaurées par [**glPushAttrib**](glpushattrib.md) et [**glPopAttrib**](glpopattrib.md).

Bien qu’aucune erreur ne soit générée lorsque vous appelez **glTexCoordPointer** dans des paires [**glBegin**](glbegin.md) et [**glEnd**](glend.md) , les résultats ne sont pas définis.

Les fonctions suivantes récupèrent les informations relatives à **glTexCoordPointer**:

[**glIsEnabled**](glisenabled.md) avec argument **GL \_ texture \_ Coord \_ tableau**

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) avec argument **taille de la texture du GL \_ \_ \_ \_ taille du tableau**

**glGet** avec argument **GL \_ texture \_ Coord \_ tableau \_ Stride**

**glGet** avec argument **\_ \_ \_ \_ nombre** de coordonnées de la texture du GL

**glGet** avec argument de la **\_ texture GL \_ \_ \_ type de tableau** de coordonnées

[**glGetPointerv**](glgetpointerv.md) avec argument de la **texture du GL \_ pointeur de \_ \_ tableau \_ de repère**

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

[**glColorPointer**](glcolorpointer.md)
</dt> <dt>

[**glDrawArrays**](gldrawarrays.md)
</dt> <dt>

[**glDrawElements**](gldrawelements.md)
</dt> <dt>

[**glEdgeFlagPointer**](gledgeflagpointer.md)
</dt> <dt>

[**glEnable**](glenable.md)
</dt> <dt>

[**glGetPointerv**](glgetpointerv.md)
</dt> <dt>

[**glGetString**](glgetstring.md)
</dt> <dt>

[**glIndexPointer**](glindexpointer.md)
</dt> <dt>

[**glIsEnabled**](glisenabled.md)
</dt> <dt>

[**glNormalPointer**](glnormalpointer.md)
</dt> <dt>

[**glPopClientAttrib**](glpopclientattrib.md)
</dt> <dt>

[**glPushClientAttrib**](glpushclientattrib.md)
</dt> <dt>

[**glTexCoord**](gltexcoord-functions.md)
</dt> <dt>

[**glVertexPointer**](glvertexpointer.md)
</dt> </dl>

 

 





