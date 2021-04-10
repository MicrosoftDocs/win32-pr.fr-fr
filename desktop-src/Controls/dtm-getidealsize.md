---
title: Message DTM_GETIDEALSIZE (commctrl. h)
description: Obtient la taille nécessaire pour afficher le contrôle sans découpage. Envoyez ce message explicitement ou à l’aide de la \_ macro DateTime GetIdealSize.
ms.assetid: 15ec26a1-645b-4a96-af66-1031e1a46c6c
keywords:
- DTM_GETIDEALSIZE les contrôles de message Windows
topic_type:
- apiref
api_name:
- DTM_GETIDEALSIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a979883f431fea4627f52fe19c3716341e3f2328
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104200546"
---
# <a name="dtm_getidealsize-message"></a>\_Message DTM GETIDEALSIZE

Obtient la taille nécessaire pour afficher le contrôle sans découpage. Envoyez ce message explicitement ou à l’aide de la macro [**DateTime \_ GetIdealSize**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_getidealsize) .

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Non utilisé. Doit être zéro.

</dd> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure de [**taille**](/previous-versions//dd145106(v=vs.85)) pour recevoir la taille idéale. L’application appelante est chargée d’allouer cette structure.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne la **valeur true**.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

