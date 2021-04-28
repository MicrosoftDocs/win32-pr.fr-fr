---
title: Message TDM_UPDATE_ELEMENT_TEXT (commctrl. h)
description: TDM_UPDATE_ELEMENT_TEXT message-met à jour un élément de texte dans une boîte de dialogue de tâche.
ms.assetid: 2df446c8-db87-42b5-b5bd-40fadbf9d45b
keywords:
- TDM_UPDATE_ELEMENT_TEXT les contrôles de message Windows
topic_type:
- apiref
api_name:
- TDM_UPDATE_ELEMENT_TEXT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c155b426b92645c0b9cdbabe00c44ffa722b89f3
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085807"
---
# <a name="tdm_update_element_text-message"></a>\_Message texte de l’élément de mise à jour TDM \_ \_

Met à jour un élément de texte dans une boîte de dialogue de tâche.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* \[ dans\]
</dt> <dd>

Indique l’élément à mettre à jour. (Pour obtenir une illustration des éléments, consultez [à propos des boîtes de dialogue de tâches](task-dialogs-overview.md).) Ce paramètre doit avoir l’une des valeurs suivantes :



| Valeur                                                                                                                                                                                           | Signification                          |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------|
| <span id="TDE_CONTENT"></span><span id="tde_content"></span><dl> <dt>**\_contenu TDE**</dt> </dl>                                         | Contenu.<br/>              |
| <span id="TDE_EXPANDED_INFORMATION"></span><span id="tde_expanded_information"></span><dl> <dt>**\_informations développées \_ TDE**</dt> </dl> | Informations développées.<br/> |
| <span id="TDE_FOOTER"></span><span id="tde_footer"></span><dl> <dt>**\_pied de page TDE**</dt> </dl>                                            | Texte de pied de page.<br/>          |
| <span id="TDE_MAIN_INSTRUCTION"></span><span id="tde_main_instruction"></span><dl> <dt>**\_instruction principale \_ TDE**</dt> </dl>             | Instruction principale.<br/>     |



 

</dd> <dt>

*lParam* \[ dans\]
</dt> <dd>

Pointeur vers une chaîne Unicode qui contient le nouveau texte.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

La valeur de retour est ignorée.

## <a name="remarks"></a>Notes 

Pour éviter le découpage, le nouveau texte ne doit pas être plus long que le texte existant. La définition du texte sur une chaîne plus petite n’entraîne pas le redimensionnement de la boîte de dialogue.

Si le membre **pszExpandedInformation** de la structure [**TASKDIALOGCONFIG**](/windows/desktop/api/Commctrl/ns-commctrl-taskdialogconfig) utilisée pour créer la boîte de dialogue de tâche a la **valeur null** et que vous envoyez un message **\_ \_ \_ texte d’élément de mise à jour TDM** avec des \_ informations développées TDE \_ , rien ne se produit.

Les éléments ci-dessus s’appliquent également aux pieds de page et pieds de \_ page TDE.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**texte de l' \_ élément de jeu TDM \_ \_**](tdm-set-element-text.md)
</dt> </dl>

 

 





