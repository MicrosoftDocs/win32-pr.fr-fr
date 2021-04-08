---
title: Message TTM_SETTITLE (commctrl. h)
description: Ajoute une icône standard et une chaîne de titre à une info-bulle.
ms.assetid: e745a592-eef7-4e0d-8939-a48b52c4ab9f
keywords:
- TTM_SETTITLE les contrôles de message Windows
topic_type:
- apiref
api_name:
- TTM_SETTITLE
- TTM_SETTITLEA
- TTM_SETTITLEW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d7972a9d40347995e9d641e7fc8706f9ad4c58bd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103844258"
---
# <a name="ttm_settitle-message"></a>\_Message atténuation SETTITLE

Ajoute une icône standard et une chaîne de titre à une info-bulle.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Affectez l’une des valeurs suivantes à *wParam* pour spécifier l’icône à afficher. À compter de Windows XP SP2 et versions ultérieures, ce paramètre peut également contenir une valeur **HICON** . Toute valeur supérieure à TTI \_ erreur est supposée être un **HICON**.



| Valeur                                                                                                                                                                      | Signification                     |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------|
| <span id="TTI_NONE"></span><span id="tti_none"></span><dl> <dt>**TTI \_ aucun**</dt> </dl>                             | Pas d'icône.<br/>         |
| <span id="TTI_INFO"></span><span id="tti_info"></span><dl> <dt>**\_informations TTI**</dt> </dl>                             | Icône info.<br/>       |
| <span id="TTI_WARNING"></span><span id="tti_warning"></span><dl> <dt>**\_Avertissement TTI**</dt> </dl>                    | Icône d'avertissement<br/>     |
| <span id="TTI_ERROR"></span><span id="tti_error"></span><dl> <dt>**\_erreur TTI**</dt> </dl>                          | Icône d’erreur<br/>       |
| <span id="TTI_INFO_LARGE"></span><span id="tti_info_large"></span><dl> <dt>**TTI \_ info \_ grand**</dt> </dl>          | Icône d’erreur importante<br/> |
| <span id="TTI_WARNING_LARGE"></span><span id="tti_warning_large"></span><dl> <dt>**\_Avertissement TTI \_ grand**</dt> </dl> | Icône d’erreur importante<br/> |
| <span id="TTI_ERROR_LARGE"></span><span id="tti_error_large"></span><dl> <dt>**erreur TTI de \_ \_ grande taille**</dt> </dl>       | Icône d’erreur importante<br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Pointeur vers la chaîne de titre. Vous devez assigner une valeur à *lParam*.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne la **valeur true** en cas de réussite, **false** dans le cas contraire.

## <a name="remarks"></a>Notes

Le titre d’une info-bulle s’affiche au-dessus du texte, dans une police différente. Il n’est pas suffisant d’avoir un titre ; l’info-bulle doit également comporter du texte ou elle ne s’affiche pas.

Lorsque *wParam* contient un **HICON**, une copie de l’icône est créée par la fenêtre d’info-bulle.

Lors de l’appel de **atténuation \_ SETTITLE**, la chaîne vers laquelle pointe *lParam* ne doit pas dépasser 100 **TCHARs** , y compris le caractère **null** de fin.

## <a name="examples"></a>Exemples

L’exemple suivant montre comment ajouter un titre et une icône système à une info-bulle.


```C++
// hwndTip is the handle of the tooltip window.
HICON hIcon = LoadIcon(NULL, IDI_INFORMATION);
SendMessage(hwndTip, TTM_SETTITLE, (WPARAM)hIcon, L"Title text");
DestroyIcon(hIcon);
```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Noms Unicode et ANSI<br/>   | **Atténuation \_ SETTITLEW** (Unicode) et **atténuation \_ SETTITLEA** (ANSI)<br/>                 |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[À propos des contrôles ToolTip](tooltip-controls.md)
</dt> </dl>

 

 





