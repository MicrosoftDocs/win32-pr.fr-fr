---
title: fonction glColor4b (GL. h)
description: Définit la couleur actuelle. | fonction glColor4b (GL. h)
ms.assetid: 50d829f2-f336-40be-8598-a255c86f0722
keywords:
- glColor4b fonction OpenGL
topic_type:
- apiref
api_name:
- glColor4b
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bd16d3bb752b5e640e86636929de9d8706ab49a9
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127096649"
---
# <a name="glcolor4b-function"></a>glColor4b fonction)

Définit la couleur actuelle.

## <a name="syntax"></a>Syntaxe


```C++
void WINAPI glColor4b(
   GLbyte red,
   GLbyte green,
   GLbyte blue,
   GLbyte alpha
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*rouge* 
</dt> <dd>

Nouvelle valeur rouge pour la couleur actuelle.

</dd> <dt>

*écologie* 
</dt> <dd>

Nouvelle valeur verte pour la couleur actuelle.

</dd> <dt>

*bleu* 
</dt> <dd>

Nouvelle valeur bleue pour la couleur actuelle.

</dd> <dt>

*alpha* 
</dt> <dd>

Nouvelle valeur alpha pour la couleur actuelle.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Cette fonction ne retourne pas de valeur.

## <a name="remarks"></a>Notes

Le GL stocke à la fois un index de couleurs à valeur unique actuel et une couleur RVBA à quatre valeurs actuelle. **glcolor** définit une nouvelle couleur RVBA à quatre valeurs. **glcolor** a deux variantes majeures : **glcolor3** et **glcolor4**. les variantes **glcolor3** spécifient les nouvelles valeurs de rouge, de vert et de bleu explicitement et définissent la valeur alpha actuelle sur 1,0 (intensité complète) de manière implicite. les variantes **glcolor4** spécifient les quatre composants de couleur de manière explicite.

**glcolor3b**, **glcolor4b**, **glcolor3s**, **glcolor4s**, **glcolor3i** et **glcolor4i** prennent trois ou quatre entiers signés Byte, short ou long comme arguments. Quand v est ajouté au nom, les commandes de couleur peuvent prendre un pointeur vers un tableau de telles valeurs.

Les valeurs de couleur actuelles sont stockées dans un format à virgule flottante, avec la mantisse et les tailles d’exposant non spécifiées. Les composants de couleur d’entier non signé, lorsqu’ils sont spécifiés, sont mappés de manière linéaire aux valeurs à virgule flottante, de sorte que la plus grande valeur représentable correspond à 1,0 (intensité complète) et 0 correspond à 0,0 (intensité nulle). Les composants de couleur d’entier signé, lorsqu’ils sont spécifiés, sont mappés de manière linéaire aux valeurs à virgule flottante, de sorte que la valeur représentable la plus positive correspond à 1,0, et la valeur représentable la plus négative correspond à-1,0. (Notez que ce mappage ne convertit pas 0 de manière précise en 0,0.) Les valeurs à virgule flottante sont mappées directement.

Ni les valeurs d’entier à virgule flottante ni les valeurs entières signées ne sont ancrées à la plage \[ 0, 1 \] avant la mise à jour de la couleur actuelle. Toutefois, les composants de couleur sont bloqués dans cette plage avant d’être interpolés ou écrits dans une mémoire tampon de couleur.

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

[**glEnd**](glend.md)
</dt> <dt>

[**glGetBooleanv, glGetDoublev, glGetFloatv, glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[**glIndex**](glindexd.md)
</dt> </dl>

 

 





