---
description: Décrit l’état actuel du clip.
ms.assetid: 3ea8631c-a967-4d24-a49a-1751b3ee6077
title: D3DCLIPSTATUS9, structure (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DCLIPSTATUS9
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 3b22fdfcc136c05ec8fe03ae491612606b2df62f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106531325"
---
# <a name="d3dclipstatus9-structure"></a>D3DCLIPSTATUS9, structure

Décrit l’état actuel du clip.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct D3DCLIPSTATUS9 {
  DWORD ClipUnion;
  DWORD ClipIntersection;
} D3DCLIPSTATUS9, *LPD3DCLIPSTATUS9;
```



## <a name="members"></a>Membres

<dl> <dt>

**ClipUnion**
</dt> <dd>

Type : **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Découpez les indicateurs d’Union qui décrivent l’état actuel du clip. Ce membre peut être un ou plusieurs des indicateurs suivants :



| Valeur                                                                                                                                                      | Signification                                                                         |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| <span id="D3DCS_ALL"></span><span id="d3dcs_all"></span><dl> <dt>**D3DCS \_ tout**</dt> </dl>          | Combinaison de tous les indicateurs de clip.<br/>                                       |
| <span id="D3DCS_LEFT"></span><span id="d3dcs_left"></span><dl> <dt>**D3DCS \_ gauche**</dt> </dl>       | Tous les vertex sont découpés par le plan gauche du frustum d’affichage.<br/>   |
| <span id="D3DCS_RIGHT"></span><span id="d3dcs_right"></span><dl> <dt>**D3DCS \_ droit**</dt> </dl>    | Tous les vertex sont découpés par le plan droit du frustum de visualisation.<br/>  |
| <span id="D3DCS_TOP"></span><span id="d3dcs_top"></span><dl> <dt>**D3DCS \_ Top**</dt> </dl>          | Tous les vertex sont découpés par le plan supérieur du frustum d’affichage.<br/>    |
| <span id="D3DCS_BOTTOM"></span><span id="d3dcs_bottom"></span><dl> <dt>**D3DCS \_ bas**</dt> </dl> | Tous les vertex sont découpés par le plan inférieur du frustum d’affichage.<br/> |
| <span id="D3DCS_FRONT"></span><span id="d3dcs_front"></span><dl> <dt>**D3DCS \_ avant**</dt> </dl>    | Tous les vertex sont découpés par le plan frontal de l’frustum de visualisation.<br/>  |
| <span id="D3DCS_BACK"></span><span id="d3dcs_back"></span><dl> <dt>**D3DCS \_**</dt> </dl>       | Tous les vertex sont découpés par le plan arrière du frustum d’affichage.<br/>   |
| <span id="D3DCS_PLANE0"></span><span id="d3dcs_plane0"></span><dl> <dt>**D3DCS \_ PLANE0**</dt> </dl> | Plans de découpage définis par l’application.<br/>                                 |
| <span id="D3DCS_PLANE1"></span><span id="d3dcs_plane1"></span><dl> <dt>**D3DCS \_ PLANE1**</dt> </dl> | Plans de découpage définis par l’application.<br/>                                 |
| <span id="D3DCS_PLANE2"></span><span id="d3dcs_plane2"></span><dl> <dt>**D3DCS \_ PLANE2**</dt> </dl> | Plans de découpage définis par l’application.<br/>                                 |
| <span id="D3DCS_PLANE3"></span><span id="d3dcs_plane3"></span><dl> <dt>**D3DCS \_ PLANE3**</dt> </dl> | Plans de découpage définis par l’application.<br/>                                 |
| <span id="D3DCS_PLANE4"></span><span id="d3dcs_plane4"></span><dl> <dt>**D3DCS \_ PLANE4**</dt> </dl> | Plans de découpage définis par l’application.<br/>                                 |
| <span id="D3DCS_PLANE5"></span><span id="d3dcs_plane5"></span><dl> <dt>**D3DCS \_ PLANE5**</dt> </dl> | Plans de découpage définis par l’application.<br/>                                 |



 

</dd> <dt>

**ClipIntersection**
</dt> <dd>

Type : **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Indicateurs d’intersection de clips qui décrivent l’état actuel du clip. Ce membre peut prendre les mêmes indicateurs que ClipUnion.

</dd> </dl>

## <a name="remarks"></a>Notes

Lorsque le découpage est activé pendant le traitement du vertex (par [**ProcessVertices**](/windows/desktop/api), [**DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive)ou d’autres fonctions de dessin), Direct3D calcule un code de découpage pour chaque vertex. Le code de la séquence est une combinaison de \_ \* bits D3DCS. Lorsqu’un vertex se trouve en dehors d’un plan de découpage particulier, le bit correspondant est défini dans le code de découpage. Direct3D conserve l’état du clip à l’aide de **D3DCLIPSTATUS9**, qui a des membres ClipUnion et ClipIntersection. ClipUnion est un or au niveau du bit de tous les codes de clip de vertex et ClipIntersection est une opération and au niveau du bit de tous les codes de clip de vertex. Les valeurs initiales sont égales à zéro pour ClipUnion et 0xFFFFFFFF pour ClipIntersection. Lorsque le \_ découpage D3DRS a la valeur **false**, ClipUnion et ClipIntersection sont définis sur zéro. Direct3D met à jour l’état du clip pendant les appels de dessin. Pour calculer l’état du clip d’un objet particulier, définissez ClipUnion et ClipIntersection sur leur valeur initiale et poursuivez le dessin.

L’état du clip n’est pas mis à jour par [**DrawRectPatch**](/windows/desktop/api) et [**DrawTriPatch**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawtripatch) , car il n’y a aucune émulation logicielle pour eux.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|----------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Structures Direct3D](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[**GetClipStatus**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getclipstatus)
</dt> <dt>

[**SetClipStatus**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setclipstatus)
</dt> </dl>

 

 
