---
title: fonction glClear (GL. h)
description: La fonction glClear efface les mémoires tampons à des valeurs prédéfinies.
ms.assetid: 9818f969-3145-45ea-aa9c-2abed953a8e0
keywords:
- glClear fonction OpenGL
topic_type:
- apiref
api_name:
- glClear
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0bb48a1b2832a5f9c046bb450b7cfba9ec4f83a759b093df91f3ec2064f23a3d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120082099"
---
# <a name="glclear-function"></a>glClear fonction)

La fonction **glClear** efface les mémoires tampons à des valeurs prédéfinies.

## <a name="syntax"></a>Syntaxe


```C++
void WINAPI glClear(
   GLbitfield mask
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*mask* 
</dt> <dd>

Opérateurs de bits or de masques qui indiquent les mémoires tampons à effacer. Les quatre masques sont les suivants :



| Valeur                                                                                                                                                                                   | Signification                                                     |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| <span id="GL_COLOR_BUFFER_BIT"></span><span id="gl_color_buffer_bit"></span><dl> <dt>**\_bit de \_ mémoire tampon de couleur GL \_**</dt> </dl>       | Mémoires tampons actuellement activées pour l’écriture de couleurs.<br/> |
| <span id="GL_DEPTH_BUFFER_BIT"></span><span id="gl_depth_buffer_bit"></span><dl> <dt>**\_bit de \_ mémoire tampon de profondeur GL \_**</dt> </dl>       | Mémoire tampon de profondeur.<br/>                                |
| <span id="GL_ACCUM_BUFFER_BIT"></span><span id="gl_accum_buffer_bit"></span><dl> <dt>**\_bit de tampon amort \_ \_**</dt> </dl>       | Mémoire tampon d’accumulation.<br/>                         |
| <span id="GL_STENCIL_BUFFER_BIT"></span><span id="gl_stencil_buffer_bit"></span><dl> <dt>**\_bit de \_ tampon de stencil du GL \_**</dt> </dl> | Mémoire tampon de stencil.<br/>                              |



 

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Cette fonction ne retourne pas de valeur.

## <a name="error-codes"></a>Codes d’erreur

Les codes d’erreur suivants peuvent être récupérés par la fonction [**glGetError**](glgeterror.md) .



| Name                                                                                                  | Signification                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_valeur non valide du GL \_**</dt> </dl>     | Tout bit autre que les quatre bits définis a été défini dans *Mask*.<br/>                                                                |
| <dl> <dt>**\_opération non valide du GL \_**</dt> </dl> | La fonction a été appelée entre un appel à [**glBegin**](glbegin.md) et l’appel correspondant à [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Remarques

La **fonction glClear** définit la zone Bitplane de la fenêtre sur les valeurs précédemment sélectionnées par [**glClearColor**](glclearcolor.md), [**glClearIndex**](glclearindex.md), [**glClearDepth**](glcleardepth.md), [**glClearStencil**](glclearstencil.md)et [**glClearAccum**](glclearaccum.md). Vous pouvez effacer plusieurs mémoires tampons de couleurs simultanément en sélectionnant plusieurs mémoires tampons à la fois à l’aide de [**glDrawBuffer**](gldrawbuffer.md).

Le test de propriété en pixels, le test de ciseaux, le tramage et la mémoire tampon writemasks affectent le fonctionnement de **glClear**. La zone de ciseaux délimite la région effacée. La fonction **glClear** ignore la fonction alpha, la fonction Blend, l’opération logique, le stencil, le mappage de texture et la mise en mémoire tampon *z*.

La fonction **glClear** accepte un seul argument (*Mask*) qui est l’opération de bits or de plusieurs valeurs indiquant la mémoire tampon à effacer.

La valeur à laquelle chaque mémoire tampon est désactivée dépend du paramètre de la valeur Clear de cette mémoire tampon.

Si aucune mémoire tampon n’est présente, un appel **glClear** dirigé vers cette mémoire tampon n’a aucun effet.

Les fonctions suivantes récupèrent les informations relatives à **glClear**:

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) avec argument GL \_ Amort \_ Clear \_ value

**glGet** avec argument GL \_ profondeur \_ effacer la \_ valeur

**glGet** avec argument \_ \_ valeur Clear de l’index GL \_

**glGet** avec argument \_ \_ valeur Clear de couleur GL \_

**glGet** avec argument \_ \_ valeur Clear du stencil du GL \_

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

[**glClearAccum**](glclearaccum.md)
</dt> <dt>

[**glClearColor**](glclearcolor.md)
</dt> <dt>

[**glClearDepth**](glcleardepth.md)
</dt> <dt>

[**glClearIndex**](glclearindex.md)
</dt> <dt>

[**glClearStencil**](glclearstencil.md)
</dt> <dt>

[**glDrawBuffer**](gldrawbuffer.md)
</dt> <dt>

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[**glScissor**](glscissor.md)
</dt> </dl>

 

 





