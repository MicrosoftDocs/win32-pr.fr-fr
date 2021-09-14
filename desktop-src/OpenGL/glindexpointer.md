---
title: fonction glIndexPointer (GL. h)
description: La fonction glIndexPointer définit un tableau d’index de couleurs.
ms.assetid: b435d950-1f87-4041-93e4-f1f8786cabdb
keywords:
- glIndexPointer fonction OpenGL
topic_type:
- apiref
api_name:
- glIndexPointer
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cca6858d7d1e3f13e4155bd40307a53b22e80a56
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127229409"
---
# <a name="glindexpointer-function"></a>glIndexPointer fonction)

La fonction **glIndexPointer** définit un tableau d’index de couleurs.

## <a name="syntax"></a>Syntaxe


```C++
void WINAPI glIndexPointer(
         GLenum  type,
         GLsizei stride,
   const GLvoid  *pointer
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*type* 
</dt> <dd>

Type de données de chaque index de couleur dans le tableau à l’aide des constantes symboliques suivantes : GL \_ short, GL \_ int, GL \_ float, GL \_ double.

</dd> <dt>

*progrès* 
</dt> <dd>

Décalage d’octet entre les index de couleurs consécutifs. Lorsque la valeur de *Stride* est égale à zéro, les index de couleur sont fortement compressés dans le tableau.

</dd> <dt>

*pointeur* 
</dt> <dd>

Pointeur vers le premier index de couleur dans le tableau.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Cette fonction ne retourne pas de valeur.

## <a name="error-codes"></a>Codes d’erreur

Les codes d’erreur suivants peuvent être récupérés par la fonction [**glGetError**](glgeterror.md) .



| Nom                                                                                              | Signification                                      |
|---------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>**\_enum GL non valide \_**</dt> </dl>  | le *type* n’est pas une valeur acceptée.<br/> |
| <dl> <dt>**\_valeur non valide du GL \_**</dt> </dl> | *Stride* ou *Count* était négatif.<br/> |



## <a name="remarks"></a>Notes

La fonction **glIndexPointer** spécifie l’emplacement et les données d’un tableau d’index de couleurs à utiliser lors du rendu. Le paramètre de *type* spécifie le type de données de chaque index de couleur et *Stride* détermine le décalage d’octets d’un index de couleur à l’autre, ce qui permet de compresser les vertex et les attributs dans un tableau unique ou de stocker dans des tableaux séparés. Dans certaines implémentations, le stockage des vertex et des attributs dans un tableau unique peut être plus efficace que l’utilisation de tableaux séparés. Pour plus d’informations, consultez [**glInterleavedArrays**](glinterleavedarrays.md).

Un tableau d’index de couleurs est activé lorsque vous spécifiez \_ la \_ constante de tableau d’index GL avec [**glEnableClientState**](glenableclientstate.md). Quand cette option est activée, [**glDrawArrays**](gldrawarrays.md) et [**glArrayElement**](glarrayelement.md) utilisent le tableau d’index de couleurs. Par défaut, le tableau d’index de couleurs est désactivé.

Vous ne pouvez pas inclure des **glIndexPointer** dans des listes d’affichage.

Lorsque vous spécifiez un tableau d’index de couleurs à l’aide de **glIndexPointer**, les valeurs de tous les paramètres du tableau d’index de couleurs de la fonction sont enregistrées dans un État côté client et les éléments de tableau statique peuvent être mis en cache. Étant donné que les paramètres de tableau d’index de couleurs sont un État côté client, leurs valeurs ne sont pas enregistrées ou restaurées par [**glPushAttrib**](glpushattrib.md) et **glPopAttrib**.

Bien qu’aucune erreur ne soit générée lorsque vous appelez **glIndexPointer** dans des paires [**glBegin**](glbegin.md) et **glEnd** , les résultats ne sont pas définis.

Les fonctions suivantes récupèrent les informations relatives à **glIndexPointer**:

[**glIsEnabled**](glisenabled.md) avec argument \_ table d’index GL \_

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) avec argument GL \_ index \_ tableau \_ Stride

**glGet** avec argument \_ nombre de \_ tableaux d’index GL \_

**glGet** avec argument \_ \_ type tableau d’index GL \_

**glGet** avec argument \_ taille du \_ tableau d’index GL \_

[**glGetPointerv**](glgetpointerv.md) avec argument, \_ \_ pointeur de tableau d’index GL \_

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

[**glColorPointer**](glcolorpointer.md)
</dt> <dt>

[**glDrawArrays**](gldrawarrays.md)
</dt> <dt>

[**glEdgeFlagPointer**](gledgeflagpointer.md)
</dt> <dt>

[**glGetPointerv**](glgetpointerv.md)
</dt> <dt>

[**glGetString**](glgetstring.md)
</dt> <dt>

[**glNormalPointer**](glnormalpointer.md)
</dt> <dt>

[**glPushAttrib**](glpushattrib.md)
</dt> <dt>

[**glTexCoordPointer**](gltexcoordpointer.md)
</dt> <dt>

[**glVertexPointer**](glvertexpointer.md)
</dt> </dl>

 

 





