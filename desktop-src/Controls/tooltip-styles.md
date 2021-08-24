---
title: Styles d’info-bulle (CommCtrl. h)
description: Cette section répertorie les styles de contrôle utilisés avec les contrôles ToolTip.
ms.assetid: a6aeac71-6a69-4903-af78-0bfe1f83e632
topic_type:
- apiref
api_name:
- TTS_ALWAYSTIP
- TTS_BALLOON
- TTS_CLOSE
- TTS_NOANIMATE
- TTS_NOFADE
- TTS_NOPREFIX
- TTS_USEVISUALSTYLE
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2dddd890f8bf3aad35d20ec2eabcbe34f89b3ef262fbe30586f9a0a893f85e3b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119751021"
---
# <a name="tooltip-styles"></a>Styles d’info-bulle

Cette section répertorie les styles de contrôle utilisés avec les contrôles ToolTip.



| Constante                                                                                                                                                                     | Description                                                                                                                                                                                                                                                                                                                                                       |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TTS_ALWAYSTIP"></span><span id="tts_alwaystip"></span><dl> <dt>**\_ALWAYSTIP TTS**</dt> </dl>                | Indique que le contrôle ToolTip apparaît lorsque le curseur se trouve sur un outil, même si la fenêtre propriétaire du contrôle ToolTip est inactive. Sans ce style, l’info-bulle s’affiche uniquement lorsque la fenêtre propriétaire de l’outil est active.<br/>                                                                                                                                  |
| <span id="TTS_BALLOON"></span><span id="tts_balloon"></span><dl> <dt>**\_bulle TTS**</dt> </dl>                      | [Version 5,80](common-control-versions.md). Indique que le contrôle ToolTip a l’apparence d’un « ballon » animé, avec des angles arrondis et une tige pointant sur l’élément. <br/>                                                                                                                                                                      |
| <span id="TTS_CLOSE"></span><span id="tts_close"></span><dl> <dt>**\_fermeture TTS**</dt> </dl>                            | Affiche un bouton **Fermer** dans l’info-bulle. Valide uniquement lorsque l’info-bulle a le \_ style de bulle TTS et un titre ; consultez [**atténuation \_ SETTITLE**](ttm-settitle.md).<br/>                                                                                                                                                                                             |
| <span id="TTS_NOANIMATE"></span><span id="tts_noanimate"></span><dl> <dt>**\_NOanimate TTS**</dt> </dl>                | [Version 5,80](common-control-versions.md). désactive l’animation de l’info-bulle glissante sur les systèmes Windows 98 et Windows 2000. Ce style est ignoré sur les systèmes précédents.<br/>                                                                                                                                                                                      |
| <span id="TTS_NOFADE"></span><span id="tts_nofade"></span><dl> <dt>**TTS avec \_ fondu**</dt> </dl>                         | [Version 5,80](common-control-versions.md). Désactive l’animation des info-bulles de fondu. <br/>                                                                                                                                                                                                                                                                       |
| <span id="TTS_NOPREFIX"></span><span id="tts_noprefix"></span><dl> <dt>**le \_ préfixe TTS**</dt> </dl>                   | Empêche le système de commettre des caractères perluète d’une chaîne ou de terminer une chaîne au niveau d’un caractère de tabulation. Sans ce style, le système supprime automatiquement les caractères perluète et met fin à une chaîne au premier caractère de tabulation. Cela permet à une application d’utiliser la même chaîne qu’à la fois comme élément de menu et comme texte dans un contrôle ToolTip.<br/> |
| <span id="TTS_USEVISUALSTYLE"></span><span id="tts_usevisualstyle"></span><dl> <dt>**\_USEVISUALSTYLE TTS**</dt> </dl> | Utilise des liens hypertexte à thème. Le thème définit les styles des liens dans l’info-bulle. Ce style requiert toujours la \_ définition de la PARSELINKS ttf. <br/>                                                                                                                                                                                                          |



## <a name="remarks"></a>Remarques

Un contrôle ToolTip a toujours les \_ styles de fenêtre popup et WS \_ ex \_ TOOLWINDOW, que vous les spécifiiez ou non lors de la création du contrôle.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|---------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>CommCtrl. h</dt> </dl> |



 

 





