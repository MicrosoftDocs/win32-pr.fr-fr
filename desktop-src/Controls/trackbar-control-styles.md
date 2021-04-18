---
title: Styles de contrôle TrackBar (CommCtrl. h)
description: Cette section contient des informations sur les styles utilisés avec les contrôles TrackBar.
ms.assetid: ac2f59c6-85a2-4f41-aace-4132971d3559
topic_type:
- apiref
api_name:
- TBS_AUTOTICKS
- TBS_VERT
- TBS_HORZ
- TBS_TOP
- TBS_BOTTOM
- TBS_LEFT
- TBS_RIGHT
- TBS_BOTH
- TBS_NOTICKS
- TBS_ENABLESELRANGE
- TBS_FIXEDLENGTH
- TBS_NOTHUMB
- TBS_TOOLTIPS
- TBS_REVERSED
- TBS_DOWNISLEFT
- TBS_NOTIFYBEFOREMOVE
- TBS_TRANSPARENTBKGND
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 42966f98db18257c9a6a9ca463d5bd88028a02f7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540406"
---
# <a name="trackbar-control-styles"></a>Styles de contrôle TrackBar

Cette section contient des informations sur les styles utilisés avec les contrôles TrackBar.



| Constante                                                                                                                                                                           | Description                                                                                                                                                                                                                                                                                                                                                           |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TBS_AUTOTICKS"></span><span id="tbs_autoticks"></span><dl> <dt>**\_pulsations tbs**</dt> </dl>                      | Le contrôle TrackBar a une graduation pour chaque incrément dans sa plage de valeurs. <br/>                                                                                                                                                                                                                                                                           |
| <span id="TBS_VERT"></span><span id="tbs_vert"></span><dl> <dt>**TBS en \_ vert**</dt> </dl>                                     | Le contrôle TrackBar est orienté verticalement.<br/>                                                                                                                                                                                                                                                                                                               |
| <span id="TBS_HORZ"></span><span id="tbs_horz"></span><dl> <dt>**TBS \_ Horiz**</dt> </dl>                                     | Le contrôle TrackBar est orienté horizontalement. Il s’agit de l’orientation par défaut. <br/>                                                                                                                                                                                                                                                                           |
| <span id="TBS_TOP"></span><span id="tbs_top"></span><dl> <dt>**TBS en \_ haut**</dt> </dl>                                        | Le contrôle TrackBar affiche des graduations au-dessus du contrôle. Ce style est valide uniquement avec TBS \_ horiz. <br/>                                                                                                                                                                                                                                                      |
| <span id="TBS_BOTTOM"></span><span id="tbs_bottom"></span><dl> <dt>**TBS en \_ bas**</dt> </dl>                               | Le contrôle TrackBar affiche des graduations sous le contrôle. Ce style est valide uniquement avec TBS \_ horiz. <br/>                                                                                                                                                                                                                                                      |
| <span id="TBS_LEFT"></span><span id="tbs_left"></span><dl> <dt>**TBS à \_ gauche**</dt> </dl>                                     | Le contrôle TrackBar affiche des graduations à gauche du contrôle. Ce style est valide uniquement avec TBS en \_ vert. <br/>                                                                                                                                                                                                                                             |
| <span id="TBS_RIGHT"></span><span id="tbs_right"></span><dl> <dt>**\_droits tbs**</dt> </dl>                                  | Le contrôle TrackBar affiche des graduations à droite du contrôle. Ce style est valide uniquement avec TBS en \_ vert. <br/>                                                                                                                                                                                                                                            |
| <span id="TBS_BOTH"></span><span id="tbs_both"></span><dl> <dt>**TBS \_**</dt> </dl>                                     | Le contrôle TrackBar affiche les graduations des deux côtés du contrôle. Ils sont à la fois en haut et en bas lorsqu’ils sont utilisés avec TBS \_ horint ou les deux à gauche et à droite s’ils sont utilisés avec tbs en \_ vert. <br/>                                                                                                                                                                           |
| <span id="TBS_NOTICKS"></span><span id="tbs_noticks"></span><dl> <dt>**\_NOtiques tbs**</dt> </dl>                            | Le contrôle TrackBar n’affiche aucune graduation. <br/>                                                                                                                                                                                                                                                                                                     |
| <span id="TBS_ENABLESELRANGE"></span><span id="tbs_enableselrange"></span><dl> <dt>**\_ENABLESELRANGE tbs**</dt> </dl>       | Le contrôle TrackBar affiche une plage de sélection uniquement. Les graduations situées aux positions de début et de fin d’une plage de sélection sont affichées sous forme de triangles (au lieu de tirets verticaux) et la plage de sélection est mise en surbrillance. <br/>                                                                                                                           |
| <span id="TBS_FIXEDLENGTH"></span><span id="tbs_fixedlength"></span><dl> <dt>**\_multiple tbs**</dt> </dl>                | Le contrôle TrackBar permet de modifier la taille du curseur avec le message [**TBM \_ SETTHUMBLENGTH**](tbm-setthumblength.md) . <br/>                                                                                                                                                                                                                      |
| <span id="TBS_NOTHUMB"></span><span id="tbs_nothumb"></span><dl> <dt>**TBS \_ NOthumb**</dt> </dl>                            | Le contrôle TrackBar n’affiche pas de curseur. <br/>                                                                                                                                                                                                                                                                                                           |
| <span id="TBS_TOOLTIPS"></span><span id="tbs_tooltips"></span><dl> <dt>**\_info-bulles tbs**</dt> </dl>                         | [Version 4,70](common-control-versions.md). Le contrôle TrackBar prend en charge les info-bulles. Lorsqu’un contrôle TrackBar est créé à l’aide de ce style, il crée automatiquement un contrôle ToolTip par défaut qui affiche la position actuelle du curseur. Vous pouvez modifier l’emplacement d’affichage des info-bulles à l’aide du message [**TBM \_ SETTIPSIDE**](tbm-settipside.md) . <br/> |
| <span id="TBS_REVERSED"></span><span id="tbs_reversed"></span><dl> <dt>**TBS \_ inversé**</dt> </dl>                         | [Version 5,80.](common-control-versions.md) Ce bit de style est utilisé pour le trackbars « inversé », où un nombre plus petit indique « supérieur » et un nombre plus élevé indique « inférieur ». Elle n’a aucun effet sur le contrôle. Il s’agit simplement d’une étiquette qui peut être vérifiée pour déterminer si un TrackBar est normal ou inversé.<br/>                                             |
| <span id="TBS_DOWNISLEFT"></span><span id="tbs_downisleft"></span><dl> <dt>**\_DOWNISLEFT tbs**</dt> </dl>                   | Par défaut, le contrôle TrackBar utilise la valeur inférieure à droite et la valeur supérieure à la gauche. Utilisez le \_ style tbs DOWNISLEFT pour inverser la valeur par défaut, en allant à gauche et à droite égal à droite. <br/>                                                                                                                                                                          |
| <span id="TBS_NOTIFYBEFOREMOVE"></span><span id="tbs_notifybeforemove"></span><dl> <dt>**\_NOTIFYBEFOREMOVE tbs**</dt> </dl> | [Version 6,00](common-control-versions.md) et **Windows Vista.** TrackBar doit notifier le parent avant de repositionner le curseur en raison d’une action de l’utilisateur (activation de l’alignement). <br/>                                                                                                                                                                                   |
| <span id="TBS_TRANSPARENTBKGND"></span><span id="tbs_transparentbkgnd"></span><dl> <dt>**\_TRANSPARENTBKGND tbs**</dt> </dl> | [Version 6,00](common-control-versions.md) et **Windows Vista.** L’arrière-plan est peint par le parent via le \_ message WM PRINTCLIENT. <br/>                                                                                                                                                                                                                   |



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|---------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>CommCtrl. h</dt> </dl> |



 

 





