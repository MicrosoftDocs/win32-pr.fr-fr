---
title: fonction glColorPointer (GL. h)
description: La fonction glColorPointer définit un tableau de couleurs.
ms.assetid: 4d9d05fb-691d-4b71-b079-c42dc7103055
keywords:
- glColorPointer fonction OpenGL
topic_type:
- apiref
api_name:
- glColorPointer
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9abced52f0d0664e998ad8380e33d43d4af36bcc
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127311834"
---
# <a name="glcolorpointer-function"></a>glColorPointer fonction)

La fonction **glColorPointer** définit un tableau de couleurs.

## <a name="syntax"></a>Syntaxe


```C++
void WINAPI glColorPointer(
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

Nombre de composants par couleur. La valeur doit être 3 ou 4.

</dd> <dt>

*type* 
</dt> <dd>

Type de données de chaque composant de couleur dans un tableau de couleurs. Les types de données acceptables sont spécifiés avec les constantes suivantes : GL \_ Byte, GL \_ unsigned \_ Byte, GL \_ short, GL \_ unsigned \_ short, GL \_ int, GL \_ unsigned \_ int, GL \_ float ou GL \_ double.

</dd> <dt>

*progrès* 
</dt> <dd>

Décalage d’octet entre les couleurs consécutives. Quand *Stride* est égal à zéro, les couleurs sont étroitement compressées dans le tableau.

</dd> <dt>

*pointeur* 
</dt> <dd>

Pointeur vers le premier composant du premier élément de couleur dans un tableau de couleurs.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Cette fonction ne retourne pas de valeur.

## <a name="error-codes"></a>Codes d’erreur

Les codes d’erreur suivants peuvent être récupérés par la fonction [**glGetError**](glgeterror.md) .



| Nom                                                                                              | Signification                                      |
|---------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>**\_valeur non valide du GL \_**</dt> </dl> | la *taille* n’est pas 3 ou 4.<br/>            |
| <dl> <dt>**\_enum GL non valide \_**</dt> </dl>  | le *type* n’est pas une valeur acceptée.<br/> |
| <dl> <dt>**\_valeur non valide du GL \_**</dt> </dl> | *Stride* ou *Count* était négatif.<br/> |



## <a name="remarks"></a>Notes

La fonction **glColorPointer** spécifie l’emplacement et le format de données d’un tableau de composants de couleur à utiliser lors du rendu. Le paramètre *Stride* détermine le décalage d’octets d’une couleur à l’autre, ce qui permet de compresser des attributs vertex dans un tableau unique ou un stockage dans des tableaux séparés. Dans certaines implémentations, le stockage des attributs de vertex dans un tableau unique peut être plus efficace que l’utilisation de tableaux séparés.

Activez le tableau de couleurs en spécifiant \_ la \_ constante de tableau de couleur GL avec [**glEnableClientState**](glenableclientstate.md). L’appel de [**glArrayElement**](glarrayelement.md), [**glDrawElements**](gldrawelements.md)ou [**glDrawArrays**](gldrawarrays.md) utilise le tableau de couleurs qui est donc activé. Par défaut, le tableau de couleurs est désactivé. Les appels **glColorPointer** ne peuvent pas être entrés dans les listes d’affichage.

Lorsque vous spécifiez un tableau de couleurs à l’aide de **glColorPointer**, les valeurs de tous les paramètres du tableau de couleurs de la fonction sont enregistrées dans un État côté client et vous pouvez mettre en cache des éléments de tableau statique. Étant donné que les paramètres du tableau de couleurs sont dans un État côté client, [**glPushAttrib**](glpushattrib.md) et [**glPopAttrib**](glpopattrib.md) n’enregistrent ni ne restaurent les valeurs des paramètres.

Bien que la spécification du tableau de couleurs dans les paires [**glBegin**](glbegin.md) et [**Glend**](glend.md) ne génère pas d’erreur, les résultats ne sont pas définis.

Les fonctions suivantes récupèrent les informations relatives à la fonction **glColorPointer** :

[**glIsEnabled**](glisenabled.md) avec argument de \_ tableau de couleur de GL \_

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) avec argument GL \_ \_ taille de tableau de couleurs \_

**glGet** avec argument GL \_ couleur \_ de \_ type tableau

**glGet** avec argument GL \_ tableau des couleurs \_ \_ Stride

**glGet** avec argument \_ nombre de \_ MATRICEs de couleurs GL \_

[**glGetPointerv**](glgetpointerv.md) avec argument, \_ \_ pointeur de tableau de couleur de GL \_

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

[**glDrawArrays**](gldrawarrays.md)
</dt> <dt>

[**glEdgeFlagPointer**](gledgeflagpointer.md)
</dt> <dt>

[**glEnableClientState**](glenableclientstate.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[**glGetString**](glgetstring.md)
</dt> <dt>

[**glGetPointerv**](glgetpointerv.md)
</dt> <dt>

[**glIndexPointer**](glindexpointer.md)
</dt> <dt>

[**glIsEnabled**](glisenabled.md)
</dt> <dt>

[**glNormalPointer**](glnormalpointer.md)
</dt> <dt>

[**glPopAttrib**](glpopattrib.md)
</dt> <dt>

[**glPushAttrib**](glpushattrib.md)
</dt> <dt>

[**glTexCoordPointer**](gltexcoordpointer.md)
</dt> <dt>

[**glVertexPointer**](glvertexpointer.md)
</dt> </dl>

 

 





