---
title: Message EM_SETTYPOGRAPHYOPTIONS (RichEdit. h)
description: Définit l’état actuel des options typographiques d’un contrôle RichEdit.
ms.assetid: 000e72a6-3f8c-4735-8190-3ac06a2206ac
keywords:
- EM_SETTYPOGRAPHYOPTIONS les contrôles de message Windows
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
ms.openlocfilehash: 0528e19aacec394c5af6250536fdc4f693e60ece
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942293"
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

## <a name="remarks"></a>Notes

Le saut de ligne avancé est activé automatiquement par le contrôle RichEdit si nécessaire, par exemple pour la gestion de scripts complexes tels que l’arabe et l’hébreu, ainsi que pour les mathématiques. Elle est également nécessaire pour les paragraphes justifiés, la césure et d’autres fonctionnalités typographiques.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
| Composant redistribuable<br/>          | Édition enrichie 3,0<br/>                                                              |
| En-tête<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_GETTYPOGRAPHYOPTIONS em**](em-gettypographyoptions.md)
</dt> </dl>

 

 





