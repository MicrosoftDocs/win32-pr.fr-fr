---
title: fonction glStencilMask (GL. h)
description: La fonction glStencilMask contrôle l’écriture de bits individuels dans les plans de gabarit.
ms.assetid: c586f9db-bad5-4f06-a194-a8d979842d0c
keywords:
- glStencilMask fonction OpenGL
topic_type:
- apiref
api_name:
- glStencilMask
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9eb2e0af89bf2c66e7fa73cf6e4ace8bc8272e8ea581e17bab17754164d3f068
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120036519"
---
# <a name="glstencilmask-function"></a>glStencilMask fonction)

La fonction **glStencilMask** contrôle l’écriture de bits individuels dans les plans de gabarit.

## <a name="syntax"></a>Syntaxe


```C++
void WINAPI glStencilMask(
   GLuint mask
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*mask* 
</dt> <dd>

Masque de bits permettant d’activer et de désactiver l’écriture de bits individuels dans les plans de gabarit. Initialement, le masque est tous les éléments.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Cette fonction ne retourne pas de valeur.

## <a name="error-codes"></a>Codes d’erreur

Le code d’erreur suivant peut être récupéré par la fonction [**glGetError**](glgeterror.md) .



| Nom                                                                                                  | Signification                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_opération non valide du GL \_**</dt> </dl> | La fonction a été appelée entre un appel à [**glBegin**](glbegin.md) et l’appel correspondant à [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Remarques

La fonction **glStencilMask** contrôle l’écriture de bits individuels dans les plans de gabarit. Les *n* bits les moins significatifs du *masque*, où *n* est le nombre de bits dans la mémoire tampon du stencil, spécifient un masque. Chaque fois qu’un seul apparaît dans le masque, le bit correspondant dans la mémoire tampon du stencil est rendu accessible en écriture. Lorsqu’un zéro s’affiche, le bit est protégé en écriture. Initialement, tous les bits sont activés pour l’écriture.

Les fonctions suivantes récupèrent les informations relatives à **glStencilMask**:

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) avec argument \_ WRITEMASK de gabarit \_

glGet avec arguments de stencil de la comptabilité GL \_ \_

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

[**glColorMask**](glcolormask.md)
</dt> <dt>

[**glDepthMask**](gldepthmask.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glIndexMask**](glindexmask.md)
</dt> <dt>

[**glStencilFunc**](glstencilfunc.md)
</dt> <dt>

[**glStencilOp**](glstencilop.md)
</dt> </dl>

 

 





