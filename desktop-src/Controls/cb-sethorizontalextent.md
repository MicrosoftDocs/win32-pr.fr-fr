---
title: Message CB_SETHORIZONTALEXTENT (winuser. h)
description: Une application envoie le \_ message CB SETHORIZONTALEXTENT pour définir la largeur, en pixels, par laquelle une zone de liste peut faire défiler horizontalement (la largeur avec défilement).
ms.assetid: 85e8ff4f-ad9a-451c-b791-bd442b32d716
keywords:
- CB_SETHORIZONTALEXTENT les contrôles de message Windows
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
ms.openlocfilehash: f51e505f36f7cfd3fa47644a288db4a97ba89ca4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465250"
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
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                                           |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                                     |
| En-tête<br/>                   | <dl> <dt>Winuser. h (inclure Windows. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_GETHORIZONTALEXTENT CB**](cb-gethorizontalextent.md)
</dt> </dl>

 

 





