---
description: Énumération utilisée pour indiquer la raison pour laquelle un pixel a été rejeté.
MS-HAID: vspixengine.PIXELKILLREASON
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Énumération PIXELKILLREASON
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 43836288-554B-430C-861D-AAC58DE3B282
api_name:
- PIXELKILLREASON
api_type:
- HeaderDef
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: f87b072eec1ac98ca68171593765567f5e77e70e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104317705"
---
# <a name="span-idvspixenginepixelkillreasonspanpixelkillreason-enumeration"></a><span id="vspixengine.pixelkillreason"></span>Énumération PIXELKILLREASON

Énumération utilisée pour indiquer la raison pour laquelle un pixel a été rejeté.

## <a name="syntax"></a>Syntaxe


```C++
};
```

## <a name="constants"></a>Constantes

<span id="PKR_NONE"></span><span id="pkr_none"></span>**PKR \_ aucun**  
Valeur qui indique que le pixel n’a pas été rejeté.

<span id="PKR_SHADERKILL"></span><span id="pkr_shaderkill"></span>**PKR \_ SHADERKILL**  
Valeur qui indique que le pixel a été rejeté car le nuanceur n’a pas été exécuté.

<span id="PKR_SCISSORTEST"></span><span id="pkr_scissortest"></span>**PKR \_ SCISSORTEST**  
Valeur qui indique que le pixel a été rejeté en raison de l’échec du test de la ciseaux.

<span id="PKR_ALPHATEST"></span><span id="pkr_alphatest"></span>**PKR \_ ALPHATEST**  
Valeur qui indique que le pixel a été rejeté en raison de l’échec du test alpha.

<span id="PKR_STENCILTEST"></span><span id="pkr_stenciltest"></span>**PKR \_ STENCILTEST**  
Valeur qui indique que le pixel a été rejeté en raison de l’échec du test du stencil.

<span id="PKR_DEPTHTEST"></span><span id="pkr_depthtest"></span>**PKR \_ DEPTHTEST**  
Valeur qui indique que le pixel a été rejeté en raison de l’échec du test de profondeur.

<span id="PKR_NOTCOMPUTABLE"></span><span id="pkr_notcomputable"></span>**PKR \_ NOTCOMPUTABLE**  
Valeur qui indique que l’historique des pixels ne peut pas être calculé.

<span id="PKR_ERROR"></span><span id="pkr_error"></span>**\_erreur PKR**  
Valeur qui indique que le pixel a été rejeté en raison d’une erreur générale.

<span id="PKR_NOINTERSECTION"></span><span id="pkr_nointersection"></span>**nointersection PKR \_**  
Valeur qui indique que le pixel a été rejeté parce que l’appel de dessin ne croise pas le pixel.

<span id="PKR_OCCLUDED"></span><span id="pkr_occluded"></span>**PKR \_ bloqués**  
Valeur qui indique que le pixel a été rejeté car le dessin était bloqués.

<span id="PKR_DEPTHSTENCILTEST"></span><span id="pkr_depthstenciltest"></span>**PKR \_ DEPTHSTENCILTEST**  
Valeur qui indique que le pixel a été rejeté en raison de l’échec du test de profondeur et du stencil.

## <a name="requirements"></a>Configuration requise

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>En-tête</p></td><td>Vspixengine. h</td></tr></tbody></table>

 

 



