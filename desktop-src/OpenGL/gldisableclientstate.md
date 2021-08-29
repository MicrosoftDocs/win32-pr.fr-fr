---
title: fonction glDisableClientState (GL. h)
description: Les fonctions glEnableClientState et glDisableClientState activent et désactivent les tableaux, respectivement. | fonction glDisableClientState (GL. h)
ms.assetid: b3316519-00ed-45f8-9c4b-2e04c483751e
keywords:
- glDisableClientState fonction OpenGL
topic_type:
- apiref
api_name:
- glDisableClientState
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7d2a5db54a78dd393d9d9507860e68fb8f9f405d76930b730798454c521c20ae
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120081639"
---
# <a name="gldisableclientstate-function"></a>glDisableClientState fonction)

Les fonctions [**glEnableClientState**](glenableclientstate.md) et **glDisableClientState** activent et désactivent les tableaux, respectivement.

## <a name="syntax"></a>Syntaxe


```C++
void WINAPI glDisableClientState(
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



| Name                                                                                             | Signification                                       |
|--------------------------------------------------------------------------------------------------|-----------------------------------------------|
| <dl> <dt>**\_enum GL non valide \_**</dt> </dl> | le *tableau* n’est pas une valeur acceptée.<br/> |



## <a name="remarks"></a>Remarques

Les fonctions [**glEnableClientState**](glenableclientstate.md) et **glDisableClientState** activent et désactivent différents tableaux individuels. Utilisez [**glIsEnabled**](glisenabled.md) ou [**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) pour déterminer la valeur actuelle de toutes les fonctionnalités.

L’appel de [**glEnableClientState**](glenableclientstate.md) et **glDisableClientState** entre les appels à [**glBegin**](glbegin.md) et l’appel correspondant à [**glEnd**](glend.md) peut provoquer une erreur. Si aucune erreur n’est générée, le comportement n’est pas défini.

> [!Note]  
> Les fonctions [**glEnableClientState**](glenableclientstate.md) et **glDisableClientState** sont uniquement disponibles dans OpenGL version 1,1 ou ultérieure.

 

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

[**glDrawArrays**](gldrawarrays.md)
</dt> <dt>

[**glDrawElements**](gldrawelements.md)
</dt> <dt>

[**glEdgeFlagPointer**](gledgeflagpointer.md)
</dt> <dt>

[**glEnable**](glenable.md)
</dt> <dt>

[**glEnableClientState**](glenableclientstate.md)
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

 

 





