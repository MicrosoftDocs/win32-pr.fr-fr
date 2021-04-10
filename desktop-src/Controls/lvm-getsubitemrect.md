---
title: Message LVM_GETSUBITEMRECT (commctrl. h)
description: Récupère des informations sur le rectangle englobant d’un sous-élément dans un contrôle d’affichage de liste.
ms.assetid: 985876b2-6eb3-4c96-88ea-ddec67ef5b5a
keywords:
- LVM_GETSUBITEMRECT les contrôles de message Windows
topic_type:
- apiref
api_name:
- LVM_GETSUBITEMRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd1184c52d60b86e008685b87c9f5555cf801b35
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105490"
---
# <a name="lvm_getsubitemrect-message"></a>\_Message GETSUBITEMRECT LVM

Récupère des informations sur le rectangle englobant d’un sous-élément dans un contrôle d’affichage de liste. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**\_ GetSubItemRect ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getsubitemrect) (recommandé). Ce message est destiné à être utilisé uniquement avec des contrôles d’affichage de liste qui utilisent le style de [**\_ rapport LVS**](list-view-window-styles.md) .

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Index de l’élément parent du sous-élément.

</dd> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure [**Rect**](/previous-versions//dd162897(v=vs.85)) qui recevra les informations de rectangle englobant du sous-élément. Ses membres doivent être initialisés conformément aux relations de membre/valeur suivantes :



| Valeur                                                                                                                             | Signification                                                                                                                           |
|-----------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| <span id="top"></span><span id="TOP"></span><dl> <dt>**Retour au début**</dt> </dl>    | Index de base un du sous-élément.<br/>                                                                                    |
| <span id="left"></span><span id="LEFT"></span><dl> <dt>**gauche**</dt> </dl> | Valeur de l’indicateur (consultez la section Notes). Indique la partie du sous-élément de vue de liste pour lequel récupérer le rectangle englobant.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne une valeur différente de zéro en cas de réussite, ou zéro dans le cas contraire.

## <a name="remarks"></a>Notes

Voici les valeurs d’indicateur qui peuvent être définies.



| Condition requise | Valeur |
|----------------|---------------------------------------------------------------------------------------------------------------------|
| **Valeur de l’indicateur** | **Signification**                                                                                                         |
| \_limites LVIR   | Retourne le rectangle englobant de l’élément entier, y compris l’icône et l’étiquette.                                    |
| \_icône LVIR     | Retourne le rectangle englobant de l’icône ou de la petite icône.                                                           |
| \_étiquette LVIR    | Retourne le rectangle englobant de l’élément entier, y compris l’icône et l’étiquette. Cela est identique aux limites de LVIR \_ . |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

