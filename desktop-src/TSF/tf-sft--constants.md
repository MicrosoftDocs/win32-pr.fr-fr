---
title: Constantes TF_SFT_ (Ctfutb. h)
description: Les \_ \_ constantes TF SFT \ définissent les paramètres d’affichage d’une barre de langue flottante.
ms.assetid: 628e1d85-9614-4327-b89b-723f6eeb0718
topic_type:
- apiref
api_name:
- TF_SFT_SHOWNORMAL
- TF_SFT_DOCK
- TF_SFT_MINIMIZED
- TF_SFT_HIDDEN
- TF_SFT_NOTRANSPARENCY
- TF_SFT_LOWTRANSPARENCY
- TF_SFT_HIGHTRANSPARENCY
- TF_SFT_LABELS
- TF_SFT_NOLABELS
- TF_SFT_EXTRAICONSONMINIMIZED
- TF_SFT_NOEXTRAICONSONMINIMIZED
- TF_SFT_DESKBAND
api_location:
- Ctfutb.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 93a947960bfbe67585dc02a37de2da3dc6737540
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127416334"
---
# <a name="tf_sft_-constants"></a>\_ \_ \* Constantes TF SFT

Les constantes **tf \_ SFT \_ \*** spécifient les paramètres d’affichage d’une barre de langue flottante.



| Constante/valeur                                                                                                                                                                                                                                                                    | Description                                                                                                                                                                                                                                                                             |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TF_SFT_SHOWNORMAL"></span><span id="tf_sft_shownormal"></span><dl> <dt>**Tf \_ SFT \_ SHOWNORMAL**</dt> <dt>0x00000001</dt> </dl>                                        | Affichez la barre de langue sous forme de fenêtre flottante. Cette constante ne peut pas être combinée avec \_ l' \_ ancrage TF SFT, TF \_ SFT \_ réduit, TF \_ SFT \_ masqué ou les \_ \_ constantes DESKBAND TF SFT.<br/>                                                                                                 |
| <span id="TF_SFT_DOCK"></span><span id="tf_sft_dock"></span><dl> <dt>**Tf \_ \_Dock SFT**</dt> <dt>0x00000002</dt> </dl>                                                          | Ancrez la barre de langue dans son propre volet de tâches. Cette constante ne peut pas être combinée avec \_ les \_ constantes TF SFT SHOWNORMAL, TF \_ SFT \_ minimied, TF \_ SFT \_ Hidden ou TF \_ SFT \_ DESKBAND. disponible uniquement sur Windows XP.<br/>                                                                |
| <span id="TF_SFT_MINIMIZED"></span><span id="tf_sft_minimized"></span><dl> <dt>**Tf \_ SFT \_ réduit**</dt> <dt>0x00000004</dt> </dl>                                           | Affichez la barre de langue sous la forme d’une icône unique dans la barre d’état système. Cette constante ne peut pas être combinée avec \_ les \_ constantes TF SFT SHOWNORMAL, TF \_ SFT \_ Dock, TF \_ SFT \_ Hidden ou TF \_ SFT \_ DESKBAND. dans Windows XP, utilisez à \_ la \_ place TF SFT DESKBAND.<br/>                                   |
| <span id="TF_SFT_HIDDEN"></span><span id="tf_sft_hidden"></span><dl> <dt>**Tf \_ SFT \_ masqué**</dt> ( <dt>0x00000008</dt> ) </dl>                                                    | Masque la barre de langue. Cette constante ne peut pas être combinée avec \_ les \_ constantes TF SFT SHOWNORMAL, TF \_ SFT \_ Dock, TF \_ SFT \_ minimied ou TF \_ SFT \_ DESKBAND.<br/>                                                                                                                     |
| <span id="TF_SFT_NOTRANSPARENCY"></span><span id="tf_sft_notransparency"></span><dl> <dt>**Tf \_ SFT \_ notransparent**</dt> <dt>0x00000010</dt> </dl>                            | Rendez la barre de langue opaque.<br/>                                                                                                                                                                                                                                                |
| <span id="TF_SFT_LOWTRANSPARENCY"></span><span id="tf_sft_lowtransparency"></span><dl> <dt>**Tf \_ SFT \_ LOWTRANSPARENCY**</dt> <dt>0x00000020</dt> </dl>                         | Rendez la barre de langue partiellement transparente. disponible uniquement sur Windows 2000 ou version ultérieure.<br/>                                                                                                                                                                                        |
| <span id="TF_SFT_HIGHTRANSPARENCY"></span><span id="tf_sft_hightransparency"></span><dl> <dt>**Tf \_ SFT \_ HIGHTRANSPARENCY**</dt> <dt>0x00000040</dt> </dl>                      | Rendez la barre de langue très transparente. disponible uniquement sur Windows 2000 ou version ultérieure.<br/>                                                                                                                                                                                           |
| <span id="TF_SFT_LABELS"></span><span id="tf_sft_labels"></span><dl> <dt>**Tf \_ \_Étiquettes SFT**</dt> <dt>0x00000080</dt> </dl>                                                    | Afficher les étiquettes de texte en regard des icônes de la barre de langue.<br/>                                                                                                                                                                                                                              |
| <span id="TF_SFT_NOLABELS"></span><span id="tf_sft_nolabels"></span><dl> <dt>**Tf \_ 0x00000100 \_ NOlabels SFT**</dt> <dt></dt> </dl>                                              | Masquer les étiquettes de texte de l’icône de la barre de langue.<br/>                                                                                                                                                                                                                                          |
| <span id="TF_SFT_EXTRAICONSONMINIMIZED"></span><span id="tf_sft_extraiconsonminimized"></span><dl> <dt>**Tf \_ SFT \_ EXTRAICONSONMINIMIZED**</dt> <dt>0x00000200</dt> </dl>       | Affichez les icônes de service de texte sur la barre des tâches lorsque la barre de langue est réduite.<br/>                                                                                                                                                                                                |
| <span id="TF_SFT_NOEXTRAICONSONMINIMIZED"></span><span id="tf_sft_noextraiconsonminimized"></span><dl> <dt>**Tf \_ SFT \_ NOEXTRAICONSONMINIMIZED**</dt> <dt>0x00000400</dt> </dl> | Masquer les icônes de service de texte dans la barre des tâches lorsque la barre de langue est réduite.<br/>                                                                                                                                                                                                   |
| <span id="TF_SFT_DESKBAND"></span><span id="tf_sft_deskband"></span><dl> <dt>**Tf \_ SFT \_ DESKBAND**</dt> <dt>0x00000800</dt> </dl>                                              | Ancrez la barre de langue à l’extrémité droite de la barre des tâches système (immédiatement à gauche de la barre d’état système/horloge). Cette constante ne peut pas être combinée avec les constantes de SHOWNORMAL TF SFT, \_ \_ tf \_ SFT \_ Dock, TF \_ SFT \_ minimied ou TF \_ SFT \_ Hidden. disponible uniquement sur Windows XP.<br/> |



## <a name="remarks"></a>Notes

La méthode [ITfLangBarMgr :: ShowFloating](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbarmgr-showfloating) définit le résultat d’une opération **or** logique sur une ou plusieurs de ces constantes pour spécifier les attributs de l’élément de la barre de langue.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                            |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                  |
| Composant redistribuable<br/>          | TSF 1,0 sur Windows 2000 Professional<br/>                                       |
| En-tête<br/>                   | <dl> <dt>Ctfutb. h</dt> </dl>   |
| MIDL<br/>                      | <dl> <dt>Ctfutb. idl</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[ITfLangBarMgr::ShowFloating](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbarmgr-showfloating)
</dt> </dl>

 

 





