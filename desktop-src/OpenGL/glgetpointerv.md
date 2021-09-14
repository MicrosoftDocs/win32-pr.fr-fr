---
title: fonction glGetPointerv (GL. h)
description: La fonction glGetPointerv retourne l’adresse d’un tableau de données de vertex.
ms.assetid: 6f85c508-9335-4474-8cc5-e67c7421a8e4
keywords:
- glGetPointerv fonction OpenGL
topic_type:
- apiref
api_name:
- glGetPointerv
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 569861922514af88835fbb4e313dab3286b7c47d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127229476"
---
# <a name="glgetpointerv-function"></a>glGetPointerv fonction)

La fonction **glGetPointerv** retourne l’adresse d’un tableau de données de vertex.

## <a name="syntax"></a>Syntaxe


```C++
void WINAPI glGetPointerv(
   GLenum pname,
   GLvoid **params
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pname* 
</dt> <dd>

Type de pointeur de tableau à retourner à partir des constantes symboliques suivantes : pointeur de tableau de couleur de GL, pointeur de tableau d' \_ indicateurs de périphérie du GL, pointeur de \_ tampon de \_ \_ \_ \_ \_ \_ Commentaires GL \_ \_ , pointeur de tableau d' \_ index GL \_ \_ , pointeur de tableau de GL normal, pointeur de tableau de coordonnées de la comptabilité GL, pointeur de \_ \_ tampon de \_ \_ \_ \_ \_ \_ sélection GL \_ \_ et \_ pointeur de tableau de vertex GL \_ \_ .

</dd> <dt>

*params* 
</dt> <dd>

Retourne la valeur du pointeur de tableau spécifié par *pname*.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Cette fonction ne retourne pas de valeur.

## <a name="error-codes"></a>Codes d’erreur

Le code d’erreur suivant peut être récupéré par la fonction [**glGetError**](glgeterror.md) .



| Nom                                                                                             | Signification                                       |
|--------------------------------------------------------------------------------------------------|-----------------------------------------------|
| <dl> <dt>**\_enum GL non valide \_**</dt> </dl> | *pname* n’est pas une valeur acceptée.<br/> |



## <a name="remarks"></a>Notes

La fonction **glGetPointerv** retourne les informations de pointeur de tableau. Le paramètre *pname* est une constante symbolique spécifiant le type de pointeur de tableau à retourner, et *params* est un pointeur vers un emplacement où placer les données retournées.

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

 

 





