---
title: gluOrtho2D, fonction (Glu. h)
description: La fonction gluOrtho2D définit une matrice de projection orthographique 2D.
ms.assetid: ba83fb5c-e5c7-4486-a815-a1aff0469757
keywords:
- gluOrtho2D fonction OpenGL
topic_type:
- apiref
api_name:
- gluOrtho2D
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a36b321f312a074a5dd78340968f1c9b2b844c6c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104383835"
---
# <a name="gluortho2d-function"></a>gluOrtho2D fonction)

La fonction **gluOrtho2D** définit une matrice de projection orthographique 2D.

## <a name="syntax"></a>Syntaxe


```C++
void WINAPI gluOrtho2D(
   GLdouble left,
   GLdouble right,
   GLdouble top,
   GLdouble bottom
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*gauche* 
</dt> <dd>

Coordonnée du plan de découpage vertical gauche.

</dd> <dt>

*Oui* 
</dt> <dd>

Coordonnée du plan de découpage vertical droit.

</dd> <dt>

*top* 
</dt> <dd>

Coordonnée du plan de découpage horizontal supérieur.

</dd> <dt>

*ballon* 
</dt> <dd>

Coordonnée du plan de découpage horizontal inférieur.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Cette fonction ne retourne pas de valeur.

## <a name="remarks"></a>Notes

La fonction **gluOrtho2D** définit une zone d’affichage orthographique à deux dimensions. Cela équivaut à appeler [**glOrtho**](glortho.md) avec near = 1 et Far = 1.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                           |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                 |
| En-tête<br/>                   | <dl> <dt>Glu. h</dt> </dl>     |
| Bibliothèque<br/>                  | <dl> <dt>Glu32. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Glu32.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**glOrtho**](glortho.md)
</dt> <dt>

[**gluPerspective**](gluperspective.md)
</dt> </dl>

 

 





