---
title: Constantes TF_MOD_ (msctf. h)
description: Les \_ \_ constantes TF mod \ spécifient des modificateurs de clé dans la \_ structure PRESERVEDKEY TF.
ms.assetid: 4642ef17-34bd-4482-a9e9-0fbed7b574b1
topic_type:
- apiref
api_name:
- TF_MOD_ALT
- TF_MOD_CONTROL
- TF_MOD_SHIFT
- TF_MOD_RALT
- TF_MOD_RCONTROL
- TF_MOD_RSHIFT
- TF_MOD_LALT
- TF_MOD_LCONTROL
- TF_MOD_LSHIFT
- TF_MOD_ON_KEYUP
- TF_MOD_IGNORE_ALL_MODIFIER
api_location:
- Msctf.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e67e081d9a0f8714410861c7c36f9f751bad8d2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032821"
---
# <a name="tf_mod_-constants"></a>\_ \_ \* CONSTANTEs mod TF

Les \_ \_ \* constantes TF mod spécifient des modificateurs de clé dans la structure [ \_ PRESERVEDKEY TF](/windows/desktop/api/Msctf/ns-msctf-tf_preservedkey) .



| Constante/valeur                                                                                                                                                                                                                                                      | Description                                                                                                                                                                          |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TF_MOD_ALT"></span><span id="tf_mod_alt"></span><dl> <dt>**Tf \_ MOD \_ ALT**</dt> <dt>0x0001</dt> </dl>                                                   | L’une des touches ALT est enfoncée<br/>                                                                                                                                         |
| <span id="TF_MOD_CONTROL"></span><span id="tf_mod_control"></span><dl> <dt>**Tf \_ 0x0002 \_ contrôle Mod**</dt> <dt></dt> </dl>                                       | L’une des touches CTRL est enfoncée<br/>                                                                                                                                        |
| <span id="TF_MOD_SHIFT"></span><span id="tf_mod_shift"></span><dl> <dt>**Tf \_ MOD \_ Shift**</dt> <dt>0x0004</dt> </dl>                                             | L’une des touches MAJ est enfoncée<br/>                                                                                                                                       |
| <span id="TF_MOD_RALT"></span><span id="tf_mod_ralt"></span><dl> <dt>**Tf \_ MOD \_ Ralt**</dt> <dt>0x0008</dt> </dl>                                                | La touche ALT de droite est enfoncée<br/>                                                                                                                                              |
| <span id="TF_MOD_RCONTROL"></span><span id="tf_mod_rcontrol"></span><dl> <dt>**Tf \_ MOD \_ RCONTROL**</dt> <dt>0x0010</dt> </dl>                                    | La touche CTRL de droite est enfoncée<br/>                                                                                                                                             |
| <span id="TF_MOD_RSHIFT"></span><span id="tf_mod_rshift"></span><dl> <dt>**Tf \_ MOD \_ RSHIFT**</dt> <dt>0x0020</dt> </dl>                                          | La touche Maj droite est enfoncée<br/>                                                                                                                                            |
| <span id="TF_MOD_LALT"></span><span id="tf_mod_lalt"></span><dl> <dt>**Tf \_ MOD \_ LALT**</dt> <dt>0x0040</dt> </dl>                                                | La touche ALT de gauche est enfoncée<br/>                                                                                                                                               |
| <span id="TF_MOD_LCONTROL"></span><span id="tf_mod_lcontrol"></span><dl> <dt>**Tf \_ MOD \_ LCONTROL**</dt> <dt>0x0080</dt> </dl>                                    | La touche CTRL de gauche est enfoncée<br/>                                                                                                                                              |
| <span id="TF_MOD_LSHIFT"></span><span id="tf_mod_lshift"></span><dl> <dt>**Tf \_ MOD \_ LSHIFT**</dt> <dt>0x0100</dt> </dl>                                          | La touche Maj de gauche est enfoncée<br/>                                                                                                                                             |
| <span id="TF_MOD_ON_KEYUP"></span><span id="tf_mod_on_keyup"></span><dl> <dt>**Tf \_ MOD \_ on \_ KEYUP**</dt> <dt>0x0200</dt> </dl>                                   | L’événement est déclenché lorsque la touche est relâchée. Sans cet indicateur, l’événement est déclenché lorsque la touche est enfoncée.<br/>                                                          |
| <span id="TF_MOD_IGNORE_ALL_MODIFIER"></span><span id="tf_mod_ignore_all_modifier"></span><dl> <dt>**Tf \_ MOD \_ ignore \_ tous les \_ modificateurs**</dt> <dt>0x0400</dt> </dl> | L’état des touches ALT, CTRL et Maj est ignoré. Cela signifie que l’événement est déclenché lorsque la touche virtuelle est enfoncée, quelles que soient les touches de modification enfoncées.<br/> |



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                           |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                 |
| Composant redistribuable<br/>          | TSF 1,0 sur Windows 2000 professionnel<br/>                                      |
| En-tête<br/>                   | <dl> <dt>Msctf. h</dt> </dl>   |
| MIDL<br/>                      | <dl> <dt>Msctf. idl</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[TF \_ PRESERVEDKEY](/windows/desktop/api/Msctf/ns-msctf-tf_preservedkey)
</dt> </dl>

 

 





