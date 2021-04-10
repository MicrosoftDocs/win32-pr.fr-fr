---
title: fonction glNormalPointer (GL. h)
description: La fonction glNormalPointer définit un tableau de normales.
ms.assetid: 6ffb0522-87cc-4be1-a5b1-f6fd30e04b43
keywords:
- glNormalPointer fonction OpenGL
topic_type:
- apiref
api_name:
- glNormalPointer
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2c2f3abbfbd989351af647557ec64f8ee3172dc5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942867"
---
# <a name="glnormalpointer-function"></a>glNormalPointer fonction)

La fonction **glNormalPointer** définit un tableau de normales.

## <a name="syntax"></a>Syntaxe


```C++
void WINAPI glNormalPointer(
         GLenum  type,
         GLsizei stride,
   const GLvoid  *pointer
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*type* 
</dt> <dd>

Type de données de chaque coordonnée dans le tableau à l’aide des constantes symboliques suivantes : GL \_ Byte, GL \_ short, GL \_ int, GL \_ float et GL \_ double.

</dd> <dt>

*progrès* 
</dt> <dd>

Décalage d’octet entre les normales consécutives. Lorsque la valeur de *Stride* est égale à zéro, les normales sont étroitement compressées dans le tableau.

</dd> <dt>

*pointeur* 
</dt> <dd>

Pointeur vers la première normale dans le tableau.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Cette fonction ne retourne pas de valeur.

## <a name="error-codes"></a>Codes d’erreur

Les codes d’erreur suivants peuvent être récupérés par la fonction [**glGetError**](glgeterror.md) .



| Nom                                                                                                  | Signification                                      |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>**\_enum GL non valide \_**</dt> </dl>      | le *type* n’est pas une valeur acceptée.<br/> |
| <dl> <dt>**\_opération non valide du GL \_**</dt> </dl> | *Stride* ou *Count* était négatif.<br/> |



## <a name="remarks"></a>Notes

La fonction **glNormalPointer** spécifie l’emplacement et les données d’un tableau de normales à utiliser lors du rendu. Le paramètre de *type* spécifie le type de données de chaque coordonnée normale. Le paramètre *Stride* détermine le décalage d’octets d’un perpendiculaire à l’autre, ce qui permet d’empaqueter des vertex et des attributs dans un tableau unique ou un stockage dans des tableaux séparés. Dans certaines implémentations, le stockage des vertex et des attributs dans un tableau unique peut être plus efficace que l’utilisation de tableaux séparés. Pour plus d’informations, consultez [**glInterleavedArrays**](glinterleavedarrays.md) .

Un tableau normal est activé lorsque vous spécifiez la \_ \_ constante de tableau de la table normale GL avec [**glEnableClientState**](glenableclientstate.md). Quand cette option est activée, [**glDrawArrays**](gldrawarrays.md), [**glDrawElements**](gldrawelements.md) et [**glArrayElement**](glarrayelement.md) utilisent le tableau normal. Par défaut, le tableau normal est désactivé.

Vous ne pouvez pas inclure des **glNormalPointer** dans des listes d’affichage.

Lorsque vous spécifiez un tableau normal à l’aide de **glNormalPointer**, les valeurs de tous les paramètres de tableau normaux de la fonction sont enregistrées dans un État côté client. Étant donné que les paramètres de tableau normaux sont enregistrés dans un État côté client, leurs valeurs ne sont pas enregistrées ou restaurées par [**glPushAttrib**](glpushattrib.md) et [**glPopAttrib**](glpopattrib.md).

Bien qu’aucune erreur ne soit générée lorsque vous appelez **glNormalPointer** dans des paires [**glBegin**](glbegin.md) et [**glEnd**](glend.md) , les résultats ne sont pas définis.

Les fonctions suivantes sont associées à **glNormalPointer**:

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) avec argument GL \_ normal \_ tableau \_ Stride

**glGet** avec argument GL- \_ nombre normal de \_ tableaux \_

**glGet** avec argument GL \_ - \_ type tableau normal \_

**glGetPointerv** avec argument GL \_ - \_ pointeur de tableau normal \_

[**glIsEnabled**](glisenabled.md) avec argument GL \_ - \_ tableau normal

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

[**glDrawElements**](gldrawelements.md)
</dt> <dt>

[**glDrawArrays**](gldrawarrays.md)
</dt> <dt>

[**glEnable**](glenable.md)
</dt> <dt>

[**glEdgeFlagPointer**](gledgeflagpointer.md)
</dt> <dt>

[**glGetPointerv**](glgetpointerv.md)
</dt> <dt>

[**glIndexPointer**](glindexpointer.md)
</dt> <dt>

[**glIsEnabled**](glisenabled.md)
</dt> <dt>

[**glInterleavedArrays**](glinterleavedarrays.md)
</dt> <dt>

[**glTexCoordPointer**](gltexcoordpointer.md)
</dt> <dt>

[**glVertexPointer**](glvertexpointer.md)
</dt> <dt>

[**glGetString**](glgetstring.md)
</dt> </dl>

 

 





