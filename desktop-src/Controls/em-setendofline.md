---
title: Message EM_SETENDOFLINE (CommCtrl. h)
description: Définit le caractère de fin de ligne utilisé lors de l’insertion d’un LineBreak.
ms.assetid: a10b3f57-0e67-4a0f-89f3-9c8ebd1514f8
keywords:
- EM_SETENDOFLINE les contrôles de message Windows
topic_type:
- apiref
api_name:
- EM_SETENDOFLINE
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 10/19/2018
ms.openlocfilehash: 5ee7c500ba3818cad0f5ee74e9994ed8af049ea0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466543"
---
# <a name="em_setendofline-message"></a>\_Message SETENDOFLINE em

Définit le caractère de fin de ligne utilisé lors de l’insertion d’un LineBreak.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Spécifie le caractère de fin de ligne utilisé lors de l’insertion d’un LineBreak. Il peut s’agir de l’une des valeurs suivantes.


| Valeur                                                                                                                                                   | Signification                                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| <span id="EC_ENDOFLINE_DETECTFROMCONTENT"></span><span id="ec_endofline_detectfromcontent"></span><dl> <dt>**\_ENDOFLINE EC \_ DETECTFROMCONTENT**</dt> </dl> | Définit le caractère de fin de ligne utilisé pour le nouveau sauts sur le caractère utilisé par le document actif.<br/>  |
| <span id="EC_ENDOFLINE_CRLF"></span><span id="ec_endofline_crlf"></span><dl> <dt>**\_ENDOFLINE ce \_ CRLF**</dt> </dl>                                        | Définit le caractère de fin de ligne utilisé pour le nouveau sauts sur le retour chariot suivi du saut de ligne (CRLF).<br/> |
| <span id="EC_ENDOFLINE_CR"></span><span id="ec_endofline_cr"></span><dl> <dt>**\_ENDOFLINE ce \_ CR**</dt> </dl>                                              | Définit le caractère de fin de ligne utilisé pour le nouveau sauts sur le retour chariot (CR).<br/>                        |
| <span id="EC_ENDOFLINE_LF"></span><span id="ec_endofline_lf"></span><dl> <dt>**EC \_ ENDOFLINE \_ LF**</dt> </dl>                                              | Définit le caractère de fin de ligne utilisé pour le nouveau sauts de saut de ligne (LF).<br/>                               |

</dd> <dt>

*lParam* 
</dt> <dd>

Ce paramètre n'est pas utilisé.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si l’opération a échoué, la valeur de retour est différente de zéro.

Si l’opération échoue, la valeur de retour est zéro.

## <a name="remarks"></a>Notes

Lorsque le jeu de caractères de fin de ligne est **EC \_ ENDOFLINE \_ DETECTFROMCONTENT**, le contrôle d’édition détecte uniquement les caractères de fin de ligne pris en charge en fonction de son style de fenêtre étendu. consultez [modifier les styles étendus de contrôle](edit-control-window-extended-styles.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de bureau Windows 10, 1809 \[ uniquement\]<br/>                                                           |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2019 \[ uniquement\]<br/>                                                     |
| En-tête<br/>                   | <dl> <dt>CommCtrl. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_GETENDOFLINE em*](em-getendofline.md)
</dt> </dl>

 

 





