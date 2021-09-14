---
title: Message EM_SETCHARFORMAT (RichEdit. h)
description: Définit la mise en forme des caractères dans un contrôle RichEdit.
ms.assetid: 5e7a545d-4ca4-4dc6-badb-584c11194982
keywords:
- EM_SETCHARFORMAT les contrôles de Windows de message
topic_type:
- apiref
api_name:
- EM_SETCHARFORMAT
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba8f37960659f29dd33d5b8f27f0b5a2e3d35eb0
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127006420"
---
# <a name="em_setcharformat-message"></a>\_Message SETCHARFORMAT em

Définit la mise en forme des caractères dans un contrôle RichEdit.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Mise en forme des caractères qui s’applique au contrôle. Si ce paramètre est égal à zéro, le format de caractère par défaut est défini. Dans le cas contraire, il peut s’agir de l’une des valeurs suivantes.



| Valeur                                                                                                                                                                           | Signification                                                                                                                                                                                                                                                                                                   |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SCF_ALL"></span><span id="scf_all"></span><dl> <dt>**CSAH \_ tout**</dt> </dl>                                     | Applique la mise en forme à tout le texte du contrôle. Non valide avec **la \_ sélection SCF** ou le **\_ mot SCF**.<br/>                                                                                                                                                                                         |
| <span id="SCF_ASSOCIATEFONT"></span><span id="scf_associatefont"></span><dl> <dt>**CSAH \_ ASSOCIATEFONT**</dt> </dl>       | **RichEdit 4,1 :** Associe une police à un script donné, modifiant ainsi la police par défaut pour ce script. Pour spécifier la police, utilisez les membres suivants de [**CHARFORMAT2**](/windows/desktop/api/Richedit/ns-richedit-charformat2a): **yHeight**, **bCharSet**, **bPitchAndFamily**, **szFaceName** et **LCID**.<br/>                     |
| <span id="SCF_ASSOCIATEFONT2"></span><span id="scf_associatefont2"></span><dl> <dt>**CSAH \_ ASSOCIATEFONT2**</dt> </dl>    | **RichEdit 4,1 :** Associe une police de substitution (plan-2) à un script donné, modifiant ainsi la police par défaut pour ce script. Pour spécifier la police, utilisez les membres suivants de [**CHARFORMAT2**](/windows/desktop/api/Richedit/ns-richedit-charformat2a): **yHeight**, **bCharSet**, **bPitchAndFamily**, **szFaceName** et **LCID**.<br/> |
| <span id="SCF_CHARREPFROMLCID"></span><span id="scf_charrepfromlcid"></span><dl> <dt>**CSAH \_ CHARREPFROMLCID**</dt> </dl> | Obtient le répertoire de caractères à partir du LCID.<br/>                                                                                                                                                                                                                                                   |
| <span id="SCF_DEFAULT"></span><span id="scf_default"></span><dl> <dt>**CSAH \_ par défaut**</dt> </dl>                         | **RichEdit 4,1 :** Définit la police par défaut pour le contrôle. <br/>                                                                                                                                                                                                                                      |
| <span id="SPF_DONTSETDEFAULT"></span><span id="spf_dontsetdefault"></span><dl> <dt>**\_DONTSETDEFAULT SPF**</dt> </dl>    | Empêche de définir le format de paragraphe par défaut lorsque le contrôle RichEdit est vide.<br/>                                                                                                                                                                                                             |
| <span id="SCF_NOKBUPDATE"></span><span id="scf_nokbupdate"></span><dl> <dt>**CSAH \_ NOKBUPDATE**</dt> </dl>                | **RichEdit 4,1 :** Empêche le changement de clavier de correspondre à la police. Par exemple, si une police arabe est définie, normalement la fonctionnalité de clavier automatique pour les langues bidi remplace le clavier par un clavier arabe.<br/>                                                                                 |
| <span id="SCF_SELECTION"></span><span id="scf_selection"></span><dl> <dt>**\_sélection SCF**</dt> </dl>                   | Applique la mise en forme à la sélection actuelle. Si la sélection est vide, la mise en forme des caractères est appliquée au point d’insertion et le nouveau format de caractère est en vigueur uniquement jusqu’à ce que le point d’insertion soit modifié.<br/>                                                                      |
| <span id="SPF_SETDEFAULT"></span><span id="spf_setdefault"></span><dl> <dt>**de SPF \_ SETDEFAULT**</dt> </dl>                | Définit les attributs de mise en forme par défaut des paragraphes.<br/>                                                                                                                                                                                                                                              |
| <span id="SCF_SMARTFONT"></span><span id="scf_smartfont"></span><dl> <dt>**CSAH \_ SMARTFONT**</dt> </dl>                   | Appliquez la police uniquement si elle peut gérer le script.<br/>                                                                                                                                                                                                                                                   |
| <span id="SCF_USEUIRULES"></span><span id="scf_useuirules"></span><dl> <dt>**CSAH \_ USEUIRULES**</dt> </dl>                | **RichEdit 4,1 :** Utilisé avec **la \_ sélection SCF**. Indique que le format provient d’une barre d’outils ou d’un autre outil d’interface utilisateur. les règles de mise en forme de l’interface utilisateur doivent donc être utilisées à la place de la mise en forme littérale<br/>                                                                                                               |
| <span id="SCF_WORD"></span><span id="scf_word"></span><dl> <dt>**\_mot SCF**</dt> </dl>                                  | Applique la mise en forme au ou aux mots sélectionnés. Si la sélection est vide, mais que le point d’insertion se trouve à l’intérieur d’un mot, la mise en forme est appliquée au mot. La valeur du **\_ mot SCF** doit être utilisée conjointement avec la valeur de **\_ sélection SCF** .<br/>                                        |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure [**Charformat**](/windows/win32/api/richedit/ns-richedit-charformata) spécifiant la mise en forme des caractères à utiliser. Seuls les attributs de mise en forme spécifiés par le membre **dwMask** sont modifiés.

Microsoft Rich Edit 2,0 et versions ultérieures : ce paramètre peut être un pointeur vers une structure [**CHARFORMAT2**](/windows/desktop/api/Richedit/ns-richedit-charformat2a) , qui est une extension de la structure [**Charformat**](/windows/win32/api/richedit/ns-richedit-charformata) . Avant d’envoyer le message **\_ SETCHARFORMAT em** , définissez le membre **cbSize** de la structure sur `sizeof(CHARFORMAT)` ou `sizeof(CHARFORMAT2)` Indiquez la version de la structure utilisée.

Les membres **szFaceName** et **bCharSet** peuvent être remplacés lorsqu’ils ne sont pas valides pour les caractères, par exemple : Arial sur les caractères Kanji.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Si l’opération a échoué, la valeur de retour est une valeur différente de zéro.

Si l’opération échoue, la valeur de retour est zéro.

## <a name="remarks"></a>Notes

Si ce message est envoyé plusieurs fois avec les mêmes paramètres, l’effet sur le texte est basculé. Autrement dit, l’envoi du message une fois produit l’effet, l’envoi du message à deux reprises annule l’effet, et ainsi de suite.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

**Référence**
</dt> <dt>

[**CHARFORMAT**](/windows/win32/api/richedit/ns-richedit-charformata)
</dt> <dt>

[**CHARFORMAT2**](/windows/desktop/api/Richedit/ns-richedit-charformat2a)
</dt> </dl>

 

 





