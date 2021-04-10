---
title: fonction glCallLists (GL. h)
description: La fonction glCallLists exécute une liste de listes d’affichage.
ms.assetid: 7c0a00df-91ee-44ad-9e02-97c1b078e87f
keywords:
- glCallLists fonction OpenGL
topic_type:
- apiref
api_name:
- glCallLists
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a119f3a63b0f04140a72cc5ca818833ae9ea8b20
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942266"
---
# <a name="glcalllists-function"></a>glCallLists fonction)

La fonction **glCallLists** exécute une liste de listes d’affichage.

## <a name="syntax"></a>Syntaxe


```C++
void WINAPI glCallLists(
         GLsizei n,
         GLenum  type,
   const GLvoid  *lists
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*n* 
</dt> <dd>

Nombre de listes d’affichage à exécuter.

</dd> <dt>

*type* 
</dt> <dd>

Type des valeurs dans les *listes*. Les constantes symboliques suivantes sont acceptées.



| Valeur                                                                                                                                                                      | Signification                                                                                                                                                                                                                                                                                                                                                                                            |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_BYTE"></span><span id="gl_byte"></span><dl> <dt>**\_octet GL**</dt> </dl>                                | Le paramètre *Lists* est traité comme un tableau d’octets signés, chacun compris entre-128 et 127.<br/>                                                                                                                                                                                                                                                                                       |
| <span id="GL_UNSIGNED_BYTE"></span><span id="gl_unsigned_byte"></span><dl> <dt>**\_octet non signé GL \_**</dt> </dl>    | Le paramètre *Lists* est traité comme un tableau d’octets non signés, chacun compris entre 0 et 255.<br/>                                                                                                                                                                                                                                                                                        |
| <span id="GL_SHORT"></span><span id="gl_short"></span><dl> <dt>**\_abrégé GL**</dt> </dl>                             | Le paramètre *Lists* est traité comme un tableau d’entiers de 2 octets signés, chacun dans la plage comprise entre-32768 et 32767.<br/>                                                                                                                                                                                                                                                                         |
| <span id="GL_UNSIGNED_SHORT"></span><span id="gl_unsigned_short"></span><dl> <dt>**NON signé dans le GL \_ \_**</dt> </dl> | Le paramètre *Lists* est traité comme un tableau d’entiers de 2 octets non signés, chacun compris entre 0 et 65535.<br/>                                                                                                                                                                                                                                                                            |
| <span id="GL_INT"></span><span id="gl_int"></span><dl> <dt>**GL \_ int**</dt> </dl>                                   | Le paramètre *Lists* est traité comme un tableau d’entiers signés sur 4 octets.<br/>                                                                                                                                                                                                                                                                                                                 |
| <span id="GL_UNSIGNED_INT"></span><span id="gl_unsigned_int"></span><dl> <dt>**\_entier non signé GL \_**</dt> </dl>       | Le paramètre *Lists* est traité comme un tableau d’entiers non signés sur 4 octets.<br/>                                                                                                                                                                                                                                                                                                               |
| <span id="GL_FLOAT"></span><span id="gl_float"></span><dl> <dt>**valeur \_ float du GL**</dt> </dl>                             | Le paramètre *Lists* est traité comme un tableau de valeurs à virgule flottante de 4 octets.<br/>                                                                                                                                                                                                                                                                                                          |
| <span id="GL_2_BYTES"></span><span id="gl_2_bytes"></span><dl> <dt>**GL \_ 2 \_ octets**</dt> </dl>                      | Le paramètre *Lists* est traité comme un tableau d’octets non signés. Chaque paire d’octets spécifie un nom de liste d’affichage unique. La valeur de la paire est calculée comme 256 fois la valeur non signée du premier octet plus la valeur non signée du deuxième octet.<br/>                                                                                                                                |
| <span id="GL_3_BYTES"></span><span id="gl_3_bytes"></span><dl> <dt>**GL \_ 3 \_ octets**</dt> </dl>                      | Le paramètre *Lists* est traité comme un tableau d’octets non signés. Chaque triplet d’octets spécifie un nom de liste d’affichage unique. La valeur de l’triplet est calculée comme 65536 fois la valeur non signée du premier octet, plus 256 fois la valeur non signée du deuxième octet, plus la valeur non signée du troisième octet.<br/>                                                                  |
| <span id="GL_4_BYTES"></span><span id="gl_4_bytes"></span><dl> <dt>**GL \_ 4 \_ octets**</dt> </dl>                      | Le paramètre *Lists* est traité comme un tableau d’octets non signés. Chaque quadruplet d’octets spécifie un nom de liste d’affichage unique. La valeur de l’quadruplet est calculée comme 16777216 fois la valeur non signée du premier octet, plus 65536 fois la valeur non signée du deuxième octet, plus 256 fois la valeur non signée du troisième octet, plus la valeur non signée du quatrième octet, et la valeur non signée.<br/> |



 

</dd> <dt>

*suivant* 
</dt> <dd>

Adresse d’un tableau d’offsets de nom dans la liste d’affichage. Le type de pointeur est void, car les offsets peuvent être bytes, Short, ints ou Floats, en fonction de la valeur de *type*.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Cette fonction ne retourne pas de valeur.

## <a name="remarks"></a>Notes

La fonction **glCallLists** provoque l’exécution de chaque liste d’affichage dans la liste des noms passés comme *listes* . Par conséquent, les fonctions enregistrées dans chaque liste d’affichage sont exécutées dans l’ordre, exactement comme si elles étaient appelées sans utiliser de liste d’affichage. Les noms des listes d’affichage qui n’ont pas été définies sont ignorés.

La fonction **glCallLists** fournit un moyen efficace d’exécuter des listes d’affichage. Le paramètre *n* spécifie le nombre de listes avec divers formats de noms (spécifiés par le paramètre de *type* ) **glCallLists** exécute.

La liste des noms de liste d’affichage ne se termine pas par un caractère null. Au lieu de cela, *n* spécifie le nombre de noms à prendre dans les *listes*.

La fonction [**glListBase**](gllistbase.md) rend un niveau d’indirection supplémentaire disponible. La fonction **glListBase** spécifie un décalage non signé qui est ajouté à chaque nom de liste d’affichage spécifié dans les *listes* avant l’exécution de cette liste d’affichage.

La fonction **glCallLists** peut apparaître à l’intérieur d’une liste d’affichage. Pour éviter la possibilité d’une récurrence infinie résultant de l’appel d’une liste d’affichage, une limite est placée sur le niveau d’imbrication des listes d’affichage au cours de l’exécution de la liste d’affichage. Cette limite doit être au moins de 64, et dépend de l’implémentation.

L’État OpenGL n’est pas enregistré et restauré à travers un appel à **glCallLists**. Ainsi, les modifications apportées à l’État OpenGL pendant l’exécution des listes d’affichage sont conservées une fois l’exécution terminée. Utilisez [**glPushAttrib**](glpushattrib.md), [**glPopAttrib**](glpopattrib.md), [**glPushMatrix**](glpushmatrix.md)et [**glPopMatrix**](glpopmatrix.md) pour conserver l’État OpenGL sur les appels **glCallLists** .

Vous pouvez exécuter des listes d’affichage entre un appel à [**glBegin**](glbegin.md) et l’appel correspondant à [**glEnd**](glend.md), à condition que la liste d’affichage comprenne uniquement les fonctions autorisées dans cet intervalle.

Les fonctions suivantes récupèrent les informations relatives à la fonction **glCallLists** :

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) avec argument GL \_ List \_ base

**glGet** with argument GL \_ Max \_ List \_ imbrication

[**glIsList**](glislist.md)

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

[**glCallList**](glcalllist.md)
</dt> <dt>

[**glDeleteLists**](gldeletelists.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glGenLists**](glgenlists.md)
</dt> <dt>

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[**glIsList**](glislist.md)
</dt> <dt>

[**glListBase**](gllistbase.md)
</dt> <dt>

[**glNewList**](glnewlist.md)
</dt> <dt>

[**glPopAttrib**](glpopattrib.md)
</dt> <dt>

[**glPopMatrix**](glpopmatrix.md)
</dt> <dt>

[**glPushAttrib**](glpushattrib.md)
</dt> <dt>

[**glPushMatrix**](glpushmatrix.md)
</dt> </dl>

 

 





