---
title: Constantes diverses de la barre de langage (Ctfutb. h)
description: Les constantes diverses de la barre de langage définissent certaines propriétés des barres de langue.
ms.assetid: c1740636-7ba3-4748-9005-ee94d04dbb15
topic_type:
- apiref
api_name:
- TF_DTLBI_USEPROFILEICON
- TF_INVALIDMENUITEM
- TF_LBI_BMPF_VERTICAL
- TF_LBI_DESC_MAXLEN
api_location:
- Ctfutb.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 91fd1a371581dea02226ba6539ca25a06ef98e75
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104385111"
---
# <a name="miscellaneous-language-bar-constants"></a>Constantes diverses de la barre de langage

Les constantes diverses de la barre de langage définissent certaines propriétés des barres de langue.



| Constante/valeur                                                                                                                                                                                                                                               | Description                                                                                                                                                                                                                                                                                                              |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TF_DTLBI_USEPROFILEICON"></span><span id="tf_dtlbi_useprofileicon"></span><dl> <dt>**Tf \_ DTLBI \_ USEPROFILEICON**</dt> <dt>0x00000001</dt> </dl> | L’élément de la barre de langue système doit afficher l’icône spécifiée pour le profil de langue. Utilisé dans les méthodes [ITfSystemDeviceTypeLangBarItem :: GetIconMode](/windows/desktop/api/Ctfutb/nf-ctfutb-itfsystemdevicetypelangbaritem-geticonmode) et [ITfSystemDeviceTypeLangBarItem :: SetIconMode](/windows/desktop/api/Ctfutb/nf-ctfutb-itfsystemdevicetypelangbaritem-seticonmode) .<br/> |
| <span id="TF_INVALIDMENUITEM"></span><span id="tf_invalidmenuitem"></span><dl> <dt>**Tf \_ INVALIDMENUITEM**</dt> <dt>(uint) (-1)</dt> </dl>                 | Non utilisé.<br/>                                                                                                                                                                                                                                                                                                     |
| <span id="TF_LBI_BMPF_VERTICAL"></span><span id="tf_lbi_bmpf_vertical"></span><dl> <dt>**Tf \_ IFA \_ BMPF \_ vertical**</dt> <dt>0x00000001</dt> </dl>         | Non utilisé.<br/>                                                                                                                                                                                                                                                                                                     |
| <span id="TF_LBI_DESC_MAXLEN"></span><span id="tf_lbi_desc_maxlen"></span><dl> <dt>**Tf \_ IFA \_ desc \_ MaxLen**</dt> <dt>32</dt> </dl>                       | Longueur, en caractères WCHAR, du membre de structure [tf \_ LANGBARITEMINFO. szDescription](/windows/desktop/api/Ctfutb/ns-ctfutb-tf_langbariteminfo).<br/>                                                                                                                                                                                                 |



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

[ITfSystemDeviceTypeLangBarItem::GetIconMode](/windows/desktop/api/Ctfutb/nf-ctfutb-itfsystemdevicetypelangbaritem-geticonmode)
</dt> <dt>

[ITfSystemDeviceTypeLangBarItem::SetIconMode](/windows/desktop/api/Ctfutb/nf-ctfutb-itfsystemdevicetypelangbaritem-seticonmode)
</dt> <dt>

[TF \_ LANGBARITEMINFO](/windows/desktop/api/Ctfutb/ns-ctfutb-tf_langbariteminfo)
</dt> </dl>

 

 





