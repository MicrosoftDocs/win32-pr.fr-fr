---
title: Message DTM_SETMCCOLOR (commctrl. h)
description: Définit la couleur d’une partie donnée du calendrier du mois dans un contrôle de sélecteur de dates et d’heures (PAO). Vous pouvez envoyer ce message de manière explicite ou utiliser la \_ macro DateTime SetMonthCalColor.
ms.assetid: cee72c1d-58da-4ee5-850e-a615ec6ad079
keywords:
- DTM_SETMCCOLOR les contrôles de Windows de message
topic_type:
- apiref
api_name:
- DTM_SETMCCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2e496abb4dd28b040dd4a8035073ffa32a3f3847
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127121970"
---
# <a name="dtm_setmccolor-message"></a>\_Message DTM SETMCCOLOR

Définit la couleur d’une partie donnée du calendrier du mois dans un contrôle de sélecteur de dates et d’heures (PAO). Vous pouvez envoyer ce message de manière explicite ou utiliser la macro [**DateTime \_ SetMonthCalColor**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_setmonthcalcolor) .

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Valeur de type **int** spécifiant la couleur du calendrier mensuel à définir. Cette valeur peut être l'une des suivantes :



| Valeur                                                                                                                                                                     | Signification                                                                                                                                                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="MCSC_BACKGROUND"></span><span id="mcsc_background"></span><dl> <dt>**\_arrière-plan MCSC**</dt> </dl>       | Définissez la couleur d’arrière-plan affichée entre les mois.<br/>                                                                                                                                      |
| <span id="MCSC_MONTHBK"></span><span id="mcsc_monthbk"></span><dl> <dt>**MCSC \_ MONTHBK**</dt> </dl>                | Définissez la couleur d’arrière-plan affichée dans le mois.<br/>                                                                                                                                    |
| <span id="MCSC_TEXT"></span><span id="mcsc_text"></span><dl> <dt>**\_texte MCSC**</dt> </dl>                         | Définissez la couleur utilisée pour afficher le texte dans un mois.<br/>                                                                                                                                      |
| <span id="MCSC_TITLEBK"></span><span id="mcsc_titlebk"></span><dl> <dt>**MCSC \_ TITLEBK**</dt> </dl>                | Définissez la couleur d’arrière-plan affichée dans le titre du calendrier.<br/>                                                                                                                             |
| <span id="MCSC_TITLETEXT"></span><span id="mcsc_titletext"></span><dl> <dt>**MCSC, \_ TITLETEXT**</dt> </dl>          | Définissez la couleur utilisée pour afficher le texte dans le titre du calendrier.<br/>                                                                                                                         |
| <span id="MCSC_TRAILINGTEXT"></span><span id="mcsc_trailingtext"></span><dl> <dt>**MCSC \_ TRAILINGTEXT**</dt> </dl> | Définissez la couleur utilisée pour afficher le texte du jour de l’en-tête et du jour de fin. Les jours d’en-tête et de fin sont les jours des mois précédents et suivants qui apparaissent dans le calendrier du mois en cours.<br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Valeur **COLORREF** représentant la couleur qui sera définie pour la zone spécifiée du calendrier du mois.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Retourne une valeur **COLORREF** qui représente le paramètre de couleur précédent pour la partie spécifiée du contrôle Month Calendar en cas de réussite. Dans le cas contraire, le message retourne-1.

## <a name="remarks"></a>Notes

Lorsque les styles visuels sont activés, ce message n’a aucun effet, sauf lorsque *wParam* est l' \_ arrière-plan MCSC.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





