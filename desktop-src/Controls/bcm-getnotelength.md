---
title: Message BCM_GETNOTELENGTH (commctrl. h)
description: Obtient la longueur du texte de la note qui peut s’afficher dans la description d’un bouton de lien de commande. Envoyez ce message explicitement ou à l’aide de la \_ macro Button GetNoteLength.
ms.assetid: 62385485-b553-47e9-9f15-696cc4694752
keywords:
- BCM_GETNOTELENGTH les contrôles de Windows de message
topic_type:
- apiref
api_name:
- BCM_GETNOTELENGTH
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 385cb5d7694818a0e0e03ab74bcc31b76d13f5d304c7415b1f70a0fd43e1b31b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119921659"
---
# <a name="bcm_getnotelength-message"></a>\_Message GETNOTELENGTH BCM

Obtient la longueur du texte de la note qui peut s’afficher dans la description d’un bouton de lien de commande. Envoyez ce message explicitement ou à l’aide de la macro [**Button \_ GetNoteLength**](/windows/desktop/api/Commctrl/nf-commctrl-button_getnotelength) .

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Doit être zéro.

</dd> <dt>

*lParam* 
</dt> <dd>

Doit être zéro.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne la longueur du texte de la note dans **WCHARs**, à l’exclusion de toute **valeur null** de fin, ou zéro s’il n’y a aucun texte de note.

## <a name="remarks"></a>Remarques

À partir de la version 6,01 de ComCtl32, les boutons de lien de commande peuvent avoir une note. Pour plus d’informations sur les versions de DLL, consultez [versions de contrôle courantes](common-control-versions.md).

Le **message \_ GETNOTELENGTH BCM** fonctionne uniquement avec les styles de bouton [**BS \_ COMMANDLINK**](button-styles.md) et [**BS \_ DEFCOMMANDLINK**](button-styles.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

**Référence**
</dt> <dt>

[Styles de bouton](button-styles.md)
</dt> <dt>

**Méthodologique**
</dt> <dt>

[Types de bouton](button-types-and-styles.md)
</dt> </dl>

 

 





