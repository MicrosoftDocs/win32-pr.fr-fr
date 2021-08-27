---
title: Message TDM_SET_ELEMENT_TEXT (commctrl. h)
description: TDM_SET_ELEMENT_TEXT message-met à jour un élément de texte dans une boîte de dialogue de tâche.
ms.assetid: e3f15805-5d48-4549-9959-69ec01345e57
keywords:
- TDM_SET_ELEMENT_TEXT les contrôles de Windows de message
topic_type:
- apiref
api_name:
- TDM_SET_ELEMENT_TEXT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7bb0f81867bcff4fd5f7d533c156c8af17d0f4a761b6f8560aa584a85c62b7c8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120060769"
---
# <a name="tdm_set_element_text-message"></a>\_Message texte de l’élément d’ensemble TDM \_ \_

Met à jour un élément de texte dans une boîte de dialogue de tâche.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* \[ dans\]
</dt> <dd>

Indique l’élément à mettre à jour. (Pour obtenir une illustration, consultez [à propos des boîtes de dialogue de tâches](task-dialogs-overview.md).) Ce paramètre doit avoir l’une des valeurs suivantes.



| Valeur                                                                                                                                                                                           | Signification                          |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------|
| <span id="TDE_CONTENT"></span><span id="tde_content"></span><dl> <dt>**\_contenu TDE**</dt> </dl>                                         | Contenu.<br/>              |
| <span id="TDE_EXPANDED_INFORMATION"></span><span id="tde_expanded_information"></span><dl> <dt>**\_informations développées \_ TDE**</dt> </dl> | Informations développées.<br/> |
| <span id="TDE_FOOTER"></span><span id="tde_footer"></span><dl> <dt>**\_pied de page TDE**</dt> </dl>                                            | Texte de pied de page.<br/>          |
| <span id="TDE_MAIN_INSTRUCTION"></span><span id="tde_main_instruction"></span><dl> <dt>**\_instruction principale \_ TDE**</dt> </dl>             | Instruction principale.<br/>     |



 

</dd> <dt>

*lParam* \[ dans\]
</dt> <dd>

Nouveau texte à utiliser.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

La valeur de retour est ignorée.

## <a name="remarks"></a>Remarques

La taille ou la disposition de la boîte de dialogue de tâches peut changer pour s’adapter au nouveau texte.

## <a name="examples"></a>Exemples

L’exemple de code suivant montre comment définir le texte de pied de page dans la boîte de dialogue de tâches représentée par *HWND*.


```C++
SendMessage(hwnd, TDM_SET_ELEMENT_TEXT, (WPARAM)TDE_FOOTER, (LPARAM)L"New footer text.");
```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**texte de l' \_ élément de mise à jour TDM \_ \_**](tdm-update-element-text.md)
</dt> </dl>

 

 





