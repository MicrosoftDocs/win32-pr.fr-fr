---
title: Constantes TF_LBMENUF_ (Ctfutb. h)
description: Les \_ \_ constantes TF LBMENUF \ sont utilisées dans la méthode ITfMenu AddMenuItem pour spécifier les caractéristiques d’un élément de menu dans la barre de langue.
ms.assetid: f8f3f397-b84e-4635-b454-31369c679ce2
topic_type:
- apiref
api_name:
- TF_LBMENUF_CHECKED
- TF_LBMENUF_SUBMENU
- TF_LBMENUF_SEPARATOR
- TF_LBMENUF_RADIOCHECKED
- TF_LBMENUF_GRAYED
api_location:
- Ctfutb.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a1a056e9a758419965341b4d508db083fc8f31b4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942082"
---
# <a name="tf_lbmenuf_-constants"></a>TF \_ LBMENUF, \_ \* constantes

Les constantes **tf \_ LBMENUF \_ \** _ sont utilisées dans la méthode [ITfMenu :: AddMenuItem](/windows/desktop/api/Ctfutb/nf-ctfutb-itfmenu-addmenuitem) pour spécifier les caractéristiques d’un élément de menu dans la barre de langue.



| Constante/valeur                                                                                                                                                                                                                                         | Description                                     |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------|
| <span id="TF_LBMENUF_CHECKED"></span><span id="tf_lbmenuf_checked"></span><dl> <dt>_ * TF \_ LBMENUF \_ activé * *</dt> <dt>0x01</dt> </dl>                | L’élément de menu est activé.<br/>            |
| <span id="TF_LBMENUF_SUBMENU"></span><span id="tf_lbmenuf_submenu"></span><dl> <dt>**Tf \_ \_Sous-menu LBMENUF**</dt> <dt>0x02</dt> </dl>                | L’élément de menu est un sous-menu.<br/>          |
| <span id="TF_LBMENUF_SEPARATOR"></span><span id="tf_lbmenuf_separator"></span><dl> <dt>**Tf \_ LBMENUF \_ separator**</dt> <dt>0x04</dt> </dl>          | L’élément de menu est un séparateur.<br/>        |
| <span id="TF_LBMENUF_RADIOCHECKED"></span><span id="tf_lbmenuf_radiochecked"></span><dl> <dt>**Tf \_ LBMENUF de \_ radiovérification**</dt> <dt>0x08</dt> </dl> | L’élément de menu est une coche radio.<br/> |
| <span id="TF_LBMENUF_GRAYED"></span><span id="tf_lbmenuf_grayed"></span><dl> <dt>**Tf \_ LBMENUF en \_ grisé**</dt> <dt></dt> </dl>                   | L’élément de menu est désactivé.<br/>           |



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

[ITfMenu::AddMenuItem](/windows/desktop/api/Ctfutb/nf-ctfutb-itfmenu-addmenuitem)
</dt> </dl>

 

 





