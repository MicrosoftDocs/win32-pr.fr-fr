---
title: fonction glDepthRange (GL. h)
description: La fonction glDepthRange spécifie le mappage des valeurs z des coordonnées de périphérique normalisées aux coordonnées de la fenêtre.
ms.assetid: 44aed5e5-4bd2-4e7f-ad05-1cf4be5254a5
keywords:
- glDepthRange fonction OpenGL
topic_type:
- apiref
api_name:
- glDepthRange
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d0bd6a22ae91877c9b20fa5387edd9438942a07d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127311785"
---
# <a name="gldepthrange-function"></a>glDepthRange fonction)

La fonction **glDepthRange** spécifie le mappage des valeurs *z* des coordonnées de périphérique normalisées aux coordonnées de la fenêtre.

## <a name="syntax"></a>Syntaxe


```C++
void WINAPI glDepthRange(
   GLclampd zNear,
   GLclampd zFar
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*zNear* 
</dt> <dd>

Mappage du plan de découpage near aux coordonnées de la fenêtre. La valeur par défaut est zéro.

</dd> <dt>

*zFar* 
</dt> <dd>

Mappage du plan de découpage Far aux coordonnées de la fenêtre. La valeur par défaut est 1.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Cette fonction ne retourne pas de valeur.

## <a name="error-codes"></a>Codes d’erreur

Le code d’erreur suivant peut être récupéré par la fonction [**glGetError**](glgeterror.md) .



| Nom                                                                                                  | Signification                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_opération non valide du GL \_**</dt> </dl> | La fonction a été appelée entre un appel à [**glBegin**](glbegin.md) et l’appel correspondant à [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Notes

Après découpage et division par *w*, les coordonnées *z* sont comprises entre 0,0 et 1,0, ce qui correspond aux plans de découpage near et Far. La fonction **glDepthRange** spécifie un mappage linéaire des coordonnées *z* normalisées dans cette plage aux coordonnées *z* de la fenêtre. Quelle que soit l’implémentation réelle du tampon de profondeur, les valeurs de profondeur de la coordonnée de la fenêtre sont traitées comme si elles sont comprises entre 0,0 et 1,0 (comme les composants de couleur). Ainsi, les valeurs acceptées par **glDepthRange** sont conjointes à cette plage avant d’être acceptées.

Le mappage par défaut (0, 1) mappe le plan near à 0 et le plan Far à 1. Avec ce mappage, la plage de mémoire tampon de profondeur est entièrement utilisée.

Il n’est pas nécessaire que *zNear* soit inférieur à *zFar*. Les mappages inverses tels que (1,0) sont acceptables.

La fonction suivante récupère des informations relatives à **glDepthRange**:

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) avec la \_ plage de profondeur de l’argument GL \_

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

[**glDepthFunc**](gldepthfunc.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[**glViewport**](glviewport.md)
</dt> </dl>

 

 





