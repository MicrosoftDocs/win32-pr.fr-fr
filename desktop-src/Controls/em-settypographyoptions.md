---
title: Message EM_SETTYPOGRAPHYOPTIONS (RichEdit. h)
description: Définit l’état actuel des options typographiques d’un contrôle RichEdit.
ms.assetid: 000e72a6-3f8c-4735-8190-3ac06a2206ac
keywords:
- EM_SETTYPOGRAPHYOPTIONS les contrôles de Windows de message
topic_type:
- apiref
api_name:
- EM_SETTYPOGRAPHYOPTIONS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aec3938e4322a13303ec2fc336b47d7e61a51eea58d49214001720a371f0326a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119437449"
---
# <a name="em_settypographyoptions-message"></a>\_Message SETTYPOGRAPHYOPTIONS em

Définit l’état actuel des options typographiques d’un contrôle RichEdit.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Spécifie l’une des valeurs suivantes ou les deux.



| Valeur                                                                                                                                                                                    | Signification                                                                                 |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| <span id="TO_ADVANCEDTYPOGRAPHY_"></span><span id="to_advancedtypography_"></span><dl> <dt>**À \_ ADVANCEDTYPOGRAPHY**</dt> </dl> | Le saut de ligne avancé et la mise en forme de ligne sont activés. <br/>                    |
| <span id="TO_SIMPLELINEBREAK"></span><span id="to_simplelinebreak"></span><dl> <dt>**à \_ SIMPLELINEBREAK**</dt> </dl>             | Saut de ligne plus rapide pour le texte simple (requiert **\_ ADVANCEDTYPOGRAPHY**). <br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Masque constitué d’un ou plusieurs indicateurs dans *wParam*. Seuls les indicateurs définis dans ce masque seront définis ou désactivés. Cela permet de définir ou d’effacer un seul indicateur sans lire les États de l’indicateur actuel.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne la **valeur true** si *wParam* est valide, sinon **false**.

## <a name="remarks"></a>Remarques

Le saut de ligne avancé est activé automatiquement par le contrôle RichEdit si nécessaire, par exemple pour la gestion de scripts complexes tels que l’arabe et l’hébreu, ainsi que pour les mathématiques. Elle est également nécessaire pour les paragraphes justifiés, la césure et d’autres fonctionnalités typographiques.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| Composant redistribuable<br/>          | Édition enrichie 3,0<br/>                                                              |
| En-tête<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_GETTYPOGRAPHYOPTIONS em**](em-gettypographyoptions.md)
</dt> </dl>

 

 





