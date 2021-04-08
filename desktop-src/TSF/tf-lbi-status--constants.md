---
title: Constantes TF_LBI_STATUS_ (Ctfutb. h)
description: Les \_ \_ constantes TF IFA status \_ indiquent l’état d’un élément de barre de langue. Ces valeurs sont utilisées avec la méthode GetStatus ITfLangBarItem.
ms.assetid: 5f2c0e61-f7e5-4dcc-86a3-7bd1c994b8bc
topic_type:
- apiref
api_name:
- TF_LBI_STATUS_HIDDEN
- TF_LBI_STATUS_DISABLED
- TF_LBI_STATUS_BTN_TOGGLED
api_location:
- Ctfutb.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7de9dcf0272eaf79fd001461aa555d78c9d6ae30
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742924"
---
# <a name="tf_lbi_status_-constants"></a>\_ \_ Constantes d’état de l’État IFA TF \_ \*

Les constantes **tf \_ IFA \_ Status \_ \** _ indiquent l’état d’un élément de barre de langue. Ces valeurs sont utilisées avec la méthode [ITfLangBarItem :: GetStatus](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritem-getstatus) .



| Constante/valeur                                                                                                                                                                                                                                                       | Description                                                                                                                                       |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TF_LBI_STATUS_HIDDEN"></span><span id="tf_lbi_status_hidden"></span><dl> <dt>_ * TF \_ \_État IFA \_ masqué * *</dt> <dt>0x00000001</dt> </dl>                 | L’élément est masqué. Ce style est ignoré si l’élément n’inclut pas le \_ \_ style HIDDENSTATUSCONTROL TF IFA style \_ .<br/>                  |
| <span id="TF_LBI_STATUS_DISABLED"></span><span id="tf_lbi_status_disabled"></span><dl> <dt>**Tf \_ \_État IFA \_ désactivé**</dt> <dt>0x00000002</dt> </dl>           | L’élément est désactivé.<br/>                                                                                                                  |
| <span id="TF_LBI_STATUS_BTN_TOGGLED"></span><span id="tf_lbi_status_btn_toggled"></span><dl> <dt>**Tf \_ \_État IFA \_ 0x00010000 \_ bascule**</dt> <dt></dt> </dl> | L’élément est à l’état activé ou désactivé. Ce style est ignoré si l’élément n’inclut pas le \_ style de \_ \_ basculement de style d’un type d’élément à la ligne TF IFA \_ .<br/> |



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

[ITfLangBarItem :: GetStatus](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritem-getstatus)
</dt> </dl>

 

 





