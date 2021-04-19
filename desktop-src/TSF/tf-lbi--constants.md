---
title: Constantes TF_LBI_ (Ctfutb. h)
description: Les \_ \_ constantes IFA IFA \ sont utilisées avec la méthode ITfLangBarItemSink OnUpdate pour indiquer les éléments de barre de langue qui ont été modifiés.
ms.assetid: ed84012f-19ba-43b3-bbb5-7373ed174c33
topic_type:
- apiref
api_name:
- TF_LBI_ICON
- TF_LBI_TEXT
- TF_LBI_TOOLTIP
- TF_LBI_BITMAP
- TF_LBI_BALLOON
- TF_LBI_STATUS
- TF_LBI_BMPALL
- TF_LBI_BMPBTNALL
- TF_LBI_BTNALL
api_location:
- Ctfutb.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d72b69f1cb5a5b4a24e78a2bdc1ca0e7a9d79cbf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106511354"
---
# <a name="tf_lbi_-constants"></a>\_Constantes de TF IFA \_ \*

Les constantes **tf \_ IFA \_ \** _ sont utilisées avec la méthode [ITfLangBarItemSink :: OnUpdate](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritemsink-onupdate) pour indiquer les éléments de barre de langue qui ont été modifiés.



| Constante/valeur                                                                                                                                                                                                                                                                  | Description                                                                                                                                                                                                                                                                                                         |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TF_LBI_ICON"></span><span id="tf_lbi_icon"></span><dl> <dt>_ * TF \_ \_Icône IFA * *</dt> <dt>0x00000001</dt> </dl>                                                        | L’icône de l’élément a été modifiée. La barre de langage appelle [ITfLangBarItemButton :: GetIcon](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritembutton-geticon) en réponse à cette notification.<br/>                                                                                                                                             |
| <span id="TF_LBI_TEXT"></span><span id="tf_lbi_text"></span><dl> <dt>**Tf \_ \_Texte IFA**</dt> <dt>0x00000002</dt> </dl>                                                        | Le texte d’un bouton ou d’un élément de bouton bitmap a changé. La barre de langage appelle [ITfLangBarItemButton :: gettext](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritembutton-gettext) ou [ITfLangBarItemBitmapButton :: gettext](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritembitmapbutton-gettext), selon ce qui est approprié, en réponse à cette notification.<br/>           |
| <span id="TF_LBI_TOOLTIP"></span><span id="tf_lbi_tooltip"></span><dl> <dt>**Tf \_ \_INFOBULLE IFA**</dt> <dt>0x00000004</dt> </dl>                                               | Texte d’info-bulle de l’élément modifié. La barre de langage appelle [ITfLangBarItem :: GetTooltipString](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritem-gettooltipstring) en réponse à cette notification.<br/>                                                                                                                                   |
| <span id="TF_LBI_BITMAP"></span><span id="tf_lbi_bitmap"></span><dl> <dt>**Tf \_ IFA \_ bitmap IFA**</dt> <dt></dt> </dl>                                                  | Bitmap d’un élément de bouton bitmap ou bitmap modifié. La barre de langage appelle [ITfLangBarItemBitmap ::D rawbitmap](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritembitmap-drawbitmap) ou [ITfLangBarItemBitmapButton ::D rawbitmap](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritembitmapbutton-drawbitmap), selon ce qui est approprié, en réponse à cette notification.<br/> |
| <span id="TF_LBI_BALLOON"></span><span id="tf_lbi_balloon"></span><dl> <dt>**Tf \_ \_Bulle IFA**</dt> <dt>0x00000010</dt> </dl>                                               | Les informations relatives à un élément Balloon ont été modifiées. La barre de langage appelle [ITfLangBarItemBalloon :: GetBalloonInfo](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritemballoon-getballooninfo) en réponse à cette notification.<br/>                                                                                                                   |
| <span id="TF_LBI_STATUS"></span><span id="tf_lbi_status"></span><dl> <dt>**Tf \_ 0x00010000 \_ État IFA**</dt> <dt></dt> </dl>                                                  | État de l’élément modifié. La barre de langage appelle [ITfLangBarItem :: GetStatus](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritem-getstatus) en réponse à cette notification.<br/>                                                                                                                                                              |
| <span id="TF_LBI_BMPALL"></span><span id="tf_lbi_bmpall"></span><dl> <dt>**Tf \_ icône IFA \_ BMPALL**</dt> <dt>tf \_ IFA \_ bitmap \| tf \_ IFA \_</dt> </dl>                          | Combine une \_ \_ image bitmap TF IFA et une \_ \_ info-bulle TF IFA.<br/>                                                                                                                                                                                                                                                           |
| <span id="TF_LBI_BMPBTNALL"></span><span id="tf_lbi_bmpbtnall"></span><dl> <dt>**Tf \_ IFA \_ BMPBTNALL**</dt> <dt>tf \_ IFA \_ bitmap \| tf \_ IFA \_ texte \| tf \_ IFA \_ info-bulle</dt> </dl> | Combine l' \_ \_ image bitmap TF IFA, le \_ texte TF IFA et l' \_ \_ \_ info-bulle TF IFA.<br/>                                                                                                                                                                                                                                            |
| <span id="TF_LBI_BTNALL"></span><span id="tf_lbi_btnall"></span><dl> <dt>**Tf \_ icône IFA \_ BTNALL**</dt> <dt>tf \_ IFA \_ \| tf \_ IFA \_ texte \| tf \_ IFA \_ info-bulle</dt> </dl>            | Combine l' \_ icône TF IFA \_ , le \_ texte TF IFA et l' \_ \_ \_ info-bulle TF IFA.<br/>                                                                                                                                                                                                                                              |



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                            |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                  |
| Composant redistribuable<br/>          | TSF 1,0 sur Windows 2000 professionnel<br/>                                       |
| En-tête<br/>                   | <dl> <dt>Ctfutb. h</dt> </dl>   |
| MIDL<br/>                      | <dl> <dt>Ctfutb. idl</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[ITfLangBarItemSink :: OnUpdate](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritemsink-onupdate)
</dt> </dl>

 

 





