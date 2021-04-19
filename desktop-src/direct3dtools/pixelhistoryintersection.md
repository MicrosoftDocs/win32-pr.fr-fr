---
description: Représente des informations sur un particulier.
MS-HAID: vspixengine.PixelHistoryIntersection
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: PixelHistoryIntersection, structure
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: D67A116D-B1D0-4E88-A2FF-611CDF4003B2
api_name:
- PixelHistoryIntersection
api_type:
- HeaderDef
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 735adc5396551a18b5e2e2dfba781b358289475e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "106513295"
---
# <a name="span-idvspixenginepixelhistoryintersectionspanpixelhistoryintersection-structure"></a><span id="vspixengine.pixelhistoryintersection"></span>PixelHistoryIntersection, structure

Représente des informations sur un

## <a name="syntax"></a>Syntaxe


```C++
} PixelHistoryIntersection;
```

## <a name="members"></a>Membres

**frameNumber**  
Frame de l’événement Graphics dans avec cette opération.

**Numéro**  
ID de l’événement graphique associé à cette opération.

**renderTargetPtr**  
Cible de rendu associée à l’origine (à l’intérieur de l’application capturée) avec cette opération.

**eventType**  
Type d’événement associé à cette opération (en particulier, si cet événement est un appel de dessin).

**point**  
Coordonnées du pixel dans le trame.

**bAssemblerStageGeneratesInstanceID**  
true si l’assembleur d’entrée génère des ID d’instance ; Sinon, false.

**flags**  
Combinaison de valeurs PIXELHISTORYFLAGS. Pour plus d’informations, consultez l’énumération PIXELHISTORYFLAGS.

**fbInitialRed**  
Trame : valeur du composant de couleur rouge de trame avant la fusion de toute sortie de nuanceur de pixels. autrement dit, au début de ce frame.

**fbInitialGreen**  
Trame : valeur du composant de couleur verte de trame avant la fusion de toute sortie de nuanceur de pixels. autrement dit, au début de ce frame.

**fbInitialBlue**  
Trame : valeur du composant de couleur bleu de trame avant la fusion de toute sortie de nuanceur de pixels. autrement dit, au début de ce frame.

**fbInitialAlpha**  
Trame : valeur du composant de couleur alpha de trame avant la fusion de toute sortie de nuanceur de pixels. autrement dit, au début de ce frame.

**LabelFBInitialRed**  
Chaîne COM contenant le nom de l’étiquette associée au composant de couleur rouge du trame avant tout ombrage de pixel ; autrement dit, au début de ce frame.

**LabelFBInitialGreen**  
Chaîne COM contenant le nom de l’étiquette associée au composant de couleur verte du trame avant tout ombrage de pixel ; autrement dit, au début de ce frame.

**LabelFBInitialBlue**  
Chaîne COM contenant le nom de l’étiquette associée au composant de couleur bleu du trame avant tout ombrage de pixel ; autrement dit, au début de ce frame.

**LabelFBInitialAlpha**  
Chaîne COM contenant le nom de l’étiquette associée au composant de couleur alpha du trame avant tout ombrage de pixel ; autrement dit, au début de ce frame.

**fbRed**  
Trame : valeur du composant de couleur rouge de trame une fois que toutes les sorties de nuanceur de pixels ont été fusionnées ; autrement dit, la couleur trame finale.

**fbGreen**  
Trame : valeur du composant de couleur verte de trame une fois que toutes les sorties de nuanceur de pixels ont été fusionnées ; autrement dit, la couleur trame finale.

**fbBlue**  
Trame : valeur du composant de couleur bleu de trame une fois que toutes les sorties de nuanceur de pixels ont été fusionnées ; autrement dit, la couleur trame finale.

**fbAlpha**  
Trame : valeur du composant de couleur alpha de trame une fois que toutes les sorties de nuanceur de pixels ont été fusionnées ; autrement dit, la couleur trame finale.

**LabelFBRed**  
Chaîne COM contenant le nom de l’étiquette associée au composant de couleur rouge du trame après l’ombrage des pixels ; autrement dit, la couleur trame finale.

**LabelFBGreen**  
Chaîne COM contenant le nom de l’étiquette associée au composant de couleur verte du trame après tout l’ombrage de pixel. autrement dit, la couleur trame finale.

**LabelFBBlue**  
Chaîne COM contenant le nom de l’étiquette associée au composant de couleur bleu du trame après l’ombrage des pixels ; autrement dit, la couleur trame finale.

**LabelFBAlpha**  
Chaîne COM contenant le nom de l’étiquette associée au composant de couleur alpha du trame après tout l’ombrage de pixel. autrement dit, la couleur trame finale.

**pixelKillReason**  
Spécifie la raison pour laquelle la contribution de couleur du pixel a été supprimée.

**HResult**  
Si une erreur s’est produite, contient la valeur HRESULT de DirectX qui spécifie l’erreur.

## <a name="requirements"></a>Configuration requise

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>En-tête</p></td><td>Vspixengine. h</td></tr></tbody></table>

 

 



