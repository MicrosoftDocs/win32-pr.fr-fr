---
description: Énumération contenant les indicateurs utilisés pour décrire le résultat de l’historique des pixels. Consultez PixelHistoryOperation.
MS-HAID: vspixengine.PIXELHISTORYFLAGS
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Énumération PIXELHISTORYFLAGS
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: BDB88A2D-016A-4E15-B47A-870A2959E943
api_name:
- PIXELHISTORYFLAGS
api_type:
- HeaderDef
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 559146fb1f319f5b2c02c5383015c013a662e838
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2021
ms.locfileid: "122627155"
---
# <a name="span-idvspixenginepixelhistoryflagsspanpixelhistoryflags-enumeration"></a><span id="vspixengine.pixelhistoryflags"></span>Énumération PIXELHISTORYFLAGS

Énumération contenant les indicateurs utilisés pour décrire le résultat de l’historique des pixels. Consultez PixelHistoryOperation.

## <a name="syntax"></a>Syntax


```C++
};
```

## <a name="constants"></a>Constantes

<span id="PHF_INITIALVALUE"></span><span id="phf_initialvalue"></span>**PHF \_ INITIALVALUE**  
Indicateur qui correspond à la valeur de couleur initiale (avant le cadre).

<span id="PHF_CLEAR"></span><span id="phf_clear"></span>**PHF \_ Clear**  
Indicateur qui correspond au résultat de la couleur d’effacement.

<span id="PHF_DRAW"></span><span id="phf_draw"></span>**PHF \_ dessin**  
Indicateur qui correspond au résultat de la couleur de dessin.

<span id="PHF_FINALVALUE"></span><span id="phf_finalvalue"></span>**PHF \_ FINALVALUE**  
Indicateur qui correspond au résultat final de la couleur.

<span id="PHF_HASCOLOR"></span><span id="phf_hascolor"></span>**PHF \_ HASCOLOR**  
Indicateur qui correspond à si le résultat de couleur est présent dans le struct PixelHistoryOperation.

<span id="PHF_HASFBCOLOR"></span><span id="phf_hasfbcolor"></span>**PHF \_ HASFBCOLOR**  
Indicateur qui correspond à si le résultat final de la couleur de la mémoire tampon est présent dans la structure PixelHistoryOperation.

<span id="PHF_ERROR"></span><span id="phf_error"></span>**\_erreur PHF**  

<span id="PHF_VERTEXPROCESSINGSKIPPED"></span><span id="phf_vertexprocessingskipped"></span>**PHF \_ VERTEXPROCESSINGSKIPPED**  
Non utilisé.

<span id="PHF_MODIFYRESOURCE"></span><span id="phf_modifyresource"></span>**PHF \_ MODIFYRESOURCE**  

<span id="PHF_CANNOTRUNFULLDEPTHSTENCILTEST"></span><span id="phf_cannotrunfulldepthstenciltest"></span>**PHF \_ CANNOTRUNFULLDEPTHSTENCILTEST**  
Indicateur qui correspond à ne pas pouvoir exécuter le test de profondeur ou de stencil.

## <a name="requirements"></a>Configuration requise

<table><colgroup><col  /><col  /></colgroup><tbody><tr class="odd"><td><p>En-tête</p></td><td>Vspixengine. h</td></tr></tbody></table>

 

 



