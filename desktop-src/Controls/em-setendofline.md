---
title: Message EM_SETENDOFLINE (CommCtrl. h)
description: Définit le caractère de fin de ligne utilisé lors de l’insertion d’un LineBreak.
ms.assetid: a10b3f57-0e67-4a0f-89f3-9c8ebd1514f8
keywords:
- EM_SETENDOFLINE les contrôles de Windows de message
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
ms.openlocfilehash: 5990b247757fc8e3cd39ab38edf5b88ca8ac62f74e402aac3899d51e3156231f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119437589"
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

## <a name="remarks"></a>Remarques

Lorsque le jeu de caractères de fin de ligne est **EC \_ ENDOFLINE \_ DETECTFROMCONTENT**, le contrôle d’édition détecte uniquement les caractères de fin de ligne pris en charge en fonction de son style de fenêtre étendu. consultez [modifier les styles étendus de contrôle](edit-control-window-extended-styles.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 10, 1809 \[ applications de bureau uniquement\]<br/>                                                           |
| Serveur minimal pris en charge<br/> | Windows Serveur 2019 \[ applications de bureau uniquement\]<br/>                                                     |
| En-tête<br/>                   | <dl> <dt>CommCtrl. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_GETENDOFLINE em*](em-getendofline.md)
</dt> </dl>

 

 





