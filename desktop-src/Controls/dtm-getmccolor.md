---
title: Message DTM_GETMCCOLOR (commctrl. h)
description: Obtient la couleur d’une partie donnée du calendrier du mois dans un contrôle de sélecteur de dates et d’heures (PAO). Vous pouvez envoyer ce message de manière explicite ou utiliser la \_ macro DateTime GetMonthCalColor.
ms.assetid: 892e8c23-f0d0-4fd6-98ed-39592c4d316f
keywords:
- DTM_GETMCCOLOR les contrôles de Windows de message
topic_type:
- apiref
api_name:
- DTM_GETMCCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a99a67f6ca7056f0157d131d185cb5cb68a85e06b8cbb124a16b3c2129c21963
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119878149"
---
# <a name="dtm_getmccolor-message"></a>\_Message DTM GETMCCOLOR

Obtient la couleur d’une partie donnée du calendrier du mois dans un contrôle de sélecteur de dates et d’heures (PAO). Vous pouvez envoyer ce message de manière explicite ou utiliser la macro [**DateTime \_ GetMonthCalColor**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_getmonthcalcolor) .

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Valeur de type **int** spécifiant la couleur du calendrier mensuel à récupérer. Cette valeur peut être l'une des suivantes :



| Valeur                                                                                                                                                                     | Signification                                                                                                                                                                                                 |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="MCSC_BACKGROUND"></span><span id="mcsc_background"></span><dl> <dt>**\_arrière-plan MCSC**</dt> </dl>       | Récupérez la couleur d’arrière-plan affichée entre les mois.<br/>                                                                                                                                      |
| <span id="MCSC_MONTHBK"></span><span id="mcsc_monthbk"></span><dl> <dt>**MCSC \_ MONTHBK**</dt> </dl>                | Récupérez la couleur d’arrière-plan affichée dans le mois.<br/>                                                                                                                                    |
| <span id="MCSC_TEXT"></span><span id="mcsc_text"></span><dl> <dt>**\_texte MCSC**</dt> </dl>                         | Récupérez la couleur utilisée pour afficher le texte dans un mois.<br/>                                                                                                                                      |
| <span id="MCSC_TITLEBK"></span><span id="mcsc_titlebk"></span><dl> <dt>**MCSC \_ TITLEBK**</dt> </dl>                | Récupérez la couleur d’arrière-plan affichée dans le titre du calendrier.<br/>                                                                                                                             |
| <span id="MCSC_TITLETEXT"></span><span id="mcsc_titletext"></span><dl> <dt>**MCSC, \_ TITLETEXT**</dt> </dl>          | Récupérez la couleur utilisée pour afficher le texte dans le titre du calendrier.<br/>                                                                                                                         |
| <span id="MCSC_TRAILINGTEXT"></span><span id="mcsc_trailingtext"></span><dl> <dt>**MCSC \_ TRAILINGTEXT**</dt> </dl> | Récupère la couleur utilisée pour afficher le texte du jour de l’en-tête et du jour de fin. Les jours d’en-tête et de fin sont les jours des mois précédents et suivants qui apparaissent dans le calendrier du mois en cours.<br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>Doit être zéro.</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne une valeur **COLORREF** qui représente le paramètre de couleur pour la partie spécifiée du contrôle Month Calendar en cas de réussite. Le message retourne-1 en cas d’échec.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





