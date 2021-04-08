---
title: Message LB_SETLOCALE (winuser. h)
description: Définit les paramètres régionaux actuels de la zone de liste. Vous pouvez utiliser les paramètres régionaux pour déterminer l’ordre de tri correct du texte affiché (pour les zones de liste avec le \_ style de tri lbs) et du texte ajouté par le \_ message lb ADDSTRING.
ms.assetid: e9503124-de9f-4b92-a59e-ec9320864ae7
keywords:
- LB_SETLOCALE les contrôles de message Windows
topic_type:
- apiref
api_name:
- LB_SETLOCALE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd8ea7bb7b6d19144a84ab166f56cd2c0ad49e05
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104033144"
---
# <a name="lb_setlocale-message"></a>LB \_ SETLOCALE message

Définit les paramètres régionaux actuels de la zone de liste. Vous pouvez utiliser les paramètres régionaux pour déterminer l’ordre de tri correct du texte affiché (pour les zones de liste avec le style de [**\_ Tri lbs**](list-box-styles.md) ) et du texte ajouté par le message [**lb \_ ADDSTRING**](lb-addstring.md) .

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Spécifie l’identificateur de paramètres régionaux qui sera utilisé par la zone de liste pour le tri lors de l’ajout de texte.

</dd> <dt>

*lParam* 
</dt> <dd>

Ce paramètre n'est pas utilisé.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

La valeur de retour est l’identificateur de paramètres régionaux précédent. Si le paramètre *wParam* spécifie des paramètres régionaux qui ne sont pas installés sur le système, la valeur de retour est lb \_ Err et les paramètres régionaux de la zone de liste active ne sont pas modifiés.

## <a name="remarks"></a>Notes

Utilisez la macro [**MAKELCID**](/windows/desktop/api/winnt/nf-winnt-makelcid) pour construire un identificateur de paramètres régionaux.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                                           |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                                     |
| En-tête<br/>                   | <dl> <dt>Winuser. h (inclure Windows. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

**Référence**
</dt> <dt>

[**LB \_ ADDSTRING**](lb-addstring.md)
</dt> <dt>

[**\_GETLOCALE lb**](lb-getlocale.md)
</dt> </dl>

 

