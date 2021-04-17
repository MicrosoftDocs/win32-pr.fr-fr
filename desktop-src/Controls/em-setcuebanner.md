---
title: Message EM_SETCUEBANNER (commctrl. h)
description: Définit la file d’attente textuelle, ou Tip, qui est affichée par le contrôle d’édition pour inviter l’utilisateur à fournir des informations.
ms.assetid: 1b1ff5e7-e0b8-40c1-8b7e-7003e9ef959b
keywords:
- EM_SETCUEBANNER les contrôles de message Windows
topic_type:
- apiref
api_name:
- EM_SETCUEBANNER
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d740bf0a3a055f45c6d104d44349f078d3bf9ad2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466547"
---
# <a name="em_setcuebanner-message"></a>\_Message SETCUEBANNER em

Définit la file d’attente textuelle, ou Tip, qui est affichée par le contrôle d’édition pour inviter l’utilisateur à fournir des informations.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* \[ dans\]
</dt> <dd>

**True** si la bannière de signal doit s’afficher même lorsque le contrôle d’édition a le focus ; Sinon, **false**. **False** est le comportement par défaut où la bannière de signal disparaît lorsque l’utilisateur clique sur le contrôle.

</dd> <dt>

*lParam* \[ dans\]
</dt> <dd>

Pointeur vers une chaîne Unicode qui contient le texte à afficher en tant que file d’attente textuelle.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si le message est correctement exécuté, la méthode retourne la **valeur true**. Sinon, elle retourne **false**.

## <a name="remarks"></a>Notes

Un contrôle d’édition utilisé pour commencer une recherche peut afficher « entrer la recherche ici » en texte gris comme une file d’attente textuelle. Lorsque l’utilisateur clique sur le texte, le texte disparaît et l’utilisateur peut taper.

Vous ne pouvez pas définir une bannière de signal sur un contrôle d’édition multiligne ou sur un contrôle RichEdit.

> [!Note]  
> Pour utiliser cette API, vous devez fournir un manifeste spécifiant Comclt32.dll version 6,0. Pour plus d’informations sur les manifestes, consultez [activation des styles visuels](cookbook-overview.md).

 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Modifier \_ SetCueBannerText**](/windows/desktop/api/Commctrl/nf-commctrl-edit_setcuebannertext)
</dt> </dl>

 

 





