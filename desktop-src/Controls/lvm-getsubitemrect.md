---
title: Message LVM_GETSUBITEMRECT (commctrl. h)
description: Récupère des informations sur le rectangle englobant d’un sous-élément dans un contrôle d’affichage de liste.
ms.assetid: 985876b2-6eb3-4c96-88ea-ddec67ef5b5a
keywords:
- LVM_GETSUBITEMRECT les contrôles de Windows de message
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
ms.openlocfilehash: 651be72c23113940fc30adb2e7a9de581289a8f4ddf580f27d01e2edf337c053
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119293889"
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
| <span id="top"></span><span id="TOP"></span><dl> <dt>**top**</dt> </dl>    | Index de base un du sous-élément.<br/>                                                                                    |
| <span id="left"></span><span id="LEFT"></span><dl> <dt>**gauche**</dt> </dl> | Valeur de l’indicateur (consultez la section Notes). Indique la partie du sous-élément de vue de liste pour lequel récupérer le rectangle englobant.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne une valeur différente de zéro en cas de réussite, ou zéro dans le cas contraire.

## <a name="remarks"></a>Remarques

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
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

