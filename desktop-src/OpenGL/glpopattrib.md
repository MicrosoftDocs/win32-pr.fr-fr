---
title: fonction glPopAttrib (GL. h)
description: Exécute un pop sur la pile d’attributs.
ms.assetid: 6a11392c-d5af-47bb-a66a-691730a58260
keywords:
- glPopAttrib fonction OpenGL
topic_type:
- apiref
api_name:
- glPopAttrib
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e2258b0f16e6f61e660384931abc394300a29516
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106511772"
---
# <a name="glpopattrib-function"></a>glPopAttrib fonction)

Exécute un pop sur la pile d’attributs.

## <a name="syntax"></a>Syntaxe


```C++
void WINAPI glPopAttrib(void);
```



## <a name="parameters"></a>Paramètres

Cette fonction n’a pas de paramètres.

## <a name="return-value"></a>Valeur retournée

Cette fonction ne retourne pas de valeur.

## <a name="error-codes"></a>Codes d’erreur

Les codes d’erreur suivants peuvent être récupérés par la fonction [**glGetError**](glgeterror.md) .



| Nom                                                                                                  | Signification                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**DÉPASSEMENT de capacité de la \_ pile GL \_**</dt> </dl>   | La fonction a été appelée alors que la pile d’attributs était vide.<br/>                                                               |
| <dl> <dt>**\_opération non valide du GL \_**</dt> </dl> | La fonction a été appelée entre un appel à [**glBegin**](glbegin.md) et l’appel correspondant à [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Notes

La fonction [**glPushAttrib**](glpushattrib.md) prend un argument, un masque qui indique les groupes de variables d’État à enregistrer sur la pile d’attributs. Les constantes symboliques sont utilisées pour définir des bits dans le masque. Le paramètre Mask est généralement construit par **ou** à partir de plusieurs de ces constantes ensemble. Le fichier de masque spécial GL \_ tous les \_ \_ bits d’attrib peut être utilisé pour enregistrer tous les États empilables.

La fonction **glPopAttrib** restaure les valeurs des variables d’état enregistrées avec la dernière commande [**glPushAttrib**](glpushattrib.md) . Ceux qui ne sont pas enregistrés restent inchangés.

C’est une erreur de transmettre des attributs à une pile complète, ou d’afficher des attributs sur une pile vide. Dans les deux cas, l’indicateur d’erreur est défini et aucune autre modification n’est apportée à l’État OpenGL.

Initialement, la pile d’attributs est vide.

Toutes les valeurs de l’État OpenGL ne peuvent pas être enregistrées dans la pile d’attributs. Par exemple, les États pixel Pack et unpack, l’état du mode de rendu et l’état de sélection et de commentaires ne peuvent pas être enregistrés.

La profondeur de la pile d’attributs dépend de l’implémentation, mais elle doit être au moins égale à 16.

Les fonctions suivantes récupèrent les informations relatives à [**glPushAttrib**](glpushattrib.md) et **glPopAttrib**:

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) avec argument la \_ profondeur de la pile GL attrib \_ \_

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) avec l’argument GL max. profondeur de la \_ \_ \_ pile \_

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

[**glEnd**](glend.md)
</dt> <dt>

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[**glGetClipPlane**](glgetclipplane.md)
</dt> <dt>

[**glGetError**](glgeterror.md)
</dt> <dt>

[**glGetLight**](glgetlight.md)
</dt> <dt>

[**glGetMap**](glgetmap.md)
</dt> <dt>

[**glGetMaterial**](glgetmaterial.md)
</dt> <dt>

[**glGetPixelMap**](glgetpixelmap.md)
</dt> <dt>

[**glGetPolygonStipple**](glgetpolygonstipple.md)
</dt> <dt>

[**glGetString**](glgetstring.md)
</dt> <dt>

[**glGetTexEnv**](glgettexenv.md)
</dt> <dt>

[**glGetTexGen**](glgettexgen.md)
</dt> <dt>

[**glGetTexImage**](glgetteximage.md)
</dt> <dt>

[**glGetTexLevelParameter**](glgettexlevelparameter.md)
</dt> <dt>

[**glGetTexParameter**](glgettexparameter.md)
</dt> <dt>

[**glIsEnabled**](glisenabled.md)
</dt> </dl>

 

 





