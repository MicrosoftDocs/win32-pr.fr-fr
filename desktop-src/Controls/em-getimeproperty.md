---
title: Message EM_GETIMEPROPERTY (RichEdit. h)
description: Récupère la propriété et les fonctionnalités de l’éditeur de méthode d’entrée (IME) associé aux paramètres régionaux d’entrée actuels.
ms.assetid: 0cbe52d4-c3e7-40bd-a6f6-da0a11056976
keywords:
- EM_GETIMEPROPERTY les contrôles de Windows de message
topic_type:
- apiref
api_name:
- EM_GETIMEPROPERTY
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3b96ad255d9d68cc76869b6f9163aedf549da19ff0c3ddba756f8da42267135c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119541109"
---
# <a name="em_getimeproperty-message"></a>\_Message GETIMEPROPERTY em

Récupère la propriété et les fonctionnalités de l’éditeur de méthode d’entrée (IME) associé aux paramètres régionaux d’entrée actuels.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Spécifie le type d’informations de propriété à récupérer. Ce paramètre peut prendre les valeurs suivantes.



| Valeur                                                                                                                                                                     | Signification                                                                                  |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------|
| <span id="IGP_PROPERTY"></span><span id="igp_property"></span><dl> <dt>**\_propriété IGP**</dt> </dl>                | Informations sur les propriétés.<br/>                                                         |
| <span id="IGP_CONVERSION"></span><span id="igp_conversion"></span><dl> <dt>**\_conversion IGP**</dt> </dl>          | Fonctionnalités de conversion. <br/>                                                     |
| <span id="IGP_SENTENCE"></span><span id="igp_sentence"></span><dl> <dt>**\_phrase IGP**</dt> </dl>                | Fonctionnalités du mode phrase. <br/>                                                  |
| <span id="IGP_UI"></span><span id="igp_ui"></span><dl> <dt>**\_interface utilisateur IGP**</dt> </dl>                                  | Fonctionnalités de l’interface utilisateur. <br/>                                                 |
| <span id="IGP_SETCOMPSTR"></span><span id="igp_setcompstr"></span><dl> <dt>**IGP \_ SETCOMPSTR**</dt> </dl>          | Fonctionnalités de la chaîne de composition. <br/>                                             |
| <span id="IGP_SELECT"></span><span id="igp_select"></span><dl> <dt>**IGP, \_ Sélectionner**</dt> </dl>                      | Fonctionnalités d’héritage de la sélection. <br/>                                          |
| <span id="IGP_GETIMEVERSION"></span><span id="igp_getimeversion"></span><dl> <dt>**IGP \_ GETIMEVERSION**</dt> </dl> | Récupère le numéro de version du système pour lequel l’IME spécifié a été créé. <br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Non utilisé ; doit être égal à zéro.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne la valeur de la propriété ou de la fonctionnalité, selon la valeur du paramètre *lParam* . Pour plus d'informations, consultez la section Notes.

## <a name="remarks"></a>Remarques

Si *wParam* est \_ la propriété IGP, elle retourne une ou plusieurs des valeurs suivantes.



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_prop IME \_ au \_ signe insertion                | Si cette valeur est définie, la fenêtre de conversion se trouve à l’emplacement du signe insertion. Si cette case est désactivée, la fenêtre est proche de la position du signe insertion.                                                                                                                                                                  |
| \_ \_ interface utilisateur spéciale prop IME \_              | S’il est défini, l’éditeur IME a une interface utilisateur non standard. L’application ne doit pas être dessinée dans la fenêtre IME.                                                                                                                                                                  |
| \_ \_ CANDLIST du prop IME \_ Démarrer \_ à partir de \_ 1 | Si cette valeur est définie, les chaînes de la liste candidate sont numérotées à partir de 1. Si la valeur est Clear, les chaînes commencent à zéro.                                                                                                                                                                |
| \_Unicode prop \_ Unicode                  | Si cette valeur est définie, l’IME est affiché en tant que UnicodeIME. Le système et l’IME communiquent par l’intermédiaire de l’interface UnicodeIME. Si la valeur est Clear, IME utilise l’interface ANSI pour communiquer avec le système.                                                                    |
| la \_ prop IME est \_ terminée \_ lors de la \_ désélection   | Si cette valeur est définie, la fenêtre de conversion se trouve à l’emplacement du signe insertion. Si cette case est désactivée, la fenêtre est proche de la position du signe insertion.                                                                                                                                                                  |
| IME \_ prop \_ Accept \_ \_ VKEY       | Si cette valeur est définie, l’IME traite le Unicode injecté qui provient de la fonction [**SendInput**](/windows/desktop/api/winuser/nf-winuser-sendinput) à l’aide du \_ paquet VK. Si elle est désactivée, l’IME peut ne pas traiter le Unicode injecté et le Unicode injecté peut être envoyé directement à l’application. |



 

Si *wParam* est \_ une interface utilisateur IGP, elle retourne une ou plusieurs des valeurs suivantes.



| Condition requise | Valeur |
|-----------------|-------------------------------------------------------------------------------------------------------|
| Interface utilisateur \_ CAP \_ 2700   | Prend en charge les valeurs d’échappement de texte 0 ou 2700. Pour plus d’informations, consultez **lfEscapement**.             |
| \_ROT90 Cap de l’interface utilisateur \_  | Prend en charge les valeurs d’échappement de texte 0, 900, 1800 ou 2700. Pour plus d’informations, consultez **lfEscapement**. |
| \_ROTANY Cap de l’interface utilisateur \_ | Prend en charge toute valeur d’échappement de texte. Pour plus d’informations, consultez **lfEscapement**.                       |



 

Si *wParam* est IGP \_ SETCOMPSTR, il retourne une ou plusieurs des valeurs suivantes.



| Condition requise | Valeur |
|------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| SCS- \_ Cap \_ COMPSTR            | Peut créer la chaîne de composition en appelant la fonction [**ImmSetCompositionString**](/windows/desktop/api/imm/nf-imm-immsetcompositionstringa) avec la \_ valeur SCS SETSTR.                                                      |
| SCS- \_ Cap \_ MAKEREAD           | Peut créer la chaîne de lecture à partir de la chaîne de composition correspondante lors de l’utilisation de la fonction [**ImmSetCompositionString**](/windows/desktop/api/imm/nf-imm-immsetcompositionstringa) avec SCS \_ SETSTR et sans définir *lpRead*. |
| SCS- \_ Cap \_ SETRECONVERTSTRING | Cet IME peut prendre en charge la reconversion. Utilisez [**ImmSetCompositionString**](/windows/desktop/api/imm/nf-imm-immsetcompositionstringa) pour effectuer la reconversion.                                                                             |



 

Si *wParam* est IGP \_ , sélectionnez, il retourne une ou plusieurs des valeurs suivantes.



| Condition requise | Valeur |
|-----------------------|------------------------------------------------------|
| SÉLECTIONNER \_ un \_ CONVMODE Cap | Hérite du mode de conversion lorsqu’un nouvel IME est sélectionné. |
| SÉLECTIONNER \_ une \_ phrase d’extrémité | Hérite du mode phrase lorsqu’un nouvel IME est sélectionné.   |



 

Si *wParam* est IGP \_ GETIMEVERSION, il retourne une ou plusieurs des valeurs suivantes.



| Condition requise | Valeur |
|--------------|---------------------------------------------|
| JAMAIS \_ 0310 | l’IME a été créé pour Windows 3,1.        |
| JAMAIS \_ 0400 | l’IME a été créé pour Windows 95 ou version ultérieure |



 

Ce message est semblable à [**ImmGetProperty**](/windows/desktop/api/imm/nf-imm-immgetproperty), à ceci près qu’il utilise les paramètres régionaux d’entrée actuels. L’application doit appeler [**em \_ ISIME**](em-isime.md) avant d’appeler cette fonction.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

**Référence**
</dt> <dt>

[**\_ISIME em**](em-isime.md)
</dt> <dt>

**Autres ressources**
</dt> <dt>

[**ImmGetProperty**](/windows/desktop/api/imm/nf-imm-immgetproperty)
</dt> </dl>

 

