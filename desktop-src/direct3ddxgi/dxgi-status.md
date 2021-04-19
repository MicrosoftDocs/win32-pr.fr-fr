---
description: Codes d’État qui peuvent être retournés par les fonctions DXGI.
ms.assetid: dd7480b4-8218-4716-ab9f-74a9955b8aa7
title: DXGI_STATUS (DXGI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b39c402880ccdcbda009402d56127e70a61543d0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106523818"
---
# <a name="dxgi_status"></a>État de DXGI \_

Codes d’État qui peuvent être retournés par les fonctions DXGI.



| Constante/valeur                                                                                                                                                                                                                                                                                      | Description                                                                                                                                                                                                                                                                                              |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DXGI_STATUS_OCCLUDED"></span><span id="dxgi_status_occluded"></span><dl> <dt>**Dxgi \_ ÉTAT \_ bloqués**</dt> <dt>0x087A0001</dt> </dl>                                                 | Le contenu de la fenêtre n’est pas visible. Lors de la réception de cet État, une application peut arrêter le rendu et utiliser le \_ test dxgi présente \_ pour déterminer quand reprendre le rendu. Vous ne recevrez pas \_ d’État dxgi \_ bloqués si vous utilisez une chaîne de permutation de modèle.<br/>                                                                                                                           |
| <span id="DXGI_STATUS_MODE_CHANGED"></span><span id="dxgi_status_mode_changed"></span><dl> <dt>**Dxgi \_ MODE d’état \_ \_ modifié**</dt> <dt>0x087A0007</dt> </dl>                                    | Le mode d’affichage du Bureau a été modifié, il peut y avoir une conversion/étirement de couleurs. L’application doit appeler [**IDXGISwapChain :: ResizeBuffers**](/windows/desktop/api/DXGI/nf-dxgi-idxgiswapchain-resizebuffers) pour qu’elle corresponde au nouveau mode d’affichage.<br/>                                                                       |
| <span id="DXGI_STATUS_MODE_CHANGE_IN_PROGRESS"></span><span id="dxgi_status_mode_change_in_progress"></span><dl> <dt>**Dxgi \_ \_ \_ Changement du mode \_ d’État en \_ cours**</dt> <dt>0x087A0008</dt> </dl> | [**IDXGISwapChain :: ResizeTarget**](/windows/desktop/api/DXGI/nf-dxgi-idxgiswapchain-resizetarget) et [**IDXGISwapChain :: SetFullscreenState**](/windows/desktop/api/DXGI/nf-dxgi-idxgiswapchain-setfullscreenstate) retournent \_ \_ \_ la modification du mode d’État dxgi \_ en \_ cours si une transition de mode plein écran/avec fenêtre se produit lorsque l’une des API est appelée.<br/> |



## <a name="remarks"></a>Notes

La valeur **HRESULT** pour chaque valeur d' **\_ État dxgi** est déterminée à partir de cette macro qui est définie dans DXGItype. h :


```
#define _FACDXGI    0x87a
#define MAKE_DXGI_STATUS(code)  MAKE_HRESULT(0, _FACDXGI, code)
```



Par exemple, **dxgi \_ Status \_ bloqués** est défini comme **0x087A0001**:


```
#define DXGI_STATUS_OCCLUDED                    MAKE_DXGI_STATUS(1)
```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|-----------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>DXGI. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Constantes DXGI](d3d10-graphics-reference-dxgi-constants.md)
</dt> </dl>

 

 




