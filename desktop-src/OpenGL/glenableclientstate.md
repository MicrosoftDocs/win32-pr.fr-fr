---
title: fonction glEnableClientState (GL. h)
description: Les fonctions glEnableClientState et glDisableClientState activent et désactivent les tableaux, respectivement. | fonction glEnableClientState (GL. h)
ms.assetid: 02520f81-0b0d-4774-b1e2-713cf226347f
keywords:
- glEnableClientState fonction OpenGL
topic_type:
- apiref
api_name:
- glEnableClientState
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0d1ebb9b0278ca6a696183da54c40a6463880a24f6a29a7cca3c2fdd9dd1213a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118360416"
---
# <a name="glenableclientstate-function"></a>glEnableClientState fonction)

Les fonctions **glEnableClientState** et [**glDisableClientState**](gldisableclientstate.md) activent et désactivent les tableaux, respectivement.

## <a name="syntax"></a>Syntaxe


```C++
void WINAPI glEnableClientState(
   GLenum array
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*array* 
</dt> <dd>

Constante symbolique pour le tableau que vous souhaitez activer ou désactiver. Ce paramètre peut prendre l’une des valeurs suivantes.



| Valeur                                                                                                                                                                                      | Signification                                                                                                                                                                                                                                                             |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_COLOR_ARRAY"></span><span id="gl_color_array"></span><dl> <dt>**\_tableau de couleurs GL \_**</dt> </dl>                          | S’il est activé, utilisez des tableaux de couleurs avec des appels à [**glArrayElement**](glarrayelement.md), [**glDrawElements**](gldrawelements.md)ou [**glDrawArrays**](gldrawarrays.md).<br/> Voir aussi [**glColorPointer**](glcolorpointer.md).<br/>                    |
| <span id="GL_EDGE_FLAG_ARRAY"></span><span id="gl_edge_flag_array"></span><dl> <dt>**\_tableau d' \_ indicateurs de périphérie du GL \_**</dt> </dl>             | S’il est activé, utilisez des tableaux d’indicateurs de bord avec des appels à [**glArrayElement**](glarrayelement.md), [**glDrawElements**](gldrawelements.md)ou [**glDrawArrays**](gldrawarrays.md).<br/> Voir aussi [**glEdgeFlagPointer**](gledgeflagpointer.md).<br/>          |
| <span id="GL_INDEX_ARRAY"></span><span id="gl_index_array"></span><dl> <dt>**\_tableau d’index GL \_**</dt> </dl>                          | S’il est activé, utilisez des tableaux d’index avec des appels à [**glArrayElement**](glarrayelement.md), [**glDrawElements**](gldrawelements.md)ou [**glDrawArrays**](gldrawarrays.md).<br/> Voir aussi [**glIndexPointer**](glindexpointer.md).<br/>                    |
| <span id="GL_NORMAL_ARRAY"></span><span id="gl_normal_array"></span><dl> <dt>**\_tableau normal du GL \_**</dt> </dl>                       | S’il est activé, utilisez des tableaux normaux avec des appels à [**glArrayElement**](glarrayelement.md), [**glDrawElements**](gldrawelements.md)ou [**glDrawArrays**](gldrawarrays.md).<br/> Voir aussi [**glNormalPointer**](glnormalpointer.md).<br/>                 |
| <span id="GL_TEXTURE_COORD_ARRAY"></span><span id="gl_texture_coord_array"></span><dl> <dt>**Tableau de coordonnées de la \_ texture GL \_ \_**</dt> </dl> | S’il est activé, utilisez des tableaux de coordonnées de texture avec des appels à [**glArrayElement**](glarrayelement.md), [**glDrawElements**](gldrawelements.md)ou [**glDrawArrays**](gldrawarrays.md).<br/> Voir aussi [**glTexCoordPointer**](gltexcoordpointer.md).<br/> |
| <span id="GL_VERTEX_ARRAY"></span><span id="gl_vertex_array"></span><dl> <dt>**\_tableau de vertex GL \_**</dt> </dl>                       | S’il est activé, utilisez des tableaux de vertex avec des appels à [**glArrayElement**](glarrayelement.md), [**glDrawElements**](gldrawelements.md)ou [**glDrawArrays**](gldrawarrays.md).<br/> Voir aussi [**glVertexPointer**](glvertexpointer.md).<br/>                 |



 

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Cette fonction ne retourne pas de valeur.

## <a name="error-codes"></a>Codes d’erreur

Le code d’erreur suivant peut être récupéré par la fonction [**glGetError**](glgeterror.md) .



| Nom                                                                                             | Signification                                       |
|--------------------------------------------------------------------------------------------------|-----------------------------------------------|
| <dl> <dt>**\_enum GL non valide \_**</dt> </dl> | le *tableau* n’est pas une valeur acceptée.<br/> |



## <a name="remarks"></a>Remarques

Les fonctions **glEnableClientState** et **glDisableClientState** activent et désactivent différents tableaux individuels. Utilisez [**glIsEnabled**](glisenabled.md) ou [**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) pour déterminer la valeur actuelle de toutes les fonctionnalités.

L’appel de **glEnableClientState** et **glDisableClientState** entre les appels à [**glBegin**](glbegin.md) et l’appel correspondant à [**glEnd**](glend.md) peut provoquer une erreur. Si aucune erreur n’est générée, le comportement n’est pas défini.

> [!Note]  
> Les fonctions **glEnableClientState** et **glDisableClientState** sont uniquement disponibles dans OpenGL version 1,1 ou ultérieure.

 

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

[**glArrayElement**](glarrayelement.md)
</dt> <dt>

[**glBegin**](glbegin.md)
</dt> <dt>

[**glColorPointer**](glcolorpointer.md)
</dt> <dt>

[**glDisableClientState**](gldisableclientstate.md)
</dt> <dt>

[**glDrawArrays**](gldrawarrays.md)
</dt> <dt>

[**glDrawElements**](gldrawelements.md)
</dt> <dt>

[**glEdgeFlagPointer**](gledgeflagpointer.md)
</dt> <dt>

[**glEnable**](glenable.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glGetPointerv**](glgetpointerv.md)
</dt> <dt>

[**glIndexPointer**](glindexpointer.md)
</dt> <dt>

[**glInterleavedArrays**](glinterleavedarrays.md)
</dt> <dt>

[**glNormalPointer**](glnormalpointer.md)
</dt> <dt>

[**glTexCoordPointer**](gltexcoordpointer.md)
</dt> <dt>

[**glVertexPointer**](glvertexpointer.md)
</dt> </dl>

 

 





