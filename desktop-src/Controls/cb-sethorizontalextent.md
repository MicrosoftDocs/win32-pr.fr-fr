---
title: Message CB_SETHORIZONTALEXTENT (winuser. h)
description: Une application envoie le \_ message CB SETHORIZONTALEXTENT pour définir la largeur, en pixels, par laquelle une zone de liste peut faire défiler horizontalement (la largeur avec défilement).
ms.assetid: 85e8ff4f-ad9a-451c-b791-bd442b32d716
keywords:
- CB_SETHORIZONTALEXTENT les contrôles de Windows de message
topic_type:
- apiref
api_name:
- CB_SETHORIZONTALEXTENT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c8aac1fc0d10a38b292a4f37b3b170060d7e76ef5c8d303f39180b3f5063ffee
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120089019"
---
# <a name="cb_sethorizontalextent-message"></a>\_Message SETHORIZONTALEXTENT CB

Une application envoie le message **CB \_ SETHORIZONTALEXTENT** pour définir la largeur, en pixels, par laquelle une zone de liste peut faire défiler horizontalement (la largeur avec défilement). Si la largeur de la zone de liste est inférieure à cette valeur, la barre de défilement horizontale fait défiler horizontalement les éléments de la zone de liste. Si la largeur de la zone de liste est supérieure ou égale à cette valeur, la barre de défilement horizontale est masquée ou, si la zone de liste déroulante a le style [**CBS \_ DISABLENOSCROLL**](combo-box-styles.md) , désactivé.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Spécifie la largeur de défilement de la zone de liste, en pixels.

</dd> <dt>

*lParam* 
</dt> <dd>

Ce paramètre n'est pas utilisé.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                                           |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                                     |
| En-tête<br/>                   | <dl> <dt>Winuser. h (inclure Windows. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_GETHORIZONTALEXTENT CB**](cb-gethorizontalextent.md)
</dt> </dl>

 

 





