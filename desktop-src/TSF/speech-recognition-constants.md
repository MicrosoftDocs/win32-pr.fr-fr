---
title: Constantes de reconnaissance vocale (Ctffunc. h)
description: Les valeurs suivantes sont utilisées avec le service de texte de reconnaissance vocale.
ms.assetid: ac433d15-738a-46ab-8f69-0fbfb6a8b654
topic_type:
- apiref
api_name:
- TF_DICTATION_ON
- TF_DICTATION_ENABLED
- TF_COMMANDING_ENABLED
- TF_COMMANDING_ON
- TF_SPEECHUI_SHOWN
- TF_SHOW_BALLOON
- TF_DISABLE_BALLOON
- TF_DISABLE_SPEECH
- TF_DISABLE_DICTATION
- TF_DISABLE_COMMANDING
api_location:
- Ctffunc.h
- Msctf.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 04c9cfd340e79415d12202765a8db1578abba74e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103016"
---
# <a name="speech-recognition-constants"></a>Constantes de reconnaissance vocale

Les valeurs suivantes sont utilisées avec le service de texte de reconnaissance vocale.



| Constante/valeur                                                                                                                                                                                                                                         | Description                                                                                                                                                                                                                                                 |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TF_DICTATION_ON"></span><span id="tf_dictation_on"></span><dl> <dt>**Tf \_ DICTée \_ sur**</dt> <dt>0x00000001</dt> </dl>                   | Si ce bit est 1, la dictée vocale est active. Dans le cas contraire, la dictée vocale est inactive. Cette valeur ne peut pas être combinée avec la \_ commande tf \_ sur. Utilisé avec le [compartiment \_ \_ \_ DICTATIONSTAT de reconnaissance vocale des compartiments GUID](predefined-compartments.md) .<br/> |
| <span id="TF_DICTATION_ENABLED"></span><span id="tf_dictation_enabled"></span><dl> <dt>**Tf \_ La DICTée est \_ activée**</dt> <dt>0x00000002</dt> </dl>    | Si ce bit est 1, la dictée vocale est activée. Dans le cas contraire, la dictée vocale est désactivée. Utilisé avec le [compartiment \_ \_ \_ DICTATIONSTAT de reconnaissance vocale des compartiments GUID](predefined-compartments.md) .<br/>                                                       |
| <span id="TF_COMMANDING_ENABLED"></span><span id="tf_commanding_enabled"></span><dl> <dt>**Tf \_ \_Activation des commandes**</dt> <dt>0x00000004</dt> </dl> | Si ce bit est 1, la commande Speech est activée. Dans le cas contraire, la commande Speech est désactivée. Utilisé avec le [compartiment \_ \_ \_ DICTATIONSTAT de reconnaissance vocale des compartiments GUID](predefined-compartments.md) .<br/>                                                           |
| <span id="TF_COMMANDING_ON"></span><span id="tf_commanding_on"></span><dl> <dt>**Tf \_ COMMANDE \_ sur**</dt> <dt>0x00000008</dt> </dl>                | Si ce bit est 1, la commande Speech est active. Dans le cas contraire, la commande Speech est inactive. Cette valeur ne peut pas être combinée avec la \_ dictée TF \_ sur. Utilisé avec le [compartiment \_ \_ \_ DICTATIONSTAT de reconnaissance vocale des compartiments GUID](predefined-compartments.md) .<br/>      |
| <span id="TF_SPEECHUI_SHOWN"></span><span id="tf_speechui_shown"></span><dl> <dt>**Tf \_ SPEECHUI \_ affiché**</dt> <dt>0x00000010</dt> </dl>             | Pas utilisé pour l'instant.<br/>                                                                                                                                                                                                                              |
| <span id="TF_SHOW_BALLOON"></span><span id="tf_show_balloon"></span><dl> <dt>**Tf \_ AFFICHER la \_ bulle**</dt> <dt>0x00000001</dt> </dl>                   | Pas utilisé pour l'instant. Utilisé avec le compartiment de l’état de l' [ \_ \_ \_ interface \_ utilisateur Speech des compartiments GUID](predefined-compartments.md) .<br/>                                                                                                                              |
| <span id="TF_DISABLE_BALLOON"></span><span id="tf_disable_balloon"></span><dl> <dt>**Tf \_ DÉSACTIVER l' \_ info-bulle**</dt> <dt>0x00000002</dt> </dl>          | Si ce bit est 1, l’affichage du ballon pour le mode vocal actuel est désactivé. Dans le cas contraire, l’affichage du ballon pour le mode vocal actuel est activé. Utilisé avec le compartiment de l’état de l' [ \_ \_ \_ interface \_ utilisateur Speech des compartiments GUID](predefined-compartments.md) .<br/>    |
| <span id="TF_DISABLE_SPEECH"></span><span id="tf_disable_speech"></span><dl> <dt>**Tf \_ DÉSACTIVER la \_ reconnaissance vocale**</dt> <dt>0x00000001</dt> </dl>             | Si ce bit est 1, l’entrée vocale est désactivée. Dans le cas contraire, l’entrée vocale est activée. Utilisé avec le compartiment [GUID désactivé par la \_ \_ reconnaissance vocale \_ des compartiments](predefined-compartments.md) .<br/>                                                                    |
| <span id="TF_DISABLE_DICTATION"></span><span id="tf_disable_dictation"></span><dl> <dt>**Tf \_ DÉSACTIVER la \_ dictée**</dt> <dt>0x00000002</dt> </dl>    | Si ce bit est 1, la dictée vocale est désactivée. Dans le cas contraire, la dictée vocale est activée. Utilisé avec le compartiment [GUID désactivé par la \_ \_ reconnaissance vocale \_ des compartiments](predefined-compartments.md) .<br/>                                                            |
| <span id="TF_DISABLE_COMMANDING"></span><span id="tf_disable_commanding"></span><dl> <dt>**Tf \_ DÉSACTIVER le \_ commande**</dt> <dt>0x00000004</dt> </dl> | Si ce bit est 1, la commande Speech est désactivée. Dans le cas contraire, la commande Speech est activée. Utilisé avec le compartiment [GUID désactivé par la \_ \_ reconnaissance vocale \_ des compartiments](predefined-compartments.md) .<br/>                                                                |



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                                                                                              |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                                                                                    |
| Composant redistribuable<br/>          | TSF 1,0 sur Windows 2000 professionnel<br/>                                                                                                         |
| En-tête<br/>                   | <dl> <dt>Ctffunc. h ; </dt> <dt>Msctf. h</dt> </dl>     |
| MIDL<br/>                      | <dl> <dt>Ctffunc. idl ; </dt> <dt>Msctf. idl</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Compartiments prédéfinis](predefined-compartments.md)
</dt> </dl>

 

 





