---
title: Message EM_GETENDOFLINE (commctrl. h)
description: Récupère le caractère de fin de ligne utilisé lors de l’insertion d’un LineBreak. Envoyez ce message explicitement ou à l’aide de la \_ macro Edit GetEndOfLine.
ms.assetid: 557f796e-c9d1-4ea1-b8a6-44ae0bed5ffc
keywords:
- EM_GETENDOFLINE les contrôles de Windows de message
topic_type:
- apiref
api_name:
- EM_GETENDOFLINE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 10/19/2018
ms.openlocfilehash: 64ddb55ce592b71c7abaa8c35b1bf14a004b324586094f27a3b418a67e5b24e9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119019687"
---
# <a name="em_getendofline-message"></a>\_Message GETENDOFLINE em

Récupère le caractère de fin de ligne d’un contrôle d’édition. Envoyez ce message explicitement ou à l’aide de la macro [**Edit \_ GetEndOfLine**](/windows/desktop/api/Commctrl/nf-commctrl-edit_getendofline) .

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>Doit être zéro.</dd> <dt>

*lParam* 
</dt> <dd>Doit être zéro.</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne le caractère de fin de ligne utilisé par le contrôle d’édition. Il peut s’agir de l’une des valeurs suivantes.

| Valeur                                                                                                                                                   | Signification                                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| <span id="EC_ENDOFLINE_CRLF"></span><span id="ec_endofline_crlf"></span><dl> <dt>**\_ENDOFLINE ce \_ CRLF**</dt> </dl> | Le caractère de fin de ligne utilisé pour le nouveau sauts est le retour chariot suivi du saut de ligne (CRLF).<br/> |
| <span id="EC_ENDOFLINE_CR"></span><span id="ec_endofline_cr"></span><dl> <dt>**\_ENDOFLINE ce \_ CR**</dt> </dl>       | Le caractère de fin de ligne utilisé pour le nouveau sauts est le retour chariot (CR).<br/>                        |
| <span id="EC_ENDOFLINE_LF"></span><span id="ec_endofline_lf"></span><dl> <dt>**EC \_ ENDOFLINE \_ LF**</dt> </dl>       | Le caractère de fin de ligne utilisé pour le nouveau sauts est un saut de ligne (LF).<br/>                               |

## <a name="remarks"></a>Remarques

Lorsque le caractère de fin de ligne utilisé est défini sur **EC \_ ENDOFLINE \_ DETECTFROMCONTENT** à l’aide de [**Edit \_ SetEndOfLine**](/windows/desktop/api/Commctrl/nf-commctrl-edit_setendofline), ce message retourne le caractère de fin de ligne détecté.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 10, version 1809 \[ applications de bureau uniquement\]<br/>                             |
| Serveur minimal pris en charge<br/> | Windows Serveur 2019 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_SETENDOFLINE em*](em-setendofline.md)
</dt> </dl>
 

 





