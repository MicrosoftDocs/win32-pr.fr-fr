---
description: Représente les options disponibles lors de l’affichage d’un menu contextuel.
title: Constantes MP_POPUPFLAGS (ShObjIdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: cc1d9ff0-a03b-4bd3-b481-9b78d20eb771
api_name:
- MPPF_SETFOCUS
- MPPF_INITIALSELECT
- MPPF_NOANIMATE
- MPPF_KEYBOARD
- MPPF_REPOSITION
- MPPF_FORCEZORDER
- MPPF_FINALSELECT
- MPPF_ALIGN_LEFT
- MPPF_ALIGN_RIGHT
- MPPF_TOP
- MPPF_LEFT
- MPPF_RIGHT
- MPPF_BOTTOM
- MPPF_POS_MASK
api_type:
- HeaderDef
api_location:
- Shobjidl.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: a1f6211769eca021f76fcbef34625f705cd3bf3fed02ca548d2965f17de80af7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119710009"
---
# <a name="mp_popupflags-constants"></a>\_Constantes POPUPFLAGS MP

Représente les options disponibles lors de l’affichage d’un menu contextuel.



| Constante/valeur                                                                                                                                                                                                                               | Description                                                                                                                                                                                                                                                              |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="MPPF_SETFOCUS"></span><span id="mppf_setfocus"></span><dl> <dt>**MPPF \_ SETFOCUS**</dt> <dt>0x00000001</dt> </dl>                | Donnez le focus au menu contextuel.<br/>                                                                                                                                                                                                                               |
| <span id="MPPF_INITIALSELECT"></span><span id="mppf_initialselect"></span><dl> <dt>**MPPF \_ INITIALSELECT**</dt> <dt>0x00000002</dt> </dl> | Sélectionnez le premier élément dans le menu contextuel.<br/>                                                                                                                                                                                                                     |
| <span id="MPPF_NOANIMATE"></span><span id="mppf_noanimate"></span><dl> <dt>**MPPF \_ Noanimate**</dt> <dt>0x00000004</dt> </dl>             | N’utilisez pas les animations système par défaut, par exemple en fondu, lors de l’affichage du menu.<br/>                                                                                                                                                                     |
| <span id="MPPF_KEYBOARD"></span><span id="mppf_keyboard"></span><dl> <dt>**MPPF \_ CLAVIER**</dt> <dt>0x00000010</dt> </dl>                | Activez le menu à l’aide d’un raccourci clavier.<br/>                                                                                                                                                                                                                     |
| <span id="MPPF_REPOSITION"></span><span id="mppf_reposition"></span><dl> <dt>**MPPF \_ Repositionner**</dt> <dt>0x00000020</dt> </dl>          | Affichez la barre à une autre position, en fonction des modifications apportées au menu.<br/>                                                                                                                                                                                        |
| <span id="MPPF_FORCEZORDER"></span><span id="mppf_forcezorder"></span><dl> <dt>**MPPF \_ FORCEZORDER**</dt> <dt>0x00000040</dt> </dl>       | Réservé. Ne pas utiliser.<br/>                                                                                                                                                                                                                                         |
| <span id="MPPF_FINALSELECT"></span><span id="mppf_finalselect"></span><dl> <dt>**MPPF \_ FINALSELECT**</dt> <dt>0x00000080</dt> </dl>       | Sélectionnez le dernier élément dans le menu.<br/>                                                                                                                                                                                                                             |
| <span id="MPPF_ALIGN_LEFT"></span><span id="mppf_align_left"></span><dl> <dt>**MPPF \_ Aligner à \_ gauche**</dt> <dt>0x02000000</dt> </dl>         | **Windows Vista ou version ultérieure**: alignez le menu contextuel à gauche de la zone spécifiée dans le paramètre *prcExclude* de [**ITrackShellMenu ::P opup**](/windows/desktop/api/Shdeprecated/nf-shdeprecated-itrackshellmenu-popup) ou [**IMenuPopup ::P opup**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-imenupopup-popup). Il s’agit de l’alignement par défaut.<br/> |
| <span id="MPPF_ALIGN_RIGHT"></span><span id="mppf_align_right"></span><dl> <dt>**MPPF \_ Aligner à \_ droite**</dt> <dt>0x04000000</dt> </dl>      | **Windows Vista ou version ultérieure**: alignez le menu contextuel à droite de la zone spécifiée dans le paramètre *prcExclude* de [**ITrackShellMenu ::P opup**](/windows/desktop/api/Shdeprecated/nf-shdeprecated-itrackshellmenu-popup) ou [**IMenuPopup ::P opup**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-imenupopup-popup).<br/>                               |
| <span id="MPPF_TOP"></span><span id="mppf_top"></span><dl> <dt>**MPPF \_ TOP**</dt> <dt>0x20000000</dt> </dl>                               | Placez le menu contextuel au-dessus du point initial spécifié dans le paramètre *PPT* de [**ITrackShellMenu ::P opup**](/windows/desktop/api/Shdeprecated/nf-shdeprecated-itrackshellmenu-popup) ou [**IMenuPopup ::P opup**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-imenupopup-popup).<br/>                                                                |
| <span id="MPPF_LEFT"></span><span id="mppf_left"></span><dl> <dt>**MPPF \_**</dt> <dt>0x40000000</dt> gauche </dl>                            | Placez le menu contextuel à gauche du point initial.<br/>                                                                                                                                                                                                    |
| <span id="MPPF_RIGHT"></span><span id="mppf_right"></span><dl> <dt>**MPPF \_**</dt> <dt>0x60000000</dt> droit </dl>                         | Placez le menu contextuel à droite du point initial.<br/>                                                                                                                                                                                                   |
| <span id="MPPF_BOTTOM"></span><span id="mppf_bottom"></span><dl> <dt>**MPPF \_ BOTTOM**</dt> <dt>(int) 0x80000000</dt> </dl>                 | Placez le menu contextuel sous le point initial.<br/>                                                                                                                                                                                                             |
| <span id="MPPF_POS_MASK"></span><span id="mppf_pos_mask"></span><dl> <dt>**MPPF \_ 0xE0000000 \_ masque de PDV**</dt> <dt>(int)</dt> </dl>          | Masque de position de menu.<br/>                                                                                                                                                                                                                                       |



## <a name="remarks"></a>Remarques

ces constantes sont définies dans le fichier Shobjidl. h à partir de Windows XP Service Pack 1 (SP1) et Windows Server 2003

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows XP avec les \[ applications de bureau SP1 uniquement\]<br/>                                    |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                    |
| En-tête<br/>                   | <dl> <dt>ShObjIdl. h</dt> </dl>   |
| MIDL<br/>                      | <dl> <dt>ShObjIdl. idl</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IMenuPopup ::P opup**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-imenupopup-popup)
</dt> <dt>

[**ITrackShellMenu ::P opup**](/windows/desktop/api/Shdeprecated/nf-shdeprecated-itrackshellmenu-popup)
</dt> </dl>

 

 




