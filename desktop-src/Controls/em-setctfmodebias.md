---
title: Message EM_SETCTFMODEBIAS (RichEdit. h)
description: Définit le décalage du mode Text Services Framework (TSF) pour un contrôle RichEdit.
ms.assetid: 17e3aac8-2ba8-4c06-bfd6-e118cfb82529
keywords:
- EM_SETCTFMODEBIAS les contrôles de Windows de message
topic_type:
- apiref
api_name:
- EM_SETCTFMODEBIAS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b872fa5489c898ec4482ecdc094de7df6e3180be
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127006409"
---
# <a name="em_setctfmodebias-message"></a>\_Message SETCTFMODEBIAS em

Définit le décalage du mode Text Services Framework (TSF) pour un contrôle RichEdit.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Valeur de décalage du mode. Il peut s’agir de l’une des valeurs suivantes.



| Valeur                                                                                                                                                                                                                     | Signification                                                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| <span id="CTFMODEBIAS_DEFAULT"></span><span id="ctfmodebias_default"></span><dl> <dt>**CTFMODEBIAS \_ par défaut**</dt> </dl>                                           | Il n’y a pas de décalage de mode.<br/>                             |
| <span id="CTFMODEBIAS_FILENAME"></span><span id="ctfmodebias_filename"></span><dl> <dt>**\_nom de fichier CTFMODEBIAS**</dt> </dl>                                        | Le décalage est vers un nom de fichier.<br/>                         |
| <span id="CTFMODEBIAS_NAME"></span><span id="ctfmodebias_name"></span><dl> <dt>**nom de CTFMODEBIAS \_**</dt> </dl>                                                    | Le biais correspond à un nom.<br/>                             |
| <span id="CTFMODEBIAS_READING"></span><span id="ctfmodebias_reading"></span><dl> <dt>**\_lecture CTFMODEBIAS**</dt> </dl>                                           | Le décalage concerne la lecture.<br/>                        |
| <span id="CTFMODEBIAS_DATETIME"></span><span id="ctfmodebias_datetime"></span><dl> <dt>**CTFMODEBIAS \_ DateTime**</dt> </dl>                                        | L’écart concerne une date ou une heure.<br/>                     |
| <span id="CTFMODEBIAS_CONVERSATION"></span><span id="ctfmodebias_conversation"></span><dl> <dt>**\_conversation CTFMODEBIAS**</dt> </dl>                            | Le décalage concerne une conversation.<br/>                     |
| <span id="CTFMODEBIAS_NUMERIC"></span><span id="ctfmodebias_numeric"></span><dl> <dt>**CTFMODEBIAS \_ numérique**</dt> </dl>                                           | Le biais est un nombre.<br/>                           |
| <span id="CTFMODEBIAS_HIRAGANA"></span><span id="ctfmodebias_hiragana"></span><dl> <dt>**CTFMODEBIAS \_ hiragana**</dt> </dl>                                        | Le décalage est vers des chaînes Hiragana.<br/>                   |
| <span id="CTFMODEBIAS_KATAKANA"></span><span id="ctfmodebias_katakana"></span><dl> <dt>**CTFMODEBIAS \_ Katakana**</dt> </dl>                                        | Le décalage est le biais des chaînes Katakana.<br/>                   |
| <span id="CTFMODEBIAS_HANGUL"></span><span id="ctfmodebias_hangul"></span><dl> <dt>**\_HANGUL CTFMODEBIAS**</dt> </dl>                                              | Le décalage concerne les caractères Hangul.<br/>                  |
| <span id="CTFMODEBIAS_HALFWIDTHKATAKANA"></span><span id="ctfmodebias_halfwidthkatakana"></span><dl> <dt>**CTFMODEBIAS \_ HALFWIDTHKATAKANA**</dt> </dl>             | Le décalage est vers les chaînes katakana à demi-chasse.<br/>        |
| <span id="CTFMODEBIAS_FULLWIDTHALPHANUMERIC"></span><span id="ctfmodebias_fullwidthalphanumeric"></span><dl> <dt>**CTFMODEBIAS \_ FULLWIDTHALPHANUMERIC**</dt> </dl> | L’écart est de caractères alphanumériques à pleine chasse.<br/> |
| <span id="CTFMODEBIAS_HALFWIDTHALPHANUMERIC"></span><span id="ctfmodebias_halfwidthalphanumeric"></span><dl> <dt>**CTFMODEBIAS \_ HALFWIDTHALPHANUMERIC**</dt> </dl> | Le décalage se fait en caractères alphanumériques à demi-chasse.<br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Non utilisé ; doit être égal à zéro.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

En cas de réussite, la valeur de retour est la nouvelle valeur de biais du mode TSF. En cas d’échec, la valeur de retour est l’ancienne valeur de biais du mode TSF.

## <a name="remarks"></a>Notes

Quand une application RichEdit (Microsoft Rich Edit) utilise TSF, elle peut sélectionner le biais du mode TSF. Ce message définit les critères selon lesquels un autre choix apparaît en haut de la liste pour la sélection.

Pour définir le décalage de mode pour l’éditeur de méthode d’entrée (IME), utilisez [**em \_ SETIMEMODEBIAS**](em-setimemodebias.md).

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows XP avec les \[ applications de bureau SP1 uniquement\]<br/>                                  |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

**Référence**
</dt> <dt>

[**\_GETCTFMODEBIAS em**](em-getctfmodebias.md)
</dt> <dt>

[**\_SETIMEMODEBIAS em**](em-setimemodebias.md)
</dt> </dl>

 

 





