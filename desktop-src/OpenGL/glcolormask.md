---
title: fonction glColorMask (GL. h)
description: La fonction glColorMask active et désactive l’écriture des composants de couleur de mémoire tampon de trame.
ms.assetid: 23d7f94e-f290-423c-a841-f86caf94009d
keywords:
- glColorMask fonction OpenGL
topic_type:
- apiref
api_name:
- glColorMask
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3a9aa36eeceeae4aaa9373d73b50fda09663edb7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127311846"
---
# <a name="glcolormask-function"></a>glColorMask fonction)

La fonction **glColorMask** active et désactive l’écriture des composants de couleur de mémoire tampon de trame.

## <a name="syntax"></a>Syntaxe


```C++
void WINAPI glColorMask(
   GLboolean red,
   GLboolean green,
   GLboolean blue,
   GLboolean alpha
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*rouge* 
</dt> <dd>

Spécifiez si le rouge peut ou ne peut pas être écrit dans le trame. Les valeurs par défaut sont GL \_ true, indiquant que le composant Color peut être écrit.

</dd> <dt>

*écologie* 
</dt> <dd>

Spécifiez si le vert peut ou ne peut pas être écrit dans le trame. La valeur par défaut est GL \_ true, indiquant que le composant Color peut être écrit.

</dd> <dt>

*bleu* 
</dt> <dd>

Spécifiez si le bleu peut ou ne peut pas être écrit dans le trame. La valeur par défaut est GL \_ true, indiquant que le composant Color peut être écrit.

</dd> <dt>

*alpha* 
</dt> <dd>

Spécifiez si alpha peut ou ne peut pas être écrit dans le trame. La valeur par défaut est GL \_ true, indiquant que le composant Color peut être écrit.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Cette fonction ne retourne pas de valeur.

## <a name="error-codes"></a>Codes d’erreur

Le code d’erreur suivant peut être récupéré par la fonction [**glGetError**](glgeterror.md) .



| Nom                                                                                                  | Signification                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_opération non valide du GL \_**</dt> </dl> | La fonction a été appelée entre un appel à [**glBegin**](glbegin.md) et l’appel correspondant à [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Notes

La fonction **glColorMask** spécifie si les composants de couleur individuels du trame peuvent ou ne peuvent pas être écrits. Si le *rouge* est \_ défini sur GL false, par exemple, aucune modification n’est apportée au composant rouge d’un pixel dans une des mémoires tampons de couleur, quelle que soit l’opération de dessin tentée.

Les modifications apportées aux différents bits des composants ne peuvent pas être contrôlées. Au lieu de cela, les modifications sont activées ou désactivées pour l’ensemble des composants de couleur.

Les fonctions suivantes récupèrent les informations relatives à **glColorMask**:

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) avec argument GL \_ couleur \_ WRITEMASK

**glGet** avec argument GL \_ RVBA \_ mode

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

[**glBegin**](glbegin.md)
</dt> <dt>

[**glColor**](glcolor-functions.md)
</dt> <dt>

[**glDepthMask**](gldepthmask.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[**glIndex**](glindex-functions.md)
</dt> <dt>

[**glIndexMask**](glindexmask.md)
</dt> <dt>

[**glStencilMask**](glstencilmask.md)
</dt> </dl>

 

 





