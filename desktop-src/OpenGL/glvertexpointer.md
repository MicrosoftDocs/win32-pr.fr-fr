---
title: fonction glVertexPointer (GL. h)
description: La fonction glVertexPointer définit un tableau de données de vertex.
ms.assetid: e5f97fdc-9448-4389-8533-3855a3213feb
keywords:
- glVertexPointer fonction OpenGL
topic_type:
- apiref
api_name:
- glVertexPointer
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 422dd1a7938cc5adb183ff7e17c59a8f52eb4909
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466315"
---
# <a name="glvertexpointer-function"></a>glVertexPointer fonction)

La fonction **glVertexPointer** définit un tableau de données de vertex.

## <a name="syntax"></a>Syntaxe


```C++
void WINAPI glVertexPointer(
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

Nombre de coordonnées par vertex. La valeur de *Size* doit être 2, 3 ou 4.

</dd> <dt>

*type* 
</dt> <dd>

Type de données de chaque coordonnée dans le tableau à l’aide des constantes symboliques suivantes : GL \_ short, GL \_ int, GL \_ float et GL \_ double.

</dd> <dt>

*progrès* 
</dt> <dd>

Décalage d’octet entre les vertex consécutifs. Lorsque la valeur de *Stride* est égale à zéro, les vertex sont étroitement empaquetés dans le tableau.

</dd> <dt>

*pointeur* 
</dt> <dd>

Pointeur vers la première coordonnée du premier vertex dans le tableau.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Cette fonction ne retourne pas de valeur.

## <a name="error-codes"></a>Codes d’erreur

Les codes d’erreur suivants peuvent être récupérés par la fonction [**glGetError**](glgeterror.md) .



| Nom                                                                                              | Signification                                       |
|---------------------------------------------------------------------------------------------------|-----------------------------------------------|
| <dl> <dt>**\_valeur non valide du GL \_**</dt> </dl> | la *taille* n’est pas 2, 3 ou 4. <br/>        |
| <dl> <dt>**\_enum GL non valide \_**</dt> </dl>  | le *type* n’est pas une valeur acceptée.<br/>  |
| <dl> <dt>**\_valeur non valide du GL \_**</dt> </dl> | *Stride* ou *Count* était négatif. <br/> |



## <a name="remarks"></a>Notes

La fonction **glVertexPointer** spécifie l’emplacement et les données d’un tableau de coordonnées de vertex à utiliser lors du rendu. Le paramètre *Size* spécifie le nombre de coordonnées par vertex. Le paramètre de *type* spécifie le type de données de chaque coordonnée de vertex. Le paramètre *Stride* détermine le décalage d’octets d’un vertex à l’autre, ce qui permet d’empaqueter des vertex et des attributs dans un tableau unique ou un stockage dans des tableaux séparés. Dans certaines implémentations, le stockage des vertex et des attributs dans un tableau unique peut être plus efficace que l’utilisation de tableaux distincts (consultez [**glInterleavedArrays**](glinterleavedarrays.md)).

Un tableau de vertex est activé quand vous spécifiez \_ la \_ constante de tableau de vertex GL avec [**glEnableClientState**](glenableclientstate.md). Quand cette option est activée, [**glDrawArrays**](gldrawarrays.md), [**glDrawElements**](gldrawelements.md)et [**glArrayElement**](glarrayelement.md) utilisent le tableau de vertex. Par défaut, le tableau de vertex est désactivé.

Vous ne pouvez pas inclure des **glVertexPointer** dans des listes d’affichage.

Lorsque vous spécifiez un tableau de vertex à l’aide de **glVertexPointer**, les valeurs de tous les paramètres de tableau de vertex de la fonction sont enregistrées dans un État côté client et les éléments de tableau statique peuvent être mis en cache. Étant donné que les paramètres du tableau de vertex sont l’État côté client, leurs valeurs ne sont pas enregistrées ou restaurées par [**glPushAttrib**](glpushattrib.md) et **glPopAttrib**.

Bien qu’aucune erreur ne soit générée si vous appelez **glVertexPointer** dans des paires [**glBegin**](glbegin.md) et [**glEnd**](glend.md) , les résultats ne sont pas définis.

Les fonctions suivantes récupèrent les informations relatives à **glVertexPointer**:

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) avec argument GL \_ vertex de \_ tableau \_ taille

**glGet** avec argument GL \_ vertex de \_ tableau \_ Stride

**glGet** avec argument \_ nombre de \_ tableaux de vertex GL \_

**glGet** avec argument \_ type de \_ tableau de vertex GL \_

[**glGetPointerv**](glgetpointerv.md) avec un \_ pointeur de \_ tableau de vertex d’argument GL \_

[**glIsEnabled**](glisenabled.md) avec argument GL \_ vertex \_ Array

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

[**glEdgeFlagPointer**](gledgeflagpointer.md)
</dt> <dt>

[**glEnableClientState**](glenableclientstate.md)
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

[**glTexCoordPointer**](gltexcoordpointer.md)
</dt> </dl>

 

 





