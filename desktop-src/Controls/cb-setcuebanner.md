---
title: Message CB_SETCUEBANNER (winuser. h)
description: Définit le texte de bannière de signal qui est affiché pour le contrôle d’édition d’une zone de liste déroulante.
ms.assetid: 4b2b5042-ba64-4e3f-adeb-9aea66773b0e
keywords:
- CB_SETCUEBANNER les contrôles de Windows de message
topic_type:
- apiref
api_name:
- CB_SETCUEBANNER
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cb546b7113247f09d8929364984d5e73c3e28b6541d2ca04bd631405040bf6fb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120089039"
---
# <a name="cb_setcuebanner-message"></a>\_Message SETCUEBANNER CB

Définit le texte de bannière de signal qui est affiché pour le contrôle d’édition d’une zone de liste déroulante.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Doit être zéro.

</dd> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une mémoire tampon de chaîne Unicode se terminant par un caractère null qui contient le texte.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne 1 en cas de réussite, ou une valeur d’erreur dans le cas contraire.

## <a name="remarks"></a>Remarques

La bannière de signal est du texte affiché dans le contrôle d’édition d’une zone de liste déroulante lorsqu’il n’y a aucune sélection.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                                           |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                                     |
| En-tête<br/>                   | <dl> <dt>CommCtrl. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fonctionnalités de zone de liste modifiable](combo-box-features.md)
</dt> </dl>

 

 





