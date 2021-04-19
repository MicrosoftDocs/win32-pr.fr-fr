---
title: Indicateurs de masque d’événement de contrôle Rich Edit (RichEdit. h)
description: Le masque d’événement spécifie les codes de notification qu’un contrôle RichEdit envoie à sa fenêtre parente. Le masque d’événement peut être None ou une combinaison de ces valeurs.
ms.assetid: ae0d2cbe-5cbc-42bb-aeb1-7e6be846a4ba
topic_type:
- apiref
api_name:
- ENM_CHANGE
- ENM_CLIPFORMAT
- ENM_CORRECTTEXT
- ENM_DRAGDROPDONE
- ENM_DROPFILES
- ENM_IMECHANGE
- ENM_KEYEVENTS
- ENM_LINK
- ENM_LOWFIRTF
- ENM_MOUSEEVENTS
- ENM_OBJECTPOSITIONS
- ENM_PARAGRAPHEXPANDED
- ENM_PROTECTED
- ENM_REQUESTRESIZE
- ENM_SCROLL
- ENM_SCROLLEVENTS
- ENM_SELCHANGE
- ENM_UPDATE
api_location:
- RichEdit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 006a6d82e7aa4958b03360d05d29a78564f99db7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106539218"
---
# <a name="rich-edit-control-event-mask-flags"></a>Indicateurs de masque d’événement de contrôle RichEdit

Le masque d’événement spécifie les codes de notification qu’un contrôle RichEdit envoie à sa fenêtre parente. Le masque d’événement peut être None ou une combinaison de ces valeurs.



| Constante                                                                                                                                                                              | Description                                                                                                                                                                                                                                                                                                       |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="ENM_CHANGE"></span><span id="enm_change"></span><dl> <dt>**modification de ENM \_**</dt> </dl>                                  | Envoie des notifications de [ \_ modification](en-change--rich-edit-control-.md) .<br/>                                                                                                                                                                                                                                   |
| <span id="ENM_CLIPFORMAT"></span><span id="enm_clipformat"></span><dl> <dt>**ENM \_ CLIPFORMAT**</dt> </dl>                      | Envoie des notifications en [ \_ CLIPFORMAT](/windows/desktop/Controls/en-clipformat) .<br/>                                                                                                                                                                                                                                          |
| <span id="ENM_CORRECTTEXT"></span><span id="enm_correcttext"></span><dl> <dt>**ENM \_ CORRECTTEXT**</dt> </dl>                   | Envoie des notifications en [ \_ CORRECTTEXT](en-correcttext.md) .<br/>                                                                                                                                                                                                                                             |
| <span id="ENM_DRAGDROPDONE"></span><span id="enm_dragdropdone"></span><dl> <dt>**ENM \_ DRAGDROPDONE**</dt> </dl>                | Envoie des notifications en [ \_ DRAGDROPDONE](en-dragdropdone.md) .<br/>                                                                                                                                                                                                                                           |
| <span id="ENM_DROPFILES"></span><span id="enm_dropfiles"></span><dl> <dt>**ENM \_ DROPFILES**</dt> </dl>                         | Envoie des notifications en [ \_ DROPFILES](en-dropfiles.md) .<br/>                                                                                                                                                                                                                                                 |
| <span id="ENM_IMECHANGE"></span><span id="enm_imechange"></span><dl> <dt>**ENM \_ IMECHANGE**</dt> </dl>                         | Microsoft Rich Edit 1,0 uniquement : envoie des notifications en [ \_ IMECHANGE](en-imechange.md) lorsque l’état de conversion IME a changé. Uniquement pour les versions en langue asiatique du système d’exploitation.<br/>                                                                                                              |
| <span id="ENM_KEYEVENTS"></span><span id="enm_keyevents"></span><dl> <dt>**\_événements ENM**</dt> </dl>                         | Envoie des notifications en [ \_ msgfilter](en-msgfilter.md) pour les événements de clavier.<br/>                                                                                                                                                                                                                             |
| <span id="ENM_LINK"></span><span id="enm_link"></span><dl> <dt>**\_lien ENM**</dt> </dl>                                        | **Édition enrichie 2,0 et versions ultérieures :** Envoie des notifications en [ \_ lien](en-link.md) lorsque le pointeur de la souris se trouve sur le texte qui a le lien CFE et que l' \_ une des nombreuses actions de la souris est effectuée.<br/>                                                                                                                     |
| <span id="ENM_LOWFIRTF"></span><span id="enm_lowfirtf"></span><dl> <dt>**ENM \_ LOWFIRTF**</dt> </dl>                            | Envoie des notifications en [ \_ LOWFIRTF](en-lowfirtf.md) .<br/>                                                                                                                                                                                                                                                   |
| <span id="ENM_MOUSEEVENTS"></span><span id="enm_mouseevents"></span><dl> <dt>**ENM \_ MOUSEEVENTS**</dt> </dl>                   | Envoie des notifications en [ \_ msgfilter](en-msgfilter.md) pour les événements de souris.<br/>                                                                                                                                                                                                                                |
| <span id="ENM_OBJECTPOSITIONS"></span><span id="enm_objectpositions"></span><dl> <dt>**ENM \_ OBJECTPOSITIONS**</dt> </dl>       | Envoie des notifications en [ \_ OBJECTPOSITIONS](en-objectpositions.md) .<br/>                                                                                                                                                                                                                                     |
| <span id="ENM_PARAGRAPHEXPANDED"></span><span id="enm_paragraphexpanded"></span><dl> <dt>**ENM \_ PARAGRAPHEXPANDED**</dt> </dl> | Envoie des notifications en [ \_ PARAGRAPHEXPANDED](/windows/desktop/Controls/en-paragraphexpanded) .<br/>                                                                                                                                                                                                                            |
| <span id="ENM_PROTECTED"></span><span id="enm_protected"></span><dl> <dt>**ENM \_ protégé**</dt> </dl>                         | Envoie des notifications en [ \_ protection](en-protected.md) .<br/>                                                                                                                                                                                                                                                 |
| <span id="ENM_REQUESTRESIZE"></span><span id="enm_requestresize"></span><dl> <dt>**ENM \_ REQUESTRESIZE**</dt> </dl>             | Envoie des notifications en [ \_ REQUESTRESIZE](en-requestresize.md) .<br/>                                                                                                                                                                                                                                         |
| <span id="ENM_SCROLL"></span><span id="enm_scroll"></span><dl> <dt>**ENM \_ défilement**</dt> </dl>                                  | Envoie les notifications en [ \_ HSCROLL](en-hscroll.md) et en [ \_ VSCROLL](en-vscroll.md) .<br/>                                                                                                                                                                                                                   |
| <span id="ENM_SCROLLEVENTS"></span><span id="enm_scrollevents"></span><dl> <dt>**ENM \_ SCROLLEVENTS**</dt> </dl>                | Envoie des notifications en [ \_ msgfilter](en-msgfilter.md) pour les événements de roulette de la souris.<br/>                                                                                                                                                                                                                          |
| <span id="ENM_SELCHANGE"></span><span id="enm_selchange"></span><dl> <dt>**ENM \_ selChange**</dt> </dl>                         | Envoie des notifications en [ \_ selChange](en-selchange.md) .<br/>                                                                                                                                                                                                                                                 |
| <span id="ENM_UPDATE"></span><span id="enm_update"></span><dl> <dt>**\_mise à jour ENM**</dt> </dl>                                  | Envoie des notifications de [ \_ mise à jour](en-update.md) . <br/> **Édition enrichie 2,0 et versions ultérieures :** cet indicateur est ignoré et les notifications de [ \_ mise à jour](en-update.md) sont toujours envoyées. Toutefois, si Rich Edit 3,0 émule Microsoft Rich Edit 1,0, vous devez utiliser cet indicateur pour envoyer \_ des notifications de mise à jour.<br/> |



## <a name="remarks"></a>Notes

Le masque d’événement par défaut est ENM \_ aucun. dans ce cas, aucune notification n’est envoyée à la fenêtre parente. Vous pouvez récupérer et définir le masque d’événement pour un contrôle RichEdit à l’aide des messages [**em \_ GETEVENTMASK**](em-geteventmask.md) et [**em \_ SETEVENTMASK**](em-seteventmask.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|---------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>RichEdit. h</dt> </dl> |



 

