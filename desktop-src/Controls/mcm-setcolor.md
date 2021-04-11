---
title: Message MCM_SETCOLOR (commctrl. h)
description: Définit la couleur d’une partie donnée d’un contrôle calendrier du mois. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro calendrier monthcal setColor.
ms.assetid: 4ceb7b0e-82be-474a-a163-7e71356818c0
keywords:
- MCM_SETCOLOR les contrôles de message Windows
topic_type:
- apiref
api_name:
- MCM_SETCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 476aafd8356359cf6b4313f4b945253af6b493c8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105988"
---
# <a name="mcm_setcolor-message"></a>Message de la \_ SETCOLOR MCM

Définit la couleur d’une partie donnée d’un contrôle calendrier du mois. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**calendrier monthcal \_ setColor**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setcolor) .

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

Valeur [**COLORREF**](/windows/desktop/gdi/colorref) qui représente la couleur qui sera définie pour la zone spécifiée du calendrier du mois.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne une valeur [**COLORREF**](/windows/desktop/gdi/colorref) qui représente le paramètre de couleur précédent pour la partie spécifiée du contrôle Month Calendar en cas de réussite. Sinon, le retour est-1.

## <a name="remarks"></a>Notes

Si les styles visuels sont actifs, ce message n’a aucun effet, sauf lorsque *wParam* est l' \_ arrière-plan MCSC.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

