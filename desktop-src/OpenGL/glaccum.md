---
title: fonction glAccum (GL. h)
description: La fonction glAccum opère sur la mémoire tampon d’accumulation.
ms.assetid: 3ddd69fe-74fc-4ac0-be8d-bcaa71ac0292
keywords:
- glAccum fonction OpenGL
topic_type:
- apiref
api_name:
- glAccum
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f6d25e02971d07d54567c462708aa4efd87b2d32
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741948"
---
# <a name="glaccum-function"></a>glAccum fonction)

La fonction **glAccum** opère sur la mémoire tampon d’accumulation.

## <a name="syntax"></a>Syntaxe


```C++
void WINAPI glAccum(
   GLenum  op,
   GLfloat value
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*opérationnel* 
</dt> <dd>

Opération de tampon d’accumulation. Les constantes symboliques acceptées sont les suivantes.



| Valeur                                                                                                                                             | Signification                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_ACCUM"></span><span id="gl_accum"></span><dl> <dt>**\_total amort**</dt> </dl>    | Obtient R, G, B et une valeur de la mémoire tampon actuellement sélectionnée pour la lecture (consultez [**glReadBuffer**](glreadbuffer.md)). Chaque valeur de composant est divisée par 2 *n*  1, où *n* est le nombre de bits alloués à chaque composant de couleur dans la mémoire tampon actuellement sélectionnée. Le résultat est une valeur à virgule flottante dans la plage \[ 0, 1 \] , qui est multipliée par *valeur* et ajoutée au composant de pixel correspondant dans la mémoire tampon d’accumulation, ce qui a pour effet de mettre à jour la mémoire tampon d’accumulation.<br/> |
| <span id="GL_LOAD"></span><span id="gl_load"></span><dl> <dt>**charge du GL \_**</dt> </dl>       | Semblable à la \_ valeur de l’amortissement GL, à la différence que la valeur actuelle de la mémoire tampon d’accumulation n’est pas utilisée dans le calcul de la nouvelle valeur. Autrement dit, les valeurs R, G, B et A de la mémoire tampon actuellement sélectionnée sont divisées par 2 *n*  1, multiplié par *valeur*, puis stockées dans la cellule de mémoire tampon d’accumulation correspondante, remplaçant la valeur actuelle.<br/>                                                                                                                                      |
| <span id="GL_ADD"></span><span id="gl_add"></span><dl> <dt>**ajout au GL \_**</dt> </dl>          | Ajoute la *valeur* à chaque R, G, B et A dans la mémoire tampon d’accumulation.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span id="GL_MULT"></span><span id="gl_mult"></span><dl> <dt>**GL \_ mult**</dt> </dl>       | Multiplie chaque R, G, B et A dans la mémoire tampon d’accumulation par *valeur* et retourne le composant mis à l’échelle à l’emplacement de la mémoire tampon d’accumulation correspondante.<br/>                                                                                                                                                                                                                                                                                                                                |
| <span id="GL_RETURN"></span><span id="gl_return"></span><dl> <dt>**\_retour GL**</dt> </dl> | Transfère les valeurs de mémoire tampon de l’accumulation à la mémoire tampon de couleur ou aux mémoires tampons actuellement sélectionnées pour l’écriture. Chaque R, G, B et un composant sont multipliés par la *valeur*, puis multipliés par 2 *n*  1, fixés à la plage \[ 0, 2 *n*  1 \] et stockés dans la cellule de mémoire tampon d’affichage correspondante. Les seules opérations de fragment appliquées à ce transfert sont la propriété de pixel, la ciseaux, le tramage et la couleur writemasks.<br/>                                                                        |



 

</dd> <dt>

*value* 
</dt> <dd>

Valeur à virgule flottante utilisée dans l’opération de tampon d’accumulation. Le paramètre *op* détermine la façon dont la *valeur* est utilisée.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Cette fonction ne retourne pas de valeur.

## <a name="error-codes"></a>Codes d’erreur

Les codes d’erreur suivants peuvent être récupérés par la fonction [**glGetError**](glgeterror.md) .



| Nom                                                                                                  | Signification                                                                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_enum GL non valide \_**</dt> </dl>      | *op* n’est pas une valeur acceptée.<br/>                                                                                                                                            |
| <dl> <dt>**\_opération non valide du GL \_**</dt> </dl> | Il n’y avait pas de mémoire tampon d’accumulation ou la fonction **glAccum** a été appelée entre un appel à [**glBegin**](glbegin.md) et l’appel correspondant à [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Notes

La mémoire tampon d’accumulation est une mémoire tampon de plage étendue. Les images ne sont pas rendues dans celui-ci. Au lieu de cela, les images rendues dans l’une des mémoires tampons de couleur sont ajoutées au contenu de la mémoire tampon d’accumulation après le rendu. Vous pouvez créer des effets tels que l’anticrénelage (des points, lignes et polygones), le flou directionnel et la profondeur de champ en cumulant les images générées avec des matrices de transformation différentes.

Chaque pixel de la mémoire tampon d’accumulation se compose de valeurs rouge, vert, bleu et alpha. Le nombre de bits par composant dans la mémoire tampon d’accumulation dépend de l’implémentation. Vous pouvez examiner ce nombre en appelant quatre fois [**glGetIntegerv**](glgetintegerv.md) , à l’aide des arguments GL \_ Amort total \_ \_ bits, GL \_ Amort \_ Green \_ bits, GL \_ Amort \_ Blue bits \_ et GL \_ Amort \_ alpha \_ bits, respectivement. Quel que soit le nombre de bits par composant, toutefois, la plage de valeurs stockées par chaque composant est \[ 1, ? 1 \] . Les pixels de la mémoire tampon d’accumulation sont mappés un-à-un avec trame pixels.

La fonction **glAccum** opère sur la mémoire tampon d’accumulation. Le premier argument, *op*, est une constante symbolique qui sélectionne une opération de tampon d’accumulation. Le deuxième argument, *value*, est une valeur à virgule flottante à utiliser dans cette opération. Cinq opérations sont spécifiées : GL \_ Amort, GL \_ Load, GL \_ Add, GL \_ mult et GL \_ Return.

Toutes les opérations de mémoire tampon d’accumulation sont limitées à la zone de la zone de ciseaux actuelle et sont appliquées de la même façon que les composants rouge, vert, bleu et alpha de chaque pixel. Le contenu d’un composant de pixel de mémoire tampon d’accumulation n’est pas défini si l’opération **glAccum** génère une valeur en dehors de la plage \[ 1, 1 \] .

Pour effacer la mémoire tampon d’accumulation, utilisez la fonction [**glClearAccum**](glclearaccum.md) pour spécifier R, G, B et une valeur pour la définir, puis émettez une fonction [**glClear**](glclear.md) avec la mémoire tampon d’accumulation activée.

Seuls les pixels de la zone de ciseaux actuelle sont mis à jour par toute opération **glAccum** .

Les fonctions suivantes récupèrent les informations relatives à la fonction **glAccum** :

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) avec argument GL \_ Amort \_ bits en rouge \_

**glGet** avec argument GL \_ Amort \_ Green \_ bits

**glGet** avec argument GL \_ Amort \_ Blue \_ bits

**glGet** avec argument GL \_ Amort \_ alpha \_ bits

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

[**glBlendFunc**](glblendfunc.md)
</dt> <dt>

[**glClear**](glclear.md)
</dt> <dt>

[**glClearAccum**](glclearaccum.md)
</dt> <dt>

[**glCopyPixels**](glcopypixels.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[**glLogicOp**](gllogicop.md)
</dt> <dt>

[**glPixelStore**](glpixelstore-functions.md)
</dt> <dt>

[**glPixelTransfer**](glpixeltransfer.md)
</dt> <dt>

[**glReadBuffer**](glreadbuffer.md)
</dt> <dt>

[**glReadPixels**](glreadpixels.md)
</dt> <dt>

[**glScissor**](glscissor.md)
</dt> <dt>

[**glStencilOp**](glstencilop.md)
</dt> </dl>

 

 





