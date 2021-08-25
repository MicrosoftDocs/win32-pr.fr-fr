---
description: La méthode UOPValid récupère une valeur qui indique si l’opération utilisateur spécifiée (UOP) est actuellement valide.
ms.assetid: 0d2c4693-95eb-4cc8-a8f6-61fd0b6d57be
title: Méthode UOPValid (segment. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2eee8f11fbcc51c982b2a619f35fdd56b0f0eebe86945e84f18d6ce62afa783b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120078669"
---
# <a name="uopvalid-method"></a>Méthode UOPValid

> [!Note]  
> ce composant peut être utilisé dans les systèmes d’exploitation Microsoft Windows 2000, Windows XP et Windows Server 2003. Il sera peut-être modifié ou indisponible dans les versions ultérieures.

 

La `UOPValid` méthode récupère une valeur qui indique si l’opération utilisateur spécifiée (UOP) est actuellement valide.

``` syntax
[ bIsValid = ] MSWebDVD.UOPValid(iUOP)
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="iUOP"></span><span id="iuop"></span><span id="IUOP"></span>*iUOP*
</dt> <dd>

Spécifie l’opération de l’utilisateur (UOP) sous la forme d’un entier.



| Valeur | Description                                                                                                                                                                                                              |
|-------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0     | [**PlayTitle**](playtitle-method.md), [**PlayAtTime**](playattime-method.md)[**PlayAtTimeInTitle**](playattimeintitle-method.md)                                                                                      |
| 1     | [**PlayChapter**](playchapter-method.md)                                                                                                                                                                                |
| 2     | [**PlayTitle**](playtitle-method.md)                                                                                                                                                                                    |
| 3     | [**Erreur**](stop-method.md)                                                                                                                                                                                              |
| 4     | [**ReturnFromSubmenu**](returnfromsubmenu-method.md)                                                                                                                                                                    |
| 5     | [**PlayChapter**](playchapter-method.md)                                                                                                                                                                                |
| 6     | [**PlayPrevChapter**](playprevchapter-method.md), [ **ReplayChapter**](replaychapter-method.md)                                                                                                                         |
| 7     | [**PlayNextChapter**](playnextchapter-method.md)                                                                                                                                                                        |
| 8     | [**PlayForwards**](playforwards-method.md)                                                                                                                                                                              |
| 9     | [**PlayBackwards**](playbackwards-method.md)                                                                                                                                                                            |
| 10    | [**ShowMenu**](showmenu-method.md) avec une valeur de paramètre de 2 ( \_ titre de menu DVD \_ )                                                                                                                                       |
| 11    | [**ShowMenu**](showmenu-method.md) avec une valeur de paramètre de 3 ( \_ racine du menu du DVD \_ )                                                                                                                                        |
| 12    | [**ShowMenu**](showmenu-method.md) avec une valeur de paramètre de 4 ( \_ sous-image du menu DVD \_ )                                                                                                                                  |
| 13    | [**ShowMenu**](showmenu-method.md) avec une valeur de paramètre de 5 ( \_ menu DVD \_ audio)                                                                                                                                       |
| 14    | [**ShowMenu**](showmenu-method.md) avec une valeur de paramètre de 6 ( \_ angle de menu DVD \_ )                                                                                                                                       |
| 15    | [**ShowMenu**](showmenu-method.md) avec une valeur de paramètre de 7 ( \_ chapitre du menu DVD \_ )                                                                                                                                     |
| 16    | [**Reprendre**](resume-method.md)                                                                                                                                                                                          |
| 17    | [**SelectLeftButton**](selectleftbutton-method.md), [**SelectRightButton**](selectrightbutton-method.md), [**SelectUpperButton**](selectupperbutton-method.md), [**SelectLowerButton**](selectlowerbutton-method.md) |
| 18    | [**StillOff**](stilloff-method.md)                                                                                                                                                                                      |
| 19    | [**Suspendre**](pause-method.md)                                                                                                                                                                                            |
| 20    | [**CurrentAudioStream**](currentaudiostream-property.md)                                                                                                                                                                |
| 21    | [**CurrentSubpictureStream**](currentsubpicturestream-property.md)                                                                                                                                                      |
| 22    | [**CurrentAngle**](currentangle-property.md), [ **SelectParentalLevel**](selectparentallevel-method.md)                                                                                                                 |
| 23    | [**KaraokeAudioPresentationMode**](karaokeaudiopresentationmode-property.md)                                                                                                                                            |
| 24    | Sélectionnez préférence du mode vidéo.                                                                                                                                                                                            |



 

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Retourne une valeur booléenne indiquant si l’opération spécifiée est autorisée par le contrôle UOP.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|--------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>Segment. h</dt> </dl> |



 

 




