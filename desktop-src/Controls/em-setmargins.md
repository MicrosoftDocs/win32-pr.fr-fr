---
title: Message EM_SETMARGINS (winuser. h)
description: Définit les largeurs des marges gauche et droite d’un contrôle d’édition. Le message redessine le contrôle pour refléter les nouvelles marges. Vous pouvez envoyer ce message à un contrôle d’édition ou à un contrôle d’édition enrichi.
ms.assetid: 23eb6c9e-3cf9-4c90-b33e-8da84034b49b
keywords:
- EM_SETMARGINS les contrôles de Windows de message
topic_type:
- apiref
api_name:
- EM_SETMARGINS
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 396bba6dda0f6dbd132b9f67fa5a1ef012758bbf7cf8fa9517b656dcf164c94c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120048359"
---
# <a name="em_setmargins-message"></a>\_Message setMargins em

Définit les largeurs des marges gauche et droite d’un contrôle d’édition. Le message redessine le contrôle pour refléter les nouvelles marges. Vous pouvez envoyer ce message à un contrôle d’édition ou à un contrôle d’édition enrichi.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Marges à définir. Ce paramètre peut être une ou plusieurs des valeurs suivantes.



| Valeur                                                                                                                                                            | Signification                                                                                                                                                                                                                                                                                                                                                                                                              |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="EC_LEFTMARGIN"></span><span id="ec_leftmargin"></span><dl> <dt>**\_LEFTMARGIN EC**</dt> </dl>    | Définit la marge de gauche.<br/>                                                                                                                                                                                                                                                                                                                                                                                     |
| <span id="EC_RIGHTMARGIN"></span><span id="ec_rightmargin"></span><dl> <dt>**\_RIGHTMARGIN EC**</dt> </dl> | Définit la marge de droite.<br/>                                                                                                                                                                                                                                                                                                                                                                                    |
| <span id="EC_USEFONTINFO"></span><span id="ec_usefontinfo"></span><dl> <dt>**\_USEFONTINFO EC**</dt> </dl> | **Contrôles RichEdit :** Définit les marges de gauche et de droite sur une largeur étroite calculée à l’aide des métriques de texte de la police actuelle du contrôle. Si aucune police n’a été définie pour le contrôle, les marges sont définies sur zéro. Le paramètre *lParam* est ignoré. <br/> **Contrôles d’édition :** La valeur **EC \_ USEFONTINFO** ne peut pas être utilisée dans le paramètre *wParam* . Elle ne peut être utilisée que dans le paramètre *lParam* .<br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) spécifie la nouvelle largeur de la marge de gauche, en pixels. Cette valeur est ignorée si *wParam* n’inclut pas l' **UE \_ LEFTMARGIN**.

**Modifiez les contrôles et la modification complète 3,0 et versions ultérieures :** Le [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) peut spécifier la **valeur \_ USEFONTINFO EC** pour définir la marge de gauche sur une largeur étroite calculée à l’aide des mesures du texte de la police actuelle du contrôle. Si aucune police n’a été définie pour le contrôle, la marge est définie sur zéro.

[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) spécifie la nouvelle largeur de la marge de droite, en pixels. Cette valeur est ignorée si *wParam* n’inclut pas **ce \_ RIGHTMARGIN**.

**Modifiez les contrôles et la modification complète 3,0 et versions ultérieures :** Le [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) peut spécifier la **valeur \_ USEFONTINFO EC** pour définir la marge de droite sur une largeur étroite calculée à l’aide des métriques de texte de la police actuelle du contrôle. Si aucune police n’a été définie pour le contrôle, la marge est définie sur zéro.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Ce message ne retourne pas de valeur.

## <a name="remarks"></a>Remarques

**Contrôles d’édition :** Vous ne pouvez pas utiliser **EC \_ USEFONTINFO** dans le paramètre *wParam* , mais vous pouvez l’utiliser dans le paramètre *lParam* .

**Modification riche :** Pris en charge dans Microsoft Rich Edit 1,0 et versions ultérieures. Toutes les versions RichEdit prennent en charge l’utilisation de la **\_ USEFONTINFO EC** dans le paramètre *wParam* . Toutefois, seul Microsoft Rich Edit 3,0 et versions ultérieures prennent en charge l’utilisation de **ce \_ USEFONTINFO** dans le paramètre *lParam* . Pour plus d’informations sur la compatibilité des versions RichEdit avec les différentes versions du système, consultez [à propos des contrôles](about-rich-edit-controls.md)RichEdit.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                                           |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                                     |
| En-tête<br/>                   | <dl> <dt>Winuser. h (inclure Windows. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_GETMARGINS em**](em-getmargins.md)
</dt> </dl>

 

